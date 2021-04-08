---
title: iid_is - атрибут
description: Атрибут \ IID = \_ \ указывает идентификатор IID COM-интерфейса, на который указывает указатель интерфейса.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is атрибута MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068832"
---
# <a name="iid_is-attribute"></a><span data-ttu-id="8e59c-104">IID \_ является атрибутом</span><span class="sxs-lookup"><span data-stu-id="8e59c-104">iid\_is attribute</span></span>

<span data-ttu-id="8e59c-105">**\[ IID \_ — это \]** атрибут указателя, указывающий идентификатор IID COM-интерфейса, на который указывает указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8e59c-105">The **\[iid\_is\]** pointer attribute specifies the IID of the COM interface pointed to by an interface pointer.</span></span>

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a><span data-ttu-id="8e59c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e59c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e59c-107">*ограниченное выражение*</span><span class="sxs-lookup"><span data-stu-id="8e59c-107">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="8e59c-108">Указывает выражение языка C.</span><span class="sxs-lookup"><span data-stu-id="8e59c-108">Specifies a C-language expression.</span></span> <span data-ttu-id="8e59c-109">Компилятор MIDL поддерживает условные выражения, логические выражения, реляционные выражения и арифметические выражения.</span><span class="sxs-lookup"><span data-stu-id="8e59c-109">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="8e59c-110">MIDL не разрешает вызовы функций в выражениях и не поддерживает операторы инкремента и декремента.</span><span class="sxs-lookup"><span data-stu-id="8e59c-110">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e59c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e59c-111">Remarks</span></span>

<span data-ttu-id="8e59c-112">**\[ \_ IID \]** можно использовать в списках атрибутов для параметров функции, а также для элементов структуры или объединения.</span><span class="sxs-lookup"><span data-stu-id="8e59c-112">You can use **\[iid\_is\]** in attribute lists for function parameters and for structure or union members.</span></span> <span data-ttu-id="8e59c-113">Заглушки используют IID для определения способа маршалирования указателя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8e59c-113">The stubs use the IID to determine how to marshal the interface pointer.</span></span> <span data-ttu-id="8e59c-114">Это полезно для указателя интерфейса, который типизирован как параметр базового класса.</span><span class="sxs-lookup"><span data-stu-id="8e59c-114">This is useful for an interface pointer that is typed as a base class parameter.</span></span>

<span data-ttu-id="8e59c-115">Файлы, использующие **\[ IID \_ \]** , должны быть скомпилированы с помощью компилятора MIDL в режиме по умолчанию, который не использует параметр [**/ОСФ**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="8e59c-115">Files that use the **\[iid\_is\]** attribute must be compiled with the MIDL compiler in default mode, that is not using the [**/osf**](-osf.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="8e59c-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="8e59c-116">Examples</span></span>

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a><span data-ttu-id="8e59c-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e59c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e59c-118">**объектами**</span><span class="sxs-lookup"><span data-stu-id="8e59c-118">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="8e59c-119">**UUID**</span><span class="sxs-lookup"><span data-stu-id="8e59c-119">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




