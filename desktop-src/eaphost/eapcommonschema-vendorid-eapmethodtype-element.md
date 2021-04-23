---
title: VendorId (Еапмесодтипе), элемент
description: Относится к поставщику, который определил метод, если элемент Type (Еапмесодтипе) имеет значение 254 (Расширенный метод EAP).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Элемент VendorId EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534277"
---
# <a name="vendorid-eapmethodtype-element"></a><span data-ttu-id="4ade9-104">VendorId (Еапмесодтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="4ade9-104">VendorId (EapMethodType) Element</span></span>

<span data-ttu-id="4ade9-105">Элемент **VendorID (еапмесодтипе)** ссылается на поставщика, который определил метод, если элемент [**Type (еапмесодтипе)**](eapcommonschema-type-eapmethodtype-element.md) имеет значение 254 (Расширенный метод EAP).</span><span class="sxs-lookup"><span data-stu-id="4ade9-105">The **VendorId (EapMethodType)** element refers to the vendor who defined the method if the [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span>

<span data-ttu-id="4ade9-106">**ИД поставщика** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4ade9-106">The **VendorId** is optional.</span></span> <span data-ttu-id="4ade9-107">Если используется, то **ИД поставщика** — это уникальный номер, выданный IANA.</span><span class="sxs-lookup"><span data-stu-id="4ade9-107">If used, the **VendorId** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="4ade9-108">Элемент **VendorID** определяется сложным типом [**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4ade9-108">The **VendorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ade9-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ade9-109">Remarks</span></span>

<span data-ttu-id="4ade9-110">Элементы [**аусорид**](eapcommonschema-authorid-eapmethodtype-element.md) и **VendorID** не обязательно должны быть одинаковыми для конкретного метода.</span><span class="sxs-lookup"><span data-stu-id="4ade9-110">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and **VendorId** elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ade9-111">Требования</span><span class="sxs-lookup"><span data-stu-id="4ade9-111">Requirements</span></span>



| <span data-ttu-id="4ade9-112">Требование</span><span class="sxs-lookup"><span data-stu-id="4ade9-112">Requirement</span></span> | <span data-ttu-id="4ade9-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4ade9-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4ade9-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ade9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4ade9-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ade9-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4ade9-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ade9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4ade9-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ade9-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ade9-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ade9-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="4ade9-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="4ade9-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4ade9-120">**еапмесодтипе**</span><span class="sxs-lookup"><span data-stu-id="4ade9-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="4ade9-121">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="4ade9-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4ade9-122">Схема еапкоммон</span><span class="sxs-lookup"><span data-stu-id="4ade9-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





