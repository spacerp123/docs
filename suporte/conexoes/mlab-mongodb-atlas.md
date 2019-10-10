description
Setting up your Mongo Bank on a Discloud hosted Bot.
MongoDB Atlas (mLab)


When connecting your MongoDB database to a DisCloud-hosted Bot Discord you may come across the possible error:
{% hint style = "danger"%}

Error Connecting to MyDB : MongoNetworkError : connection 0 to meudb - shard - 00 - 00 - 9m7sg . mongodb . net : 27017 closed
{% endhint%}

According to a Github issue I encountered, you will get this error message if you have not whitelisted MongoDB Atlas addresses, the IP where your Bot is hosted.

{% hint style = "info"%} Due to the way DisCloud works, we cannot provide you with an IP address. {% endhint%}


So according to the MongoDB Atlas documentation , the only way to make DisCloud instances connect to your bank is to add 0.0.0.0/0(ie all addresses) to your MongoDB Atlas whitelist.

