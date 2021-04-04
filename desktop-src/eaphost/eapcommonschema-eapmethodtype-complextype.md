---
title: Сложный тип Еапмесодтипе
description: Определяет элементы, которые уникально идентифицируют один тип метода EAP, VendorId, Вендортипе и Аусорид.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- Еапмесодтипе сложный тип EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802531"
---
# <a name="eapmethodtype-complex-type"></a><span data-ttu-id="76def-104">Сложный тип Еапмесодтипе</span><span class="sxs-lookup"><span data-stu-id="76def-104">EapMethodType Complex Type</span></span>

<span data-ttu-id="76def-105">Сложный тип **еапмесодтипе** определяет элементы, которые уникально идентифицируют один метод EAP: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md), [**вендортипе**](eapcommonschema-vendortype-eapmethodtype-element.md)и [**аусорид**](eapcommonschema-authorid-eapmethodtype-element.md).</span><span class="sxs-lookup"><span data-stu-id="76def-105">The **EapMethodType** complex type defines the elements that uniquely identify a single EAP method: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md), and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).</span></span>

<span data-ttu-id="76def-106">[**Type**](eapcommonschema-type-eapmethodtype-element.md) и [**аусорид**](eapcommonschema-authorid-eapmethodtype-element.md) являются обязательными элементами, тогда как [**вендортипе**](eapcommonschema-vendortype-eapmethodtype-element.md) и [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) являются обязательными только в том случае, если элемент **Type** имеет значение 254 (Расширенный метод EAP).</span><span class="sxs-lookup"><span data-stu-id="76def-106">[**Type**](eapcommonschema-type-eapmethodtype-element.md) and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) are mandatory elements, whereas [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) are required only when the **Type** element is 254 (an expanded EAP method).</span></span>

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="76def-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="76def-107">Child elements</span></span>



| <span data-ttu-id="76def-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="76def-108">Element</span></span>                                                                | <span data-ttu-id="76def-109">Тип</span><span class="sxs-lookup"><span data-stu-id="76def-109">Type</span></span>         | <span data-ttu-id="76def-110">Описание</span><span class="sxs-lookup"><span data-stu-id="76def-110">Description</span></span>                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76def-111">**аусорид**</span><span class="sxs-lookup"><span data-stu-id="76def-111">**AuthorId**</span></span>](eapcommonschema-authorid-eapmethodtype-element.md)     | <span data-ttu-id="76def-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76def-112">unsignedInt</span></span>  | <span data-ttu-id="76def-113">Ссылается на автора метода.</span><span class="sxs-lookup"><span data-stu-id="76def-113">Refers to the method author.</span></span> <br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="76def-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="76def-114">**Type**</span></span>](eapcommonschema-type-eapmethodtype-element.md)             | <span data-ttu-id="76def-115">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="76def-115">unsignedByte</span></span> | <span data-ttu-id="76def-116">Относится к типу метода EAP.</span><span class="sxs-lookup"><span data-stu-id="76def-116">Refers to the EAP method type.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="76def-117">**Поставщика**</span><span class="sxs-lookup"><span data-stu-id="76def-117">**VendorId**</span></span>](eapcommonschema-vendorid-eapmethodtype-element.md)     | <span data-ttu-id="76def-118">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76def-118">unsignedInt</span></span>  | <span data-ttu-id="76def-119">Относится к поставщику, который определил метод — если элемент [**Type**](eapcommonschema-type-eapmethodtype-element.md) равен 254 (Расширенный метод EAP).</span><span class="sxs-lookup"><span data-stu-id="76def-119">Refers to the vendor who defined the method - if the [**Type**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span> <span data-ttu-id="76def-120">[**ИД поставщика**](eapcommonschema-vendorid-eapmethodtype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="76def-120">The [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) is optional.</span></span> <br/> |
| [<span data-ttu-id="76def-121">**вендортипе**</span><span class="sxs-lookup"><span data-stu-id="76def-121">**VendorType**</span></span>](eapcommonschema-vendortype-eapmethodtype-element.md) | <span data-ttu-id="76def-122">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76def-122">unsignedInt</span></span>  | <span data-ttu-id="76def-123">Тип, определяемый поставщиком для метода.</span><span class="sxs-lookup"><span data-stu-id="76def-123">Is the vendor defined type for the method.</span></span> <span data-ttu-id="76def-124">[**Вендортипе**](eapcommonschema-vendortype-eapmethodtype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="76def-124">The [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) is optional.</span></span> <br/>                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="76def-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76def-125">Remarks</span></span>

<span data-ttu-id="76def-126">Элементы [**аусорид**](eapcommonschema-authorid-eapmethodtype-element.md) и [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) не обязательно должны быть одинаковыми для конкретного метода.</span><span class="sxs-lookup"><span data-stu-id="76def-126">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

<span data-ttu-id="76def-127">Элементы [**аусорид**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) и [**вендортипе**](eapcommonschema-vendortype-eapmethodtype-element.md) — это уникальные номера, выдаваемые центром Интернета, которым назначены номера (IANA).</span><span class="sxs-lookup"><span data-stu-id="76def-127">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) and [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) elements are each a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

## <a name="requirements"></a><span data-ttu-id="76def-128">Требования</span><span class="sxs-lookup"><span data-stu-id="76def-128">Requirements</span></span>



| <span data-ttu-id="76def-129">Требование</span><span class="sxs-lookup"><span data-stu-id="76def-129">Requirement</span></span> | <span data-ttu-id="76def-130">Значение</span><span class="sxs-lookup"><span data-stu-id="76def-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="76def-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76def-131">Minimum supported client</span></span><br/> | <span data-ttu-id="76def-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76def-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="76def-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76def-133">Minimum supported server</span></span><br/> | <span data-ttu-id="76def-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76def-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="76def-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76def-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76def-136">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="76def-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="76def-137">Схема еапкоммон</span><span class="sxs-lookup"><span data-stu-id="76def-137">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





