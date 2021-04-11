---
title: Подавлять (QueryType) элемент
description: Запрос XPath, определяющий события, исключаемые из результирующего набора запроса.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Подавлять элемент EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137666"
---
# <a name="suppress-querytype-element"></a><span data-ttu-id="2241c-104">Подавлять (QueryType) элемент</span><span class="sxs-lookup"><span data-stu-id="2241c-104">Suppress (QueryType) Element</span></span>

<span data-ttu-id="2241c-105">Запрос XPath, определяющий события, исключаемые из результирующего набора запроса.</span><span class="sxs-lookup"><span data-stu-id="2241c-105">An XPath query that identifies the events to exclude from the query result set.</span></span>

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="2241c-106">Элемент **подавлять** определяется сложным типом [**QueryType**](queryschema-querytype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2241c-106">The **Suppress** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="2241c-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2241c-107">Attributes</span></span>



| <span data-ttu-id="2241c-108">Имя</span><span class="sxs-lookup"><span data-stu-id="2241c-108">Name</span></span> | <span data-ttu-id="2241c-109">Тип</span><span class="sxs-lookup"><span data-stu-id="2241c-109">Type</span></span>   | <span data-ttu-id="2241c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="2241c-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2241c-111">Путь</span><span class="sxs-lookup"><span data-stu-id="2241c-111">Path</span></span> | <span data-ttu-id="2241c-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="2241c-112">anyURI</span></span> | <span data-ttu-id="2241c-113">Имя канала или путь к файлу журнала, содержащему события.</span><span class="sxs-lookup"><span data-stu-id="2241c-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2241c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2241c-114">Requirements</span></span>



| <span data-ttu-id="2241c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2241c-115">Requirement</span></span> | <span data-ttu-id="2241c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2241c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2241c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2241c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2241c-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2241c-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2241c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2241c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2241c-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2241c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2241c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2241c-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="2241c-122">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="2241c-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="2241c-123">**Запрос (Куерилисттипе)**</span><span class="sxs-lookup"><span data-stu-id="2241c-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





