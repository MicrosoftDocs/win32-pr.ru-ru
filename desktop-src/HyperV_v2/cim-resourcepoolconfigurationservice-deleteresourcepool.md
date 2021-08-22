---
description: Запуск задания для удаления пула ресурсов.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Метод Делетересаурцепул класса CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a5fb895eb76a503d6199bf1057a9f9eaff0c72e4af59460c63551a7c581ff0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648093"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Метод Делетересаурцепул \_ класса CIM ресаурцепулконфигуратионсервице

Запуск задания для удаления пула ресурсов. Нет невыполненных выделений, или операция удаления завершится с ошибкой "используется". Если пул ресурсов является корневым пулом ресурсов, все ресурсы узла возвращаются к базовой системе.

## <a name="syntax"></a>Синтаксис


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Пул* \[ окне\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) , ссылающийся на удаляемый пул.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

[**\_ Конкретежоб CIM**](cim-concretejob.md) , который ссылается на задание (может иметь **значение NULL** , если задание завершено).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.

<dl> <dt>

**Задание завершено без ошибок** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Неизвестно** (2)
</dt> <dt>

**Время ожидания** (3)
</dt> <dt>

**Сбой** (4)
</dt> <dt>

**Недопустимый параметр** (5)
</dt> <dt>

**Используется** (6)
</dt> <dt>

**Неверный ResourceType для пула** (7)
</dt> <dt>

**Зарезервировано DMTF** (..)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Метод зарезервирован** (4097.. 32767)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_РЕСАУРЦЕПУЛКОНФИГУРАТИОНСЕРВИЦЕ CIM**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




