---
description: Извлекает ошибку из-за невыполненного задания.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: Метод method класса CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aa9ed87f2d484286d91d14c4183d2ce3b6f41cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682953"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a>Метод \_ конкретежоб класса CIM

Извлекает ошибку из-за невыполненного задания. При выполнении или завершении задания без ошибок этот метод не возвращает экземпляр [**\_ ошибки CIM**](cim-error.md) . Однако если задание завершилось сбоем из-за внутренней проблемы или из-за завершения задания клиентом, то возвращается экземпляр **\_ ошибки CIM** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ошибка при* \[ заполняет\]
</dt> <dd>

Возвращает экземпляр [**\_ ошибки CIM**](cim-error.md) , если **OperationalStatus** в задании не имеет значение "ОК"; в противном случае возвращает **null**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.

<dl> <dt>

**Успешно** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Неопределенная ошибка** (2)
</dt> <dt>

**Время ожидания** (3)
</dt> <dt>

**Сбой** (4)
</dt> <dt>

**Недопустимый параметр** (5)
</dt> <dt>

**Отказано в доступе** (6)
</dt> <dt>

**Зарезервировано DMTF** (..)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
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

[**\_КОНКРЕТЕЖОБ CIM**](cim-concretejob.md)
</dt> </dl>

 

 




