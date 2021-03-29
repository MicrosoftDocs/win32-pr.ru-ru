---
description: '\_Класс WMI взаимосвязей Win32 шаретодиректори связывает общий ресурс в компьютерной системе и каталог, с которым он сопоставлен.'
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Класс Win32_ShareToDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807018"
---
# <a name="win32_sharetodirectory-class"></a>\_Класс Win32 шаретодиректори

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ шаретодиректори** связывает общий ресурс в компьютерной системе и каталог, с которым он сопоставлен.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ шаретодиректори** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ шаретодиректори** имеет следующие свойства.

<dl> <dt>

**Предоставить общий доступ**
</dt> <dd> <dl> <dt>

Тип данных: **\_ общий ресурс Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \_ общий ресурс Win32 WMI")
</dt> </dl>

Ссылка на экземпляр, представляющий свойства общего ресурса, доступного через каталог.

</dd> <dt>

**шаределемент**
</dt> <dd> <dl> <dt>

Тип данных: **\_ Каталог CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ Directory")
</dt> </dl>

Ссылка на экземпляр, представляющий свойства каталога, сопоставленного с общим ресурсом.

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

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
