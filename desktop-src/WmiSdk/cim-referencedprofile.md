---
description: Используется для связывания экземпляра CIM \_ регистередпрофиле с экземпляром CIM \_ регистередпрофиле другого профиля, который ссылается на зависимый профиль в качестве связанного профиля.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: Класс CIM_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 39cfa6dac2fd827b2ce690afa5cdd7126322c2f81182db674517c75911791a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556819"
---
# <a name="cim_referencedprofile-class"></a>\_Класс CIM референцедпрофиле

Используется для связывания экземпляра [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) с экземпляром **CIM \_ регистередпрофиле** другого профиля, который ссылается на зависимый профиль в качестве связанного профиля.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ референцедпрофиле** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ референцедпрофиле** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает экземпляр [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) , на который ссылается **зависимый** профиль.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает экземпляр [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) , который ссылается на другие профили.

</dd> </dl>

## <a name="remarks"></a>Remarks

Использование свойств **Dependent** и **Antecedent** в ассоциации **CIM \_ референцедпрофиле** определено таким образом, что к профилю, на который указывает ссылка, относится предшествующая задача, а профиль, ссылающийся на ссылку, является зависимым.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                      |
| Пространство имен<br/>                | Корневое \\ взаимодействие<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Interop. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зависимость CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

