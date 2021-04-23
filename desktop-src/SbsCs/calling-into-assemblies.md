---
description: При вызове EntryPoint сборки рекомендуется использовать тот же контекст активации, который был активным при поиске сборки.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Вызов сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4742b19ea47e03fac5f7d0318248ea167182e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998732"
---
# <a name="calling-into-assemblies"></a><span data-ttu-id="3c764-103">Вызов сборок</span><span class="sxs-lookup"><span data-stu-id="3c764-103">Calling Into Assemblies</span></span>

<span data-ttu-id="3c764-104">При вызове EntryPoint сборки рекомендуется использовать тот же контекст активации, который был активным при поиске сборки.</span><span class="sxs-lookup"><span data-stu-id="3c764-104">When calling into the entrypoints of an assembly, it is recommended that you use the same activation context that was active when searching for the assembly.</span></span> <span data-ttu-id="3c764-105">Как минимум, убедитесь, что компонент, загружающий сборку, не получает контекст активации, который использует ваше приложение.</span><span class="sxs-lookup"><span data-stu-id="3c764-105">At minimum, ensure that the component loading the assembly does not accidentally get the activation context your application is using.</span></span> <span data-ttu-id="3c764-106">Утечка контекста активации по границам DLL может привести к непредвиденным зависимостям.</span><span class="sxs-lookup"><span data-stu-id="3c764-106">Leaking activation context across DLL boundaries can lead to unexpected dependencies.</span></span> <span data-ttu-id="3c764-107">Это не является проблемой, если приложение \_ \_ выполняет компиляцию включенной в режиме изоляции, так как в этом случае контекст активации по умолчанию не активен.</span><span class="sxs-lookup"><span data-stu-id="3c764-107">This is not a problem if your application compiles ISOLATION\_AWARE\_ENABLED because in that case no activation context is active by default.</span></span> <span data-ttu-id="3c764-108">Если не выполнить компиляцию с \_ \_ включенной поддержкой режима изоляции, необходимо активировать контекст активации **null** или тот же контекст активации, который использовался для загрузки сборки.</span><span class="sxs-lookup"><span data-stu-id="3c764-108">If you do not compile with ISOLATION\_AWARE\_ENABLED defined, you should activate the **NULL** activation context or the same activation context that was used to load the assembly.</span></span>

<span data-ttu-id="3c764-109">В следующем примере выполняется проверка того, что размещенная библиотека DLL запускается в контексте, который он распознает:</span><span class="sxs-lookup"><span data-stu-id="3c764-109">The following example ensures that the hosted DLL runs in a context that it recognizes:</span></span>

``` syntax
ULONG_PTR ulpCookie;
ActivateActCtx(hTheActCtxForMyDll, &ulpCookie);
__try 
{
        MyDllIsolatedFunction();
    myDllIsolatedComInterface->Funct();
}
__finally 
{
    DeactivateActCtx(0, ulpCookie);
}
```

 

 



