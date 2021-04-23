---
title: Элемент Keyword (Кэйвордлисттипе)
description: Определяет ключевое слово, определяющее категорию событий. | Элемент Keyword (Кэйвордлисттипе)
ms.assetid: c921eb01-f1b0-455c-8ff9-06895f1e40f9
keywords:
- Журнал событий элемента ключевого слова
topic_type:
- apiref
api_name:
- keyword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f4b1b0b60502339db55c3227add9bb5a263200aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693999"
---
# <a name="keyword-keywordlisttype-element"></a><span data-ttu-id="cd9cb-105">Элемент Keyword (Кэйвордлисттипе)</span><span class="sxs-lookup"><span data-stu-id="cd9cb-105">keyword (KeywordListType) Element</span></span>

<span data-ttu-id="cd9cb-106">Определяет ключевое слово, определяющее категорию событий.</span><span class="sxs-lookup"><span data-stu-id="cd9cb-106">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="cd9cb-107">Ключевое слово — это тег, который присоединяется к событию для группирования событий в зависимости от их использования.</span><span class="sxs-lookup"><span data-stu-id="cd9cb-107">A keyword is a tag that you attach to an event to group events based on their usage.</span></span>

``` syntax
<xs:element name="keyword"
    type="KeywordType"
 />
```

<span data-ttu-id="cd9cb-108">Элемент **keyword** определяется сложным типом [**кэйвордлисттипе**](eventmanifestschema-keywordlisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cd9cb-108">The **keyword** element is defined by the [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9cb-109">Требования</span><span class="sxs-lookup"><span data-stu-id="cd9cb-109">Requirements</span></span>



| <span data-ttu-id="cd9cb-110">Требование</span><span class="sxs-lookup"><span data-stu-id="cd9cb-110">Requirement</span></span> | <span data-ttu-id="cd9cb-111">Значение</span><span class="sxs-lookup"><span data-stu-id="cd9cb-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd9cb-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd9cb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cd9cb-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd9cb-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cd9cb-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd9cb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cd9cb-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd9cb-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd9cb-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd9cb-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd9cb-117">**Родительские элементы**</span><span class="sxs-lookup"><span data-stu-id="cd9cb-117">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="cd9cb-118">**Ключевые слова (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="cd9cb-118">**keywords (ProviderType)**</span></span>](eventmanifestschema-keywords-providertype-element.md)
</dt> <dt>

[<span data-ttu-id="cd9cb-119">**Ключевые слова (Метадататипе)**</span><span class="sxs-lookup"><span data-stu-id="cd9cb-119">**keywords (MetadataType)**</span></span>](eventmanifestschema-keywords-metadatatype-element.md)
</dt> </dl>

 

 





