---
title: Config (Еафостконфиг), элемент
description: Используется, когда конфигурация метода находится в текстовом формате XML вместо двоичного BLOB-объекта.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Элемент конфигурации EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491061"
---
# <a name="config-eaphostconfig-element"></a><span data-ttu-id="cc161-104">Config (Еафостконфиг), элемент</span><span class="sxs-lookup"><span data-stu-id="cc161-104">Config (EapHostConfig) Element</span></span>

<span data-ttu-id="cc161-105">Элемент **config (еафостконфиг)** используется, когда конфигурация метода находится в текстовой XML-форме вместо двоичного BLOB.</span><span class="sxs-lookup"><span data-stu-id="cc161-105">The **Config (EapHostConfig)** element is used when the method configuration is in XML text form instead of a binary BLOB.</span></span>

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

<span data-ttu-id="cc161-106">Элемент **config** определяется элементом [**еафостконфиг**](eaphostconfigschema-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cc161-106">The **Config** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc161-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc161-107">Remarks</span></span>

<span data-ttu-id="cc161-108">Элементы **config** и [**конфигблоб**](eaphostconfigschema-configblob-eaphostconfig-element.md) не могут одновременно использоваться одновременно.</span><span class="sxs-lookup"><span data-stu-id="cc161-108">The **Config** and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc161-109">Требования</span><span class="sxs-lookup"><span data-stu-id="cc161-109">Requirements</span></span>



| <span data-ttu-id="cc161-110">Требование</span><span class="sxs-lookup"><span data-stu-id="cc161-110">Requirement</span></span> | <span data-ttu-id="cc161-111">Значение</span><span class="sxs-lookup"><span data-stu-id="cc161-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc161-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc161-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cc161-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc161-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cc161-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc161-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cc161-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc161-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc161-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc161-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc161-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="cc161-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="cc161-118">**еафостконфиг**</span><span class="sxs-lookup"><span data-stu-id="cc161-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="cc161-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="cc161-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="cc161-120">**еафостконфиг**</span><span class="sxs-lookup"><span data-stu-id="cc161-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="cc161-121">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="cc161-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="cc161-122">Схема еафостконфиг</span><span class="sxs-lookup"><span data-stu-id="cc161-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





