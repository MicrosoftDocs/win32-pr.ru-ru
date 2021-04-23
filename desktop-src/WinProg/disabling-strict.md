---
title: Отключение
description: Чтобы отключить проверку СТРОГОго типа, определите имя символа без \_ строгого указания. В Visual C/C++ можно также указать это определение в командной строке или в файле makefile, указав/дно в \_ качестве параметра компилятора.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777513"
---
# <a name="disabling-strict"></a><span data-ttu-id="79d86-104">Отключение</span><span class="sxs-lookup"><span data-stu-id="79d86-104">Disabling STRICT</span></span>

<span data-ttu-id="79d86-105">Чтобы отключить проверку **строгого** типа, определите имя символа **без \_ строгого** указания.</span><span class="sxs-lookup"><span data-stu-id="79d86-105">To disable **STRICT** type checking, define the symbol name **NO\_STRICT**.</span></span> <span data-ttu-id="79d86-106">В Visual C/C++ можно также указать это определение в командной строке или в файле makefile, указав **/дно \_** в качестве параметра компилятора.</span><span class="sxs-lookup"><span data-stu-id="79d86-106">In Visual C/C++, you can also specify this definition on the command line or in a makefile by specifying **/DNO\_STRICT** as a compiler option.</span></span>

<span data-ttu-id="79d86-107">Чтобы **не задавать никаких \_ мер** для каждого файла, вставьте инструкцию **\# define** перед включением Windows. h:</span><span class="sxs-lookup"><span data-stu-id="79d86-107">To define **NO\_STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define NO_STRICT
#include <windows.h>
```



<span data-ttu-id="79d86-108">Для получения наилучших результатов следует также установить уровень предупреждений для сообщений об ошибках по меньшей мере в **/W3**.</span><span class="sxs-lookup"><span data-stu-id="79d86-108">For best results, you should also set the warning level for error messages to at least **/W3**.</span></span> <span data-ttu-id="79d86-109">Это всегда рекомендуется при работе с приложениями для Windows, так как практика написания кода, вызывающая предупреждение (например, передавая неверное число параметров), обычно вызывает неустранимую ошибку во время выполнения, если она не исправлена.</span><span class="sxs-lookup"><span data-stu-id="79d86-109">This is always advisable with applications for Windows, because a coding practice that causes a warning (for example, passing the wrong number of parameters) usually causes a fatal error at run time if it is not corrected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79d86-110">См. также</span><span class="sxs-lookup"><span data-stu-id="79d86-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79d86-111">Включение параметра</span><span class="sxs-lookup"><span data-stu-id="79d86-111">Enabling STRICT</span></span>](enabling-strict.md)
</dt> <dt>

[<span data-ttu-id="79d86-112">ЖЕСТКОЕ соответствие</span><span class="sxs-lookup"><span data-stu-id="79d86-112">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 




