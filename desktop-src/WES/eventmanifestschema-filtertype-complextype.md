---
title: Сложный тип FilterType
description: Определяет фильтр данных, используемый сеансом для фильтрации событий на основе данных событий.
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- Журнал событий сложных типов FilterType
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493167"
---
# <a name="filtertype-complex-type"></a><span data-ttu-id="b1324-104">Сложный тип FilterType</span><span class="sxs-lookup"><span data-stu-id="b1324-104">FilterType Complex Type</span></span>

<span data-ttu-id="b1324-105">Определяет фильтр данных, используемый сеансом для фильтрации событий на основе данных событий.</span><span class="sxs-lookup"><span data-stu-id="b1324-105">Defines a data filter that a session uses to filter events based on event data.</span></span>

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="b1324-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b1324-106">Attributes</span></span>



| <span data-ttu-id="b1324-107">Имя</span><span class="sxs-lookup"><span data-stu-id="b1324-107">Name</span></span>    | <span data-ttu-id="b1324-108">Тип</span><span class="sxs-lookup"><span data-stu-id="b1324-108">Type</span></span>                                                              | <span data-ttu-id="b1324-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b1324-109">Description</span></span>                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1324-110">message</span><span class="sxs-lookup"><span data-stu-id="b1324-110">message</span></span> | [<span data-ttu-id="b1324-111">**стртаблереф**</span><span class="sxs-lookup"><span data-stu-id="b1324-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="b1324-112">Локализованное описание для фильтра.</span><span class="sxs-lookup"><span data-stu-id="b1324-112">The localized description for the filter.</span></span> <span data-ttu-id="b1324-113">Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста.</span><span class="sxs-lookup"><span data-stu-id="b1324-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                   |
| <span data-ttu-id="b1324-114">name</span><span class="sxs-lookup"><span data-stu-id="b1324-114">name</span></span>    | <span data-ttu-id="b1324-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="b1324-115">**QName**</span></span>                                                         | <span data-ttu-id="b1324-116">Имя, идентифицирующее фильтр.</span><span class="sxs-lookup"><span data-stu-id="b1324-116">A name that identifies the filter.</span></span><br/>                                                                                                                                                                                                    |
| <span data-ttu-id="b1324-117">символ</span><span class="sxs-lookup"><span data-stu-id="b1324-117">symbol</span></span>  | [<span data-ttu-id="b1324-118">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="b1324-118">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="b1324-119">Символ, используемый для ссылки на фильтр в приложении.</span><span class="sxs-lookup"><span data-stu-id="b1324-119">The symbol to use to reference the filter in your application.</span></span> <span data-ttu-id="b1324-120">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для фильтра в файле заголовка, создаваемом компилятором.</span><span class="sxs-lookup"><span data-stu-id="b1324-120">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the filter in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="b1324-121">tid</span><span class="sxs-lookup"><span data-stu-id="b1324-121">tid</span></span>     | <span data-ttu-id="b1324-122">token</span><span class="sxs-lookup"><span data-stu-id="b1324-122">token</span></span>                                                             | <span data-ttu-id="b1324-123">Идентификатор шаблона, описывающий данные фильтра, которые сеанс передает поставщику, когда он включает поставщик.</span><span class="sxs-lookup"><span data-stu-id="b1324-123">A template identifier that describes the filter data that the session passes to the provider when it enables the provider.</span></span><br/>                                                                                                            |
| <span data-ttu-id="b1324-124">значение</span><span class="sxs-lookup"><span data-stu-id="b1324-124">value</span></span>   | [<span data-ttu-id="b1324-125">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="b1324-125">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="b1324-126">Целочисленное значение, уникально идентифицирующее фильтр в списке фильтров, которые вы определяете.</span><span class="sxs-lookup"><span data-stu-id="b1324-126">An integer value that uniquely identifies the filter within the list of filters that you define.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="b1324-127">version</span><span class="sxs-lookup"><span data-stu-id="b1324-127">version</span></span> | [<span data-ttu-id="b1324-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="b1324-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="b1324-129">Целочисленное значение, определяющее эту версию фильтра.</span><span class="sxs-lookup"><span data-stu-id="b1324-129">An integer value that identifies this version of the filter.</span></span> <span data-ttu-id="b1324-130">Если не указано, значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b1324-130">If not specified, the value is zero.</span></span><br/>                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="b1324-131">Требования</span><span class="sxs-lookup"><span data-stu-id="b1324-131">Requirements</span></span>



| <span data-ttu-id="b1324-132">Требование</span><span class="sxs-lookup"><span data-stu-id="b1324-132">Requirement</span></span> | <span data-ttu-id="b1324-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b1324-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b1324-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1324-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b1324-135">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b1324-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b1324-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1324-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b1324-137">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1324-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





