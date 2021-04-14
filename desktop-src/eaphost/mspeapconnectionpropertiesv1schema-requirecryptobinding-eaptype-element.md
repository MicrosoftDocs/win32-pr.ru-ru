---
title: Рекуирекриптобиндинг (Еаптипе), элемент
description: Указывает, следует ли выполнять проверку подлинности на серверах, поддерживающих криптобиндинг.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- Элемент Рекуирекриптобиндинг EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63ee456f87205346a935ad047cb8db9828febba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415960"
---
# <a name="requirecryptobinding-eaptype-element"></a><span data-ttu-id="f5c84-104">Рекуирекриптобиндинг (Еаптипе), элемент</span><span class="sxs-lookup"><span data-stu-id="f5c84-104">RequireCryptoBinding (EapType) Element</span></span>

<span data-ttu-id="f5c84-105">Элемент **рекуирекриптобиндинг (еаптипе)** указывает, следует ли выполнять проверку подлинности на серверах, поддерживающих криптобиндинг.</span><span class="sxs-lookup"><span data-stu-id="f5c84-105">The **RequireCryptoBinding (EapType)** element indicates whether to authenticate with servers that support cryptobinding.</span></span>

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

<span data-ttu-id="f5c84-106">Элемент **рекуирекриптобиндинг** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f5c84-106">The **RequireCryptoBinding** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5c84-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5c84-107">Remarks</span></span>

<span data-ttu-id="f5c84-108">Если элемент **рекуирекриптобиндинг** имеет значение true, PEAP будет проходить проверку подлинности на серверах, не поддерживающих криптобиндинг. Если значение равно FALSE, PEAP будет проходить проверку подлинности только на серверах, поддерживающих криптобиндинг.</span><span class="sxs-lookup"><span data-stu-id="f5c84-108">If the **RequireCryptoBinding** element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="f5c84-109">Элемент **рекуирекриптобиндинг** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f5c84-109">The **RequireCryptoBinding** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c84-110">Требования</span><span class="sxs-lookup"><span data-stu-id="f5c84-110">Requirements</span></span>



| <span data-ttu-id="f5c84-111">Требование</span><span class="sxs-lookup"><span data-stu-id="f5c84-111">Requirement</span></span> | <span data-ttu-id="f5c84-112">Значение</span><span class="sxs-lookup"><span data-stu-id="f5c84-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f5c84-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5c84-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c84-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5c84-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f5c84-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5c84-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c84-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5c84-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5c84-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5c84-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="f5c84-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="f5c84-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f5c84-119">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="f5c84-119">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="f5c84-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="f5c84-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f5c84-121">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="f5c84-121">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="f5c84-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f5c84-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f5c84-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="f5c84-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f5c84-124">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f5c84-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f5c84-125">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f5c84-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





