---
description: Отладка компонентов, написанных на Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Отладка компонентов, написанных на Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701281"
---
# <a name="debugging-components-written-in-visual-basic"></a><span data-ttu-id="86d0f-103">Отладка компонентов, написанных на Visual Basic</span><span class="sxs-lookup"><span data-stu-id="86d0f-103">Debugging Components Written in Visual Basic</span></span>

<span data-ttu-id="86d0f-104">Для отладки в определенных сценариях можно использовать среду разработки Microsoft Visual Basic 6,0.</span><span class="sxs-lookup"><span data-stu-id="86d0f-104">You can use the Microsoft Visual Basic 6.0 development environment for debugging within certain scenarios.</span></span> <span data-ttu-id="86d0f-105">Использование Visual Basic для отладки обеспечивает доступ к средствам, знакомым Visual Basic программистам.</span><span class="sxs-lookup"><span data-stu-id="86d0f-105">Using Visual Basic for debugging allows access to tools familiar to Visual Basic programmers.</span></span> <span data-ttu-id="86d0f-106">С другой стороны, поскольку во время отладки Visual Basic компоненты выполняются в процессе Visual Basic среды, может потребоваться отладка компонента после его компиляции с помощью среды разработки Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="86d0f-106">On the other hand, because during debugging Visual Basic components run within the Visual Basic environment's process, it may be necessary to debug your component after it has been compiled by using the Microsoft Visual C++ development environment.</span></span>

<span data-ttu-id="86d0f-107">Дополнительные сведения об отладке в Visual Basic интегрированной среде разработки (IDE) см. [в разделе Отладка в среде ide Visual Basic](debugging-in-the-visual-basic-ide.md).</span><span class="sxs-lookup"><span data-stu-id="86d0f-107">For more information about debugging within the Visual Basic integrated development environment (IDE), see [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md).</span></span> <span data-ttu-id="86d0f-108">Дополнительные сведения об отладке Visual Basic компонентов после их компиляции с помощью среды разработки Visual C++ см. в разделе [Отладка, скомпилированная Visual Basic компонентов](debugging-compiled-visual-basic-components.md).</span><span class="sxs-lookup"><span data-stu-id="86d0f-108">For more on debugging Visual Basic components after they're compiled using the Visual C++ development environment, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

<span data-ttu-id="86d0f-109">Кроме того, некоторые ограничения, связанные с использованием среды Visual Basic для отладки компонентов с помощью MTS, были разрешены для COM+.</span><span class="sxs-lookup"><span data-stu-id="86d0f-109">Also, several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="86d0f-110">Дополнительные сведения см. в разделе [Поддержка отладки COM+ Visual Basic, которая отличается от MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span><span class="sxs-lookup"><span data-stu-id="86d0f-110">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

> [!Note]  
> <span data-ttu-id="86d0f-111">Если вы уже использовали Visual Basic на том же компьютере, что и COM+, возможно, вы заметили, что надстройка служб компонентов доступна в среде Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="86d0f-111">If you have already used Visual Basic on the same computer as COM+, you may have noticed the Component Services add-in available in the Visual Basic environment.</span></span> <span data-ttu-id="86d0f-112">Изначально в MTS эта функция была разработана для обновления реестра при каждой повторной компиляции компонента в приложении COM+.</span><span class="sxs-lookup"><span data-stu-id="86d0f-112">Originally in MTS, this feature was designed to update the registry each time you recompiled a component in a COM+ application.</span></span> <span data-ttu-id="86d0f-113">Однако, учитывая характер взаимодействия реестра Microsoft Windows и базы данных регистрации COM+, некоторые параметры могут быть не обновлены полностью.</span><span class="sxs-lookup"><span data-stu-id="86d0f-113">However, given the nature of the interaction of the Microsoft Windows Registry and the COM+ registration database, some settings may not be completely updated.</span></span> <span data-ttu-id="86d0f-114">Поэтому вместо использования команд, доступных в этой надстройке, следует удалить и переустановить компоненты, чтобы обновить параметры после повторной компиляции.</span><span class="sxs-lookup"><span data-stu-id="86d0f-114">Therefore, instead of using the commands available with this add-in, you should remove and reinstall your components to update settings after recompiling.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="86d0f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="86d0f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86d0f-116">Отладка компонентов, написанных на Visual C++</span><span class="sxs-lookup"><span data-stu-id="86d0f-116">Debugging Components Written in Visual C++</span></span>](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



