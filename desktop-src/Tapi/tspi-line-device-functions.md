---
description: В этом разделе содержится алфавитный список доступных функций устройств в телефонной линии SPI.
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: Функции для устройства телефонной связи TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52282154e99ca4e400f6b2d5f32d00a19d62cfe98f0b789d4ee24b9a240293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119403714"
---
# <a name="tspi-line-device-functions"></a>Функции для устройства телефонной связи TSPI

В этом разделе содержится алфавитный список доступных функций устройств в телефонной линии SPI. Сведения для каждой функции включают следующее:

-   Оператор назначения функции.
-   Правильный синтаксис функции.
-   Описание параметров функции, включая допустимые состояния вызова.
-   Описание возвращаемого значения функции.
-   Раздел примечаний, который может включать любые или все из следующих элементов: список допустимых состояний вызова для записи функции и типичные переходы состояния вызова по завершении запроса. Описание того, какие члены больших структур данных должны быть заполнены поставщиком услуг, и какие члены должны сохранять свои значения без изменений; и сравнение с соответствующей функцией в TAPI.
-   Ссылки на другие функции, сообщения или структуры данных.
    > [!Note]  
    > Реальные состояния, в которых может выполняться функция, могут быть ограничены возможностями поставщика услуг. Поставщики услуг должны задать элемент **двкаллфеатурес** в структуре [**Линекаллстатус**](/windows/win32/api/tapi/ns-tapi-linecallstatus) , элемент **дваддрессфеатурес** в структуре [**линеаддрессстатус**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) и элемент **двлинефеатурес** в структуре [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) , чтобы указать приложениям, разрешены ли в этот момент времени функция или нет.

     

В этом разделе содержатся следующие функции устройства ТСПИ Line:

-   [**ТСПИ \_ линеакцепт**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [**ТСПИ \_ линеаддтоконференце**](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [**ТСПИ \_ линеансвер**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [**ТСПИ \_ линеблиндтрансфер**](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [**ТСПИ \_ линеклосе**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [**ТСПИ \_ линеклосекалл**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [**ТСПИ \_ линеклосемспинстанце**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**ТСПИ \_ линекомплетекалл**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [**ТСПИ \_ линекомплететрансфер**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**ТСПИ \_ линекондитионалмедиадетектион**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [**ТСПИ \_ линеконфигдиалог**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [**ТСПИ \_ линеконфигдиаложедит**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [**ТСПИ \_ линекреатемспинстанце**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**ТСПИ \_ линедевспеЦифик**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [**ТСПИ \_ линедевспеЦификфеатуре**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [**ТСПИ \_ линедиал**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [**ТСПИ \_ линедроп**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [ТСПИ \_ линедропнувнер](tspi-linedropnoowner.md)
-   [ТСПИ \_ линедропонклосе](tspi-linedroponclose.md)
-   [**ТСПИ \_ линефорвард**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**ТСПИ \_ линегасердигитс**](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [**ТСПИ \_ линеженератедигитс**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [**ТСПИ \_ линеженератетоне**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [**ТСПИ \_ линежетаддресскапс**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [**ТСПИ \_ линежетаддрессид**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [**ТСПИ \_ линежетаддрессстатус**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [**ТСПИ \_ линежеткалладдрессид**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [**ТСПИ \_ линежеткаллхубтраккинг**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [**ТСПИ \_ линежеткаллидс**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [**ТСПИ \_ линежеткаллинфо**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [**ТСПИ \_ линежеткаллстатус**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [**ТСПИ \_ линежетдевкапс**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [**ТСПИ \_ линежетдевконфиг**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [**ТСПИ \_ линежетекстенсионид**](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [**ТСПИ \_ линежетикон**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [**ТСПИ \_ линежетид**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**ТСПИ \_ линежетлинедевстатус**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [**ТСПИ \_ линежетнумаддрессидс**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [**ТСПИ \_ линехолд**](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [**ТСПИ \_ линемакекалл**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**ТСПИ \_ линемонитордигитс**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [**ТСПИ \_ линемонитормедиа**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [**ТСПИ \_ линемонитортонес**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [**ТСПИ \_ линемспидентифи**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**ТСПИ \_ линенеготиатикстверсион**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [**ТСПИ \_ линенеготиатетспиверсион**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [**ТСПИ \_ линеопен**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [**ТСПИ \_ линепарк**](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [**ТСПИ \_ линепиккуп**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**ТСПИ \_ линепрепареаддтоконференце**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**ТСПИ \_ линерецеивемспдата**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**ТСПИ \_ линередирект**](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [**ТСПИ \_ линерелеасеусерусеринфо**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [**ТСПИ \_ линеремовефромконференце**](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [**ТСПИ \_ линесекурекалл**](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [**ТСПИ \_ линеселектекстверсион**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [**ТСПИ \_ линесендусерусеринфо**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [**ТСПИ \_ линесетаппспеЦифик**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [**ТСПИ \_ линесеткаллдата**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**ТСПИ \_ линесеткаллхубтраккинг**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [**ТСПИ \_ линесеткаллпарамс**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [**ТСПИ \_ линесеткаллкуалитйофсервице**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**ТСПИ \_ линесеткаллтреатмент**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [ТСПИ \_ линесеткуррентлокатион](tspi-linesetcurrentlocation.md)
-   [**ТСПИ \_ линесетдефаултмедиадетектион**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [**ТСПИ \_ линесетдевконфиг**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [**ТСПИ \_ линесетлинедевстатус**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**ТСПИ \_ линесетмедиаконтрол**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [**ТСПИ \_ линесетмедиамоде**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [**ТСПИ \_ линесетстатусмессажес**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [**ТСПИ \_ линесеттерминал**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [**ТСПИ \_ линесетупконференце**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**ТСПИ \_ линесетуптрансфер**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**ТСПИ \_ линесвафолд**](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [**ТСПИ \_ линеункомплетекалл**](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [**ТСПИ \_ линеунхолд**](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [**ТСПИ \_ линеунпарк**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
