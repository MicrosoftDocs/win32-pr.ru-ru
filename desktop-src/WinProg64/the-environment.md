---
title: Среда
description: Разработчики, работающие с приложениями для 64-разрядной версии Windows, найдут среду разработки практически идентично среде разработки для 32-разрядной версии Windows.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- среда разработки 64-разрядное программирование для Windows
- среда 64-разрядное программирование для Windows
- 64-разрядное руководством по программированию Windows 64-разрядное программирование для Windows, среда разработки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067643"
---
# <a name="the-environment"></a><span data-ttu-id="e4c7a-106">Среда</span><span class="sxs-lookup"><span data-stu-id="e4c7a-106">The Environment</span></span>

<span data-ttu-id="e4c7a-107">Разработчики, работающие с приложениями для 64-разрядной версии Windows, найдут среду разработки практически идентично среде разработки для 32-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="e4c7a-107">Developers working on applications for 64-bit Windows will find the development environment virtually identical to the development environment for 32-bit Windows.</span></span> <span data-ttu-id="e4c7a-108">Существующие API-интерфейсы были изменены там, где это необходимо, чтобы они отражали точность платформы, в которой они выполняются.</span><span class="sxs-lookup"><span data-stu-id="e4c7a-108">The existing APIs have been modified where necessary to allow them to reflect the precision of the platform on which they are running.</span></span> <span data-ttu-id="e4c7a-109">Результатом является простота и короткая кривая обучения для разработчика — написание кода для 64-разрядной версии Windows так же, как написание кода для 32-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="e4c7a-109">The result is simplicity and a short learning curve for the developer—writing code for 64-bit Windows is just like writing code for 32-bit Windows.</span></span>

<span data-ttu-id="e4c7a-110">Файлы заголовков Windows поддерживают новые типы данных, позволяющие использовать указатели и связанные с указателями переменные для отражения точности платформы.</span><span class="sxs-lookup"><span data-stu-id="e4c7a-110">The Windows header files support new data types that allow pointers and pointer-associated variables to reflect the precision of the platform.</span></span> <span data-ttu-id="e4c7a-111">Это означает, что разработчики могут компилировать одну базу исходного кода для собственного запуска в 32-разрядной Windows или 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="e4c7a-111">This means that developers can compile a single source base to run natively on either 32-bit Windows or 64-bit Windows.</span></span> <span data-ttu-id="e4c7a-112">Эта стратегия сокращает затраты на разработку приложений, использующих 64-разрядное оборудование, например процессоры AMD Opteron или Athlon64 или процессоры Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="e4c7a-112">This strategy reduces the cost of developing applications that leverage 64-bit hardware such as AMD Opteron or Athlon64 processors or Intel Itanium processors.</span></span>

<span data-ttu-id="e4c7a-113">Вы получите больше времени на создание приложений 64-bit, если хотите как можно скорее присвоить новые соглашения о типе данных.</span><span class="sxs-lookup"><span data-stu-id="e4c7a-113">You will have more time to make your applications 64-bit ready if you adopt the new data-type conventions as soon as possible.</span></span> <span data-ttu-id="e4c7a-114">При изменении кода необходимо одновременно изменить определения данных.</span><span class="sxs-lookup"><span data-stu-id="e4c7a-114">If you are changing your code, you should change the data definitions at the same time.</span></span> <span data-ttu-id="e4c7a-115">Протестируйте приложение в 32-разрядной версии Windows, запустите его с помощью 64-разрядного компилятора (описанного в разделе [средства](the-tools.md)), и приложение будет готово к тестированию при наличии соответствующего 64-разрядного оборудования.</span><span class="sxs-lookup"><span data-stu-id="e4c7a-115">Test the application on 32-bit Windows, run it through the 64-bit compiler (described in [The Tools](the-tools.md)), and the application will be ready to test when you have the appropriate 64-bit hardware.</span></span>

 

 




