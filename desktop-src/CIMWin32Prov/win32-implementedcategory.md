---
description: '\_Класс WMI взаимосвязей Win32 имплементедкатегори связывает категорию компонента и класс модели COM с помощью своих интерфейсов.'
ms.assetid: 7cf32b50-9ae6-44e5-b364-bc74dea3dc17
ms.tgt_platform: multiple
title: Класс Win32_ImplementedCategory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ImplementedCategory
- Win32_ImplementedCategory.Category
- Win32_ImplementedCategory.Component
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d885c8c8e92ea661e06b46f338924355438ff9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807912"
---
# <a name="win32_implementedcategory-class"></a>\_Класс Win32 имплементедкатегори

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ имплементедкатегори** связывает категорию компонента и класс модели COM с помощью своих интерфейсов.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5B-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ImplementedCategory
{
  Win32_ComponentCategory REF Category;
  Win32_ClassicCOMClass   REF Component;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ имплементедкатегори** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ имплементедкатегори** имеет следующие свойства.

<dl> <dt>

**Категория**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ компоненткатегори**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ компоненткатегори")
</dt> </dl>

Ссылка на экземпляр, представляющий категорию компонента, используемую классом COM.

</dd> <dt>

**Компонент**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ классиккомкласс**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ классиккомкласс")
</dt> </dl>

Ссылка на экземпляр, представляющий COM-класс, используя связанную категорию.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

