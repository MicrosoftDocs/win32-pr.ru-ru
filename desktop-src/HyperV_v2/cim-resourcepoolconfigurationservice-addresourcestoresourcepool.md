---
description: Запускает задание по добавлению ресурсов в пул ресурсов.
ms.assetid: b163619a-19bd-43d7-ba35-ec4bd8192100
title: Метод Аддресаурцесторесаурцепул класса CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.AddResourcesToResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55191f3ddce5672d1b76987b8a7c2ce1f87b9cca330a7ba14aa4ae10bacc5b67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980934"
---
# <a name="addresourcestoresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Метод Аддресаурцесторесаурцепул \_ класса CIM ресаурцепулконфигуратионсервице

Запускает задание по добавлению ресурсов в пул ресурсов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 AddResourcesToResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Хостресаурцес* \[ окне\]
</dt> <dd>

Массив экземпляров [**CIM \_**](cim-logicaldevice.md) , добавляемых в пул.

</dd> <dt>

*Пул* \[ окне\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) , представляющий пул, в который добавляются ресурсы.

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

**Размер не поддерживается** (4097)
</dt> <dt>

**Метод зарезервирован** (4098.. 32767)
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

 

 




