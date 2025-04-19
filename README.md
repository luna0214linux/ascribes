# ascribes
<!DOCTYPE html>
<html lang="ja">
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
        <title>超田代砲改 Ver.1.3</title>
    </head>
    <body>
        <script>
        var wind, add;
        
        function tashiro() {
            wind.location = add;
            setTimeout("tashiro()", f.inter.value*1000);
            f.fired.value++;
        }
        
        function display() {
            add = f.address.value;
            wind = window.open(add, 'target', 'width=400, height=400');
            tashiro();
        }
        </script>
        <form name="f">
            <font size="4" color="#000000">超田代砲改 Ver.1.3</font><br><br>
            <a>目標アドレス:</a><br>
            <input type="text" size="50" name="address" value="ここに目標URLを入れる"><br><br>
            <a>発射間隔:</a><br>
            <input type="text" size="5" name="inter" value="10"><a>秒</a><br><br>
            <a>既発射弾数:</a><br>
            <input type="text" name="fired" value="0"><br>
            <input type="button" value="発射" onclick="display()">
        </form>
    </body>
</html>
