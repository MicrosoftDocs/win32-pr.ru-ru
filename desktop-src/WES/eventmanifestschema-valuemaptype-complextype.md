---
title: Сложный тип Валуемаптипе
description: Определяет список сопоставлений имен и значений между целочисленными значениями и строковыми значениями.
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- Журнал событий сложных типов Валуемаптипе
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28fde51466ba506802c8dbc5379f1628fd943fa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800935"
---
# <a name="valuemaptype-complex-type"></a><span data-ttu-id="3710e-104">Сложный тип Валуемаптипе</span><span class="sxs-lookup"><span data-stu-id="3710e-104">ValueMapType Complex Type</span></span>

<span data-ttu-id="3710e-105">Определяет список сопоставлений имен и значений между целочисленными значениями и строковыми значениями.</span><span class="sxs-lookup"><span data-stu-id="3710e-105">Defines a list of name/value mappings between integer values and string values.</span></span>

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3710e-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3710e-106">Child elements</span></span>



| <span data-ttu-id="3710e-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="3710e-107">Element</span></span>                                                     | <span data-ttu-id="3710e-108">Тип</span><span class="sxs-lookup"><span data-stu-id="3710e-108">Type</span></span>                                                                           | <span data-ttu-id="3710e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3710e-109">Description</span></span>                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="3710e-110">**Таблица**</span><span class="sxs-lookup"><span data-stu-id="3710e-110">**map**</span></span>](eventmanifestschema-map-valuemaptype-element.md) | [<span data-ttu-id="3710e-111">**валуемапвалуетипе**</span><span class="sxs-lookup"><span data-stu-id="3710e-111">**ValueMapValueType**</span></span>](eventmanifestschema-valuemapvaluetype-complextype.md) | <span data-ttu-id="3710e-112">Определяет сопоставление между целочисленным значением и строковым значением.</span><span class="sxs-lookup"><span data-stu-id="3710e-112">Defines the mapping between an integer value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="3710e-113">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3710e-113">Attributes</span></span>



| <span data-ttu-id="3710e-114">Имя</span><span class="sxs-lookup"><span data-stu-id="3710e-114">Name</span></span>   | <span data-ttu-id="3710e-115">Тип</span><span class="sxs-lookup"><span data-stu-id="3710e-115">Type</span></span>                                                              | <span data-ttu-id="3710e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="3710e-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3710e-117">name</span><span class="sxs-lookup"><span data-stu-id="3710e-117">name</span></span>   | <span data-ttu-id="3710e-118">строка</span><span class="sxs-lookup"><span data-stu-id="3710e-118">string</span></span>                                                            | <span data-ttu-id="3710e-119">Имя схемы значений.</span><span class="sxs-lookup"><span data-stu-id="3710e-119">The name of the value map.</span></span> <span data-ttu-id="3710e-120">Используйте имя в элементе Data для ссылки на сопоставления.</span><span class="sxs-lookup"><span data-stu-id="3710e-120">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                     |
| <span data-ttu-id="3710e-121">символ</span><span class="sxs-lookup"><span data-stu-id="3710e-121">symbol</span></span> | [<span data-ttu-id="3710e-122">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="3710e-122">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="3710e-123">Символ, используемый для ссылки на сопоставления в приложении.</span><span class="sxs-lookup"><span data-stu-id="3710e-123">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="3710e-124">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ для создания константы для Map в файле заголовка, создаваемого компилятором.</span><span class="sxs-lookup"><span data-stu-id="3710e-124">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="3710e-125">Если не указать символ, компилятор создаст его.</span><span class="sxs-lookup"><span data-stu-id="3710e-125">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3710e-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3710e-126">Requirements</span></span>



| <span data-ttu-id="3710e-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3710e-127">Requirement</span></span> | <span data-ttu-id="3710e-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3710e-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3710e-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3710e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3710e-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3710e-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3710e-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3710e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3710e-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3710e-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





