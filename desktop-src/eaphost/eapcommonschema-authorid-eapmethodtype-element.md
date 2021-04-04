---
title: Аусорид (Еапмесодтипе), элемент
description: Сведения об элементе Аусорид (Еапмесодтипе). Элемент Аусорид (Еапмесодтипе) ссылается на автора метода.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Элемент Аусорид EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c9a756d8ad1fc88154d3d99d4304de6dd50166b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987893"
---
# <a name="authorid-eapmethodtype-element"></a><span data-ttu-id="115bd-105">Аусорид (Еапмесодтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="115bd-105">AuthorId (EapMethodType) Element</span></span>

<span data-ttu-id="115bd-106">Элемент **аусорид (еапмесодтипе)** ссылается на автора метода.</span><span class="sxs-lookup"><span data-stu-id="115bd-106">The **AuthorId (EapMethodType)** element refers to the method author.</span></span>

<span data-ttu-id="115bd-107">Аусорид — это уникальный номер, выданный IANA.</span><span class="sxs-lookup"><span data-stu-id="115bd-107">The AuthorId is a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="115bd-108">Элемент **аусорид** определяется сложным типом [**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="115bd-108">The **AuthorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="115bd-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="115bd-109">Remarks</span></span>

<span data-ttu-id="115bd-110">Элементы **аусорид** и [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) не обязательно должны быть одинаковыми для конкретного метода.</span><span class="sxs-lookup"><span data-stu-id="115bd-110">The **AuthorId** and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="115bd-111">Требования</span><span class="sxs-lookup"><span data-stu-id="115bd-111">Requirements</span></span>



| <span data-ttu-id="115bd-112">Роль</span><span class="sxs-lookup"><span data-stu-id="115bd-112">Role</span></span> | <span data-ttu-id="115bd-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="115bd-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="115bd-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="115bd-114">Client</span></span><br/> | <span data-ttu-id="115bd-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="115bd-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="115bd-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="115bd-116">Server</span></span><br/> | <span data-ttu-id="115bd-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="115bd-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="115bd-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="115bd-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="115bd-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="115bd-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="115bd-120">**еапмесодтипе**</span><span class="sxs-lookup"><span data-stu-id="115bd-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="115bd-121">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="115bd-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="115bd-122">Схема еапкоммон</span><span class="sxs-lookup"><span data-stu-id="115bd-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





