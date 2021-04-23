---
title: Сложный тип Кэйвордлисттипе
description: Определяет список ключевых слов, которые классифицируют события. | Сложный тип Кэйвордлисттипе
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- Журнал событий сложных типов Кэйвордлисттипе
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693997"
---
# <a name="keywordlisttype-complex-type"></a><span data-ttu-id="9dbdf-105">Сложный тип Кэйвордлисттипе</span><span class="sxs-lookup"><span data-stu-id="9dbdf-105">KeywordListType Complex Type</span></span>

<span data-ttu-id="9dbdf-106">Определяет список ключевых слов, которые классифицируют события.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-106">Defines a list of keywords that categorize events.</span></span>

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9dbdf-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9dbdf-107">Child elements</span></span>



| <span data-ttu-id="9dbdf-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="9dbdf-108">Element</span></span>                                                                | <span data-ttu-id="9dbdf-109">Тип</span><span class="sxs-lookup"><span data-stu-id="9dbdf-109">Type</span></span>                                                               | <span data-ttu-id="9dbdf-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9dbdf-110">Description</span></span>                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9dbdf-111">**This**</span><span class="sxs-lookup"><span data-stu-id="9dbdf-111">**keyword**</span></span>](eventmanifestschema-keyword-keywordlisttype-element.md) | [<span data-ttu-id="9dbdf-112">**кэйвордтипе**</span><span class="sxs-lookup"><span data-stu-id="9dbdf-112">**KeywordType**</span></span>](eventmanifestschema-keywordtype-complextype.md) | <span data-ttu-id="9dbdf-113">Определяет ключевое слово, определяющее категорию событий.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-113">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="9dbdf-114">Можно указать не более 48 ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-114">You can specify a maximum of 48 keywords.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9dbdf-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9dbdf-115">Requirements</span></span>



| <span data-ttu-id="9dbdf-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9dbdf-116">Requirement</span></span> | <span data-ttu-id="9dbdf-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9dbdf-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9dbdf-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9dbdf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9dbdf-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9dbdf-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9dbdf-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9dbdf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9dbdf-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9dbdf-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





