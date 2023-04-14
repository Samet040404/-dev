# -dev
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NAVBAR</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.13.1/css/all.min.css">
    
    <style>
    *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

body{
    background-image: url(resim.jpg);
    background-size: cover;  /*ÇOK ÖNEMLİ: Arka plan resmini tam boyutlandırdık.*/
    font-family: sans-serif;
}

.menu-bar{
    background: #5b71b5;
    text-align: center;
}

.menu-bar ul{
    display: inline-flex;
    list-style: none;
}

.menu-bar ul li{
    width: 140px;
    margin: 15px;
    padding: 15px;
}

.menu-bar ul li a{
    text-decoration: none;
    color: #fff;
}

.active, .menu-bar ul li:hover{  /*active'nin css kodu*/
    background: #d4c995;
    border-radius: 10px;
}

.menu-bar .fas{
    margin-right: 8px;
}


.sub-menu-1{ /*Öncelikle gizlenmesini istiyoruz.*/
    display: none;
}

.menu-bar ul li:hover .sub-menu-1{
    display: block;
    position: absolute; /*sub-menu-1 divine göre kendini konumlandırmasını istedik.*/
    background: #5b71b5;
    margin-top: 15px;
    margin-left: -15px;
    font-size: 10px;
}

.menu-bar ul li:hover .sub-menu-1 ul{
    display: block;
}

.menu-bar ul li:hover .sub-menu-1 ul li{
    width: 150px;
    padding: 10px;
    border-bottom: 1px dotted #fff;
    background: transparent; /*arka plan rengini transparant yaptık ki daha saydam görüntü olsun.*/
    text-align: left;
    border-radius: 0; /*Alt beyaz çizgi yukarı doğru oynamasını engellemk için.*/
    cursor: pointer;
}

.menu-bar ul li:hover .sub-menu-1 ul li a:hover{
    color: #b2ff00;
}

.fa-caret-right{
    font-size: 14px;
    color: #fff;
    float:right;
}

.sub-menu-2{
    display: none; /*gizlenmesini sağladık.*/
}


.hover-me:hover .sub-menu-2{
    position: absolute;
    display: block;
    margin-top: -40px; /*bottom görevi gibi görüldü -40px*/
    margin-left: 140px;
    background: #5b71b5;
}
    </style>
</head>
<body>

    <div class="menu-bar">
        <ul>
            <li class="active"><a href="#"><i class="fas fa-home"></i>Anasayfa</a></li>
            <li><a href="#"><i class="fas fa-user"></i>Hakkımızda</a>
                <div class="sub-menu-1">
                    <ul>
                        <li><a href="#">Misyonumuz</a></li>
                        <li><a href="#">Vizyonumuz</a></li>
                        <li><a href="#">Takımımız</a></li>
                    </ul>
                </div>
            </li>
            <li><a href="#"><i class="fas fa-clone"></i>Servisler</a>
                <div class="sub-menu-1">
                    <ul>
                    <li><a href="#">Web Tasarım</a></li>
                    <li class="hover-me"><a href="#">Market</a><i class="fas fa-caret-right"></i>
                        <div class="sub-menu-2">
                            <ul>
                                <li><a href="#">SEO</a></li>
                                <li><a href="#">Sosyal Medya</a></li>
                                <li><a href="#">Email Market</a></li>
                            </ul>
                        </div>
                    </li>
                    <li class="hover-me"><a href="#">Mobile App</a><i class="fas fa-caret-right"></i>
                        <div class="sub-menu-2">
                            <ul>
                                <li><a href="#">Android App</a></li>
                                <li><a href="#">Ios App</a></li>
                                <li><a href="#">Windows App</a></li>
                                <li><a href="#">Flutter App</a></li>
                                <li><a href="#">Unity App</a></li>
                            </ul>
                        </div>
                    </li>
                     </ul>
                </div>
            </li>
            <li><a href="#"><i class="fas fa-users"></i>Müşteriler</a></li>
            <li><a href="#"><i class="fas fa-headset"></i>Destek</a></li>
            <li><a href="#"><i class="fas fa-fa-lira-sign"></i>Fiyatlandırma</a></li>
            <li><a href="#"><i class="fas fa-edit"></i>Eğitim</a></li>
            <li><a href="#"><i class="fas fa-phone"></i>İletişim</a></li>
        </ul>
    </div>
    
</body>
</html>
