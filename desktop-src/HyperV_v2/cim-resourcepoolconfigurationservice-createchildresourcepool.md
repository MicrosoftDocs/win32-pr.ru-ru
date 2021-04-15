---
description: Запуск задания для создания подпула из родительского пула с указанными параметрами выделения.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Метод Креатечилдресаурцепул класса CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4e709fd240c849581f6dcd343001a9b1dee7003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662476"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Метод Креатечилдресаурцепул \_ класса CIM ресаурцепулконфигуратионсервице

Запуск задания для создания подпула из родительского пула с указанными параметрами выделения.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ElementName* \[ окне\]
</dt> <dd>

Имя, соответствующее конечному пользователю для создаваемого пула. Если **значение равно NULL**, можно использовать имя по умолчанию, предоставляемое системой. Значение будет храниться в свойстве **ElementName** для созданного элемента.

</dd> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Строка, содержащая представление экземпляра [**CIM типа \_**](cim-settingdata.md) "Категория", который используется для указания параметров дочернего пула.

</dd> <dt>

*Парентпул* \[ окне\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) , из которого создается новый пул.

</dd> <dt>

*Пул* \[ заполняет\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) , который ссылается на полученный пул.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Ссылка на задание (может иметь значение null, если задание завершено).

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

 

 




