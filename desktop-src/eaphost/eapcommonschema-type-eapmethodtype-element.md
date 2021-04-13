---
title: Элемент Type (Еапмесодтипе)
description: Сведения об элементе Type (Еапмесодтипе), который ссылается на тип метода EAP. См. раздел требования и просмотрите дополнительные доступные ресурсы.
ms.assetid: 7911e97c-9436-4d60-8497-bee45cdb8db4
keywords:
- Элемент Type EAPHost
topic_type:
- apiref
api_name:
- Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d45defd098f560d4deb8698e0fd569492668e0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413736"
---
# <a name="type-eapmethodtype-element"></a><span data-ttu-id="072f2-105">Элемент Type (Еапмесодтипе)</span><span class="sxs-lookup"><span data-stu-id="072f2-105">Type (EapMethodType) Element</span></span>

<span data-ttu-id="072f2-106">Элемент **Type (еапмесодтипе)** ссылается на тип метода EAP.</span><span class="sxs-lookup"><span data-stu-id="072f2-106">The **Type (EapMethodType)** element refers to the EAP method type.</span></span>

<span data-ttu-id="072f2-107">Тип — это уникальный номер, выданный IANA.</span><span class="sxs-lookup"><span data-stu-id="072f2-107">The Type is a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="Type"
    type="unsignedByte"
 />
```

<span data-ttu-id="072f2-108">Элемент **Type** определяется сложным типом [**еапмесодтипе**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="072f2-108">The **Type** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="072f2-109">Требования</span><span class="sxs-lookup"><span data-stu-id="072f2-109">Requirements</span></span>



| <span data-ttu-id="072f2-110">Роль</span><span class="sxs-lookup"><span data-stu-id="072f2-110">Role</span></span> | <span data-ttu-id="072f2-111">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="072f2-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="072f2-112">Клиент</span><span class="sxs-lookup"><span data-stu-id="072f2-112">Client</span></span><br/> | <span data-ttu-id="072f2-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="072f2-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="072f2-114">Сервер</span><span class="sxs-lookup"><span data-stu-id="072f2-114">Server</span></span><br/> | <span data-ttu-id="072f2-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="072f2-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="072f2-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="072f2-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="072f2-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="072f2-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="072f2-118">**еапмесодтипе**</span><span class="sxs-lookup"><span data-stu-id="072f2-118">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="072f2-119">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="072f2-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="072f2-120">Схема еапкоммон</span><span class="sxs-lookup"><span data-stu-id="072f2-120">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





