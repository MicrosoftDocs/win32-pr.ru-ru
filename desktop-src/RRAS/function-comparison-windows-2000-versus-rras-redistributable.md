---
title: Сравнение функций Windows 2000 и распространяемого компонента RRAS
description: API RAS распространяется как компонент Windows 2000 и более поздних операционных систем и доступен в качестве распространяемого пакета для Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранних версий.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 745ad0c50654c8269c3e62b03629a7ae12a17476
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105650300"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a>Сравнение функций: Windows 2000 и распространяемый компонент RRAS

API RAS распространяется как компонент Windows 2000 и более поздних операционных систем и доступен в качестве распространяемого пакета для Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранних версий. Служба RAS предоставляет те же функциональные возможности, что и в обеих формах, но используемое соглашение об именовании отличается для элементов ссылок в каждой версии API службы RAS.

Функции RAS для Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранних версий обычно начинаются с префикса "Расадмин". Аналогичные функции службы маршрутизации и удаленного доступа (RRAS) начинаются с префикса "Мпрадмин". Например, служба RAS предоставляет функцию с именем [**расадминпортжетинфо**](rasadminportgetinfo.md). Аналогичная функция в RRAS называется [**мпрадминпортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo). Как и тот же пример, служба RAS предоставляет функцию обратного вызова [**расадминжетипаддрессфорусер**](rasadmingetipaddressforuser.md). RRAS предоставляет аналогичную функцию обратного вызова с именем [**мпрадминжетипаддрессфорусер**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser). Исключениями из этого правила являются [**расадминпортклеарстатистикс**](rasadminportclearstatistics.md), для которых в качестве RRAS используется [**Мпрадминпортклеарстатс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), а [**расадминфрибуффер**](rasadminfreebuffer.md)— [**мпрадминбуфферфри**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).

В следующей таблице перечислены функции RAS Windows NT 4,0 SP3 и соответствующие функции RRAS.



| Служба RAS Windows NT 4,0                                                                   | УДАЛЕННОГО                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**расадминакцептневконнектион**](rasadminacceptnewconnection.md)                   | [**мпрадминакцептневконнектион**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [**расадминконнектионхангупнотификатион**](rasadminconnectionhangupnotification.md) | [**мпрадминконнектионхангупнотификатион**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [**расадминфрибуффер**](rasadminfreebuffer.md)                                     | [**мпрадминбуфферфри**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [**расадминжетеррорстринг**](rasadmingeterrorstring.md)                             | [**мпрадминжетеррорстринг**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [**расадминжетипаддрессфорусер**](rasadmingetipaddressforuser.md)                   | [**мпрадминжетипаддрессфорусер**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [**расадминпортклеарстатистикс**](rasadminportclearstatistics.md)                   | [**мпрадминпортклеарстатс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [**расадминпортдисконнект**](rasadminportdisconnect.md)                             | [**мпрадминпортдисконнект**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [**расадминпортенум**](rasadminportenum.md)                                         | [**мпрадминпортенум**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [**расадминпортжетинфо**](rasadminportgetinfo.md)                                   | [**мпрадминпортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [**расадминрелеасеипаддресс**](rasadminreleaseipaddress.md)                         | [**мпрадминрелеасеипаддресс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [**расадминусержетинфо**](rasadminusergetinfo.md)                                   | [**мпрадминусержетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [**расадминусерсетинфо**](rasadminusersetinfo.md)                                   | [**мпрадминусерсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

Хотя функции RRAS аналогичны функциям Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранним аналогам службы удаленного доступа, функции RRAS часто используют разные наборы параметров. Полные сведения о списке параметров этой функции см. на странице справки по определенной функции.

Распространяемый компонент RRAS для Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранних версий добавляет следующие функции, которые не имеют аналогов для RAS:

[**мпрадминакцептневлинк**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**мпрадминконнектионклеарстатс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[**мпрадминконнектионенум**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[**мпрадминконнектионжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[**мпрадминжетпдксервер**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[**мпрадминиссервицеруннинг**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[**мпрадминлинкхангупнотификатион**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**мпрадминпортресет**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[**мпрадминсерверконнект**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[**мпрадминсервердисконнект**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

Помимо описанных выше функций, Windows 2000 и более поздних операционных систем добавляют следующие функции:

[**мпрадминсендусермессаже**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




