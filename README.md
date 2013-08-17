Session
=======

A PHP class that makes it easy to use sessions with static methods.

How to use it
=======

`````php
include "Session.class.php";

//check if session is started
if(Session::isStarted()){
  echo "Session is started!";
} else {
  //if session is not started we must start session
  $username = "claudio";
  $pippo = "pippo";
  $sessionData = array(
    'username'=>$username,
    'pippo'=>$pippo
  );
  //we start session and we put into it two variables: username and pippo
  Session::startSession($data);
  
  //now we need to print username
  echo "Username: ".Session::get('username');
  
  //now we need to set pippo with another value
  Session::set('pippo','foo');
}

//finally we can destroy session
Session::destroySession();
`````

Dependencies
=======

<ul>
  <li>PHP 5</li>
</ul>
