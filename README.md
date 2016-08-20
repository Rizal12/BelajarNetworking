The Basics of Unity 5 Networking


Creating multiplayer game it more complex, you should be learn how to post/get value from another player such as position, name of player and many more.
Fortunately, Unity has a feature its called "Network Manager",
that a simple way manage multiplayer, set which GameObject as Client Offline/Online,
and also C# in Unity is easy to post/get value
you can use [SyncVar], write above variable, its mean that variable will be sync with all observer player

Ex:
[SyncVar]
public string pname = "player";

and then to broadcast data(such as pname has been changed), write [Command] above method of set data

Ex:
[Command]
public void ChangeName(string newName){
  pname = newName;
}

Don't forget use isLocalPlayer to check own object player

Special Thanks to Holistic3d , https://www.youtube.com/watch?v=JlKf0h0K5PU



