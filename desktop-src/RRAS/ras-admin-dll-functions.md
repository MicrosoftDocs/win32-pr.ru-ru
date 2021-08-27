---
title: Функции DLL администрирования RAS
description: Библиотека DLL администрирования RAS должна реализовывать и экспортировать все следующие функции.
ms.assetid: bf2bd4d4-6da2-471e-843c-c0f0563d3795
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d4ed327cf3114ec4bf7844518f3c1500845450021f80bbd59ddd642de9eeac1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036394"
---
# <a name="ras-administration-dll-functions"></a>Функции DLL администрирования RAS

Библиотека DLL администрирования RAS должна реализовывать и экспортировать все следующие функции:

-   [**мпрадминакцептневлинк**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)
-   [**Мпрадминакцептреаусентикатион**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthentication) или [ **мпрадминакцептреаусентикатионекс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptreauthenticationex)
-   [**Мпрадмининитиализедлл**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) или [ **мпрадмининитиализедллекс**](/windows/win32/api/mprapi/nf-mprapi-mpradmininitializedllex)
-   [**мпрадминлинкхангупнотификатион**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)
-   [**мпрадминтерминатедлл**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

**Windows 2000/NT:** Библиотека DLL администрирования RAS должна также реализовывать и экспортировать следующую пару функций: [**мпрадминжетипаддрессфорусер**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) и [**мпрадминрелеасеипаддресс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) .

Кроме того, Библиотека DLL администрирования RAS должна реализовать и экспортировать одну из следующих пар функций:

-   [**Мпрадминакцептневконнектион**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) и [ **мпрадминконнектионхангупнотификатион**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)
-   [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) и [ **MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)
-   [**MprAdminAcceptNewConnection3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection3) и [ **MprAdminConnectionHangupNotification3**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification3)
-   [**Мпрадминакцептневконнектионекс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnectionex) и [ **мпрадминконнектионхангупнотификатионекс**](/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotificationex)

Если одна из требуемых функций не реализована, служба удаленного доступа не запускается.

Библиотека DLL администрирования не требуется для реализации следующих пар функций:

-   [**Мпрадминжетипаддрессфорусер**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) и [ **мпрадминрелеасеипаддресс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)
-   [*MprAdminGetIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipv6addressforuser) и [ *MprAdminReleaseIpv6AddressForUser*](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipv6addressforuser)

Однако если библиотека DLL реализует одну функцию в приведенной выше паре, она должна также реализовать другую функцию в паре.

Дополнительные сведения о библиотеках DLL администрирования службы удаленного доступа см. в разделе Обзор, [Библиотека DLL администрирования RAS](ras-administration-dll.md).

 

 