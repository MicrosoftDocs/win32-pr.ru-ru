---
description: '\_Класс WMI взаимосвязей Win32 лоадордерграупсервицедепенденЦиес связывает базовую службу и группу порядка загрузки, от которой зависит служба, чтобы начать выполнение.'
ms.assetid: 56739b80-9028-4a2e-85ed-973a078860c1
ms.tgt_platform: multiple
title: Класс Win32_LoadOrderGroupServiceDependencies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceDependencies
- Win32_LoadOrderGroupServiceDependencies.Antecedent
- Win32_LoadOrderGroupServiceDependencies.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55684bb5382c5e253c8f72b929674b9730ba7cab51a6c0cae9c27946fad5ff8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085794"
---
# <a name="win32_loadordergroupservicedependencies-class"></a>\_Класс Win32 лоадордерграупсервицедепенденЦиес

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ лоадордерграупсервицедепенденЦиес** связывает базовую службу и группу порядка загрузки, от которой зависит служба, чтобы начать выполнение.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceDependencies : CIM_Dependency
{
  Win32_LoadOrderGroup REF Antecedent;
  Win32_BaseService    REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ лоадордерграупсервицедепенденЦиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ лоадордерграупсервицедепенденЦиес** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ лоадордерграуп**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ лоадордерграуп")
</dt> </dl>

Ссылка на экземпляр, представляющий свойства группы порядка загрузки, которые должны быть запущены до запуска зависимой базовой службы этого класса.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ басесервице**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ басесервице")
</dt> </dl>

Ссылка на экземпляр, представляющий свойства базовой службы, зависящие от группы порядка загрузки, с которой начинается выполнение.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ лоадордерграупсервицедепенденЦиес** является производным от [**\_ зависимости CIM**](cim-dependency.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

