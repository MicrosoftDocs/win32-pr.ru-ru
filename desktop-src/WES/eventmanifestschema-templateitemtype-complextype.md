---
title: Сложный тип Темплатеитемтипе
description: Шаблон, определяющий данные, включаемые в событие. | Сложный тип Темплатеитемтипе
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- Журнал событий сложных типов Темплатеитемтипе
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273534"
---
# <a name="templateitemtype-complex-type"></a><span data-ttu-id="d39d1-105">Сложный тип Темплатеитемтипе</span><span class="sxs-lookup"><span data-stu-id="d39d1-105">TemplateItemType Complex Type</span></span>

<span data-ttu-id="d39d1-106">Шаблон, определяющий данные, включаемые в событие.</span><span class="sxs-lookup"><span data-stu-id="d39d1-106">A template that defines the data to include with an event.</span></span>

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d39d1-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d39d1-107">Child elements</span></span>



| <span data-ttu-id="d39d1-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="d39d1-108">Element</span></span>                                                                   | <span data-ttu-id="d39d1-109">Тип</span><span class="sxs-lookup"><span data-stu-id="d39d1-109">Type</span></span>                                                                                 | <span data-ttu-id="d39d1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d39d1-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d39d1-111">**двоичный**</span><span class="sxs-lookup"><span data-stu-id="d39d1-111">**binary**</span></span>](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | <span data-ttu-id="d39d1-112">Зарезервировано только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="d39d1-112">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="d39d1-113">**Data**</span><span class="sxs-lookup"><span data-stu-id="d39d1-113">**data**</span></span>](eventmanifestschema-data-templateitemtype-element.md)         | [<span data-ttu-id="d39d1-114">**датадефинитионтипе**</span><span class="sxs-lookup"><span data-stu-id="d39d1-114">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md)     | <span data-ttu-id="d39d1-115">Определяет элемент данных, который необходимо включить в событие.</span><span class="sxs-lookup"><span data-stu-id="d39d1-115">Defines a data item that you want to include with the event.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="d39d1-116">**struct**</span><span class="sxs-lookup"><span data-stu-id="d39d1-116">**struct**</span></span>](eventmanifestschema-struct-templateitemtype-element.md)     | [<span data-ttu-id="d39d1-117">**структдефинитионтипе**</span><span class="sxs-lookup"><span data-stu-id="d39d1-117">**StructDefinitionType**</span></span>](eventmanifestschema-structdefinitiontype-complextype.md) | <span data-ttu-id="d39d1-118">Определяет структуру, содержащую один или несколько элементов данных, которые необходимо включить в событие.</span><span class="sxs-lookup"><span data-stu-id="d39d1-118">Defines a structure that includes one or more data items that you want to include with the event.</span></span> <span data-ttu-id="d39d1-119">Поставщики записывают структуру в виде большого двоичного объекта, а не отдельных членов структуры.</span><span class="sxs-lookup"><span data-stu-id="d39d1-119">Providers write the structure as a blob and not as individual members of the structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="d39d1-120">**UserData**</span><span class="sxs-lookup"><span data-stu-id="d39d1-120">**UserData**</span></span>](eventmanifestschema-userdata-templateitemtype-element.md) | [<span data-ttu-id="d39d1-121">**XmlType**</span><span class="sxs-lookup"><span data-stu-id="d39d1-121">**XmlType**</span></span>](eventmanifestschema-xmltype-complextype.md)                           | <span data-ttu-id="d39d1-122">Фрагмент XML-кода, используемый для визуализации данных события.</span><span class="sxs-lookup"><span data-stu-id="d39d1-122">An XML fragment that is used to render the event data.</span></span> <span data-ttu-id="d39d1-123">Если фрагмент не включен, данные события подготавливаются к просмотру в том порядке, в котором элементы данных определены в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="d39d1-123">If you do not include the fragment, the event data is rendered in the order that the data items are defined in the template.</span></span> <span data-ttu-id="d39d1-124">Содержимым этого элемента является любой допустимый фрагмент XML.</span><span class="sxs-lookup"><span data-stu-id="d39d1-124">The contents of this element is any valid XML fragment.</span></span> <span data-ttu-id="d39d1-125">Фрагмент должен содержать только один узел верхнего уровня, а узел верхнего уровня должен указывать собственное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="d39d1-125">The fragment must contain only one top-level node and the top-level node must specify its own namespace.</span></span> <br/> <span data-ttu-id="d39d1-126">Чтобы сослаться на элемент данных в фрагменте, задайте для текста узла в фрагменте значение%*n*, где *n* — это Отсчитываемый от единицы индекс элементов данных верхнего уровня в списке элементов данных (ссылки на члены структуры не могут быть сослаться).</span><span class="sxs-lookup"><span data-stu-id="d39d1-126">To reference a data item in the fragment, set the text body for a node in the fragment to %*n*, where *n* is the one-based index of the top-level data items in the list of data items (you cannot reference members of a structure).</span></span> <span data-ttu-id="d39d1-127">Указанное значение индекса не должно превышать число элементов данных верхнего уровня в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="d39d1-127">The index value that you specify must not be greater than the number of top-level data items in the template.</span></span><br/> <span data-ttu-id="d39d1-128">Этот элемент соответствует всем **данным** и элементам **структуры** .</span><span class="sxs-lookup"><span data-stu-id="d39d1-128">This element follows all **data** and **struct** elements.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="d39d1-129">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d39d1-129">Attributes</span></span>



