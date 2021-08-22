---
title: Сведения о версиях моделей объектов
description: Сведения о версиях моделей объектов
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- проигрыватель Windows Media, версии
- объектная модель проигрыватель Windows Media, версии
- Объектная модель, версии
- проигрыватель Windows Media ActiveX элемент управления, версии для объектной модели
- элемент управления ActiveX, версии для объектной модели
- проигрыватель Windows Media управление мобильными ActiveXми, версии для объектной модели
- проигрыватель Windows Media Мобильные устройства, версии для объектной модели
- версии проигрыватель Windows Media, объектная модель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce90455d93d71f6fde62b97d3b4d38e34963307e60b831c8110a914cc535cffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510064"
---
# <a name="about-the-object-model-versions"></a>Сведения о версиях моделей объектов

в проигрыватель Windows Media 7,0 появилась новая объектная модель. эта объектная модель расширена с помощью проигрыватель Windows Media 7,1, проигрыватель Windows Media для Windows XP, проигрыватель Windows Media 9 Series, проигрыватель Windows Media 10, проигрыватель Windows Media 11 и проигрыватель Windows Media 12. Каждый раздел в справочнике по объектной модели содержит раздел требований, в котором подробно описаны минимальные требования к отдельному свойству, методу или событию. Ниже приведены сведения о новых объектах, методах, свойствах и событиях, которые были добавлены для каждой версии с момента выпуска версии 7,0. В эти списки также входят новые интерфейсы, методы и события C++.

Когда новый или обновленный интерфейс также предоставляется как объект, в списке отображается только объект. Чтобы найти интерфейс, обратитесь к [Справочнику по объектной модели для C++](object-model-reference-for-c.md). Как правило, необходимо просто добавить префикс ИВМП в имя объекта. Если новый интерфейс расширяет существующий, может потребоваться найти номер последней версии. например, в проигрыватель Windows Media 9 Series появились новые свойства и методы, доступные из объекта [**Параметры**](settings-object.md) . В C++ они доступны через интерфейс [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) , который расширяет [**ивмпсеттингс**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).

## <a name="added-for-windows-media-player-71"></a>добавлено для проигрыватель Windows Media 7,1

