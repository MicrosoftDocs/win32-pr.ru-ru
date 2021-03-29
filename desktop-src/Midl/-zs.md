---
title: /ZS, параметр
description: Параметр/ZS указывает, что компилятор проверяет только синтаксис и не создает выходные файлы.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- MIDL/ZS Switch
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469802434d54319aa55c1e409ccb8d64e942836f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783699"
---
# <a name="zs-switch"></a><span data-ttu-id="a7b37-104">/ZS, параметр</span><span class="sxs-lookup"><span data-stu-id="a7b37-104">/Zs switch</span></span>

<span data-ttu-id="a7b37-105">Параметр **/ZS** указывает, что компилятор проверяет только синтаксис и не создает выходные файлы.</span><span class="sxs-lookup"><span data-stu-id="a7b37-105">The **/Zs** switch indicates that the compiler only checks syntax and does not generate output files.</span></span>

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a><span data-ttu-id="a7b37-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="a7b37-106">Switch Options</span></span>

<span data-ttu-id="a7b37-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a7b37-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7b37-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7b37-108">Remarks</span></span>

<span data-ttu-id="a7b37-109">Этот параметр переопределяет все другие параметры, которые задают сведения о выходных файлах.</span><span class="sxs-lookup"><span data-stu-id="a7b37-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="a7b37-110">Кроме того, можно указать режим проверки синтаксиса с параметром компилятора MIDL [**/синтакс \_ Check**](-syntax-check.md).</span><span class="sxs-lookup"><span data-stu-id="a7b37-110">You can also specify syntax-checking mode with the MIDL compiler switch [**/syntax\_check**](-syntax-check.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a7b37-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="a7b37-111">Examples</span></span>

<span data-ttu-id="a7b37-112">**MIDL/ZS filename. idl**</span><span class="sxs-lookup"><span data-stu-id="a7b37-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="a7b37-113">**MIDL/синтакс \_ проверить filename. idl**</span><span class="sxs-lookup"><span data-stu-id="a7b37-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="a7b37-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7b37-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b37-115">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="a7b37-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="a7b37-116">**\_Проверка/синтакс**</span><span class="sxs-lookup"><span data-stu-id="a7b37-116">**/syntax\_check**</span></span>](-syntax-check.md)
</dt> </dl>

 

 




