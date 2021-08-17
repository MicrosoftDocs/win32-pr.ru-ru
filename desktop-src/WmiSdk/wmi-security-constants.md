---
description: WMI проверяет права доступа для приложений и скриптов.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Константы безопасности WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2f3a8ff4727852637fe6e4b808f0b8d3a74c958808cb3beb7bc9df32b0c995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739421"
---
# <a name="wmi-security-constants"></a>Константы безопасности WMI

WMI проверяет права доступа для приложений и скриптов для таких объектов, как пространства имен WMI, принтер, службы, приложения DCOM, файлы, общие папки и другие защищаемые объекты. Доступ к этим защищаемым объектам контролируется записями управления доступом (ACE). Каждый элемент ACE содержит списки, которые определяют, к каким группам или пользователям имеет доступ. Дополнительные сведения о списках управления доступом и безопасности (ACL, DACL и SACL) см. в разделе [списки управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) и [дескрипторы безопасности](/windows/desktop/SecAuthZ/security-descriptors).

Многие методы поставщика в WMI, которые влияют на защищаемые объекты, требуют, чтобы администратор включил определенные привилегии. Какая версия привилегий, которую вы используете, зависит от языка программирования, как показано в [**константах прав**](privilege-constants.md).

Константы безопасности определяются в следующих разделах:

-   [**Константы безопасности событий**](event-security-constants.md)
-   [**Константы прав доступа к файлам и каталогам**](file-and-directory-access-rights-constants.md)
-   [**Константы прав доступа к пространству имен**](namespace-access-rights-constants.md)
-   [**Константы флагов пространства имен ACE**](namespace-ace-flag-constants.md)
-   [**Константы типа ACE пространства имен**](namespace-ace-type-constants.md)
-   [**Константы прав доступа**](privilege-constants.md)

 

 