-   [**Свойство Player. Стретчтофит**](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a>добавлен для проигрыватель Windows Media для Windows XP

-   [**Метод Controls. Step**](controls-step.md)
-   [**Объект DVD**](dvd-object.md)
-   [**Свойство Media. Error**](media-error.md)
-   [**Событие Player. Домаинчанже**](player-player-domainchange.md)
-   [**Событие Player. Медиаеррор**](player-player-mediaerror.md)
-   [**Событие Player. Опенплайлистсвитч**](player-player-openplaylistswitch.md)
-   [**Свойство Player. Виндовлессвидео**](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a>добавлено для серии проигрыватель Windows Media 9

-   [**Клоседкаптион. Жетсамилангид, метод**](closedcaption-getsamilangid.md)
-   [**Клоседкаптион. Жетсамилангнаме, метод**](closedcaption-getsamilangname.md)
-   [**Клоседкаптион. Жетсамистиленаме, метод**](closedcaption-getsamistylename.md)
-   [**Клоседкаптион. Самилангкаунт, свойство**](closedcaption-samilangcount.md)
-   [**Клоседкаптион. Самистилекаунт, свойство**](closedcaption-samistylecount.md)
-   [**Свойство Controls. Аудиолангуажекаунт**](controls-audiolanguagecount.md)
-   [**Свойство Controls. Куррентаудиолангуаже**](controls-currentaudiolanguage.md)
-   [**Свойство Controls. Куррентаудиолангуажеиндекс**](controls-currentaudiolanguageindex.md)
-   [**Свойство Controls. Куррентпоситионтимекоде**](controls-currentpositiontimecode.md)
-   [**Controls. Жетаудиолангуажедескриптион, метод**](controls-getaudiolanguagedescription.md)
-   [**Controls. Жетаудиолангуажеид, метод**](controls-getaudiolanguageid.md)
-   [**Controls. Жетлангуаженаме, метод**](controls-getlanguagename.md)
-   [**Ерроритем. Condition, свойство**](erroritem-condition.md)
-   [**Свойство external. Аппколорлигхт**](external-appcolorlight.md)
-   [**Внешнее событие Онколорчанже**](external-oncolorchange-event.md)
-   [**Свойство external. Version**](external-version.md)
-   [**Ивмпевентс: событие Лайердоккедстатечанже:P**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [**Ивмпевентс: событие Лайерреконнект:P**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [**Событие Ивмпевентс:: Свитчедтоконтрол**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [**Событие Ивмпевентс:: Свитчедтоплайераппликатион**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [**Интерфейс Ивмпплайерсервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [**Интерфейс Ивмпремотемедиасервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [**Интерфейс Ивмпскинманажер**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [**Метод Media. Жетаттрибутекаунтбитипе**](media-getattributecountbytype.md)
-   [**Метод Media. Жетитеминфобитипе**](media-getiteminfobytype.md)
-   [**Объект Метадатапиктуре**](metadatapicture-object.md)
-   [**Объект Метадататекст**](metadatatext-object.md)
-   [**Событие Player. Аудиолангуажечанже**](player-player-audiolanguagechange.md)
-   [**Свойство Player. Remote**](player-isremote.md)
-   [**Событие Player. Медиаколлектионаттрибутестрингчанжед**](player-player-mediacollectionattributestringchanged.md)
-   [**Метод Player. Невмедиа**](player-newmedia.md)
-   [**Метод Player. Невплайлист**](player-newplaylist.md)
-   [**Метод Player. Опенплайер**](player-openplayer.md)
-   [**Свойство Player. Плайераппликатион**](player-playerapplication.md)
-   [**Событие Player. StatusChange**](player-player-statuschange.md)
-   [**Объект Плайераппликатион**](playerapplication-object.md)
-   [**свойство Параметры. дефаултаудиолангуаже**](settings-defaultaudiolanguage.md)
-   [**свойство Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
-   [**метод Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a>добавлено для проигрыватель Windows Media 10

-   [**Интерфейс Ивмпграфкреатион**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [**Интерфейс IWMPPlayerServices2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [**Интерфейс Ивмпсинкдевице**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [**Интерфейс Ивмпсинксервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [**Перечисление Вмпдевицестатус**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [**Перечисление Вмпсинкстате**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a>добавлено для проигрыватель Windows Media 11

-   [**Интерфейс Ивмпкдромбурн**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Интерфейс Ивмпкдромбурн (VB и C#)**](iwmpcdromburn--vb-and-c.md)
-   [**Интерфейс Ивмпкдромрип**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Интерфейс Ивмпкдромрип (VB и C#)**](iwmpcdromrip--vb-and-c.md)
-   [**Интерфейс IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [**Интерфейс Ивмпфолдермониторсервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**Интерфейс Ивмплибрари**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Интерфейс Ивмплибрари (VB и C#)**](iwmplibrary--vb-and-c.md)
-   [**Интерфейс Ивмплибрарисервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Интерфейс Ивмплибрарисервицес (VB и C#)**](iwmplibraryservices--vb-and-c.md)
-   [**Интерфейс Ивмплибраришарингсервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**Интерфейс IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Интерфейс IWMPMediaCollection2 (VB и C#)**](iwmpmediacollection2--vb-and-c.md)
-   [**Интерфейс Ивмпкуери**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Интерфейс Ивмпкуери (VB и C#)**](iwmpquery--vb-and-c.md)
-   [**Интерфейс Ивмпрендерконфиг**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [**Интерфейс IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Интерфейс IWMPStringCollection2 (VB и C#)**](iwmpstringcollection2--vb-and-c.md)
-   [**Интерфейс IWMPSyncDevice2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Интерфейс Ивмпвидеорендерконфиг**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**Объект запроса**](query-object.md)
-   [**Перечисление Вмпбурнформат**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [**Перечисление Вмпбурнстате**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [**Перечисление Вмплибраритипе**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [**Перечисление Вмприпстате**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a>добавлено для проигрыватель Windows Media 12

-   [**Интерфейс Ивмпаудиорендерконфиг**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**Интерфейс IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**Интерфейс IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**Интерфейс IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Сведения об объектной модели проигрывателя**](about-the-player-object-model.md)
</dt> <dt>

[**Справочник по объектной модели для создания сценариев**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