| <span data-ttu-id="d39d1-130">Имя</span><span class="sxs-lookup"><span data-stu-id="d39d1-130">Name</span></span> | <span data-ttu-id="d39d1-131">Тип</span><span class="sxs-lookup"><span data-stu-id="d39d1-131">Type</span></span>   | <span data-ttu-id="d39d1-132">Описание</span><span class="sxs-lookup"><span data-stu-id="d39d1-132">Description</span></span>                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d39d1-133">name</span><span class="sxs-lookup"><span data-stu-id="d39d1-133">name</span></span> | <span data-ttu-id="d39d1-134">строка</span><span class="sxs-lookup"><span data-stu-id="d39d1-134">string</span></span> | <span data-ttu-id="d39d1-135">Зарезервировано только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="d39d1-135">Reserved for internal use only.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="d39d1-136">name</span><span class="sxs-lookup"><span data-stu-id="d39d1-136">name</span></span> | <span data-ttu-id="d39d1-137">строка</span><span class="sxs-lookup"><span data-stu-id="d39d1-137">string</span></span> | <span data-ttu-id="d39d1-138">Имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="d39d1-138">The name of the template.</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="d39d1-139">tid</span><span class="sxs-lookup"><span data-stu-id="d39d1-139">tid</span></span>  | <span data-ttu-id="d39d1-140">token</span><span class="sxs-lookup"><span data-stu-id="d39d1-140">token</span></span>  | <span data-ttu-id="d39d1-141">Идентификатор, который уникальным образом идентифицирует шаблон в списке шаблонов, определяемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="d39d1-141">An identifier that uniquely identifies the template within the list of templates that the provider defines.</span></span> <span data-ttu-id="d39d1-142">Используйте это имя для ссылки на шаблон при определении определения события.</span><span class="sxs-lookup"><span data-stu-id="d39d1-142">Use this name to reference the template when you define your event definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d39d1-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d39d1-143">Remarks</span></span>

<span data-ttu-id="d39d1-144">Определение шаблона должно иметь по крайней мере один дочерний элемент данных или структуры.</span><span class="sxs-lookup"><span data-stu-id="d39d1-144">The template definition must have at least one data or struct child element.</span></span> <span data-ttu-id="d39d1-145">Поставщик должен записывать данные события в порядке элементов данных, определенных в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="d39d1-145">The provider must write the event data in the order of the data items defined in the template.</span></span>

<span data-ttu-id="d39d1-146">Размер всех элементов данных в шаблоне должен быть менее 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="d39d1-146">The size of all the data items in the template must be less than 64 KB.</span></span>

## <a name="examples"></a><span data-ttu-id="d39d1-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="d39d1-147">Examples</span></span>

<span data-ttu-id="d39d1-148">В следующем примере показано, как создать определение шаблона.</span><span class="sxs-lookup"><span data-stu-id="d39d1-148">The following example shows how to create a template definition.</span></span>


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a><span data-ttu-id="d39d1-149">Требования</span><span class="sxs-lookup"><span data-stu-id="d39d1-149">Requirements</span></span>



| <span data-ttu-id="d39d1-150">Требование</span><span class="sxs-lookup"><span data-stu-id="d39d1-150">Requirement</span></span> | <span data-ttu-id="d39d1-151">Значение</span><span class="sxs-lookup"><span data-stu-id="d39d1-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d39d1-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d39d1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d39d1-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d39d1-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d39d1-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d39d1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d39d1-155">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d39d1-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





