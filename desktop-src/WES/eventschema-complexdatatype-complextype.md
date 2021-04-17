---
title: Сложный тип Комплексдататипе
description: Определяет структуру, содержащую один или несколько элементов данных.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- Журнал событий сложных типов Комплексдататипе
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691898"
---
# <a name="complexdatatype-complex-type"></a><span data-ttu-id="15791-104">Сложный тип Комплексдататипе</span><span class="sxs-lookup"><span data-stu-id="15791-104">ComplexDataType Complex Type</span></span>

<span data-ttu-id="15791-105">Определяет структуру, содержащую один или несколько элементов данных.</span><span class="sxs-lookup"><span data-stu-id="15791-105">Defines a structure that contains one or more data items.</span></span>

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="15791-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="15791-106">Child elements</span></span>



| <span data-ttu-id="15791-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="15791-107">Element</span></span>                                                  | <span data-ttu-id="15791-108">Тип</span><span class="sxs-lookup"><span data-stu-id="15791-108">Type</span></span>                                                      | <span data-ttu-id="15791-109">Описание</span><span class="sxs-lookup"><span data-stu-id="15791-109">Description</span></span>                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15791-110">**Данные**</span><span class="sxs-lookup"><span data-stu-id="15791-110">**Data**</span></span>](eventschema-data-complexdatatype-element.md) | [<span data-ttu-id="15791-111">**DataType**</span><span class="sxs-lookup"><span data-stu-id="15791-111">**DataType**</span></span>](eventschema-datafieldtype-complextype.md) | <span data-ttu-id="15791-112">Список элементов данных в структуре.</span><span class="sxs-lookup"><span data-stu-id="15791-112">The list of data items in the structure.</span></span> <span data-ttu-id="15791-113">Список элементов находится в том же порядке, что и определено в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="15791-113">The list of items are in the same order as defined in the template.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="15791-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="15791-114">Attributes</span></span>



| <span data-ttu-id="15791-115">Имя</span><span class="sxs-lookup"><span data-stu-id="15791-115">Name</span></span> | <span data-ttu-id="15791-116">Тип</span><span class="sxs-lookup"><span data-stu-id="15791-116">Type</span></span>   | <span data-ttu-id="15791-117">Описание</span><span class="sxs-lookup"><span data-stu-id="15791-117">Description</span></span>                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15791-118">Название</span><span class="sxs-lookup"><span data-stu-id="15791-118">Name</span></span> | <span data-ttu-id="15791-119">строка</span><span class="sxs-lookup"><span data-stu-id="15791-119">string</span></span> | <span data-ttu-id="15791-120">Имя структуры.</span><span class="sxs-lookup"><span data-stu-id="15791-120">The name of the structure.</span></span> <span data-ttu-id="15791-121">Это имя, указанное при определении структуры в шаблоне (см. сложный тип [**темплатеитемтипе**](eventmanifestschema-templateitemtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="15791-121">This is the name that is specified when you defined the structure in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="15791-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15791-122">Remarks</span></span>

<span data-ttu-id="15791-123">Функция [**евтрендер**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) визуализирует содержимое структуры как двоичный BLOB-объект. функция не отображает отдельные элементы данных структуры.</span><span class="sxs-lookup"><span data-stu-id="15791-123">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders the contents of a structure as a binary blob; the function does not render the individual data items of the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="15791-124">Требования</span><span class="sxs-lookup"><span data-stu-id="15791-124">Requirements</span></span>



| <span data-ttu-id="15791-125">Требование</span><span class="sxs-lookup"><span data-stu-id="15791-125">Requirement</span></span> | <span data-ttu-id="15791-126">Значение</span><span class="sxs-lookup"><span data-stu-id="15791-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15791-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15791-127">Minimum supported client</span></span><br/> | <span data-ttu-id="15791-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15791-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="15791-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15791-129">Minimum supported server</span></span><br/> | <span data-ttu-id="15791-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15791-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





