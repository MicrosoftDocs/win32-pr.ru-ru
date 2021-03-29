---
title: Пример документа ServiceInfo для Интернет-магазина типа 1
description: Пример документа ServiceInfo для Интернет-магазина типа 1
ms.assetid: 7d997773-1c11-44d5-ae67-05ba3909c481
keywords:
- Интернет-магазины проигрывателя Windows Media, пример документа ServiceInfo
- Интернет-магазины, пример документа ServiceInfo
- Тип 1 Интернет-магазины, пример документа ServiceInfo
- Интернет-магазины проигрывателя Windows Media, документ ServiceInfo
- Интернет-магазины, документ ServiceInfo
- Тип 1 Интернет-магазины, документ ServiceInfo
- Пример кода в Интернет-магазинах проигрывателя Windows Media
- Интернет-магазины, пример кода
- Тип 1 Интернет-магазины, пример кода
- Пример документа ServiceInfo
- Документ ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1378c30a8dbbb46844923e9c73c242a28d5da3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778020"
---
# <a name="example-serviceinfo-document-for-a-type-1-online-store"></a>Пример документа ServiceInfo для Интернет-магазина типа 1

В следующем примере кода показан полный ServiceInfo.xml документ. Этот XML-код можно использовать в качестве отправной точки для собственного документа ServiceInfo.


```C++
<?xml version="1.0" encoding="utf-8" ?>
<ServiceInfo Version="1.00" Key="Proseware" ContentPartner="true">

    <FriendlyName>Proseware Service</FriendlyName>

    <Description>
        Proseware Music has all your favorite songs.
    </Description>

    <Image 
        EulaURL = "https://www.proseware.com/service/images/eula.png"
        MenuURL = "https://www.proseware.com/service/images/menuicon.jpg"
        ServiceLargeURL = "https://www.proseware.com/service/images/45x13Large.png"
        ServiceSmallURL = "https://www.proseware.com/service/images/45x13Small.png" />

    <Color
        MediaPlayer = "#FF8040"
        MediaPlayerText = "#FFFFFF"/>

    <ServiceTask1
        URL = "https://www.proseware.com/service/html/Music.asp">
        <ButtonText>Proseware\nMusic</ButtonText>
        <ButtonTip>Proseware Music Store</ButtonTip>
    </ServiceTask1>

    <Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
    </Navigate>

    <InfoCenter
        URL = "https://www.proseware.com/service/html/InfoCenter.asp"/>

    <AlbumInfo
        URL = "https://www.proseware.com/service/html/AlbumInfo.asp"/>

    <BuyCD
        MediaPlayerURL = "https://www.proseware.com/service/html/BuyCDMediaPlayer.asp"
        MediaCenterURL = "https://www.proseware.com/service/html/BuyCDMediaCenter.asp"
        BrowserURL = "https://www.proseware.com/service/html/BuyCDBrowser.asp"/>

    <DownloadStatus
        URL = "https://www.proseware.com/service/html/Music_Download.htm"/>

    <HTMLView
        BaseURL = "https://www.proseware.com/"/>

    <Install
        EULAURL="https://www.proseware.com/service/html/eula.txt"
        CodeURL="https://www.proseware.com/service/html/ProsewareInstall.cab"
        PrivacyInfoURL="https://www.proseware.com/service/html/PrivacyPolicy.htm"
        InstallApp="ProsewareSetup.exe"  
        CatalogURL="https://www.proseware.com/service/html/Catalog.asp"/>

</ServiceInfo>
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Справка по программированию для Интернет-магазинов типа 1**](programming-guide-for-type-1-online-stores.md)
</dt> <dt>

[**Документ ServiceInfo для Интернет-магазина типа 1**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Документ ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




