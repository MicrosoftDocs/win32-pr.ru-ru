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
# <a name="adsi-attribute-modification-types"></a><span data-ttu-id="be43a-104">Типы изменения атрибутов ADSI</span><span class="sxs-lookup"><span data-stu-id="be43a-104">ADSI Attribute Modification Types</span></span>

<span data-ttu-id="be43a-105">Следующие константы используются с членом **двконтролкоде** в [**информационной структуре \_ attr \_**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) , чтобы указать тип операции, которая должна быть выполнена при изменении атрибута с помощью метода [**идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="be43a-105">The following constants are used with the **dwControlCode** member of [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure to specify the type of operation to be performed when an attribute is modified with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="be43a-106">Дополнительные сведения об использовании этих значений см. в разделе [изменение атрибутов с помощью ADSI](modifying-attributes-with-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="be43a-106">For more information about using these values, see [Modifying Attributes with ADSI](modifying-attributes-with-adsi.md).</span></span>

<dl> <dt>

<span data-ttu-id="be43a-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**\_ \_ четкое объявление attr**</span><span class="sxs-lookup"><span data-stu-id="be43a-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**ADS\_ATTR\_CLEAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be43a-108">1</span><span class="sxs-lookup"><span data-stu-id="be43a-108">1</span></span>
</dt> <dt>



<span data-ttu-id="be43a-109">Приводит к удалению всех значений атрибутов из объекта.</span><span class="sxs-lookup"><span data-stu-id="be43a-109">Causes all attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be43a-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**\_Обновление attr для ADS \_**</span><span class="sxs-lookup"><span data-stu-id="be43a-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**ADS\_ATTR\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be43a-111">2</span><span class="sxs-lookup"><span data-stu-id="be43a-111">2</span></span>
</dt> <dt>



<span data-ttu-id="be43a-112">Приводит к обновлению указанных значений атрибутов.</span><span class="sxs-lookup"><span data-stu-id="be43a-112">Causes the specified attribute values to be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be43a-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**\_Добавление attr \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="be43a-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**ADS\_ATTR\_APPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be43a-114">3</span><span class="sxs-lookup"><span data-stu-id="be43a-114">3</span></span>
</dt> <dt>



<span data-ttu-id="be43a-115">Приводит к добавлению указанных значений атрибутов к существующим значениям атрибутов.</span><span class="sxs-lookup"><span data-stu-id="be43a-115">Causes the specified attribute values to be appended to the existing attribute values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be43a-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**\_Удаление AD attr \_**</span><span class="sxs-lookup"><span data-stu-id="be43a-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS\_ATTR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be43a-117">4</span><span class="sxs-lookup"><span data-stu-id="be43a-117">4</span></span>
</dt> <dt>



<span data-ttu-id="be43a-118">Приводит к удалению указанных значений атрибутов из объекта.</span><span class="sxs-lookup"><span data-stu-id="be43a-118">Causes the specified attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be43a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be43a-119">Remarks</span></span>

<span data-ttu-id="be43a-120">Эти константы предназначены для использования со структурой [**\_ \_ сведений attr для ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) в методе [**идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="be43a-120">These constants are intended to be used with the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure in the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="be43a-121">Эти константы не следует путать с элементами перечисления перечислений [**\_ \_ операций \_ Свойства ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) , которые предназначены для использования с методом [**iAds::P утекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="be43a-121">These constants should not be confused with members of the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration, which are intended to be used with the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="be43a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="be43a-122">Requirements</span></span>



| <span data-ttu-id="be43a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="be43a-123">Requirement</span></span> | <span data-ttu-id="be43a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="be43a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="be43a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be43a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be43a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be43a-126">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="be43a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be43a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be43a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be43a-128">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="be43a-129">Header</span><span class="sxs-lookup"><span data-stu-id="be43a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="be43a-130"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="be43a-130"><dt>Iads.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be43a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be43a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be43a-132">**\_ \_ сведения о attr ADS**</span><span class="sxs-lookup"><span data-stu-id="be43a-132">**ADS\_ATTR\_INFO**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[<span data-ttu-id="be43a-133">**Идиректорйобжект:: Сетобжектаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="be43a-133">**IDirectoryObject::SetObjectAttributes**</span></span>](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="be43a-134">Изменение атрибутов с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="be43a-134">Modifying Attributes with ADSI</span></span>](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 





