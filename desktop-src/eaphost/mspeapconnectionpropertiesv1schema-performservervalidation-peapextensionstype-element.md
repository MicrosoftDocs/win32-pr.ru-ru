---
title: Элемент Перформсервервалидатион (Пеапекстенсионстипе) (схема v1)
description: Сведения об элементе Перформсервервалидатион (Пеапекстенсионстипе). Этот элемент указывает, выполняется ли проверка сервера. | Элемент Перформсервервалидатион (Пеапекстенсионстипе) (схема v1)
ms.assetid: b0483ed0-a02f-4f60-b1ae-7c5e6be8e196
keywords:
- элемент EAPHost
topic_type:
- apiref
api_name:
- PerformServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256d942d68c30788180f2d8080f963c1d79b401a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713370"
---
# <a name="performservervalidation-peapextensionstype-element-v1-schema"></a><span data-ttu-id="f4f83-106">Элемент Перформсервервалидатион (Пеапекстенсионстипе) (схема v1)</span><span class="sxs-lookup"><span data-stu-id="f4f83-106">PerformServerValidation (PeapExtensionsType) element (v1 schema)</span></span>

<span data-ttu-id="f4f83-107">Элемент **перформсервервалидатион (пеапекстенсионстипе)** указывает, выполняется ли проверка сервера.</span><span class="sxs-lookup"><span data-stu-id="f4f83-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:PerformServerValidation"
 />
```

<span data-ttu-id="f4f83-108">Элемент определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f4f83-108">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4f83-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4f83-109">Remarks</span></span>

<span data-ttu-id="f4f83-110">Элемент **перформсервервалидатион** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f4f83-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f83-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f4f83-111">Requirements</span></span>



| <span data-ttu-id="f4f83-112">Роль</span><span class="sxs-lookup"><span data-stu-id="f4f83-112">Role</span></span> | <span data-ttu-id="f4f83-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="f4f83-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="f4f83-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="f4f83-114">Client</span></span><br/> | <span data-ttu-id="f4f83-115">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f4f83-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f4f83-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="f4f83-116">Server</span></span><br/> | <span data-ttu-id="f4f83-117">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4f83-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4f83-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4f83-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4f83-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="f4f83-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f4f83-120">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="f4f83-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="f4f83-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="f4f83-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f4f83-122">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="f4f83-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="f4f83-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f4f83-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f4f83-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="f4f83-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f4f83-125">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f4f83-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f4f83-126">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f4f83-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f4f83-127">**Перформсервервалидатион (Пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="f4f83-127">**PerformServerValidation(PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md)
</dt> </dl>

 

 





