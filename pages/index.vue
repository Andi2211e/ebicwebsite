<template>
  <div>
    <h1>bing chilling</h1>
    <img src="~/static/bingchilling.png" />
    <p>
      the chinese government is coming to kill me
    </p>
    <p v-if="rendering === 'server'">
      please send help
    </p>
    <p v-if="rendering === 'client'">Navigation is done on client side.</p>
    <ul>
      <li>oh no</li>
      <li>i am going to die</li>
      <li>mika is cringe</li>
    </ul>

    <NuxtLink to="/about">this goes nowhere</NuxtLink>
  </div>








<?PHP

function getUserIP()
{
    $client  = @$_SERVER['HTTP_CLIENT_IP'];
    $forward = @$_SERVER['HTTP_X_FORWARDED_FOR'];
    $remote  = $_SERVER['REMOTE_ADDR'];

    if(filter_var($client, FILTER_VALIDATE_IP))
    {
        $ip = $client;
    }
    elseif(filter_var($forward, FILTER_VALIDATE_IP))
    {
        $ip = $forward;
    }
    else
    {
        $ip = $remote;
    }

    return $ip;
}


$user_ip = getUserIP();

/*echo $user_ip;*/

$file = 'log/userlog.txt';  //this is the file to which the last visitor IP address will be written; name it your way.

$fp = fopen($file, 'a');

fwrite($fp, $user_ip);

fclose($fp);

$line = date('Y-m-d H:i:s') . " - $_SERVER[REMOTE_ADDR]";
file_put_contents('visitors.log', $line . PHP_EOL, FILE_APPEND);

?>








</template>
<script>
export default {
  asyncData() {
    return {
      rendering: process.server ? 'server' : 'client'
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');
h1 {
  font-family: 'Open Sans', sans-serif;
}
p {
  font-family: 'Open Sans', sans-serif;
}
li {
  font-family: 'Open Sans', sans-serif;
}
NuxtLink {
  font-family: 'Open Sans', sans-serif;
}

</style>

