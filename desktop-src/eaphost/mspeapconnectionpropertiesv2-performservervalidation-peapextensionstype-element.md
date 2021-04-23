---
title: Элемент Перформсервервалидатион (Пеапекстенсионстипе) (схема v2)
description: Сведения об элементе Перформсервервалидатион (Пеапекстенсионстипе). Этот элемент указывает, выполняется ли проверка сервера. | Элемент Перформсервервалидатион (Пеапекстенсионстипе) (схема v2)
ms.assetid: a9c383d4-2582-47dd-bdf1-dd4e6c1689f7
keywords:
- Элемент Перформсервервалидатион EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 32bc213aa67e87eb8af0643a15f16b298cfb3204
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273565"
---
# <a name="performservervalidation-peapextensionstype-element-v2-schema"></a><span data-ttu-id="4329e-106">Элемент Перформсервервалидатион (Пеапекстенсионстипе) (схема v2)</span><span class="sxs-lookup"><span data-stu-id="4329e-106">PerformServerValidation (PeapExtensionsType) Element (V2 schema)</span></span>

<span data-ttu-id="4329e-107">Элемент **перформсервервалидатион (пеапекстенсионстипе)** указывает, выполняется ли проверка сервера.</span><span class="sxs-lookup"><span data-stu-id="4329e-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element name="PerformServerValidation"
    type="xs:boolean"
 />
```

<span data-ttu-id="4329e-108">Элемент **перформсервервалидатион** определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4329e-108">The **PerformServerValidation** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4329e-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4329e-109">Remarks</span></span>

<span data-ttu-id="4329e-110">Элемент **перформсервервалидатион** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4329e-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="4329e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="4329e-111">Requirements</span></span>



| <span data-ttu-id="4329e-112">Роль</span><span class="sxs-lookup"><span data-stu-id="4329e-112">Role</span></span> | <span data-ttu-id="4329e-113">Минимальная версия ОС</span><span class="sxs-lookup"><span data-stu-id="4329e-113">Minimum OS version</span></span> |
|------|--------------------|
| <span data-ttu-id="4329e-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="4329e-114">Client</span></span><br/> | <span data-ttu-id="4329e-115">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4329e-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4329e-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="4329e-116">Server</span></span><br/> | <span data-ttu-id="4329e-117">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4329e-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4329e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4329e-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="4329e-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="4329e-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4329e-120">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="4329e-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="4329e-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="4329e-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4329e-122">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="4329e-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="4329e-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="4329e-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="4329e-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="4329e-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4329e-125">Схема mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="4329e-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="4329e-126">Элементы схемы mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="4329e-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





