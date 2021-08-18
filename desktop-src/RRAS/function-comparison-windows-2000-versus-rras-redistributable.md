---
title: сравнение функций Windows 2000 и распространяемый компонент RRAS
description: API RAS распространяется как компонент Windows 2000 и более поздних операционных систем и доступен в качестве распространяемого для Windows NT 4,0 с пакетом обновления 3 (sp3) и более ранних версий.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027c120133573b1d0c452b74dd02ab8fa0aa6f3367eb1a5fc9668a2de089c758
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995344"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a>сравнение функций: Windows 2000 и распространяемый компонент RRAS

API RAS распространяется как компонент Windows 2000 и более поздних операционных систем и доступен в качестве распространяемого для Windows NT 4,0 с пакетом обновления 3 (sp3) и более ранних версий. Служба RAS предоставляет те же функциональные возможности, что и в обеих формах, но используемое соглашение об именовании отличается для элементов ссылок в каждой версии API службы RAS.

функции RAS для Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранними версиями обычно начинаются с префикса "расадмин". Аналогичные функции службы маршрутизации и удаленного доступа (RRAS) начинаются с префикса "Мпрадмин". Например, служба RAS предоставляет функцию с именем [**расадминпортжетинфо**](rasadminportgetinfo.md). Аналогичная функция в RRAS называется [**мпрадминпортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo). Как и тот же пример, служба RAS предоставляет функцию обратного вызова [**расадминжетипаддрессфорусер**](rasadmingetipaddressforuser.md). RRAS предоставляет аналогичную функцию обратного вызова с именем [**мпрадминжетипаддрессфорусер**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser). Исключениями из этого правила являются [**расадминпортклеарстатистикс**](rasadminportclearstatistics.md), для которых в качестве RRAS используется [**Мпрадминпортклеарстатс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), а [**расадминфрибуффер**](rasadminfreebuffer.md)— [**мпрадминбуфферфри**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).

в следующей таблице перечислены функции RAS Windows NT 4,0 с пакетом обновления 3 (SP3) и соответствующие функции RRAS.



| Windows NT 4,0 RAS                                                                   | УДАЛЕННОГО                                                                                 |
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



 

несмотря на то, что функции rras похожи на их Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранними аналогами службы удаленного доступа, функции rras часто используют разные наборы параметров. Полные сведения о списке параметров этой функции см. на странице справки по определенной функции.

распространяемый компонент RRAS для Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранних версий добавляет следующие функции, которые не имеют аналогов для RAS:

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

в дополнение к предыдущим функциям Windows 2000 и более поздних операционных систем добавляют следующие функции:

[**мпрадминсендусермессаже**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




