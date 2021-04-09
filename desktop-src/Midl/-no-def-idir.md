---
title: no_def_idir Switch
description: При указании каталогов с параметром/I \_ параметр идир/но DEF \_ предписывает компилятору MIDL искать только каталоги, указанные с помощью параметра/i.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir параметр MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889820"
---
# <a name="no_def_idir-switch"></a><span data-ttu-id="e5e04-104">\_ \_ коммутатор идир/но DEF</span><span class="sxs-lookup"><span data-stu-id="e5e04-104">/no\_def\_idir switch</span></span>

<span data-ttu-id="e5e04-105">При указании каталогов с параметром [**/i**](-i.md) параметр **идир/но \_ DEF \_** предписывает компилятору MIDL искать только каталоги, указанные с помощью параметра **/i** , игнорируя текущий каталог, а также каталоги, заданные переменной среды include.</span><span class="sxs-lookup"><span data-stu-id="e5e04-105">When directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the directories specified with the **/I** switch, ignoring the current directory as well as the directories specified by the INCLUDE environment variable.</span></span>

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a><span data-ttu-id="e5e04-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="e5e04-106">Switch Options</span></span>

<span data-ttu-id="e5e04-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e5e04-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5e04-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5e04-108">Remarks</span></span>

<span data-ttu-id="e5e04-109">Если с параметром [**/i**](-i.md) не указаны каталоги, параметр **идир/но \_ DEF \_** предписывает компилятору MIDL искать только текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="e5e04-109">When no directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="e5e04-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="e5e04-110">Examples</span></span>

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a><span data-ttu-id="e5e04-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5e04-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e04-112">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="e5e04-112">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="e5e04-113">**/акф**</span><span class="sxs-lookup"><span data-stu-id="e5e04-113">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="e5e04-114">**/I**</span><span class="sxs-lookup"><span data-stu-id="e5e04-114">**/I**</span></span>](-i.md)
</dt> </dl>

 

 




