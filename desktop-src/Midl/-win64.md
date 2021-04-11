---
title: /Win64, параметр
description: Параметр/Win64 направляет компилятор MIDL для создания файлов заглушек или файла библиотеки типов для 64-разрядной среды. Примечание. Этот параметр устарел.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- MIDL/Win64 Switch
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333691"
---
# <a name="win64-switch"></a><span data-ttu-id="5ebba-104">/Win64, параметр</span><span class="sxs-lookup"><span data-stu-id="5ebba-104">/win64 switch</span></span>

<span data-ttu-id="5ebba-105">Параметр **/Win64** направляет компилятор MIDL для создания файлов заглушек или файла библиотеки типов для 64-разрядной среды.</span><span class="sxs-lookup"><span data-stu-id="5ebba-105">The **/win64** switch directs the MIDL compiler to generate stub files, or a type library file, for a 64-bit environment.</span></span>

> [!Note]  
> <span data-ttu-id="5ebba-106">Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="5ebba-106">This switch is obsolete.</span></span> <span data-ttu-id="5ebba-107">Используйте вместо него параметр [**/ia64**](-ia64.md) или [**/AMD64**](-amd64.md) .</span><span class="sxs-lookup"><span data-stu-id="5ebba-107">Please use the [**/ia64**](-ia64.md) or [**/amd64**](-amd64.md) switch instead.</span></span> <span data-ttu-id="5ebba-108">Параметр **/Win64** эквивалентен параметру **/ia64** .</span><span class="sxs-lookup"><span data-stu-id="5ebba-108">The **/win64** switch is equivalent to the **/ia64** switch.</span></span>

 

``` syntax
midl /win64
```

## <a name="switch-options"></a><span data-ttu-id="5ebba-109">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="5ebba-109">Switch Options</span></span>

<span data-ttu-id="5ebba-110">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5ebba-110">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ebba-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ebba-111">Remarks</span></span>

<span data-ttu-id="5ebba-112">Параметр **/Win64** эквивалентен заданию параметра [**/env**](-env.md) для Win64.</span><span class="sxs-lookup"><span data-stu-id="5ebba-112">The **/win64** switch is equivalent to setting the [**/env**](-env.md) switch to win64.</span></span>

> [!Note]  
> <span data-ttu-id="5ebba-113">Невозможно использовать MIDL.exe для создания 64-разрядного TLB в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5ebba-113">It is not possible to use MIDL.exe to produce a 64bit tlb on Windows 2000.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5ebba-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ebba-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebba-115">**/env**</span><span class="sxs-lookup"><span data-stu-id="5ebba-115">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="5ebba-116">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="5ebba-116">**/ia64**</span></span>](-ia64.md)
</dt> <dt>

[<span data-ttu-id="5ebba-117">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="5ebba-117">**/amd64**</span></span>](-amd64.md)
</dt> </dl>

 

 




