---
description: Блокирует или освобождает носитель.
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
ms.openlocfilehash: 650a868d8e25e2ccc47271e49634827fe7d3d967
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157039"
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
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ двддриве**](msvm-dvddrive.md)
</dt> </dl>

 

 




