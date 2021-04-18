---
title: Элемент Еаптипе (базовые свойства пользователя)
description: Сведения об элементе Еаптипе. Этот элемент захватывает конфигурацию, зависящую от метода, внутри элемента EAP. | Элемент Еаптипе (базовые свойства пользователя)
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
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
ms.openlocfilehash: 5fffa74c69b5ecbf2823cfa79ae376fed524e8ca
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713399"
---
# <a name="eaptype-element-base-user-properties"></a><span data-ttu-id="a445e-106">Элемент Еаптипе (базовые свойства пользователя)</span><span class="sxs-lookup"><span data-stu-id="a445e-106">EapType element (base user properties)</span></span>

<span data-ttu-id="a445e-107">Элемент **еаптипе** фиксирует конфигурацию, относящуюся к методу, внутри элемента EAP.</span><span class="sxs-lookup"><span data-stu-id="a445e-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="a445e-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a445e-108">Remarks</span></span>

<span data-ttu-id="a445e-109">Элемент **еаптипе** является абстрактным; Каждый метод должен определять и использовать производный элемент в документах экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a445e-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="a445e-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a445e-110">Requirements</span></span>



| <span data-ttu-id="a445e-111">Роль</span><span class="sxs-lookup"><span data-stu-id="a445e-111">Role</span></span> | <span data-ttu-id="a445e-112">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="a445e-112">Minimum supported OS version</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a445e-113">Клиент</span><span class="sxs-lookup"><span data-stu-id="a445e-113">Client</span></span><br/> | <span data-ttu-id="a445e-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a445e-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a445e-115">Сервер</span><span class="sxs-lookup"><span data-stu-id="a445e-115">Server</span></span><br/> | <span data-ttu-id="a445e-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a445e-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a445e-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a445e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a445e-118">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="a445e-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a445e-119">Схема baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a445e-119">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





