---
title: Элемент Еаптипе (свойство соединения со схемой v1)
description: Сведения об элементе Еаптипе. Этот элемент захватывает конфигурацию, зависящую от метода, внутри элемента EAP. | Элемент Еаптипе (свойство соединения со схемой v1)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
keywords:
- Элемент Еаптипе EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820572"
---
# <a name="eaptype-element-v1-schema-connection-property"></a><span data-ttu-id="33592-106">Элемент Еаптипе (свойство соединения со схемой v1)</span><span class="sxs-lookup"><span data-stu-id="33592-106">EapType Element (v1 schema connection property)</span></span>

<span data-ttu-id="33592-107">Элемент **еаптипе** фиксирует конфигурацию, относящуюся к методу, внутри элемента EAP.</span><span class="sxs-lookup"><span data-stu-id="33592-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="33592-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33592-108">Remarks</span></span>

<span data-ttu-id="33592-109">Элемент **еаптипе** является абстрактным; Каждый метод должен определять и использовать производный элемент в документах экземпляра.</span><span class="sxs-lookup"><span data-stu-id="33592-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="33592-110">Требования</span><span class="sxs-lookup"><span data-stu-id="33592-110">Requirements</span></span>



| <span data-ttu-id="33592-111">Роль</span><span class="sxs-lookup"><span data-stu-id="33592-111">Role</span></span> | <span data-ttu-id="33592-112">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="33592-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="33592-113">Клиент</span><span class="sxs-lookup"><span data-stu-id="33592-113">Client</span></span><br/> | <span data-ttu-id="33592-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33592-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="33592-115">Сервер</span><span class="sxs-lookup"><span data-stu-id="33592-115">Server</span></span><br/> | <span data-ttu-id="33592-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="33592-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33592-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33592-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33592-118">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="33592-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="33592-119">Схема baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="33592-119">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





