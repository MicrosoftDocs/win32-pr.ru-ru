---
description: Методы отладки для приложений COM+ зависят от языка, на котором вы решили писать компонент.
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: Отладка приложений COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db096ceb525cd988afa55e49cc88fda0ddf52549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807799"
---
# <a name="debugging-com-applications"></a><span data-ttu-id="6e39a-103">Отладка приложений COM+</span><span class="sxs-lookup"><span data-stu-id="6e39a-103">Debugging COM+ Applications</span></span>

<span data-ttu-id="6e39a-104">Методы отладки для приложений COM+ зависят от языка, на котором вы решили писать компонент.</span><span class="sxs-lookup"><span data-stu-id="6e39a-104">Debugging techniques for COM+ applications depend on the language in which you choose to write your component.</span></span>

<span data-ttu-id="6e39a-105">При выполнении кода в Microsoft Visual C++ можно запустить отладчик на C++ или, используя удаленный клиент, можно выполнить отладку с помощью удаленного управления процедурой (RPC) OLE и JIT-отладкой.</span><span class="sxs-lookup"><span data-stu-id="6e39a-105">If you code in Microsoft Visual C++, you can launch the debugger in C++ or, with a remote client, you can debug by using OLE remote procedure control (RPC) and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="6e39a-106">Вы всегда можете использовать средство администрирования "службы компонентов" для отладки компонента с помощью параметра " **запустить com+ в отладчике** " на вкладке " **Дополнительно** " диалогового окна " **Свойства** " приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="6e39a-106">You can always use the Component Services administrative tool to debug your component with the COM+ **Launch in debugger** setting on the **Advanced** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="6e39a-107">Дополнительные сведения об отладке компонентов, закодированных в C++, см. [в разделе Отладка компонентов, написанных на Visual C++](debugging-components-written-in-visual-c--.md).</span><span class="sxs-lookup"><span data-stu-id="6e39a-107">For more information on debugging components coded in C++, see [Debugging Components Written in Visual C++](debugging-components-written-in-visual-c--.md).</span></span>

<span data-ttu-id="6e39a-108">Если вы сейчас не выполняете отладку многопоточности, отслеживания компонентов, удаленных вызовов или изоляции процессов, вы можете использовать среду Microsoft Visual Basic в целях отладки.</span><span class="sxs-lookup"><span data-stu-id="6e39a-108">Unless you are currently debugging multithreading, component tracking, remote calls, or process isolation, you can use the Microsoft Visual Basic environment for debugging purposes.</span></span> <span data-ttu-id="6e39a-109">[Отладка компонентов, написанных на Visual Basic](debugging-components-written-in-visual-basic.md) описывает процесс отладки в среде Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6e39a-109">[Debugging Components Written in Visual Basic](debugging-components-written-in-visual-basic.md) describes the debugging process within a Visual Basic environment.</span></span>

<span data-ttu-id="6e39a-110">В разделе [Отладка в Visual Basic интегрированной среде](debugging-in-the-visual-basic-ide.md) разработки содержатся общие сведения о рекомендациях, советах и процедурах отладки в интегрированной среде разработки (IDE).</span><span class="sxs-lookup"><span data-stu-id="6e39a-110">The topic [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md) provides a general overview with guidelines, tips and a procedure on debugging in the integrated development environment (IDE).</span></span>

<span data-ttu-id="6e39a-111">Дополнительные сведения об отладке дополнительных процессов см. в разделе [Отладка, скомпилированная Visual Basic компонентов](debugging-compiled-visual-basic-components.md).</span><span class="sxs-lookup"><span data-stu-id="6e39a-111">To view more information about debugging advanced processes, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

> [!Note]  
> <span data-ttu-id="6e39a-112">Некоторые ограничения, связанные с использованием среды Visual Basic для отладки компонентов с помощью MTS, были разрешены для COM+.</span><span class="sxs-lookup"><span data-stu-id="6e39a-112">Several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="6e39a-113">Дополнительные сведения см. в разделе [Поддержка отладки COM+ Visual Basic, которая отличается от MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span><span class="sxs-lookup"><span data-stu-id="6e39a-113">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6e39a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="6e39a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e39a-115">Обработка ошибок в COM+</span><span class="sxs-lookup"><span data-stu-id="6e39a-115">Handling Errors in COM+</span></span>](handling-errors-in-com-.md)
</dt> </dl>

 

 



