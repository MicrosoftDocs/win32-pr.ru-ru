---
title: Вендортипе (Еапмесодтипе), элемент
description: Сведения об элементе Вендортипе (Еапмесодтипе). Этот элемент является типом, определяемым поставщиком для метода.
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- Элемент Вендортипе EAPHost
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29030672cea0deff59f7f3026dcac98d6ff1c178
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488272"
---
# <a name="vendortype-eapmethodtype-element"></a><span data-ttu-id="04610-105">Вендортипе (Еапмесодтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="04610-105">VendorType (EapMethodType) Element</span></span>

<span data-ttu-id="04610-106">Элемент **вендортипе (еапмесодтипе)** является типом, определяемым поставщиком для метода.</span><span class="sxs-lookup"><span data-stu-id="04610-106">The **VendorType (EapMethodType)** element is the vendor defined type for the method.</span></span>

<span data-ttu-id="04610-107">Элемент **вендортипе** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="04610-107">The **VendorType** element is optional.</span></span> <span data-ttu-id="04610-108">При использовании **вендортипе** — это уникальный номер, выданный IANA.</span><span class="sxs-lookup"><span data-stu-id="04610-108">If used, the **VendorType** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

<span data-ttu-id="04610-109">Элемент **вендортипе** определяется сложным типом [**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="04610-109">The **VendorType** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="04610-110">Требования</span><span class="sxs-lookup"><span data-stu-id="04610-110">Requirements</span></span>



| <span data-ttu-id="04610-111">Роль</span><span class="sxs-lookup"><span data-stu-id="04610-111">Role</span></span> | <span data-ttu-id="04610-112">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="04610-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="04610-113">Клиент</span><span class="sxs-lookup"><span data-stu-id="04610-113">Client</span></span><br/> | <span data-ttu-id="04610-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04610-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="04610-115">Сервер</span><span class="sxs-lookup"><span data-stu-id="04610-115">Server</span></span><br/> | <span data-ttu-id="04610-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04610-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04610-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04610-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="04610-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="04610-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="04610-119">**еапмесодтипе**</span><span class="sxs-lookup"><span data-stu-id="04610-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="04610-120">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="04610-120">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="04610-121">Схема еапкоммон</span><span class="sxs-lookup"><span data-stu-id="04610-121">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





