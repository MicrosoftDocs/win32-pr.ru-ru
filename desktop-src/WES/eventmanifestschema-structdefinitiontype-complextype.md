---
title: Сложный тип Структдефинитионтипе
description: Определяет структуру, содержащую один или несколько элементов данных, которые необходимо включить в событие. | Сложный тип Структдефинитионтипе
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- Журнал событий сложных типов Структдефинитионтипе
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01e739077d38dec94c0a407e5779bec90369ffb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693987"
---
# <a name="structdefinitiontype-complex-type"></a><span data-ttu-id="06b9f-105">Сложный тип Структдефинитионтипе</span><span class="sxs-lookup"><span data-stu-id="06b9f-105">StructDefinitionType Complex Type</span></span>

<span data-ttu-id="06b9f-106">Определяет структуру, содержащую один или несколько элементов данных, которые необходимо включить в событие.</span><span class="sxs-lookup"><span data-stu-id="06b9f-106">Defines a structure that includes one or more data items that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="06b9f-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="06b9f-107">Child elements</span></span>



| <span data-ttu-id="06b9f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="06b9f-108">Element</span></span>                                                               | <span data-ttu-id="06b9f-109">Тип</span><span class="sxs-lookup"><span data-stu-id="06b9f-109">Type</span></span>                                                                             | <span data-ttu-id="06b9f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="06b9f-110">Description</span></span>                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="06b9f-111">**Data**</span><span class="sxs-lookup"><span data-stu-id="06b9f-111">**data**</span></span>](eventmanifestschema-data-structdefinitiontype-element.md) | [<span data-ttu-id="06b9f-112">**датадефинитионтипе**</span><span class="sxs-lookup"><span data-stu-id="06b9f-112">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md) | <span data-ttu-id="06b9f-113">Определяет элемент данных, который необходимо включить в структуру.</span><span class="sxs-lookup"><span data-stu-id="06b9f-113">Defines a data item that you want to include in the structure.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="06b9f-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="06b9f-114">Attributes</span></span>



| <span data-ttu-id="06b9f-115">Имя</span><span class="sxs-lookup"><span data-stu-id="06b9f-115">Name</span></span>   | <span data-ttu-id="06b9f-116">Тип</span><span class="sxs-lookup"><span data-stu-id="06b9f-116">Type</span></span>                                                            | <span data-ttu-id="06b9f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="06b9f-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06b9f-118">count</span><span class="sxs-lookup"><span data-stu-id="06b9f-118">count</span></span>  | [<span data-ttu-id="06b9f-119">**каунттипе**</span><span class="sxs-lookup"><span data-stu-id="06b9f-119">**CountType**</span></span>](eventmanifestschema-counttype-simpletype.md)   | <span data-ttu-id="06b9f-120">Число элементов в массиве структур.</span><span class="sxs-lookup"><span data-stu-id="06b9f-120">The number of elements in an array of structures.</span></span> <span data-ttu-id="06b9f-121">Этот атрибут указывает, что структура определяет массив структур.</span><span class="sxs-lookup"><span data-stu-id="06b9f-121">This attribute indicates that the structure is defining an array of structures.</span></span> <span data-ttu-id="06b9f-122">Можно указать фактическое число или имя элемента данных за пределами структуры, содержащей число.</span><span class="sxs-lookup"><span data-stu-id="06b9f-122">You can specify the actual count or the name of a data item outside of the structure that contains the count.</span></span> <br/>                               |
| <span data-ttu-id="06b9f-123">length</span><span class="sxs-lookup"><span data-stu-id="06b9f-123">length</span></span> | [<span data-ttu-id="06b9f-124">**ленгстипе**</span><span class="sxs-lookup"><span data-stu-id="06b9f-124">**LengthType**</span></span>](eventmanifestschema-lengthtype-simpletype.md) | <span data-ttu-id="06b9f-125">Недоступно.</span><span class="sxs-lookup"><span data-stu-id="06b9f-125">Not available.</span></span><br/> <span data-ttu-id="06b9f-126">**Windows Server 2008 и Windows Vista:** Длина этой структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="06b9f-126">**Windows Server 2008 and Windows Vista:** The length of this structure, in bytes.</span></span> <span data-ttu-id="06b9f-127">Недоступно начиная с Windows 7.</span><span class="sxs-lookup"><span data-stu-id="06b9f-127">Not available starting with Windows 7.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="06b9f-128">name</span><span class="sxs-lookup"><span data-stu-id="06b9f-128">name</span></span>   | <span data-ttu-id="06b9f-129">строка</span><span class="sxs-lookup"><span data-stu-id="06b9f-129">string</span></span>                                                          | <span data-ttu-id="06b9f-130">Имя структуры.</span><span class="sxs-lookup"><span data-stu-id="06b9f-130">The name to the structure.</span></span> <span data-ttu-id="06b9f-131">Имя можно использовать для ссылки на элемент данных в фрагменте XML, если в шаблоне указан раздел [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="06b9f-131">You can use the name to reference the data item in your XML fragment if you specify a [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) section in your template.</span></span><br/> <span data-ttu-id="06b9f-132">**Windows Vista:** Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="06b9f-132">**Windows Vista:** This attribute is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="06b9f-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06b9f-133">Remarks</span></span>

<span data-ttu-id="06b9f-134">Поставщики записывают структуру в виде большого двоичного объекта, а не отдельных членов структуры.</span><span class="sxs-lookup"><span data-stu-id="06b9f-134">Providers write the structure as a blob and not as individual members of the structure.</span></span> <span data-ttu-id="06b9f-135">Если написанная структура C содержит указатели (например, указатель типа LPWSTR), то данные события будут содержать значение указателя, а не данные разыменования.</span><span class="sxs-lookup"><span data-stu-id="06b9f-135">If the C structure that you are writing contains pointers (for example, a pointer of type LPWSTR), the event data will contain the pointer value, not the dereferenced data.</span></span>

<span data-ttu-id="06b9f-136">Не следует использовать структуры, а должны определять элементы данных для каждого элемента и записывать их отдельно.</span><span class="sxs-lookup"><span data-stu-id="06b9f-136">You should not use structures but instead should define data items for each member and write them separately.</span></span> <span data-ttu-id="06b9f-137">Если вы решили использовать структуру, структура должна содержать только целочисленные типы, и необходимо обеспечить, чтобы элементы структуры высовпадали с 8-байтовой границей.</span><span class="sxs-lookup"><span data-stu-id="06b9f-137">If you decide to use structure, the structure should contain only integral types and you must ensure that the members of the structure align to an 8-byte boundary.</span></span> <span data-ttu-id="06b9f-138">Если этого не сделать, то, скорее всего, будут выдаваться ошибки выравнивания при попытке доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="06b9f-138">If you do not, you will likely receive alignment errors when you try to access the data.</span></span> <span data-ttu-id="06b9f-139">Рекомендуется использовать \# директиву pragma pack () для принудительного выравнивания на 8-байтовой границе.</span><span class="sxs-lookup"><span data-stu-id="06b9f-139">Consider using the \#pragma pack() directive to force alignment on an 8-byte boundary.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b9f-140">Требования</span><span class="sxs-lookup"><span data-stu-id="06b9f-140">Requirements</span></span>



| <span data-ttu-id="06b9f-141">Требование</span><span class="sxs-lookup"><span data-stu-id="06b9f-141">Requirement</span></span> | <span data-ttu-id="06b9f-142">Значение</span><span class="sxs-lookup"><span data-stu-id="06b9f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="06b9f-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06b9f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="06b9f-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06b9f-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="06b9f-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06b9f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="06b9f-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06b9f-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





