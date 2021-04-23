---
title: Акцептсервернаме (Пеапекстенсионстипе), элемент
description: Указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе ServerName (Сервервалидатионпараметерс). | Акцептсервернаме (Пеапекстенсионстипе), элемент
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Элемент Акцептсервернаме EAPHost
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
ms.openlocfilehash: d085122104c2764896801015c58fcbc9f72a1580
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000238"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="90da3-105">Акцептсервернаме (Пеапекстенсионстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="90da3-105">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="90da3-106">Элемент **акцептсервернаме (пеапекстенсионстипе)** указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе [**ServerName (сервервалидатионпараметерс)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="90da3-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="90da3-107">Элемент **акцептсервернаме** определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="90da3-107">The **AcceptServerName** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="90da3-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90da3-108">Remarks</span></span>

<span data-ttu-id="90da3-109">Элемент **акцептсервернаме** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="90da3-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="90da3-110">Требования</span><span class="sxs-lookup"><span data-stu-id="90da3-110">Requirements</span></span>



| <span data-ttu-id="90da3-111">Требование</span><span class="sxs-lookup"><span data-stu-id="90da3-111">Requirement</span></span> | <span data-ttu-id="90da3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="90da3-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="90da3-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90da3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="90da3-114">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="90da3-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="90da3-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90da3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="90da3-116">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="90da3-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="90da3-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90da3-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="90da3-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="90da3-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="90da3-119">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="90da3-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="90da3-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="90da3-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="90da3-121">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="90da3-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="90da3-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="90da3-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="90da3-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="90da3-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="90da3-124">Схема mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="90da3-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="90da3-125">Элементы схемы mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="90da3-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





