---
description: Связывает заголовку видео с видеоадаптером, который его содержит.
ms.assetid: d15f4350-1529-4246-9ea2-8453e52516c6
title: Класс CIM_VideoHeadOnController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHeadOnController
- CIM_VideoHeadOnController.Antecedent
- CIM_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18178e6d9d7f1e684af1d4fe74336e1f2a02eedc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662806"
---
# <a name="cim_videoheadoncontroller-class"></a>\_Класс CIM видеохеадонконтроллер

Связывает заголовку видео с видеоадаптером, который его содержит.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHeadOnController : CIM_HostedDependency
{
  CIM_DisplayController REF Antecedent;
  CIM_VideoHead         REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ видеохеадонконтроллер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ видеохеадонконтроллер** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ дисплайконтроллер**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Видеоадаптер, включающий головную карту.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ видеохеад**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Головной элемент видеоадаптера.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ХОСТЕДДЕПЕНДЕНЦИ CIM**](cim-hosteddependency.md)
</dt> </dl>

 

