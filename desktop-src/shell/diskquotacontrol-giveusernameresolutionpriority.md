---
description: Помещает указанный объект пользователя в строке для разрешения имен.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Дисккуотаконтрол. Гивеусернамересолутионприорити, метод (Дсккуота. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540466"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a>Дисккуотаконтрол. Гивеусернамересолутионприорити, метод

Помещает указанный объект пользователя в строке для разрешения имен.

## <a name="syntax"></a>Синтаксис


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*аусер* 
</dt> <dd>

Тип: **объект**

Выражение объекта, результатом которого является объект [**дидисккуотаусер**](didiskquotauser-object.md) пользователя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Примечания

Если включено асинхронное разрешение имен, объекты пользователя помещаются в очередь. По умолчанию они обслуживаются в том порядке, в котором они размещены в очереди. Метод **гивеусернамересолутионприорити** перемещает объект на передний план, чтобы он находящихся рядом в строке для обслуживания.

Чтобы включить асинхронное разрешение имен, используйте свойство [**усернамересолутион**](diskquotacontrol-usernameresolution.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Дсккуота. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




