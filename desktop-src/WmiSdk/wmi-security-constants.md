---
description: WMI проверяет права доступа для приложений и скриптов.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Константы безопасности WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272429"
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

 

 
