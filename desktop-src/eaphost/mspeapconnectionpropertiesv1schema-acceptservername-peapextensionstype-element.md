---
title: Акцептсервернаме (Пеапекстенсионстипе), элемент
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
ms.openlocfilehash: 1c877819fd559cb26cd93c5d5456631a93a49545
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081786"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="3d4be-105">Акцептсервернаме (Пеапекстенсионстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="3d4be-105">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="3d4be-106">Элемент **акцептсервернаме (пеапекстенсионстипе)** указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе [**ServerName (сервервалидатионпараметерс)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3d4be-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="3d4be-107">Элемент определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3d4be-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d4be-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d4be-108">Remarks</span></span>

<span data-ttu-id="3d4be-109">Элемент **акцептсервернаме** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3d4be-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d4be-110">Требования</span><span class="sxs-lookup"><span data-stu-id="3d4be-110">Requirements</span></span>



| <span data-ttu-id="3d4be-111">Требование</span><span class="sxs-lookup"><span data-stu-id="3d4be-111">Requirement</span></span> | <span data-ttu-id="3d4be-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3d4be-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3d4be-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d4be-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3d4be-114">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3d4be-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3d4be-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d4be-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3d4be-116">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d4be-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d4be-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d4be-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d4be-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="3d4be-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3d4be-119">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="3d4be-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="3d4be-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="3d4be-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3d4be-121">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="3d4be-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="3d4be-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3d4be-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3d4be-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="3d4be-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3d4be-124">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3d4be-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3d4be-125">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3d4be-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3d4be-126">**акцептсервернаме**</span><span class="sxs-lookup"><span data-stu-id="3d4be-126">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





