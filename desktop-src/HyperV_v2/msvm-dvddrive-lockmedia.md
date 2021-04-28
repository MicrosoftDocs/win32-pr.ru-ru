---
description: Метод Локкмедиа класса Msvm_DVDDrive — блокирует или освобождает носитель.
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Метод Локкмедиа класса Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e00780fbeeeec60563b31008c8e5979a09f9d173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119152"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a>Метод Локкмедиа \_ класса Двддриве мсвм

Блокирует или освобождает носитель.

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

**значение true** , чтобы заблокировать носитель; **значение false** , чтобы освободить носитель.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений:

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Мсвм \_ двддриве**](msvm-dvddrive.md)
</dt> </dl>

 

 




