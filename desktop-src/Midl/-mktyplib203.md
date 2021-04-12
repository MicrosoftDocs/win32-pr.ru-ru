---
title: /mktyplib203, параметр
description: Параметр/mktyplib203 заставляет компилятор MIDL проанализировать входной файл.
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- MIDL/mktyplib203 Switch
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8fd972355c2f6d37300c60f4bf74e76bf4396
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889787"
---
# <a name="mktyplib203-switch"></a><span data-ttu-id="608a1-104">/mktyplib203, параметр</span><span class="sxs-lookup"><span data-stu-id="608a1-104">/mktyplib203 switch</span></span>

<span data-ttu-id="608a1-105">Параметр **/mktyplib203** заставляет компилятор MIDL проанализировать входной файл.</span><span class="sxs-lookup"><span data-stu-id="608a1-105">The **/mktyplib203** switch forces the MIDL compiler to parse the input file.</span></span>

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a><span data-ttu-id="608a1-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="608a1-106">Switch Options</span></span>

<span data-ttu-id="608a1-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="608a1-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="608a1-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="608a1-108">Remarks</span></span>

<span data-ttu-id="608a1-109">Чтобы использовать параметр **/mktyplib203** , входной файл должен следовать синтаксису ODL точно, что означает, что нельзя размещать операторы за пределами блока Library.</span><span class="sxs-lookup"><span data-stu-id="608a1-109">In order to use the **/mktyplib203** switch, the input file must follow the ODL syntax exactly, which means you cannot place any statements outside of the library block.</span></span> <span data-ttu-id="608a1-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="608a1-110">Examples</span></span>

<span data-ttu-id="608a1-111">**MIDL/mktyplib203 мйолдодл. odl**</span><span class="sxs-lookup"><span data-stu-id="608a1-111">**midl /mktyplib203 myoldodl.odl**</span></span>

<span data-ttu-id="608a1-112">**MIDL/mktyplib203 олдхабит. idl**</span><span class="sxs-lookup"><span data-stu-id="608a1-112">**midl /mktyplib203 oldhabit.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="608a1-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="608a1-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="608a1-114">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="608a1-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="608a1-115">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="608a1-115">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




