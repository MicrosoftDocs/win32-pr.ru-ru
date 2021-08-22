---
description: Используется функцией Шжетсетсеттингс для указания того, какие члены структуры ШЕЛЛСТАТЕ должны быть установлены или массивах.
title: Константы ССФ (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2a883110-fdc3-4451-9e47-e58894600e3b
api_name:
- SSF_SHOWALLOBJECTS
- SSF_SHOWEXTENSIONS
- SSF_HIDDENFILEEXTS
- SSF_SERVERADMINUI
- SSF_SHOWCOMPCOLOR
- SSF_SORTCOLUMNS
- SSF_SHOWSYSFILES
- SSF_DOUBLECLICKINWEBVIEW
- SSF_SHOWATTRIBCOL
- SSF_DESKTOPHTML
- SSF_WIN95CLASSIC
- SSF_DONTPRETTYPATH
- SSF_MAPNETDRVBUTTON
- SSF_SHOWINFOTIP
- SSF_HIDEICONS
- SSF_NOCONFIRMRECYCLE
- SSF_FILTER
- SSF_WEBVIEW
- SSF_SHOWSUPERHIDDEN
- SSF_SEPPROCESS
- SSF_NONETCRAWLING
- SSF_STARTPANELON
- SSF_SHOWSTARTPAGE
- SSF_AUTOCHECKSELECT
- SSF_ICONSONLY
- SSF_SHOWTYPEOVERLAY
- SSF_SHOWSTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c022b1d93cb411f0cce73822a47f2d8f85b30e8093bbe2064fb3c50eab5c4870
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967943"
---
# <a name="ssf-constants"></a>Константы ССФ

Используется функцией [**шжетсетсеттингс**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings) для указания того, какие члены структуры [**шеллстате**](/windows/win32/api/shlobj_core/ns-shlobj_core-shellstatea) должны быть установлены или массивах.

<dl> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**ССФ \_ шоваллобжектс**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Запрашивается элемент **фшоваллобжектс** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**ССФ \_ шовекстенсионс**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Запрашивается элемент **фшовекстенсионс** .


</dt> </dl> </dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**ССФ \_ хидденфиликстс**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Не используется.


</dt> </dl> </dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**ССФ \_ серверадминуи**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Не используется.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**ССФ \_ шовкомпколор**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Запрашивается элемент **фшовкомпколор** .


</dt> </dl> </dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**ССФ \_ сортколумнс**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Запрашиваются члены **лпарамсорт** и **исортдиректион** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**ССФ \_ шовсисфилес**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Запрашивается элемент **фшовсисфилес** .


</dt> </dl> </dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**ССФ \_ даублекликкинвебвиев**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Запрашивается элемент **фдаублекликкинвебвиев** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**ССФ \_ шоваттрибкол**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Запрашивается элемент **фшоваттрибкол** .

**Windows Vista:** Не используется.


</dt> </dl> </dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**ССФ \_ десктофтмл**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Запрашивается элемент **фдесктофтмл** . Набор недоступен. вместо этого для версий Windows, выпущенных до Windows XP, включите класс desktop HTML, [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop). однако использование **иактиведесктоп** для этой цели не рекомендуется для Windows XP и более поздних версий Windows и является устаревшим в Windows Vista.


</dt> </dl> </dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**ССФ \_ WIN95CLASSIC**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Запрашивается элемент **fWin95Classic** .


</dt> </dl> </dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**ССФ \_ донтпреттипас**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Запрашивается элемент **фдонтпреттипас** .


</dt> </dl> </dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**ССФ \_ мапнетдрвбуттон**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Запрашивается элемент **фмапнетдрвбтн** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**ССФ \_ шовинфотип**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Запрашивается элемент **фшовинфотип** .


</dt> </dl> </dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**ССФ \_ хидеиконс**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Запрашивается элемент **фхидеиконс** .


</dt> </dl> </dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**ССФ \_ ноконфирмрецикле**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Запрашивается элемент **фноконфирмрецикле** .


</dt> </dl> </dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**\_Фильтр ССФ**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Запрашивается элемент **ффилтер** .

**Windows Vista:** Не используется.


</dt> </dl> </dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**ССФ \_ WebView**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Запрашивается элемент **фвебвиев** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**ССФ \_ шовсуперхидден**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Запрашивается элемент **фшовсуперхидден** .


</dt> </dl> </dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**ССФ \_ сеппроцесс**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Запрашивается элемент **фсеппроцесс** .


</dt> </dl> </dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**ССФ \_ нонеткравлинг**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



**Windows XP и более поздних версий**. Запрашивается элемент **фнонеткравлинг** .


</dt> </dl> </dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**ССФ \_ стартпанелон**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



**Windows XP и более поздних версий**. Запрашивается элемент **фстартпанелон** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**ССФ \_ шовстартпаже**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Не используется.


</dt> </dl> </dd> <dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**ССФ \_ ауточеккселект**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



**Windows Vista и более поздних версий**. Запрашивается элемент **фауточеккселект** .


</dt> </dl> </dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**ССФ \_ иконсонли**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



**Windows Vista и более поздних версий**. Запрашивается элемент **фиконсонли** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**ССФ \_ шовтипеоверлай**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



**Windows Vista и более поздних версий**. Запрашивается элемент **фшовтипеоверлай** .


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTATUSBAR"></span><span id="ssf_showstatusbar"></span>**ССФ \_ шовстатусбар**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



**Windows 8 и более поздних версий**: запрашивается элемент **фшовстатусбар** .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
