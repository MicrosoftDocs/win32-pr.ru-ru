---
title: атрибут strict_context_handle
description: Атрибут \ " \_ \_ дескриптор контекста \ ACF \" задает ограничения для дескрипторов контекста.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle атрибута MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e66fd0754ec82de2354983e10e23ffc6329569
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987384"
---
# <a name="strict_context_handle-attribute"></a><span data-ttu-id="28a67-104">атрибут с определенным \_ \_ маркером контекста</span><span class="sxs-lookup"><span data-stu-id="28a67-104">strict\_context\_handle attribute</span></span>

<span data-ttu-id="28a67-105">Атрибут ACF **\[ \_ \_ дескриптора \] ограниченного контекста** задает ограничения для дескрипторов контекста.</span><span class="sxs-lookup"><span data-stu-id="28a67-105">The **\[strict\_context\_handle\]** ACF attribute sets restrictions on context handles.</span></span>

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="28a67-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28a67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28a67-107">*Interface-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="28a67-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="28a67-108">Другие атрибуты ACF, применяемые к интерфейсу в целом.</span><span class="sxs-lookup"><span data-stu-id="28a67-108">Other ACF attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="28a67-109">К допустимым атрибутам относятся [**Auto \_ Handle**](auto-handle.md), [**неявный \_ обработчик**](implicit-handle.md), [**явный \_ обработчик**](explicit-handle.md)и [**Оптимизация**](optimize.md), [**код**](code.md)или [**код**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="28a67-109">Valid attributes include [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), [**explicit\_handle**](explicit-handle.md), and [**optimize**](optimize.md), [**code**](code.md), or [**nocode**](nocode.md).</span></span> <span data-ttu-id="28a67-110">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="28a67-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="28a67-111">*имя интерфейса*</span><span class="sxs-lookup"><span data-stu-id="28a67-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="28a67-112">Имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="28a67-112">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="28a67-113">*Interface-операторы определения*</span><span class="sxs-lookup"><span data-stu-id="28a67-113">*interface-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="28a67-114">Одна или несколько инструкций MIDL, определяющих элементы [**интерфейса**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="28a67-114">One or more MIDL statements that define the elements of the [**interface**](interface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28a67-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28a67-115">Remarks</span></span>

<span data-ttu-id="28a67-116">Как правило, когда вызов метода интерфейса создает маркер контекста, этот обработчик освобождается бесплатно для любого другого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="28a67-116">Normally, when a call to an interface method generates a context handle, that handle becomes freely available to any other interface.</span></span> <span data-ttu-id="28a67-117">При использовании атрибута исключительного **\[ \_ \_ дескриптора \] контекста** гарантируется, что методы в этом интерфейсе будут принимать только дескрипторы контекста, созданные методом из того же интерфейса.</span><span class="sxs-lookup"><span data-stu-id="28a67-117">When you use the **\[strict\_context\_handle\]** attribute you guarantee that the methods in that interface will only accept context handles that were created by a method from the same interface.</span></span> <span data-ttu-id="28a67-118">Интерфейсы, скомпилированные без использования **\[ \_ \_ дескриптора \]** с определенными контекстами, не могут принимать дескрипторы контекста, созданные для интерфейсов, **\[ \_ \_ \] скомпилированных с помощью**</span><span class="sxs-lookup"><span data-stu-id="28a67-118">Interfaces compiled without **\[strict\_context\_handle\]** cannot accept context handles created on interfaces compiled with **\[strict\_context\_handle\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="28a67-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28a67-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a67-120">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="28a67-120">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="28a67-121">**приведен**</span><span class="sxs-lookup"><span data-stu-id="28a67-121">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="28a67-122">Дескрипторы контекста</span><span class="sxs-lookup"><span data-stu-id="28a67-122">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="28a67-123">**\_сериализация обработчика контекста \_**</span><span class="sxs-lookup"><span data-stu-id="28a67-123">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="28a67-124">**несериализуемый контекстный \_ обработчик \_**</span><span class="sxs-lookup"><span data-stu-id="28a67-124">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="28a67-125">**явный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="28a67-125">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="28a67-126">**неявный \_ обработчик**</span><span class="sxs-lookup"><span data-stu-id="28a67-126">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="28a67-127">**nocode**</span><span class="sxs-lookup"><span data-stu-id="28a67-127">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="28a67-128">**увеличить**</span><span class="sxs-lookup"><span data-stu-id="28a67-128">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="28a67-129">Тип \_ строгого \_ \_ маркера контекста</span><span class="sxs-lookup"><span data-stu-id="28a67-129">type\_strict\_context\_handle</span></span>](type-strict-context-handle.md)
</dt> </dl>

 

 