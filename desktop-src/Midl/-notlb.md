---
title: /notlb, параметр
description: Параметр/notlb предотвращает создание файла библиотеки типов (TLB) компилятором MIDL.
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- MIDL/notlb Switch
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487145"
---
# <a name="notlb-switch"></a><span data-ttu-id="bafb2-104">/notlb, параметр</span><span class="sxs-lookup"><span data-stu-id="bafb2-104">/notlb switch</span></span>

<span data-ttu-id="bafb2-105">Параметр **/notlb** предотвращает создание файла библиотеки типов (TLB) компилятором MIDL.</span><span class="sxs-lookup"><span data-stu-id="bafb2-105">The **/notlb** switch prevents the MIDL compiler from generating a type library (TLB) file.</span></span>

``` syntax
midl /notlb
```

## <a name="switch-options"></a><span data-ttu-id="bafb2-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="bafb2-106">Switch Options</span></span>

<span data-ttu-id="bafb2-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bafb2-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bafb2-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bafb2-108">Remarks</span></span>

<span data-ttu-id="bafb2-109">По умолчанию компилятор MIDL создает TLB-файл при обнаружении оператора [**Library**](library.md) .</span><span class="sxs-lookup"><span data-stu-id="bafb2-109">By default, the MIDL compiler will generate a TLB file whenever it encounters a [**LIBRARY**](library.md) statement.</span></span> <span data-ttu-id="bafb2-110">Этот параметр переопределяет поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bafb2-110">This switch overrides the default behavior.</span></span>

<span data-ttu-id="bafb2-111">Если указан параметр **/notlb** , все другие заглушки, заголовки и т. д. создаются обычным образом.</span><span class="sxs-lookup"><span data-stu-id="bafb2-111">When the **/notlb** option is specified, all other stubs, headers, etc. are generated as usual.</span></span>

## <a name="see-also"></a><span data-ttu-id="bafb2-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bafb2-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bafb2-113">**/TLB**</span><span class="sxs-lookup"><span data-stu-id="bafb2-113">**/tlb**</span></span>](-tlb.md)
</dt> </dl>

 

 




