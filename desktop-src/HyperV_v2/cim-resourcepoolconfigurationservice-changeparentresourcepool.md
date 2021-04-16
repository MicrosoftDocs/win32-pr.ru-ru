---
description: Запуск задания для изменения родительского пула с указанными параметрами выделения.
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: Метод Чанжепарентресаурцепул класса CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.ChangeParentResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6ef852d6af8f0973b6b3f29fca5fcd90e9ce726a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682814"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Метод Чанжепарентресаурцепул \_ класса CIM ресаурцепулконфигуратионсервице

Запуск задания для изменения родительского пула с указанными параметрами выделения.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ChangeParentResourcePool(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPool[],
  [in]  string               Settings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Чилдпул* \[ окне\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) , который ссылается на дочерний пул.

</dd> <dt>

*Парентпул* \[ окне\]
</dt> <dd>

Массив [**CIM \_ ResourcePool**](cim-resourcepool.md) , который ссылается на родительские пулы.

</dd> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Необязательная строка, содержащая представление [**экземпляра \_ CIM**](cim-settingdata.md) типа "Категория", которое используется для указания параметров родительского пула.

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

**Недостаточно ресурсов** (8)
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

 

 




