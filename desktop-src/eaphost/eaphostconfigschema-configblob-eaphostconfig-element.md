---
title: Конфигблоб (Еафостконфиг), элемент
description: Используется, когда конфигурация метода находится в двоичном виде двоичного объекта, а не в виде текстовой строки.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- Элемент Конфигблоб EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b220c74c6439b4b2cbb0d05a1d540d673e1bd17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800922"
---
# <a name="configblob-eaphostconfig-element"></a><span data-ttu-id="bde23-104">Конфигблоб (Еафостконфиг), элемент</span><span class="sxs-lookup"><span data-stu-id="bde23-104">ConfigBlob (EapHostConfig) Element</span></span>

<span data-ttu-id="bde23-105">Элемент **конфигблоб (еафостконфиг)** используется, когда конфигурация метода находится в двоичном виде ДВОИЧного объекта, а не в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="bde23-105">The **ConfigBlob (EapHostConfig)** element is used when the method configuration is in binary BLOB form instead of text string form.</span></span>

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="bde23-106">Элемент **конфигблоб** определяется элементом [**еафостконфиг**](eaphostconfigschema-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bde23-106">The **ConfigBlob** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="bde23-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bde23-107">Remarks</span></span>

<span data-ttu-id="bde23-108">Элементы [**config**](eaphostconfigschema-config-eaphostconfig-element.md) и **конфигблоб** не могут одновременно использоваться одновременно.</span><span class="sxs-lookup"><span data-stu-id="bde23-108">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and **ConfigBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="bde23-109">Требования</span><span class="sxs-lookup"><span data-stu-id="bde23-109">Requirements</span></span>



| <span data-ttu-id="bde23-110">Требование</span><span class="sxs-lookup"><span data-stu-id="bde23-110">Requirement</span></span> | <span data-ttu-id="bde23-111">Значение</span><span class="sxs-lookup"><span data-stu-id="bde23-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bde23-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bde23-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bde23-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bde23-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bde23-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bde23-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bde23-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bde23-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bde23-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bde23-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="bde23-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="bde23-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bde23-118">**еафостконфиг**</span><span class="sxs-lookup"><span data-stu-id="bde23-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="bde23-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="bde23-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bde23-120">**еафостконфиг**</span><span class="sxs-lookup"><span data-stu-id="bde23-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="bde23-121">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="bde23-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bde23-122">Схема еафостконфиг</span><span class="sxs-lookup"><span data-stu-id="bde23-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





