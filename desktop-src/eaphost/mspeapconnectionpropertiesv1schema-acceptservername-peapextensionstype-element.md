---
title: Элемент Акцептсервернаме (Пеапекстенсионстипе) (EAPHost)
description: Указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе ServerName (Сервервалидатионпараметерс). | Акцептсервернаме (Пеапекстенсионстипе), элемент
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- элемент EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba4874b7c8761f35fa93387b23eaf5463a31bcf4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314607"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a><span data-ttu-id="6e1d3-105">Элемент Акцептсервернаме (Пеапекстенсионстипе) (EAPHost)</span><span class="sxs-lookup"><span data-stu-id="6e1d3-105">AcceptServerName (PeapExtensionsType) Element (EAPHost)</span></span>

<span data-ttu-id="6e1d3-106">Элемент **акцептсервернаме (пеапекстенсионстипе)** указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе [**ServerName (сервервалидатионпараметерс)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6e1d3-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="6e1d3-107">Элемент определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6e1d3-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e1d3-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="6e1d3-108">Remarks</span></span>

<span data-ttu-id="6e1d3-109">Элемент **акцептсервернаме** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6e1d3-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e1d3-110">Требования</span><span class="sxs-lookup"><span data-stu-id="6e1d3-110">Requirements</span></span>



| <span data-ttu-id="6e1d3-111">Требование</span><span class="sxs-lookup"><span data-stu-id="6e1d3-111">Requirement</span></span> | <span data-ttu-id="6e1d3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6e1d3-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6e1d3-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e1d3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6e1d3-114">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6e1d3-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6e1d3-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e1d3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6e1d3-116">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e1d3-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e1d3-117">См. также</span><span class="sxs-lookup"><span data-stu-id="6e1d3-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e1d3-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="6e1d3-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6e1d3-119">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="6e1d3-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="6e1d3-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="6e1d3-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6e1d3-121">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="6e1d3-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="6e1d3-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6e1d3-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="6e1d3-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="6e1d3-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6e1d3-124">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6e1d3-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="6e1d3-125">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6e1d3-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6e1d3-126">**акцептсервернаме**</span><span class="sxs-lookup"><span data-stu-id="6e1d3-126">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





