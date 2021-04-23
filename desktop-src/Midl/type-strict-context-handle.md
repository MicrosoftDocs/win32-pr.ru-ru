---
title: атрибут type_strict_context_handle
description: '\_ \_ \_ Чтобы задать ограничения для дескрипторов контекста, используйте \ Type строгое дескриптор контекста \ в файле ACF.'
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle атрибута MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487557"
---
# <a name="type_strict_context_handle-attribute"></a><span data-ttu-id="999cc-104">\_ \_ атрибут строгого \_ обработчика контекста</span><span class="sxs-lookup"><span data-stu-id="999cc-104">type\_strict\_context\_handle attribute</span></span>

<span data-ttu-id="999cc-105">Используйте **\[ \_ строгое \_ \_ дескриптор \] контекста** в файле ACF для установки ограничений на дескрипторы контекста.</span><span class="sxs-lookup"><span data-stu-id="999cc-105">Use the **\[type\_strict\_context\_handle\]** in an ACF file to set restrictions on context handles.</span></span>

``` syntax
[ 
    type_strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="999cc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="999cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="999cc-107">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="999cc-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="999cc-108">Другие атрибуты ACF, применяемые к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="999cc-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="999cc-109">К допустимым атрибутам относятся [**Auto \_ Handle**](auto-handle.md), [**неявный \_ обработчик**](implicit-handle.md), [**явный \_ обработчик**](explicit-handle.md)и [**Оптимизация**](optimize.md), [**код**](code.md)или [**код**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="999cc-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="999cc-110">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="999cc-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="999cc-111">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="999cc-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="999cc-112">Имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="999cc-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="999cc-113">*Interface-операторы определения*</span><span class="sxs-lookup"><span data-stu-id="999cc-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="999cc-114">Одна или несколько инструкций MIDL, определяющих элементы [**интерфейса**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="999cc-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="999cc-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="999cc-115">Remarks</span></span>

<span data-ttu-id="999cc-116">Чтобы использовать этот атрибут, при запуске midl.exe для флага-target необходимо задать значение NT60 (или более высокий).</span><span class="sxs-lookup"><span data-stu-id="999cc-116">In order to use this attribute, the -target flag must be set to NT60 (or higher) when running midl.exe.</span></span>

<span data-ttu-id="999cc-117">\[Тип \_ строгого \_ \_ маркера контекста \] является функциональным надмножеством \[ строгого \_ \_ маркера контекста \] .</span><span class="sxs-lookup"><span data-stu-id="999cc-117">\[type\_strict\_context\_handle\] is a functional superset of \[strict\_context\_handle\].</span></span> <span data-ttu-id="999cc-118">В \[ строгом \_ \_ ОБРАБОТЧИКе контекста \] идентификатором типа для маркера всегда является 0; \[ в \_ строгом \_ \_ маркере контекста тип \] уникальный идентификатор типа назначается компилятором MIDL.</span><span class="sxs-lookup"><span data-stu-id="999cc-118">In \[strict\_context\_handle\], the type ID of the handle is always 0; in \[type\_strict\_context\_handle\], a unique type ID is assigned by the MIDL compiler.</span></span>

<span data-ttu-id="999cc-119">Рекомендуется использовать \[ \_ описатель контекста строгого типа \_ , \_ \] а не \[ строго \_ Контекстный \_ маркер \] .</span><span class="sxs-lookup"><span data-stu-id="999cc-119">It is recommended to use \[type\_strict\_context\_handle\] rather than \[strict\_context\_handle\].</span></span> <span data-ttu-id="999cc-120">Дескрипторы контекста по умолчанию не связаны с конкретным типом.</span><span class="sxs-lookup"><span data-stu-id="999cc-120">Context handles are not associated with a specific type by default.</span></span> <span data-ttu-id="999cc-121">Если в одном процессе используется несколько типов дескрипторов контекста, вредоносный клиент может передать дескриптор контекста вместо другого для получения нежелательных результатов.</span><span class="sxs-lookup"><span data-stu-id="999cc-121">When multiple types of context handles are used in the same process, it is possible for a malicious client to pass a context handle in place of another to produce undesirable results.</span></span> <span data-ttu-id="999cc-122">Использование \[ \_ строгого \_ \_ маркера контекста \] позволяет приложениям применять согласованность типов контекстного контекста и предотвращать несовпадение использования типа обрабатываемого контекста.</span><span class="sxs-lookup"><span data-stu-id="999cc-122">The use of \[type\_strict\_context\_handle\] allows applications to enforce context handle type consistency and prevent any mismatched context handle type usage.</span></span>

<span data-ttu-id="999cc-123">Описатель контекста с атрибутом строгого \[ \_ \_ контекста \_ \] не может также иметь атрибут с \[ строгой \_ контекстной \_ обработкой \] .</span><span class="sxs-lookup"><span data-stu-id="999cc-123">A context handle attributed with \[type\_strict\_context\_handle\] cannot also be attributed with \[strict\_context\_handle\].</span></span>

## <a name="see-also"></a><span data-ttu-id="999cc-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="999cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="999cc-125">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="999cc-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="999cc-126">**приведен**</span><span class="sxs-lookup"><span data-stu-id="999cc-126">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="999cc-127">Дескрипторы контекста</span><span class="sxs-lookup"><span data-stu-id="999cc-127">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="999cc-128">**\_сериализация обработчика контекста \_**</span><span class="sxs-lookup"><span data-stu-id="999cc-128">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="999cc-129">**несериализуемый контекстный \_ обработчик \_**</span><span class="sxs-lookup"><span data-stu-id="999cc-129">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="999cc-130">**явный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="999cc-130">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="999cc-131">**неявный \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="999cc-131">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="999cc-132">**nocode**</span><span class="sxs-lookup"><span data-stu-id="999cc-132">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="999cc-133">**увеличить**</span><span class="sxs-lookup"><span data-stu-id="999cc-133">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="999cc-134">Нечеткий \_ Контекстный \_ маркер</span><span class="sxs-lookup"><span data-stu-id="999cc-134">strict\_context\_handle</span></span>](strict-context-handle.md)
</dt> </dl>

 

 