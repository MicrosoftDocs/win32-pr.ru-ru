---
title: /Савепп, параметр
description: Если указана директива/Савепп, компилятор MIDL не удаляет выходные данные препроцессора C/C++.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- MIDL/Савепп Switch
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069019"
---
# <a name="savepp-switch"></a><span data-ttu-id="a7b46-104">/Савепп, параметр</span><span class="sxs-lookup"><span data-stu-id="a7b46-104">/savePP switch</span></span>

<span data-ttu-id="a7b46-105">Если указана директива **/савепп** , компилятор MIDL не удаляет выходные данные препроцессора C/C++.</span><span class="sxs-lookup"><span data-stu-id="a7b46-105">When the **/savePP** directive is specified, the MIDL compiler does not delete the output of the C/C++ preprocessor.</span></span>

``` syntax
midl /savePP
```

## <a name="switch-options"></a><span data-ttu-id="a7b46-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="a7b46-106">Switch Options</span></span>

<span data-ttu-id="a7b46-107">Этот параметр не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a7b46-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7b46-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7b46-108">Remarks</span></span>

<span data-ttu-id="a7b46-109">Этот параметр позволяет разработчикам определить, что анализируется компилятором MIDL, и что полезно для отладки.</span><span class="sxs-lookup"><span data-stu-id="a7b46-109">This switch enables developers to discern what is being parsed by the MIDL compiler, and is useful for debugging.</span></span> <span data-ttu-id="a7b46-110">Выходные данные препроцессора записываются в один или несколько временных файлов в каталоге, указанном переменной среды TEMP.</span><span class="sxs-lookup"><span data-stu-id="a7b46-110">The output of the preprocessor is written to one or more temporary files in the directory indicated by the TEMP environment variable.</span></span> <span data-ttu-id="a7b46-111">Имя выходного файла или файлов соответствует соглашению об именовании в файле MID \* . tmp.</span><span class="sxs-lookup"><span data-stu-id="a7b46-111">The name of the output file, or files, follows a naming convention of MID\*.tmp.</span></span> <span data-ttu-id="a7b46-112">Обратите внимание, что одна компиляция может создавать несколько предварительно обработанных входных потоков. Это связано с тем, что импорт IDL-файла, в отличие от функции **\# include**, приводит к отдельному запуску препроцессора.</span><span class="sxs-lookup"><span data-stu-id="a7b46-112">Note that a single compile may generate several preprocessed input streams; this is because importing an IDL file, as opposed to using **\#include**, causes a separate preprocessor run.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7b46-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7b46-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b46-114">**/КПП \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="a7b46-114">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="a7b46-115">**/КПП \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="a7b46-115">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="a7b46-116">/но \_ cpp,/нокпп</span><span class="sxs-lookup"><span data-stu-id="a7b46-116">/no\_cpp, /nocpp</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




