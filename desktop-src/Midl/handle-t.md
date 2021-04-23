---
title: атрибут handle_t
description: '\_Ключевое слово Handle t объявляет объект для типа маркера-примитива с типом \_ t. Простой маркер привязки — это объект данных, который может использоваться приложением для представления привязки.'
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t атрибута MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337057"
---
# <a name="handle_t-attribute"></a><span data-ttu-id="77865-105">Handle \_ t, атрибут</span><span class="sxs-lookup"><span data-stu-id="77865-105">handle\_t attribute</span></span>

<span data-ttu-id="77865-106">Ключевое слово **Handle \_ t** объявляет объект для типа маркера-примитива с **типом \_ t**.</span><span class="sxs-lookup"><span data-stu-id="77865-106">The **handle\_t** keyword declares an object to be of the primitive handle type **handle\_t**.</span></span> <span data-ttu-id="77865-107">Простой маркер привязки — это объект данных, который может использоваться приложением для представления привязки.</span><span class="sxs-lookup"><span data-stu-id="77865-107">A primitive binding handle is a data object that can be used by the application to represent the binding.</span></span>

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a><span data-ttu-id="77865-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="77865-108">Parameters</span></span>

<span data-ttu-id="77865-109">Этот атрибут не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="77865-109">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="77865-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77865-110">Remarks</span></span>

<span data-ttu-id="77865-111">Тип **« \_ Handle** » является одним из предопределенных типов языка определения интерфейса (IDL).</span><span class="sxs-lookup"><span data-stu-id="77865-111">The **handle\_t** type is one of the predefined types of the interface definition language (IDL).</span></span> <span data-ttu-id="77865-112">Он может использоваться в качестве спецификатора типа в объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в качестве спецификатора возвращаемого типа функции и описателя типа параметра).</span><span class="sxs-lookup"><span data-stu-id="77865-112">It can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="77865-113">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="77865-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="77865-114">В Microsoft RPC параметры типа **Handle \_ t** могут происходить только в качестве параметров **\[** [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="77865-114">In Microsoft RPC, parameters of type **handle\_t** can occur only as **\[**[**in**](in.md)**\]** parameters.</span></span> <span data-ttu-id="77865-115">У примитивных дескрипторов не может быть **\[** атрибута [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="77865-115">Primitive handles cannot have the **\[**[**unique**](unique.md)**\]** or **\[**[**ptr**](ptr.md)**\]** attribute.</span></span>

<span data-ttu-id="77865-116">Параметры типа **Handle \_ t** (Параметры обработчика примитива) не передаются в сети.</span><span class="sxs-lookup"><span data-stu-id="77865-116">Parameters of type **handle\_t** (primitive handle parameters) are not transmitted on the network.</span></span>

## <a name="see-also"></a><span data-ttu-id="77865-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77865-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77865-118">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="77865-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="77865-119">Привязка и дескрипторы</span><span class="sxs-lookup"><span data-stu-id="77865-119">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="77865-120">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="77865-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="77865-121">**окне**</span><span class="sxs-lookup"><span data-stu-id="77865-121">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="77865-122">**определение**</span><span class="sxs-lookup"><span data-stu-id="77865-122">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="77865-123">**ptr**</span><span class="sxs-lookup"><span data-stu-id="77865-123">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="77865-124">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="77865-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 