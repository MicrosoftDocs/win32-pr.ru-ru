---
description: Определяет имя и идентификатор поставщика для сети сотовой связи.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Элемент Provider (Датароамингпартнерс)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: b5b36c973bf44175b90e25fd2a141fed3624d8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144791"
---
# <a name="provider-dataroamingpartners-element"></a><span data-ttu-id="c6988-103">Элемент Provider (Датароамингпартнерс)</span><span class="sxs-lookup"><span data-stu-id="c6988-103">Provider (DataRoamingPartners) Element</span></span>

<span data-ttu-id="c6988-104">Элемент **provider (датароамингпартнерс)** определяет имя и идентификатор поставщика для сети сотовой связи.</span><span class="sxs-lookup"><span data-stu-id="c6988-104">The **Provider (DataRoamingPartners)** element identifies the name and provider ID for a cellular network.</span></span>

<span data-ttu-id="c6988-105">Этот элемент содержит следующие дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="c6988-105">This element has the following child elements.</span></span>

-   [<span data-ttu-id="c6988-106">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="c6988-106">**ProviderID**</span></span>](schema-providerid-providertype-element.md)
-   [<span data-ttu-id="c6988-107">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="c6988-107">**ProviderName**</span></span>](schema-providername-providertype-element.md)

<span data-ttu-id="c6988-108">Этот элемент может быть определен несколько раз в элементе [**датароамингпартнерс**](schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c6988-108">This element can be defined multiple times within the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span> <span data-ttu-id="c6988-109">Его необходимо определить по крайней мере один раз.</span><span class="sxs-lookup"><span data-stu-id="c6988-109">It must be defined at least once.</span></span>

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

<span data-ttu-id="c6988-110">Элемент **provider** определяется элементом [**датароамингпартнерс**](schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c6988-110">The **Provider** element is defined by the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6988-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c6988-111">Requirements</span></span>



| <span data-ttu-id="c6988-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c6988-112">Requirement</span></span> | <span data-ttu-id="c6988-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c6988-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c6988-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6988-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c6988-115">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="c6988-115">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c6988-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6988-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c6988-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c6988-117">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="c6988-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6988-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6988-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="c6988-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c6988-120">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="c6988-120">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="c6988-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="c6988-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c6988-122">**Датароамингпартнерс (Мбнпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="c6988-122">**DataRoamingPartners (MBNProfile)**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




