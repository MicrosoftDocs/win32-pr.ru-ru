---
title: Сложный тип Кэйвордтипе
description: Определяет ключевое слово, определяющее категорию событий. | Сложный тип Кэйвордтипе
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- Журнал событий сложных типов Кэйвордтипе
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693996"
---
# <a name="keywordtype-complex-type"></a><span data-ttu-id="0b167-105">Сложный тип Кэйвордтипе</span><span class="sxs-lookup"><span data-stu-id="0b167-105">KeywordType Complex Type</span></span>

<span data-ttu-id="0b167-106">Определяет ключевое слово, определяющее категорию событий.</span><span class="sxs-lookup"><span data-stu-id="0b167-106">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="0b167-107">Ключевое слово — это тег, который присоединяется к событию для группирования событий в зависимости от их использования.</span><span class="sxs-lookup"><span data-stu-id="0b167-107">A keyword is a tag that you attach to an event to group events based on their usage.</span></span>

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="0b167-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0b167-108">Attributes</span></span>



| <span data-ttu-id="0b167-109">Имя</span><span class="sxs-lookup"><span data-stu-id="0b167-109">Name</span></span>    | <span data-ttu-id="0b167-110">Тип</span><span class="sxs-lookup"><span data-stu-id="0b167-110">Type</span></span>                                                              | <span data-ttu-id="0b167-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0b167-111">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b167-112">маска</span><span class="sxs-lookup"><span data-stu-id="0b167-112">mask</span></span>    | [<span data-ttu-id="0b167-113">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="0b167-113">**HexInt64Type**</span></span>](eventmanifestschema-hex64type-simpletype.md)  | <span data-ttu-id="0b167-114">Битовая маска, которая должна иметь только один бит.</span><span class="sxs-lookup"><span data-stu-id="0b167-114">A bitmask that must have only a single bit set.</span></span> <span data-ttu-id="0b167-115">Бит представляет категорию событий (например, чтение событий или запись событий).</span><span class="sxs-lookup"><span data-stu-id="0b167-115">The bit represents a category of events (for example, read events or write events).</span></span> <span data-ttu-id="0b167-116">Можно указать битовые значения в диапазоне от 0x0000000000000001 до 0x0000800000000000 (от 0 до 47).</span><span class="sxs-lookup"><span data-stu-id="0b167-116">You can specify bit values in the range from 0x0000000000000001 through 0x0000800000000000 (bits 0 through 47).</span></span><br/>                                                         |
| <span data-ttu-id="0b167-117">message</span><span class="sxs-lookup"><span data-stu-id="0b167-117">message</span></span> | [<span data-ttu-id="0b167-118">**стртаблереф**</span><span class="sxs-lookup"><span data-stu-id="0b167-118">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="0b167-119">Локализованное отображаемое имя для ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="0b167-119">The localized display name for the keyword.</span></span> <span data-ttu-id="0b167-120">Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста.</span><span class="sxs-lookup"><span data-stu-id="0b167-120">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                                                                                       |
| <span data-ttu-id="0b167-121">name</span><span class="sxs-lookup"><span data-stu-id="0b167-121">name</span></span>    | <span data-ttu-id="0b167-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="0b167-122">**QName**</span></span>                                                         | <span data-ttu-id="0b167-123">Имя ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="0b167-123">The name of the keyword.</span></span> <span data-ttu-id="0b167-124">Имя должно быть уникальным в списке ключевых слов, определяемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="0b167-124">The name must be unique within the list of keywords that the provider defines.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="0b167-125">символ</span><span class="sxs-lookup"><span data-stu-id="0b167-125">symbol</span></span>  | [<span data-ttu-id="0b167-126">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="0b167-126">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="0b167-127">Символ, используемый для ссылки на ключевое слово в приложении.</span><span class="sxs-lookup"><span data-stu-id="0b167-127">The symbol to use to reference the keyword in your application.</span></span> <span data-ttu-id="0b167-128">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для ключевого слова в файле заголовка, создаваемом компилятором.</span><span class="sxs-lookup"><span data-stu-id="0b167-128">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the keyword in the header file that the compiler generates.</span></span> <span data-ttu-id="0b167-129">Если не указать символ, компилятор создаст его.</span><span class="sxs-lookup"><span data-stu-id="0b167-129">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0b167-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b167-130">Remarks</span></span>

<span data-ttu-id="0b167-131">Файл Winmeta.xml, включенный в Windows SDK, содержит список ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="0b167-131">The Winmeta.xml file that is included in the Windows SDK contains a list of keywords.</span></span> <span data-ttu-id="0b167-132">Эти ключевые слова зарезервированы и не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="0b167-132">These keywords are reserved and should not be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b167-133">Требования</span><span class="sxs-lookup"><span data-stu-id="0b167-133">Requirements</span></span>



| <span data-ttu-id="0b167-134">Требование</span><span class="sxs-lookup"><span data-stu-id="0b167-134">Requirement</span></span> | <span data-ttu-id="0b167-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0b167-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0b167-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b167-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0b167-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b167-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0b167-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b167-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0b167-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b167-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





