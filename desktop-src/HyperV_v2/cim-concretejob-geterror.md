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
ms.openlocfilehash: 0b43d433bf9d2a3967efcc4a2e927d3bf687ebfa5ac67d7c7e34c48c34832c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813270"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_КОНКРЕТЕЖОБ CIM**](cim-concretejob.md)
</dt> </dl>

 

 




