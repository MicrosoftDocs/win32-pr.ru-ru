---
description: Блокирует и разблокирует носитель в устройстве, доступном для перемещения.
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: Метод Локкмедиа класса CIM_MediaAccessDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12c4aa6c6ba9e57a2ab88e58624b246fb98065f3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104081679"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a>Метод Локкмедиа \_ класса CIM медиаакцессдевице

Блокирует и разблокирует носитель в устройстве, доступном для перемещения.

## <a name="syntax"></a>Синтаксис


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Блокировка* \[ окне\]
</dt> <dd>

Если **значение — true**, блокирует носитель. Если **значение равно false**, освобождает носитель.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_МЕДИААКЦЕССДЕВИЦЕ CIM**](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




