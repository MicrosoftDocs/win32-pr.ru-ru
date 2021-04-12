---
description: Указывает идентификатор поставщика сотовой сети.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: Элемент ProviderID (providerType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263176"
---
# <a name="providerid-providertype-element"></a><span data-ttu-id="10bcf-103">Элемент ProviderID (providerType)</span><span class="sxs-lookup"><span data-stu-id="10bcf-103">ProviderID (providerType) Element</span></span>

<span data-ttu-id="10bcf-104">Элемент **ProviderID (ProviderType)** указывает идентификатор поставщика сети сотовой связи.</span><span class="sxs-lookup"><span data-stu-id="10bcf-104">The **ProviderID (providerType)** element specifies the provider ID of the cellular network.</span></span>

<span data-ttu-id="10bcf-105">Элемент — это последовательность цифр, длина которой не может превышать 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="10bcf-105">The element is a sequence of digits with a maximum of 6 digits.</span></span>

<span data-ttu-id="10bcf-106">Этот элемент необходим в элементе [**provider**](schema-provider-dataroamingpartners-element.md) .</span><span class="sxs-lookup"><span data-stu-id="10bcf-106">This element is required within the [**Provider**](schema-provider-dataroamingpartners-element.md) element.</span></span>

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

<span data-ttu-id="10bcf-107">Элемент **ProviderID** определяется сложным типом [**ProviderType**](schema-providertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="10bcf-107">The **ProviderID** element is defined by the [**providerType**](schema-providertype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="10bcf-108">Требования</span><span class="sxs-lookup"><span data-stu-id="10bcf-108">Requirements</span></span>



| <span data-ttu-id="10bcf-109">Требование</span><span class="sxs-lookup"><span data-stu-id="10bcf-109">Requirement</span></span> | <span data-ttu-id="10bcf-110">Значение</span><span class="sxs-lookup"><span data-stu-id="10bcf-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="10bcf-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10bcf-111">Minimum supported client</span></span><br/> | <span data-ttu-id="10bcf-112">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="10bcf-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="10bcf-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10bcf-113">Minimum supported server</span></span><br/> | <span data-ttu-id="10bcf-114">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="10bcf-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="10bcf-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10bcf-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="10bcf-116">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="10bcf-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="10bcf-117">**providerType**</span><span class="sxs-lookup"><span data-stu-id="10bcf-117">**providerType**</span></span>](schema-providertype-complextype.md)
</dt> <dt>

<span data-ttu-id="10bcf-118">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="10bcf-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="10bcf-119">**Поставщик (Датароамингпартнерс)**</span><span class="sxs-lookup"><span data-stu-id="10bcf-119">**Provider (DataRoamingPartners)**</span></span>](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




