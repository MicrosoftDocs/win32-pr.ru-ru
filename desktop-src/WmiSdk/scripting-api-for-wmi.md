---
description: Справочник по скриптам WMI содержит определения для API сценариев WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API сценариев для инструментария WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898566"
---
# <a name="scripting-api-for-wmi"></a>API сценариев для инструментария WMI

Справочник по скриптам WMI содержит определения для API сценариев WMI. Используйте этот API при написании приложений с помощью Microsoft Visual Basic, Visual Basic для приложений, Visual Basic Scripting Edition (VBScript) или любого другого языка сценариев, поддерживающего активные технологии сценариев.

> [!Note]  
> PowerShell также доступен для создания сценариев с помощью инструментария WMI. Командлет Get-WMI и три типа ускорителей ( \[ WMI \] , \[ WMICLASS \] и \[ вмисеарчер \] ) обеспечивают базовый административный доступ к инструментарию WMI. Дополнительные сведения см. [в разделе Создание сценариев с помощью Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

Объекты сценариев WMI, за исключением [**SWbemDateTime**](swbemdatetime.md) , не помечены как "надежные" для сценариев, выполняющихся на HTML-страницах в Internet Explorer. Таким образом, если уровень безопасности в Internet Explorer не будет сокращен, сценарий завершится ошибкой. **SWbemDateTime** помечен как надежный для инициализации и создания сценариев. Тем не менее, используйте все объекты сценариев WMI в вызовах **GetObject** и **CreateObject** для кода на стороне сервера в Active Server Pages (ASP).

-   [Объектная модель API сценариев](scripting-api-object-model.md)
-   [Соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md)
-   [Создание скриптов для объектов API](scripting-api-objects.md)
-   [Константы API скриптов](scripting-api-constants.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по инструментарию WMI](wmi-reference.md)
</dt> <dt>

[Коды возврата WMI](wmi-return-codes.md)
</dt> </dl>

 

 



