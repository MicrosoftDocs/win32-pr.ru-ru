---
description: Shell. Application свойство — содержит объект приложения объекта.
ms.assetid: 5335f4dd-ca80-49c8-8953-e32a6e6308e0
title: Свойство Shell. Application (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: abab6e19611b927d69746d9b218da73e543f5d592f43baad8362d3406e521f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858135"
---
# <a name="shellapplication-property"></a>Свойство Shell. Application

Содержит объект приложения объекта.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a>Значение свойства

Переменная типа [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , которая получает объект приложения.

## <a name="remarks"></a>Remarks

Свойство **Application** возвращает объект автоматизации, поддерживаемый приложением, которое содержит элемент управления WebBrowser, если этот объект доступен. В противном случае это свойство возвращает объект автоматизации элемента управления WebBrowser.

это свойство можно использовать с командами **Set** и **CreateObject** или с помощью команды **getobject** для создания экземпляра Windows приложения Internet Explorer и управления им.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
