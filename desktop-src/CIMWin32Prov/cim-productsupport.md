---
description: Класс CIM \_ продуктсуппорт представляет связь между продуктом и поддержкой доступа, которая передает сведения о получении поддержки для продукта.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: Класс CIM_ProductSupport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a33efc39481ebe94b6aa8802d469e218d026aba34ab8da6cddf3f136b45a6d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118421451"
---
# <a name="cim_productsupport-class"></a>\_Класс CIM продуктсуппорт

Класс **CIM \_ продуктсуппорт** представляет связь между продуктом и поддержкой доступа, которая передает сведения о получении поддержки для продукта. Для продукта доступны различные типы поддержки. один и тот же объект поддержки может предоставить помощь для нескольких продуктов.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ продуктсуппорт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ продуктсуппорт** имеет следующие свойства.

<dl> <dt>

**Продукт**
</dt> <dd> <dl> <dt>

Тип данных: **\_ продукт CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на продукт.

</dd> <dt>

**Поддержка**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ суппортакцесс**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на службу поддержки продукта.

</dd> </dl>

## <a name="remarks"></a>Remarks

Инструментарий WMI не реализует этот класс.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




