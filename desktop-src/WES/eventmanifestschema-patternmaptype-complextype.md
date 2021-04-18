---
title: Сложный тип Паттернмаптипе
description: Не используется. Определяет сопоставление между двумя регулярными выражениями. Одно выражение используется для поиска соответствующей строки в строке сообщения, а другая — для изменения строки перед тем, как служба снова поместит ее в строку сообщения.
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- Журнал событий сложных типов Паттернмаптипе
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e39ca30520f4f595bfc73a4d80b9bc191793859a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491283"
---
# <a name="patternmaptype-complex-type"></a><span data-ttu-id="873d1-106">Сложный тип Паттернмаптипе</span><span class="sxs-lookup"><span data-stu-id="873d1-106">PatternMapType Complex Type</span></span>

<span data-ttu-id="873d1-107">Не используется.</span><span class="sxs-lookup"><span data-stu-id="873d1-107">Not used.</span></span> <span data-ttu-id="873d1-108">Определяет сопоставление между двумя регулярными выражениями.</span><span class="sxs-lookup"><span data-stu-id="873d1-108">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="873d1-109">Одно выражение используется для поиска соответствующей строки в строке сообщения, а другая — для изменения строки перед тем, как служба снова поместит ее в строку сообщения.</span><span class="sxs-lookup"><span data-stu-id="873d1-109">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="873d1-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="873d1-110">Child elements</span></span>



| <span data-ttu-id="873d1-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="873d1-111">Element</span></span>                                                       | <span data-ttu-id="873d1-112">Тип</span><span class="sxs-lookup"><span data-stu-id="873d1-112">Type</span></span>                                                                               | <span data-ttu-id="873d1-113">Описание</span><span class="sxs-lookup"><span data-stu-id="873d1-113">Description</span></span>                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="873d1-114">**Таблица**</span><span class="sxs-lookup"><span data-stu-id="873d1-114">**map**</span></span>](eventmanifestschema-map-patternmaptype-element.md) | [<span data-ttu-id="873d1-115">**паттернмапвалуетипе**</span><span class="sxs-lookup"><span data-stu-id="873d1-115">**PatternMapValueType**</span></span>](eventmanifestschema-patternmapvaluetype-complextype.md) | <span data-ttu-id="873d1-116">Определяет регулярные выражения, используемые для поиска соответствующей строки в строке сообщения и ее изменения.</span><span class="sxs-lookup"><span data-stu-id="873d1-116">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="873d1-117">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="873d1-117">Attributes</span></span>



| <span data-ttu-id="873d1-118">Имя</span><span class="sxs-lookup"><span data-stu-id="873d1-118">Name</span></span>   | <span data-ttu-id="873d1-119">Тип</span><span class="sxs-lookup"><span data-stu-id="873d1-119">Type</span></span>                                                              | <span data-ttu-id="873d1-120">Описание</span><span class="sxs-lookup"><span data-stu-id="873d1-120">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="873d1-121">format</span><span class="sxs-lookup"><span data-stu-id="873d1-121">format</span></span> | <span data-ttu-id="873d1-122">anyURI</span><span class="sxs-lookup"><span data-stu-id="873d1-122">anyURI</span></span>                                                            | <span data-ttu-id="873d1-123">Используемый обработчик регулярных выражений.</span><span class="sxs-lookup"><span data-stu-id="873d1-123">The regular expression engine to use.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="873d1-124">name</span><span class="sxs-lookup"><span data-stu-id="873d1-124">name</span></span>   | <span data-ttu-id="873d1-125">**QName**</span><span class="sxs-lookup"><span data-stu-id="873d1-125">**QName**</span></span>                                                         | <span data-ttu-id="873d1-126">Имя схемы шаблона.</span><span class="sxs-lookup"><span data-stu-id="873d1-126">The name of the pattern map.</span></span> <span data-ttu-id="873d1-127">Используйте имя в элементе Data для ссылки на сопоставления.</span><span class="sxs-lookup"><span data-stu-id="873d1-127">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="873d1-128">символ</span><span class="sxs-lookup"><span data-stu-id="873d1-128">symbol</span></span> | [<span data-ttu-id="873d1-129">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="873d1-129">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="873d1-130">Символ, используемый для ссылки на сопоставления в приложении.</span><span class="sxs-lookup"><span data-stu-id="873d1-130">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="873d1-131">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ для создания константы для Map в файле заголовка, создаваемого компилятором.</span><span class="sxs-lookup"><span data-stu-id="873d1-131">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="873d1-132">Если не указать символ, компилятор создаст его.</span><span class="sxs-lookup"><span data-stu-id="873d1-132">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="873d1-133">Требования</span><span class="sxs-lookup"><span data-stu-id="873d1-133">Requirements</span></span>



| <span data-ttu-id="873d1-134">Требование</span><span class="sxs-lookup"><span data-stu-id="873d1-134">Requirement</span></span> | <span data-ttu-id="873d1-135">Значение</span><span class="sxs-lookup"><span data-stu-id="873d1-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="873d1-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="873d1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="873d1-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="873d1-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="873d1-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="873d1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="873d1-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="873d1-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





