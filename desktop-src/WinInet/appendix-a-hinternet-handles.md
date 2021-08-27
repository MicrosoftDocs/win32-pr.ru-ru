---
title: Дескрипторы ХИНТЕРНЕТ
description: В этом разделе содержатся сведения об дескрипторах, используемых функциями WinINet и иерархией, в которой они работают.
ms.assetid: 8a9788ed-eb25-42cb-b912-8dffa3df1850
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477558887ac484ec0c3645d568bc3d91d29926af887ebadc51cf7e9523da787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051935"
---
# <a name="hinternet-handles"></a>Дескрипторы ХИНТЕРНЕТ

В этом разделе содержатся сведения об дескрипторах, используемых функциями WinINet и иерархией, в которой они работают.

-   [О дескрипторах ХИНТЕРНЕТ](#about-hinternet-handles)
-   [Иерархия маркеров](#handle-hierarchy)
-   [Иерархия FTP](#ftp-hierarchy)
-   [Иерархия HTTP](#http-hierarchy)

## <a name="about-hinternet-handles"></a>О дескрипторах ХИНТЕРНЕТ

Дескрипторы, создаваемые и используемые функциями WinINet, имеют тип **хинтернет**. Функции WinINet возвращают дескрипторы **хинтернет** , которые не взаимозаменяемы с другими типами дескрипторов. Поэтому их нельзя использовать с такими функциями, как [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) или [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). Аналогично, другие типы обработчиков нельзя использовать с функциями WinINet. Например, маркер, возвращаемый [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , не может быть передан в [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).

Функция [**интернетклосехандле**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) закрывает дескрипторы типа **хинтернет**. Обратите внимание, что значения обработчика быстро перезапускаются. Поэтому при закрытии обработчика и немедленном создании нового маркера существует хороший шанс того, что новый обработчик будет иметь то же значение, что и только что закрытый обработчик.

## <a name="handle-hierarchy"></a>Иерархия маркеров

Дескрипторы **хинтернет** поддерживаются в древовидной иерархии. Маркер, возвращаемый функцией [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , является корневым узлом. Дескрипторы, возвращаемые функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , занимают следующий уровень. Дескрипторы, возвращаемые функциями [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)и [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) , являются конечными узлами.

**Windows XP и Windows Server 2003 R2 и более ранних версий:** Дескрипторы, возвращаемые, [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)и [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) , также являются конечными узлами.

На следующей схеме показана иерархия дескрипторов **хинтернет** . Каждое поле на схеме представляет функцию, которая возвращает маркер **хинтернет** .

![функции, создающие дескрипторы](images/ax-wnt01.png)

На верхнем уровне находится функция [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , которая создает корневой маркер. Следующий уровень содержит функции [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) и [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) . Функции, использующие маркер, возвращенный [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , составляют последний уровень.

На следующей диаграмме показаны функции, зависящие от маркера, созданного с помощью [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla). Затененные поля представляют функции, которые возвращают дескрипторы **хинтернет** , а обычные поля представляют функции, использующие дескриптор **хинтернет** , созданный связанной функцией.

![функции, использующие маркер интернетопенурл](images/ax-wnt02.png)

Функции [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)и [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) используют маркер **хинтернет** , созданный [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

## <a name="ftp-hierarchy"></a>Иерархия FTP

На следующей диаграмме показаны функции FTP, зависящие от обработчика сеанса FTP, возвращаемого функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Затененные поля представляют функции, которые возвращают дескрипторы **хинтернет** , а обычные поля представляют функции, использующие дескриптор **хинтернет** , созданный функцией, от которой они зависят.

![функции, использующие обработчик сеанса FTP](images/ax-wnt06.png)

Функции [**фтпкреатедиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**фтпделетефиле**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea), [**фтпжеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**Фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**фтпремоведиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)и [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) используют обработчик **HINTERNET** , созданный [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).

На следующей диаграмме показаны две функции FTP, которые возвращают дескрипторы и зависящие от них функции. Затененные поля представляют функции, которые возвращают дескрипторы **хинтернет** , а обычные поля представляют функции, использующие дескриптор **хинтернет** , созданный функцией, от которой они зависят.

![функции, использующие маркер из фтпопен и фтпфиндфирстфиле](images/ax-wnt03.png)

Функция [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) зависит от маркера, созданного [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), тогда как [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) и [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) используют маркер, созданный [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).

## <a name="http-hierarchy"></a>Иерархия HTTP

На следующей диаграмме показаны связи функций, используемых для протокола HTTP. Затененные поля представляют функции, которые возвращают дескрипторы **хинтернет** , а обычные поля представляют функции, использующие дескриптор **хинтернет** , созданный функцией, от которой они зависят.

![функции, использующие маркер из хттпопенрекуест](images/ax-wnt05.png)

Функции [**хттпаддрекуессеадерс**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa), [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa), [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), [**хттпсендрекуестекс**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)и [**Интернетеррордлг**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) зависят от маркера, созданного [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).

На следующей диаграмме показаны функции, использующие маркер **хинтернет** , созданный [**Хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) после отправки [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Затененные поля представляют функции, которые возвращают дескрипторы **хинтернет** , а обычные поля представляют функции, использующие дескриптор **хинтернет** , созданный функцией, от которой они зависят.

![функции, использующие маркер после хттпсендрекуест](images/ax-wnt07.png)

После того как [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) использовал маркер, возвращенный [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), он может использоваться [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)и [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer).

![функции, использующие маркер после хттпсендрекуестекс](images/ax-wnt08.png)

После того как [**хттпсендрекуестекс**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa) использовал маркер, возвращенный [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), этот маркер может использоваться [**хттпендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta), [**интернетреадфиликс**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)и [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile). После вызова [**хттпендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) этот маркер может использоваться [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)и [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable).

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. для серверных реализаций или служб используйте [Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 