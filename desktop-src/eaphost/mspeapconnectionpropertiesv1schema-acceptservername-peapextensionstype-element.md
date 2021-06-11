---
title: Элемент Акцептсервернаме (Пеапекстенсионстипе) (EAPHost)
description: Элемент Акцептсервернаме (Пеапекстенсионстипе) указывает, проверяется ли имя сервера на соответствие строке имени, указанной в ServerName в схеме mspeapconnectionpropertiesv1.
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
ms.openlocfilehash: 64565b24da0b4a93fd35fd3c4a6e7075546024c4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989099"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a><span data-ttu-id="3eead-104">Элемент Акцептсервернаме (Пеапекстенсионстипе) (EAPHost)</span><span class="sxs-lookup"><span data-stu-id="3eead-104">AcceptServerName (PeapExtensionsType) Element (EAPHost)</span></span>

<span data-ttu-id="3eead-105">Элемент **акцептсервернаме (пеапекстенсионстипе)** указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе [**ServerName (сервервалидатионпараметерс)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3eead-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="3eead-106">Элемент определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3eead-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eead-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="3eead-107">Remarks</span></span>

<span data-ttu-id="3eead-108">Элемент **акцептсервернаме** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3eead-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eead-109">Требования</span><span class="sxs-lookup"><span data-stu-id="3eead-109">Requirements</span></span>



| <span data-ttu-id="3eead-110">Требование</span><span class="sxs-lookup"><span data-stu-id="3eead-110">Requirement</span></span> | <span data-ttu-id="3eead-111">Значение</span><span class="sxs-lookup"><span data-stu-id="3eead-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3eead-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3eead-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3eead-113">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3eead-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3eead-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3eead-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3eead-115">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3eead-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3eead-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3eead-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="3eead-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="3eead-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3eead-118">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="3eead-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="3eead-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="3eead-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3eead-120">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="3eead-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="3eead-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3eead-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3eead-122">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="3eead-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3eead-123">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3eead-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3eead-124">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3eead-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3eead-125">**акцептсервернаме**</span><span class="sxs-lookup"><span data-stu-id="3eead-125">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





