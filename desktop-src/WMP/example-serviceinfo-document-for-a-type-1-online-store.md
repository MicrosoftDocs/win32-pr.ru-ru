---
title: Пример документа ServiceInfo для Интернет-магазина типа 1
description: Пример документа ServiceInfo для Интернет-магазина типа 1
ms.assetid: 7d997773-1c11-44d5-ae67-05ba3909c481
keywords:
- проигрыватель Windows Media интернет-магазинов, пример документа ServiceInfo
- Интернет-магазины, пример документа ServiceInfo
- Тип 1 Интернет-магазины, пример документа ServiceInfo
- проигрыватель Windows Media интернет-магазинов, документ ServiceInfo
- Интернет-магазины, документ ServiceInfo
- Тип 1 Интернет-магазины, документ ServiceInfo
- проигрыватель Windows Media интернет-магазинов, пример кода
- Интернет-магазины, пример кода
- Тип 1 Интернет-магазины, пример кода
- Пример документа ServiceInfo
- Документ ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a414ed729733eed610b06e43748e393fa600ee46917d4f9b30ad21ae8d378d3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650214"
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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Справка по программированию для Интернет-магазинов типа 1**](programming-guide-for-type-1-online-stores.md)
</dt> <dt>

[**Документ ServiceInfo для Интернет-магазина типа 1**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Документ ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




