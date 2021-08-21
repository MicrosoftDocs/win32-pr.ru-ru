---
description: Содержит объект приложения коллекции элементов папки.
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: Свойство Фолдеритемс. Application (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3809d76576b69c53f6fc5f8a11ab954242e3a89c9a369ada2f4fa47c460f523f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032612"
---
# <a name="folderitemsapplication-property"></a>Фолдеритемс. Application, свойство

Содержит объект **приложения** коллекции элементов папки.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a>Значение свойства

Ссылка на объект приложения.

## <a name="remarks"></a>Remarks

Свойство **Application** возвращает объект автоматизации, поддерживаемый приложением, которое содержит элемент управления WebBrowser, если этот объект доступен. В противном случае это свойство возвращает объект автоматизации элемента управления WebBrowser.

это свойство можно использовать с командами **Set** и **CreateObject** или с помощью команды **getobject** для создания экземпляра Windows приложения Internet Explorer и управления им.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 




