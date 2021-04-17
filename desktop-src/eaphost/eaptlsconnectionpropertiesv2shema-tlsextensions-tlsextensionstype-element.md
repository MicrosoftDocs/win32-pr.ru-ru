---
title: Перформсервервалидатион, элемент
description: Сведения об элементе Перформсервервалидатион. Этот элемент указывает, выполняется ли проверка сервера. | Перформсервервалидатион, элемент
ms.assetid: c1dd1af1-63a0-48f7-8da5-860c50d73259
keywords:
- Элемент Перформсервервалидатион EAPHost
topic_type:
- apiref
api_name:
- PerformServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8d92bd5718e626f95cc7d08fbc01d5881ff9b59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105703585"
---
# <a name="performservervalidation-element"></a><span data-ttu-id="559ba-106">Перформсервервалидатион, элемент</span><span class="sxs-lookup"><span data-stu-id="559ba-106">PerformServerValidation element</span></span>

<span data-ttu-id="559ba-107">Элемент **перформсервервалидатион (еаптипе)** указывает, выполняется ли проверка сервера.</span><span class="sxs-lookup"><span data-stu-id="559ba-107">The **PerformServerValidation (EapType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element name="PerformServerValidation"
    type="xs:boolean"
 />
```

<span data-ttu-id="559ba-108">Элемент **перформсервервалидатион** определяется элементом [**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="559ba-108">The **PerformServerValidation** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="559ba-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="559ba-109">Remarks</span></span>

<span data-ttu-id="559ba-110">Элемент **перформсервервалидатион** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="559ba-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="559ba-111">Требования</span><span class="sxs-lookup"><span data-stu-id="559ba-111">Requirements</span></span>



| <span data-ttu-id="559ba-112">Роль</span><span class="sxs-lookup"><span data-stu-id="559ba-112">Role</span></span> | <span data-ttu-id="559ba-113">Минимальная версия ОС</span><span class="sxs-lookup"><span data-stu-id="559ba-113">Minimum OS version</span></span> |
|------|--------------------|
| <span data-ttu-id="559ba-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="559ba-114">Client</span></span><br/> | <span data-ttu-id="559ba-115">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="559ba-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="559ba-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="559ba-116">Server</span></span><br/> | <span data-ttu-id="559ba-117">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="559ba-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="559ba-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="559ba-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="559ba-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="559ba-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="559ba-120">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="559ba-120">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="559ba-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="559ba-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="559ba-122">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="559ba-122">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="559ba-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="559ba-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="559ba-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="559ba-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="559ba-125">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="559ba-125">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="559ba-126">Элементы схемы eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="559ba-126">eaptlsconnectionpropertiesv2 Schema Elements</span></span>](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[<span data-ttu-id="559ba-127">**Перформсервервалидатион (Еаптипе)**</span><span class="sxs-lookup"><span data-stu-id="559ba-127">**PerformServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md)
</dt> </dl>

 

 





