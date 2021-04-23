---
title: Элемент Identity
description: Сведения об элементе удостоверения EAPHost. Этот элемент захватывает удостоверение, используемое для проверки подлинности.
ms.assetid: 464979f0-6a2b-43e7-a207-2fbd1e2e5f51
keywords:
- Элемент Identity EAPHost
topic_type:
- apiref
api_name:
- Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 485d576155d5ac63df2776016f3aafabf8c18c25
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488301"
---
# <a name="identity-element"></a><span data-ttu-id="41860-105">Элемент Identity</span><span class="sxs-lookup"><span data-stu-id="41860-105">Identity Element</span></span>

<span data-ttu-id="41860-106">Элемент **Identity** захватывает удостоверение, используемое для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="41860-106">The **Identity** element captures the identity used for authentication.</span></span>

``` syntax
<xs:element name="Identity"
    type="string"
 />
```

## <a name="remarks"></a><span data-ttu-id="41860-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41860-107">Remarks</span></span>

<span data-ttu-id="41860-108">Элемент **Identity** является абстрактным; Каждый метод должен определять и использовать производный элемент в документах экземпляра.</span><span class="sxs-lookup"><span data-stu-id="41860-108">The **Identity** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="41860-109">Требования</span><span class="sxs-lookup"><span data-stu-id="41860-109">Requirements</span></span>



| <span data-ttu-id="41860-110">Роль</span><span class="sxs-lookup"><span data-stu-id="41860-110">Role</span></span> | <span data-ttu-id="41860-111">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="41860-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="41860-112">Клиент</span><span class="sxs-lookup"><span data-stu-id="41860-112">Client</span></span><br/> | <span data-ttu-id="41860-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41860-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="41860-114">Сервер</span><span class="sxs-lookup"><span data-stu-id="41860-114">Server</span></span><br/> | <span data-ttu-id="41860-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41860-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41860-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41860-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41860-117">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="41860-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="41860-118">Схема baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="41860-118">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





