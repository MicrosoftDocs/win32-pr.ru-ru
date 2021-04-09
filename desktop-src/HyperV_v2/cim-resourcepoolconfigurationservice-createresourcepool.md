---
description: Запускает задание для создания корневого ResourcePool. Область ResourcePool будет соответствовать той же системе, что и эта служба.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Метод CreateResourcePool класса CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810336"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Метод CreateResourcePool \_ класса CIM ресаурцепулконфигуратионсервице

Запускает задание для создания корневого ResourcePool. Область ResourcePool будет соответствовать той же системе, что и эта служба.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ElementName* \[ окне\]
</dt> <dd>

Имя, соответствующее конечному пользователю для создаваемого пула. Если **значение равно NULL**, можно использовать имя по умолчанию, предоставляемое системой. Значение будет храниться в свойстве **ElementName** для созданного пула.

</dd> <dt>

*Хостресаурцес* \[ окне\]
</dt> <dd>

Массив из нуля или более [**устройств \_ типа CIM**](cim-logicaldevice.md) , которые используются для создания пула или изменения исходных экстентов. Все элементы в массиве должны быть одного типа.

</dd> <dt>

*ResourceType* \[ окне\]
</dt> <dd>

Тип ресурсов, которыми будет управлять созданный пул. Если *хостресаурцес* содержит элементы, это свойство должно иметь свой тип.

</dd> <dt>

*Пул* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает ссылку на полученный [**\_ ResourcePool CIM**](cim-resourcepool.md). При возвращении задания это может быть **значение NULL**. в этом случае клиент должен использовать задание, чтобы найти результирующий ResourcePool после завершения задания.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Ссылка на [**CIM \_ конкретежоб**](cim-concretejob.md) , представляющий задание (может иметь значение null, если задание завершено).

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

**Размер не поддерживается** (4097)
</dt> <dt>

**Метод зарезервирован** (4098.. 32767)
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

[**\_РЕСАУРЦЕПУЛКОНФИГУРАТИОНСЕРВИЦЕ CIM**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




