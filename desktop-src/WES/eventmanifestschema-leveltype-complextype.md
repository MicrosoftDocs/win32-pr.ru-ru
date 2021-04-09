---
title: Сложный тип Левелтипе
description: Определяет значение серьезности, определяющее уровень детализации регистрируемых событий.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- Журнал событий сложных типов Левелтипе
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237b38890283769e9aac20c9b3a3703ff4b72d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135167"
---
# <a name="leveltype-complex-type"></a><span data-ttu-id="18d3a-104">Сложный тип Левелтипе</span><span class="sxs-lookup"><span data-stu-id="18d3a-104">LevelType Complex Type</span></span>

<span data-ttu-id="18d3a-105">Определяет значение серьезности, определяющее уровень детализации регистрируемых событий.</span><span class="sxs-lookup"><span data-stu-id="18d3a-105">Defines a severity value that determines the verbosity of the events being logged.</span></span>

``` syntax
<xs:complexType name="LevelType"
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
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="18d3a-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="18d3a-106">Attributes</span></span>



| <span data-ttu-id="18d3a-107">Имя</span><span class="sxs-lookup"><span data-stu-id="18d3a-107">Name</span></span>    | <span data-ttu-id="18d3a-108">Тип</span><span class="sxs-lookup"><span data-stu-id="18d3a-108">Type</span></span>                                                              | <span data-ttu-id="18d3a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="18d3a-109">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d3a-110">message</span><span class="sxs-lookup"><span data-stu-id="18d3a-110">message</span></span> | [<span data-ttu-id="18d3a-111">**стртаблереф**</span><span class="sxs-lookup"><span data-stu-id="18d3a-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="18d3a-112">Локализованное отображаемое имя для уровня.</span><span class="sxs-lookup"><span data-stu-id="18d3a-112">The localized display name for the level.</span></span> <span data-ttu-id="18d3a-113">Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста.</span><span class="sxs-lookup"><span data-stu-id="18d3a-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                    |
| <span data-ttu-id="18d3a-114">name</span><span class="sxs-lookup"><span data-stu-id="18d3a-114">name</span></span>    | <span data-ttu-id="18d3a-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="18d3a-115">**QName**</span></span>                                                         | <span data-ttu-id="18d3a-116">Имя, присваиваемое этому уровню.</span><span class="sxs-lookup"><span data-stu-id="18d3a-116">The name to assign to this level.</span></span> <span data-ttu-id="18d3a-117">Это имя должно быть уникальным в пределах области действия поставщика.</span><span class="sxs-lookup"><span data-stu-id="18d3a-117">This name must be unique within the scope of the provider.</span></span><br/>                                                                                                                                                                                                            |
| <span data-ttu-id="18d3a-118">символ</span><span class="sxs-lookup"><span data-stu-id="18d3a-118">symbol</span></span>  | [<span data-ttu-id="18d3a-119">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="18d3a-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="18d3a-120">Символ, используемый для ссылки на уровень в приложении.</span><span class="sxs-lookup"><span data-stu-id="18d3a-120">The symbol to use to reference the level in your application.</span></span> <span data-ttu-id="18d3a-121">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ для создания константы для уровня в файле заголовка, создаваемого компилятором.</span><span class="sxs-lookup"><span data-stu-id="18d3a-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the level in the header file that the compiler generates.</span></span> <span data-ttu-id="18d3a-122">Если не указать символ, компилятор создаст его.</span><span class="sxs-lookup"><span data-stu-id="18d3a-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="18d3a-123">значение</span><span class="sxs-lookup"><span data-stu-id="18d3a-123">value</span></span>   | [<span data-ttu-id="18d3a-124">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="18d3a-124">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="18d3a-125">Значение уровня.</span><span class="sxs-lookup"><span data-stu-id="18d3a-125">The level value.</span></span> <span data-ttu-id="18d3a-126">Можно указать значения в диапазоне от 16 до 255.</span><span class="sxs-lookup"><span data-stu-id="18d3a-126">You can specify values in the range 16 to 255.</span></span> <span data-ttu-id="18d3a-127">Стандартные значения уровней см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="18d3a-127">For predefined level values, see Remarks.</span></span><br/>                                                                                                                                                                                               |



## <a name="remarks"></a><span data-ttu-id="18d3a-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18d3a-128">Remarks</span></span>

<span data-ttu-id="18d3a-129">Ниже приведены стандартные значения уровня, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="18d3a-129">The following are the predefined level values that you can use.</span></span> <span data-ttu-id="18d3a-130">Эти значения определяются в Winmeta.xml файле, включенном в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="18d3a-130">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="18d3a-131">Имя</span><span class="sxs-lookup"><span data-stu-id="18d3a-131">Name</span></span>              | <span data-ttu-id="18d3a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="18d3a-132">Value</span></span> | <span data-ttu-id="18d3a-133">Символ</span><span class="sxs-lookup"><span data-stu-id="18d3a-133">Symbol</span></span>                    | <span data-ttu-id="18d3a-134">Описание</span><span class="sxs-lookup"><span data-stu-id="18d3a-134">Description</span></span>                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="18d3a-135">win:Critical</span><span class="sxs-lookup"><span data-stu-id="18d3a-135">win:Critical</span></span>      | <span data-ttu-id="18d3a-136">1</span><span class="sxs-lookup"><span data-stu-id="18d3a-136">1</span></span>     | <span data-ttu-id="18d3a-137">\_ \_ критический уровень WINEVENT</span><span class="sxs-lookup"><span data-stu-id="18d3a-137">WINEVENT\_LEVEL\_CRITICAL</span></span> | <span data-ttu-id="18d3a-138">Определяет аварийное завершение или событие завершения.</span><span class="sxs-lookup"><span data-stu-id="18d3a-138">Identifies an abnormal exit or termination event.</span></span><br/>            |
| <span data-ttu-id="18d3a-139">win:Error</span><span class="sxs-lookup"><span data-stu-id="18d3a-139">win:Error</span></span>         | <span data-ttu-id="18d3a-140">2</span><span class="sxs-lookup"><span data-stu-id="18d3a-140">2</span></span>     | <span data-ttu-id="18d3a-141">\_ошибка уровня \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="18d3a-141">WINEVENT\_LEVEL\_ERROR</span></span>    | <span data-ttu-id="18d3a-142">Определяет событие серьезной ошибки.</span><span class="sxs-lookup"><span data-stu-id="18d3a-142">Identifies a severe error event.</span></span><br/>                             |
| <span data-ttu-id="18d3a-143">win:Warning</span><span class="sxs-lookup"><span data-stu-id="18d3a-143">win:Warning</span></span>       | <span data-ttu-id="18d3a-144">3</span><span class="sxs-lookup"><span data-stu-id="18d3a-144">3</span></span>     | <span data-ttu-id="18d3a-145">\_предупреждение уровня \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="18d3a-145">WINEVENT\_LEVEL\_WARNING</span></span>  | <span data-ttu-id="18d3a-146">Определяет событие предупреждения, например сбой выделения.</span><span class="sxs-lookup"><span data-stu-id="18d3a-146">Identifies a warning event such as an allocation failure.</span></span><br/>    |
| <span data-ttu-id="18d3a-147">win:Informational</span><span class="sxs-lookup"><span data-stu-id="18d3a-147">win:Informational</span></span> | <span data-ttu-id="18d3a-148">4</span><span class="sxs-lookup"><span data-stu-id="18d3a-148">4</span></span>     | <span data-ttu-id="18d3a-149">\_ \_ сведения об уровне WINEVENT</span><span class="sxs-lookup"><span data-stu-id="18d3a-149">WINEVENT\_LEVEL\_INFO</span></span>     | <span data-ttu-id="18d3a-150">Определяет событие, не относящееся к ошибке, например событие входа или выхода.</span><span class="sxs-lookup"><span data-stu-id="18d3a-150">Identifies a non-error event such as an entry or exit event.</span></span><br/> |
| <span data-ttu-id="18d3a-151">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="18d3a-151">win:Verbose</span></span>       | <span data-ttu-id="18d3a-152">5</span><span class="sxs-lookup"><span data-stu-id="18d3a-152">5</span></span>     | <span data-ttu-id="18d3a-153">подробные сведения о \_ уровне WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="18d3a-153">WINEVENT\_LEVEL\_VERBOSE</span></span>  | <span data-ttu-id="18d3a-154">Определяет подробное событие трассировки.</span><span class="sxs-lookup"><span data-stu-id="18d3a-154">Identifies a detailed trace event.</span></span><br/>                           |



 

<span data-ttu-id="18d3a-155">Более высокие значения предполагают, что вы получаете и более низкие уровни.</span><span class="sxs-lookup"><span data-stu-id="18d3a-155">Higher numbers imply that you get lower levels as well.</span></span> <span data-ttu-id="18d3a-156">Например, при указании Win: Warning вы получаете все предупреждения, ошибки и критические события.</span><span class="sxs-lookup"><span data-stu-id="18d3a-156">For example, if you specify win:Warning, you receive all warning, error, and critical events.</span></span>

## <a name="requirements"></a><span data-ttu-id="18d3a-157">Требования</span><span class="sxs-lookup"><span data-stu-id="18d3a-157">Requirements</span></span>



| <span data-ttu-id="18d3a-158">Требование</span><span class="sxs-lookup"><span data-stu-id="18d3a-158">Requirement</span></span> | <span data-ttu-id="18d3a-159">Значение</span><span class="sxs-lookup"><span data-stu-id="18d3a-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="18d3a-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18d3a-160">Minimum supported client</span></span><br/> | <span data-ttu-id="18d3a-161">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18d3a-161">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="18d3a-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18d3a-162">Minimum supported server</span></span><br/> | <span data-ttu-id="18d3a-163">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18d3a-163">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





