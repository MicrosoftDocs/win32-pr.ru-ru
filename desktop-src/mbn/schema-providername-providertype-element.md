---
description: Содержит имя сети сотовой связи.
ms.assetid: 4169babb-7616-468a-93f0-de25cce0c88b
title: Элемент ProviderName (providerType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderName
api_type:
- Schema
ms.openlocfilehash: 47929d508ad6d3a6567c1b52e720360f4e7cfbda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647189"
---
# <a name="providername-providertype-element"></a><span data-ttu-id="5c6d3-103">Элемент ProviderName (providerType)</span><span class="sxs-lookup"><span data-stu-id="5c6d3-103">ProviderName (providerType) Element</span></span>

<span data-ttu-id="5c6d3-104">Элемент **providerName (ProviderType)** содержит имя сети сотовой связи.</span><span class="sxs-lookup"><span data-stu-id="5c6d3-104">The **ProviderName (providerType)** element contains the name of the cellular network.</span></span>

<span data-ttu-id="5c6d3-105">Элемент — это строка, длина которой не может превышать 20 символов.</span><span class="sxs-lookup"><span data-stu-id="5c6d3-105">The element is a string with a maximum of 20 characters.</span></span>

<span data-ttu-id="5c6d3-106">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5c6d3-106">This element is optional.</span></span>

``` syntax
<xs:element name="ProviderName"
    type="providerNameType"
 />
```

<span data-ttu-id="5c6d3-107">Элемент **providerName** определяется сложным типом [**ProviderType**](schema-providertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5c6d3-107">The **ProviderName** element is defined by the [**providerType**](schema-providertype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c6d3-108">Требования</span><span class="sxs-lookup"><span data-stu-id="5c6d3-108">Requirements</span></span>



| <span data-ttu-id="5c6d3-109">Требование</span><span class="sxs-lookup"><span data-stu-id="5c6d3-109">Requirement</span></span> | <span data-ttu-id="5c6d3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="5c6d3-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="5c6d3-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c6d3-111">Minimum supported client</span></span><br/> | <span data-ttu-id="5c6d3-112">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="5c6d3-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="5c6d3-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c6d3-113">Minimum supported server</span></span><br/> | <span data-ttu-id="5c6d3-114">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5c6d3-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="5c6d3-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c6d3-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c6d3-116">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="5c6d3-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5c6d3-117">**providerType**</span><span class="sxs-lookup"><span data-stu-id="5c6d3-117">**providerType**</span></span>](schema-providertype-complextype.md)
</dt> <dt>

<span data-ttu-id="5c6d3-118">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="5c6d3-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5c6d3-119">**Поставщик (Датароамингпартнерс)**</span><span class="sxs-lookup"><span data-stu-id="5c6d3-119">**Provider (DataRoamingPartners)**</span></span>](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




