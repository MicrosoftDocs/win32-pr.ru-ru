---
description: Справочник по скриптам WMI содержит определения для API сценариев WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API сценариев для инструментария WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35045aa8528c5a3c27475fff753478bd2202d9137cec6b019039aac52775f70a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640544"
---
# <a name="scripting-api-for-wmi"></a>API сценариев для инструментария WMI

Справочник по скриптам WMI содержит определения для API сценариев WMI. используйте этот API при написании приложений с помощью Microsoft Visual Basic, Visual Basic для приложений, Visual Basic scripting Edition (VBScript) или любого другого языка сценариев, поддерживающего активные технологии сценариев.

> [!Note]  
> PowerShell также доступен для создания сценариев с помощью инструментария WMI. Командлет Get-WMI и три типа ускорителей ( \[ WMI \] , \[ WMICLASS \] и \[ вмисеарчер \] ) обеспечивают базовый административный доступ к инструментарию WMI. Дополнительные сведения см. [в разделе Создание скриптов с помощью Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

Объекты сценариев WMI, за исключением [**SWbemDateTime**](swbemdatetime.md) , не помечены как "надежные" для сценариев, выполняющихся на HTML-страницах в Internet Explorer. Таким образом, если уровень безопасности в Internet Explorer не будет сокращен, сценарий завершится ошибкой. **SWbemDateTime** помечен как надежный для инициализации и создания сценариев. Тем не менее, используйте все объекты сценариев WMI в вызовах **GetObject** и **CreateObject** для кода на стороне сервера в Active Server Pages (ASP).

-   [Объектная модель API сценариев](scripting-api-object-model.md)
-   [Соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md)
-   [Создание скриптов для объектов API](scripting-api-objects.md)
-   [Константы API скриптов](scripting-api-constants.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по инструментарию WMI](wmi-reference.md)
</dt> <dt>

[Коды возврата WMI](wmi-return-codes.md)
</dt> </dl>

 

 



