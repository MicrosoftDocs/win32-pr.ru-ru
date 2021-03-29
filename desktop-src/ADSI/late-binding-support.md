---
title: Поддержка поздних привязок
description: Если установлена поддержка позднего связывания, каждый вызов функции должен пройти через интерфейс ADSI IDispatch, прежде чем перенаправлять его в соответствующее расширение.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- расширения ADSI, поддержка поздних привязок
- ADSI ADSI, пример кода Visual Basic, поддержка позднего связывания
- Привязка AD, поддержка позднего связывания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e4dd1de0000d9edbe3e73cbc47b81d094d48c2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793884"
---
# <a name="late-binding-support"></a>Поддержка поздних привязок

Если установлена поддержка позднего связывания, каждый вызов функции должен пройти через интерфейс ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , прежде чем перенаправлять его в соответствующее расширение.

Рассмотрим следующий пример кода.


```C++
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
 
x.MyNewMethod( "\\srv\public")
x.MyProperty = "Hello World"
 
x.OtherMethod()
x.OtherProperty = 4362
 
Debug.Print x.LastName
```



Нет явных вызовов метода **QueryInterface** для получения расширений. Расширения должны перенаправлять свои вызовы [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в интерфейс ADSI **IDispatch** . ADSI принимает решение и разрешает любые возникающие конфликты, а затем перенаправляет обратно в соответствующее расширение с помощью интерфейса с именем [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension). Таким образом, любое расширение, которое поддерживает позднее связывание, должно реализовывать **иадсекстенсион**.

 

 