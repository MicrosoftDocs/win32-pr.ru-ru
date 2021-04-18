---
title: Сложный тип DataType (журнал событий Windows)
description: Определяет элемент данных.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- Журнал событий сложного типа DataType
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341055"
---
# <a name="datatype-complex-type"></a><span data-ttu-id="e601b-104">Сложный тип DataType</span><span class="sxs-lookup"><span data-stu-id="e601b-104">DataType Complex Type</span></span>

<span data-ttu-id="e601b-105">Определяет элемент данных.</span><span class="sxs-lookup"><span data-stu-id="e601b-105">Defines a data item.</span></span>

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="e601b-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e601b-106">Attributes</span></span>



| <span data-ttu-id="e601b-107">Имя</span><span class="sxs-lookup"><span data-stu-id="e601b-107">Name</span></span> | <span data-ttu-id="e601b-108">Тип</span><span class="sxs-lookup"><span data-stu-id="e601b-108">Type</span></span>   | <span data-ttu-id="e601b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e601b-109">Description</span></span>                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e601b-110">Название</span><span class="sxs-lookup"><span data-stu-id="e601b-110">Name</span></span> | <span data-ttu-id="e601b-111">строка</span><span class="sxs-lookup"><span data-stu-id="e601b-111">string</span></span> | <span data-ttu-id="e601b-112">Имя элемента данных, определенного в шаблоне (см. сложный тип [**темплатеитемтипе**](eventmanifestschema-templateitemtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="e601b-112">The name of a data item that was defined in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |
| <span data-ttu-id="e601b-113">Тип</span><span class="sxs-lookup"><span data-stu-id="e601b-113">Type</span></span> | <span data-ttu-id="e601b-114">QName</span><span class="sxs-lookup"><span data-stu-id="e601b-114">QName</span></span>  | <span data-ttu-id="e601b-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="e601b-115">Not used.</span></span><br/>                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="e601b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e601b-116">Remarks</span></span>

<span data-ttu-id="e601b-117">Элемент данных может быть элементом данных верхнего уровня или элементом данных в структуре.</span><span class="sxs-lookup"><span data-stu-id="e601b-117">The data item can be a top-level data item or a data item in a structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e601b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e601b-118">Requirements</span></span>



| <span data-ttu-id="e601b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e601b-119">Requirement</span></span> | <span data-ttu-id="e601b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e601b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e601b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e601b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e601b-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e601b-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e601b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e601b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e601b-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e601b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





