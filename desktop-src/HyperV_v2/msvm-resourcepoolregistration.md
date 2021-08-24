---
description: Регистрирует службу, которая предоставляет объекты, связанные с пулом глобальных ресурсов.
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Класс Msvm_ResourcePoolRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bbcb0f2e3d5b0dfad884572c90f889d28e47fcffaf328b39d78f02d4c2baa3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535475"
---
# <a name="msvm_resourcepoolregistration-class"></a>\_Класс мсвм ресаурцепулрегистратион

Регистрирует службу, которая предоставляет объекты, связанные с пулом глобальных ресурсов.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ ресаурцепулрегистратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ ресаурцепулрегистратион** имеет следующие свойства.

<dl> <dt>

**Компонент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ ресаурцепулкомпонент**](msvm-resourcepoolcomponent.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр, описывающий COM-объект, реализующий этот класс.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ ресаурцетипедефинитион**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр, описывающий тип ресурса, поддерживаемый службой. Это свойство наследуется от [**мсвм \_ виртуализатионкомпонентрегистратион**](msvm-virtualizationcomponentregistration.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ ресаурцепулрегистратион мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Окончание поддержки клиента<br/>    | Windows 8.1<br/>                                                                                  |
| Поддержка конца сервера<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Мсвм \_ виртуализатионкомпонентрегистратион**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[**Мсвм \_ виртуализатионкомпонентрегистратион**](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

