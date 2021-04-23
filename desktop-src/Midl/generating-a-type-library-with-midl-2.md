---
title: Создание библиотеки типов с помощью MIDL
description: Элемент верхнего уровня в синтаксисе ODL является оператором Library (блоком библиотеки).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Язык MIDL MIDL, задачи, создание библиотеки типов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85f6e8f7ea6f65bc503c08872c9199ff3d5fd828
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650352"
---
# <a name="generating-a-type-library-with-midl"></a><span data-ttu-id="7c5e3-104">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="7c5e3-104">Generating a Type Library with MIDL</span></span>

<span data-ttu-id="7c5e3-105">Элемент верхнего уровня в синтаксисе ODL является оператором Library (блоком библиотеки).</span><span class="sxs-lookup"><span data-stu-id="7c5e3-105">The top-level element of the ODL syntax is the library statement (library block).</span></span> <span data-ttu-id="7c5e3-106">Каждая другая инструкция ODL, за исключением атрибутов, примененных к оператору Library, должна быть определена в блоке библиотеки.</span><span class="sxs-lookup"><span data-stu-id="7c5e3-106">Every other ODL statement, with the exception of the attributes that are applied to the library statement, must be defined within the library block.</span></span> <span data-ttu-id="7c5e3-107">Когда компилятор MIDL видит блок библиотеки, он создает библиотеку типов во многом так же, как это делает MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="7c5e3-107">When the MIDL compiler sees a library block, it generates a type library in much the same way that MkTypLib does.</span></span> <span data-ttu-id="7c5e3-108">За некоторыми исключениями, описанными в разделе [различия между MIDL и MKTYPLIB](differences-between-midl-and-mktyplib.md), инструкции в блоке библиотеки должны следовать тому же синтаксису, что и в ODL-языке и MKTYPLIB.</span><span class="sxs-lookup"><span data-stu-id="7c5e3-108">With a few exceptions, described in [Differences Between MIDL and MKTYPLIB](differences-between-midl-and-mktyplib.md), the statements within the library block should follow the same syntax as in the ODL language and MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="7c5e3-109">Средство Mktyplib.exe устарело.</span><span class="sxs-lookup"><span data-stu-id="7c5e3-109">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="7c5e3-110">Вместо этого используйте компилятор MIDL.</span><span class="sxs-lookup"><span data-stu-id="7c5e3-110">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="7c5e3-111">Атрибуты ODL можно применять к элементам, которые определены либо внутри, либо вне блока библиотеки.</span><span class="sxs-lookup"><span data-stu-id="7c5e3-111">You can apply ODL attributes to elements that are defined either inside or outside the library block.</span></span> <span data-ttu-id="7c5e3-112">Эти атрибуты не действуют за пределами блока библиотеки, если только элемент, к которому они применяются, ссылается из блока библиотеки.</span><span class="sxs-lookup"><span data-stu-id="7c5e3-112">These attributes have no effect outside the library block unless the element they are applied to is referenced from within the library block.</span></span> <span data-ttu-id="7c5e3-113">Инструкции внутри блока библиотеки могут ссылаться на внешний элемент либо с помощью его базового типа, наследования от него, либо путем ссылки на него в строке, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7c5e3-113">Statements inside the library block can reference an outside element either by using it as a base type, inheriting from it, or by referencing it on a line as shown:</span></span>

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

<span data-ttu-id="7c5e3-114">Если в блоке библиотеки имеется ссылка на элемент, определенный вне блока библиотеки, его определение будет размещено в созданной библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="7c5e3-114">If an element defined outside the library block is referenced within the library block, then its definition will be put into the generated type library.</span></span> <span data-ttu-id="7c5e3-115">Компилятор MIDL рассматривает операторы за пределами блока библиотеки как обычный IDL-файл и анализирует эти инструкции по мере того, как она выполняется всегда.</span><span class="sxs-lookup"><span data-stu-id="7c5e3-115">The MIDL compiler treats the statements outside of a library block as a typical IDL file and parses those statements as it has always done.</span></span> <span data-ttu-id="7c5e3-116">Как правило, это означает создание заглушек языка C для приложения RPC.</span><span class="sxs-lookup"><span data-stu-id="7c5e3-116">Normally, this means generating C-language stubs for an RPC application.</span></span>

<span data-ttu-id="7c5e3-117">Дополнительные сведения о синтаксисе файлов ODL см. в разделе [синтаксис ODL File](/previous-versions/windows/desktop/automat/odl-file-syntax).</span><span class="sxs-lookup"><span data-stu-id="7c5e3-117">For more information about the general syntax for an ODL file see [ODL File Syntax](/previous-versions/windows/desktop/automat/odl-file-syntax).</span></span>

 

 