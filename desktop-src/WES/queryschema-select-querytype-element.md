---
title: Элемент SELECT (QueryType)
description: Запрос XPath, определяющий события, включаемые в результирующий набор запроса.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Выбор журнала элементов
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416021"
---
# <a name="select-querytype-element"></a><span data-ttu-id="077a6-104">Элемент SELECT (QueryType)</span><span class="sxs-lookup"><span data-stu-id="077a6-104">Select (QueryType) Element</span></span>

<span data-ttu-id="077a6-105">Запрос XPath, определяющий события, включаемые в результирующий набор запроса.</span><span class="sxs-lookup"><span data-stu-id="077a6-105">An XPath query that identifies the events to include in the query result set.</span></span>

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="077a6-106">Элемент **SELECT** определяется сложным типом [**QueryType**](queryschema-querytype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="077a6-106">The **Select** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="077a6-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="077a6-107">Attributes</span></span>



| <span data-ttu-id="077a6-108">Имя</span><span class="sxs-lookup"><span data-stu-id="077a6-108">Name</span></span> | <span data-ttu-id="077a6-109">Тип</span><span class="sxs-lookup"><span data-stu-id="077a6-109">Type</span></span>   | <span data-ttu-id="077a6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="077a6-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="077a6-111">Путь</span><span class="sxs-lookup"><span data-stu-id="077a6-111">Path</span></span> | <span data-ttu-id="077a6-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="077a6-112">anyURI</span></span> | <span data-ttu-id="077a6-113">Имя канала или путь к файлу журнала, содержащему события.</span><span class="sxs-lookup"><span data-stu-id="077a6-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="077a6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="077a6-114">Requirements</span></span>



| <span data-ttu-id="077a6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="077a6-115">Requirement</span></span> | <span data-ttu-id="077a6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="077a6-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="077a6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="077a6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="077a6-118">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="077a6-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="077a6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="077a6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="077a6-120">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="077a6-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="077a6-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="077a6-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="077a6-122">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="077a6-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="077a6-123">**Запрос (Куерилисттипе)**</span><span class="sxs-lookup"><span data-stu-id="077a6-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





