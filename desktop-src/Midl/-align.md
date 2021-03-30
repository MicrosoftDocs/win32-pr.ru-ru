---
title: параметр/align
description: Ключ/align функционально аналогичен параметру MIDL/ZP и распознается компилятором MIDL исключительно для обеспечения обратной совместимости с MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- параметр/align MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532720"
---
# <a name="align-switch"></a><span data-ttu-id="7ae2e-104">параметр/align</span><span class="sxs-lookup"><span data-stu-id="7ae2e-104">/align switch</span></span>

<span data-ttu-id="7ae2e-105">Ключ **/align** функционально аналогичен параметру MIDL [**/Zp**](-zp.md) и распознается компилятором MIDL исключительно для обеспечения обратной совместимости с MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="7ae2e-105">The **/align** switch is functionally the same as the MIDL [**/Zp**](-zp.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="7ae2e-106">Средство Mktyplib.exe устарело.</span><span class="sxs-lookup"><span data-stu-id="7ae2e-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="7ae2e-107">Вместо этого используйте компилятор MIDL.</span><span class="sxs-lookup"><span data-stu-id="7ae2e-107">Use the MIDL compiler instead.</span></span>

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a><span data-ttu-id="7ae2e-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="7ae2e-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="7ae2e-109">*Выравнивание*</span><span class="sxs-lookup"><span data-stu-id="7ae2e-109">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="7ae2e-110">Задает выравнивание для типов в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7ae2e-110">Specifies the alignment for types in the library.</span></span> <span data-ttu-id="7ae2e-111">Значение *выравнивания* может быть равно 1, 2, 4 или 8.</span><span class="sxs-lookup"><span data-stu-id="7ae2e-111">The *alignment* value can be 1, 2, 4, or 8.</span></span> <span data-ttu-id="7ae2e-112">Значение 1 указывает на естественное выравнивание; *n* обозначает выравнивание по байту *n*.</span><span class="sxs-lookup"><span data-stu-id="7ae2e-112">The value 1 indicates natural alignment; *n* indicates alignment on byte *n*.</span></span> <span data-ttu-id="7ae2e-113">Если параметр **/align** не задан, по умолчанию используется значение 8.</span><span class="sxs-lookup"><span data-stu-id="7ae2e-113">When you do not specify the **/align** switch, the default is 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ae2e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ae2e-114">Remarks</span></span>

<span data-ttu-id="7ae2e-115">При создании нового файла makefile используйте параметр [**/Zp**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="7ae2e-115">If you are generating a new makefile, use the [**/Zp**](-zp.md) switch.</span></span>

<span data-ttu-id="7ae2e-116">Значение выравнивания соответствует значению параметра [**/Zp**](-zp.md) , используемому компилятором Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="7ae2e-116">The alignment value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="7ae2e-117">Обязательно укажите одинаковое выравнивание при вызове компилятора C, как при вызове компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="7ae2e-117">Be sure that you specify the same alignment when you invoke the C compiler as when you invoke the MIDL compiler.</span></span>

<span data-ttu-id="7ae2e-118">Дополнительные сведения см. в документации по программированию для Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="7ae2e-118">For more information, see your Microsoft C/C++ programming documentation.</span></span> <span data-ttu-id="7ae2e-119">Обсуждение потенциальных опасностей при использовании нестандартных уровней упаковки см. в разделе справки [**/Zp**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="7ae2e-119">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="7ae2e-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="7ae2e-120">Examples</span></span>

<span data-ttu-id="7ae2e-121">**MIDL/align: 4 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="7ae2e-121">**midl /align:4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="7ae2e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ae2e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae2e-123">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="7ae2e-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="7ae2e-124">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="7ae2e-124">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




