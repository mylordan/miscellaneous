var http = require('http');

function getJSON(options,cb){
    http.request(options,function(res){
    var body ='';
    res.on('data', function(chunk){
        body+=chunk;
    });

    res.on('end',function(){
        var hasil = JSON.parse(body);
        cb(null, hasil);
    })
    res.on('error', cb);

    })
    .on('error',cb)
    .end();

}

var options = {
    host:'pubsub.pubnub.com',
    port:80,
    path:'/time/0',
    method: 'GET'
};


getJSON(options, function(err,hasil){
    if (err){
        return console.log('error dapetin data', err);
    }else {
        console.log('hasile ndoorr', hasil);

        // setTimeout(function() {
        //        getJSON(options,cb);
        //    }, 5000);
    }



});
