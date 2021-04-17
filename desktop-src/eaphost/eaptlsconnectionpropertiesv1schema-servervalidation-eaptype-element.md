---
title: Элемент Сервервалидатион (Еаптипе) (TLS)
description: Сведения об элементе Сервервалидатион (Еаптипе). Этот элемент содержит сведения о выполнении проверки сервера. | Элемент Сервервалидатион (Еаптипе) (TLS)
ms.assetid: f4ae1579-8c61-4187-8f5a-13aca3075af2
keywords:
- Элемент Сервервалидатион EAPHost
topic_type:
- apiref
api_name:
- ServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c54905f35d673aee692efa6569eaddc6d18fc716
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713412"
---
# <a name="servervalidation-eaptype-element-tls"></a><span data-ttu-id="ea59e-106">Элемент Сервервалидатион (Еаптипе) (TLS)</span><span class="sxs-lookup"><span data-stu-id="ea59e-106">ServerValidation (EapType) element (TLS)</span></span>

<span data-ttu-id="ea59e-107">Элемент **сервервалидатион (еаптипе)** содержит сведения о выполнении проверки сервера.</span><span class="sxs-lookup"><span data-stu-id="ea59e-107">The **ServerValidation (EapType)** element contains information about how to perform server validation.</span></span>

``` syntax
<xs:element name="ServerValidation"
    type="ServerValidationParameters"
 />
```

<span data-ttu-id="ea59e-108">Элемент **сервервалидатион** определяется элементом [**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ea59e-108">The **ServerValidation** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea59e-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea59e-109">Remarks</span></span>

<span data-ttu-id="ea59e-110">Элемент **сервервалидатион** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ea59e-110">The **ServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea59e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ea59e-111">Requirements</span></span>



| <span data-ttu-id="ea59e-112">Роль</span><span class="sxs-lookup"><span data-stu-id="ea59e-112">Role</span></span> | <span data-ttu-id="ea59e-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="ea59e-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="ea59e-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="ea59e-114">Client</span></span><br/> | <span data-ttu-id="ea59e-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea59e-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ea59e-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="ea59e-116">Server</span></span><br/> | <span data-ttu-id="ea59e-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea59e-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ea59e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea59e-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea59e-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ea59e-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ea59e-120">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="ea59e-120">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="ea59e-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ea59e-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ea59e-122">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="ea59e-122">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="ea59e-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ea59e-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="ea59e-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="ea59e-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ea59e-125">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ea59e-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="ea59e-126">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ea59e-126">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





