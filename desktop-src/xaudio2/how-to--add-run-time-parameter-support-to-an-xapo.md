---
description: В КСАПО можно добавить поддержку параметров времени выполнения, реализовав интерфейс Иксапопараметерс. Поддержка параметров времени выполнения позволяет КСАПО изменять свое поведение в зависимости от параметров, передаваемых ей во время выполнения.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 'Руководство: добавление в XAPO поддержки параметра времени выполнения'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582f51b3dfbdc6d31422494906d5f945f77ccb03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497637"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a><span data-ttu-id="183a1-104">Руководство: добавление в XAPO поддержки параметра времени выполнения</span><span class="sxs-lookup"><span data-stu-id="183a1-104">How to: Add Run-time Parameter Support to an XAPO</span></span>

<span data-ttu-id="183a1-105">В КСАПО можно добавить поддержку параметров времени выполнения, реализовав интерфейс [**иксапопараметерс**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) .</span><span class="sxs-lookup"><span data-stu-id="183a1-105">You can add run-time parameter support to an XAPO by implementing the [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interface.</span></span> <span data-ttu-id="183a1-106">Поддержка параметров времени выполнения позволяет КСАПО изменять свое поведение в зависимости от параметров, передаваемых ей во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="183a1-106">Run-time parameter support allows an XAPO to change its behavior based on the parameters passed to it at run time.</span></span>

1.  <span data-ttu-id="183a1-107">Выполните действия, описанные в разделе [как создать ксапо](how-to--create-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="183a1-107">Follow the steps in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>
2.  <span data-ttu-id="183a1-108">Измените КСАПО на производный от [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) и [**кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span><span class="sxs-lookup"><span data-stu-id="183a1-108">Change the XAPO to derive from [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) and [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span></span>
3.  <span data-ttu-id="183a1-109">Добавьте вызовы методов [**кксапопараметерсбасе:: бегинпроцесс**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) и [**Кксапопараметерсбасе:: Ендпроцесс**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) в реализацию [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span><span class="sxs-lookup"><span data-stu-id="183a1-109">Add calls to the methods [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) to the implementation of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

    > [!Note]  
    > <span data-ttu-id="183a1-110">Добавление этих методов в [иксапо::P шаблоны](how-to--build-a-basic-audio-processing-graph.md) позволяет [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) сохранит свои копии параметров Effect в поточно-ориентированном состоянии.</span><span class="sxs-lookup"><span data-stu-id="183a1-110">Adding these methods to [IXAPO::Process](how-to--build-a-basic-audio-processing-graph.md) allows [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) to keep its copies of the effect parameters in a thread-safe state.</span></span> <span data-ttu-id="183a1-111">Вызовите метод [**кксапопараметерсбасе:: бегинпроцесс**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) в начале [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process)и [**кксапопараметерсбасе:: ендпроцесс**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) в конце **иксапо::P шаблоны**.</span><span class="sxs-lookup"><span data-stu-id="183a1-111">Call [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) at the beginning of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) at the end of **IXAPO::Process**.</span></span>

     

4.  <span data-ttu-id="183a1-112">Добавьте дополнительный код в реализацию [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , чтобы изменить его поведение в соответствии со значениями, хранящимися в методе [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) .</span><span class="sxs-lookup"><span data-stu-id="183a1-112">Add more code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation to change its behavior according to values stored by the [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="183a1-113">Добавление кода в метод [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) для использования параметров, заданных параметром [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) , позволяет изменять поведение ксапо в течение его жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="183a1-113">Adding code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method to use the parameters specified by [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) allows the XAPO's behavior to be changed throughout its life.</span></span>

     

5.  <span data-ttu-id="183a1-114">При создании экземпляра этого действия выделите буфер из трех структур, которые будут представлять параметры эффектов, и передайте его конструктору [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .</span><span class="sxs-lookup"><span data-stu-id="183a1-114">When you create an instance of the effect, allocate a buffer of three of the structures that will represent the effect's parameters, and pass it to the [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) constructor.</span></span>

    > [!Note]  
    > <span data-ttu-id="183a1-115">Экземпляр [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) использует этот буфер для управления параметрами эффектов, передаваемыми в него при вызове [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters).</span><span class="sxs-lookup"><span data-stu-id="183a1-115">The [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) instance internally uses this buffer to manage effect parameters passed to it when you call [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters).</span></span> <span data-ttu-id="183a1-116">Необходимо инициализировать все блоки параметров процесса в *ппараметерблоккс* до того же значения по умолчанию до вызова любого из методов [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**Иксапопараметерс:: Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)и **иксапопараметерс:: SetParameters** .</span><span class="sxs-lookup"><span data-stu-id="183a1-116">You must initialize all the process parameter blocks in *pParameterBlocks* to the same default value before you call any of the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters::GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters), and **IXAPOParameters::SetParameters** methods.</span></span> <span data-ttu-id="183a1-117">Обычно эта инициализация обрабатывается в [**иксапо:: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) или в [**Иксапо:: локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span><span class="sxs-lookup"><span data-stu-id="183a1-117">Usually this initialization is handled in [**IXAPO::Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) or in [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="183a1-118">См. также</span><span class="sxs-lookup"><span data-stu-id="183a1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="183a1-119">Звуковые эффекты</span><span class="sxs-lookup"><span data-stu-id="183a1-119">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="183a1-120">Обзор протокола XAPO</span><span class="sxs-lookup"><span data-stu-id="183a1-120">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
