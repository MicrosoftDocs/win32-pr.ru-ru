---
title: Типы изменения атрибутов ADSI (iAds. h)
description: Используется с членом Двконтролкоде в \_ \_ информационной структуре attr, чтобы указать тип операции, которая должна быть выполнена при изменении атрибута с помощью метода идиректорйобжект сетобжектаттрибутес.
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- типы изменения атрибутов ADSI
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a739241fd52a7d45d58a1b36bb7de838234d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071336"
---
# <a name="adsi-attribute-modification-types"></a>Типы изменения атрибутов ADSI

Следующие константы используются с членом **двконтролкоде** в [**информационной структуре \_ attr \_**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) , чтобы указать тип операции, которая должна быть выполнена при изменении атрибута с помощью метода [**идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) . Дополнительные сведения об использовании этих значений см. в разделе [изменение атрибутов с помощью ADSI](modifying-attributes-with-adsi.md).

<dl> <dt>

<span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**\_ \_ четкое объявление attr**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Приводит к удалению всех значений атрибутов из объекта.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**\_Обновление attr для ADS \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Приводит к обновлению указанных значений атрибутов.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**\_Добавление attr \_ ADS**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Приводит к добавлению указанных значений атрибутов к существующим значениям атрибутов.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**\_Удаление AD attr \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Приводит к удалению указанных значений атрибутов из объекта.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Эти константы предназначены для использования со структурой [**\_ \_ сведений attr для ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) в методе [**идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) . Эти константы не следует путать с элементами перечисления перечислений [**\_ \_ операций \_ Свойства ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) , которые предназначены для использования с методом [**iAds::P утекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                    |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ сведения о attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[**Идиректорйобжект:: Сетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[Изменение атрибутов с помощью ADSI](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 





