---
title: syntax_check Switch
description: '\_Параметр проверки/синтакс указывает, что компилятор проверяет только синтаксис и не создает выходные файлы.'
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /syntax_check параметр MIDL
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b064a096b5064e6996ea4288c9ae9d4a798c2e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784014"
---
# <a name="syntax_check-switch"></a><span data-ttu-id="cb25e-104">\_параметр проверки/синтакс</span><span class="sxs-lookup"><span data-stu-id="cb25e-104">/syntax\_check switch</span></span>

<span data-ttu-id="cb25e-105">Параметр **\_ проверки/синтакс** указывает, что компилятор проверяет только синтаксис и не создает выходные файлы.</span><span class="sxs-lookup"><span data-stu-id="cb25e-105">The **/syntax\_check** switch indicates that the compiler checks only syntax and does not generate output files.</span></span>

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a><span data-ttu-id="cb25e-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="cb25e-106">Switch Options</span></span>

<span data-ttu-id="cb25e-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cb25e-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb25e-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb25e-108">Remarks</span></span>

<span data-ttu-id="cb25e-109">Этот параметр переопределяет все другие параметры, которые задают сведения о выходных файлах.</span><span class="sxs-lookup"><span data-stu-id="cb25e-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="cb25e-110">Также можно указать режим проверки синтаксиса с помощью параметра компилятора MIDL [**/ZS**](-zs.md).</span><span class="sxs-lookup"><span data-stu-id="cb25e-110">You can also specify syntax-checking mode with the MIDL compiler option [**/Zs**](-zs.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cb25e-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="cb25e-111">Examples</span></span>

<span data-ttu-id="cb25e-112">**MIDL/ZS filename. idl**</span><span class="sxs-lookup"><span data-stu-id="cb25e-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="cb25e-113">**MIDL/синтакс \_ проверить filename. idl**</span><span class="sxs-lookup"><span data-stu-id="cb25e-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="cb25e-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb25e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb25e-115">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="cb25e-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="cb25e-116">**/ZS**</span><span class="sxs-lookup"><span data-stu-id="cb25e-116">**/Zs**</span></span>](-zs.md)
</dt> </dl>

 

 




