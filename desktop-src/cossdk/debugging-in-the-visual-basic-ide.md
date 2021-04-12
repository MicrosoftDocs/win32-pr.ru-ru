---
description: Использование интегрированной среды разработки (IDE) Microsoft Visual Basic для отладки дает Visual Basic разработчикам доступ к знакомым средствам и простоте использования.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Отладка в интегрированной среде разработки Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423270"
---
# <a name="debugging-in-the-visual-basic-ide"></a><span data-ttu-id="c1588-103">Отладка в интегрированной среде разработки Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c1588-103">Debugging in the Visual Basic IDE</span></span>

<span data-ttu-id="c1588-104">Использование интегрированной среды разработки (IDE) Microsoft Visual Basic для отладки дает Visual Basic разработчикам доступ к знакомым средствам и простоте использования.</span><span class="sxs-lookup"><span data-stu-id="c1588-104">Using the Microsoft Visual Basic integrated development environment (IDE) for debugging gives Visual Basic developers access to familiar tools and ease-of-use.</span></span> <span data-ttu-id="c1588-105">Хотя для многих компонентов в конечном итоге потребуется более полная Отладка с помощью Microsoft Visual C++ной среды, одна из стратегий может быть первой по возможности выполнять отладку как можно больше функций с Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c1588-105">While many components will eventually need to be more fully debugged using the Microsoft Visual C++ environment, one strategy might be to first debug as much functionality as possible with Visual Basic.</span></span> <span data-ttu-id="c1588-106">Например, можно использовать Visual Basic IDE для отладки в COM+, если еще не отладка многопоточности, отслеживание компонентов, удаленные вызовы или изоляция процессов.</span><span class="sxs-lookup"><span data-stu-id="c1588-106">For example, you might want to use the Visual Basic IDE for debugging within COM+ when you aren't yet debugging multithreading, component tracking, remote calls, or process isolation.</span></span>

<span data-ttu-id="c1588-107">Как правило, при использовании среды Visual Basic для отладки сначала необходимо скомпилировать проект и добавить библиотеку DLL в приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="c1588-107">In general, when using the Visual Basic environment for debugging, you first compile the project and add the DLL to a COM+ application.</span></span> <span data-ttu-id="c1588-108">Затем необходимо задать двоичную совместимость для проекта, ссылающуюся на созданную библиотеку DLL, и запустить проект, чтобы начать отладку.</span><span class="sxs-lookup"><span data-stu-id="c1588-108">Then you set binary compatibility for the project, referencing the DLL you made, and start the project to begin debugging.</span></span>

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a><span data-ttu-id="c1588-109">Общие рекомендации по отладке в среде Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c1588-109">General Guidelines for Debugging in the Visual Basic Environment</span></span>

-   <span data-ttu-id="c1588-110">При отладке с помощью Visual Basic COM+ обрабатывает компоненты Visual Basic как если бы они принадлежали приложению библиотеки, даже если компоненты зарегистрированы как относящиеся к серверному приложению.</span><span class="sxs-lookup"><span data-stu-id="c1588-110">While you are debugging using Visual Basic, COM+ treats the Visual Basic components as if they belong to a library application, even if the components are registered as belonging to a server application.</span></span> <span data-ttu-id="c1588-111">Так как она выполняется как приложение библиотеки, значки компонентов в средстве администрирования "службы компонентов" не проводятся при отладке компонентов.</span><span class="sxs-lookup"><span data-stu-id="c1588-111">Because it runs as a library application, the component icons in the Component Services administrative tool do not spin as the components are debugged.</span></span>
-   <span data-ttu-id="c1588-112">Если изменить атрибуты транзакции для компонента во время отладки или внести изменения в исходный код, требующие Visual Basic для создания нового идентификатора CLSID или ProgID, обязательно удалите и переустановите приложение COM+, содержащее этот компонент.</span><span class="sxs-lookup"><span data-stu-id="c1588-112">If you change transaction attributes on a component during debugging or make a source code change that requires Visual Basic to generate a new CLSID or ProgID, be sure to delete and reinstall the COM+ application containing the component.</span></span> <span data-ttu-id="c1588-113">Если для компонента задана двоичная совместимость, вы будете предупреждать о внесении изменений.</span><span class="sxs-lookup"><span data-stu-id="c1588-113">If you have set binary compatibility for the component, you will be warned that changes have occurred.</span></span>

## <a name="notes-on-debugging-within-a-com-application"></a><span data-ttu-id="c1588-114">Примечания об отладке в приложении COM+</span><span class="sxs-lookup"><span data-stu-id="c1588-114">Notes on Debugging Within a COM+ Application</span></span>

-   <span data-ttu-id="c1588-115">При внесении изменений в Visual Basic IDE в интерфейсы компонента, имена классов, имена проектов, поддержка транзакций или другие параметры могут содержать несоответствия между данными конфигурации в обозревателе служб компонентов и фактической конфигурацией, выполняемой в отладчике Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c1588-115">If you make changes in the Visual Basic IDE in your component's interfaces, class names, project names, transactional support or other settings, there may be mismatches between the configuration data in the Component Services explorer and the actual configuration running in the Visual Basic debugger.</span></span>
-   <span data-ttu-id="c1588-116">Не экспортируйте приложение COM+ во время отладки компонента в приложении.</span><span class="sxs-lookup"><span data-stu-id="c1588-116">Do not export a COM+ application while you are debugging a component in the application.</span></span> <span data-ttu-id="c1588-117">COM+ будет рассматривать среду разработки Visual Basic как компонент.</span><span class="sxs-lookup"><span data-stu-id="c1588-117">COM+ will treat the Visual Basic development environment as the component.</span></span>
-   <span data-ttu-id="c1588-118">Если вы используете компонент вне отладчика и затем решили начать отладку, экземпляр компонента может по-прежнему выполняться в COM+ при запуске в отладчике.</span><span class="sxs-lookup"><span data-stu-id="c1588-118">If you are running a component outside the debugger and then decide to begin debugging, an instance of the component may still be running in COM+ when you start it in the debugger.</span></span> <span data-ttu-id="c1588-119">COM+ определит это условие и попытается автоматически завершить работу экземпляра, который он контролирует.</span><span class="sxs-lookup"><span data-stu-id="c1588-119">COM+ will detect this condition and attempt to silently shut down the instance it controls.</span></span> <span data-ttu-id="c1588-120">Чтобы избежать этой проблемы, перед началом отладки удалите компонент из средства администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="c1588-120">To avoid this problem, remove the component from the Component Services administrative tool before you begin debugging.</span></span>

<span data-ttu-id="c1588-121">**Отладка с использованием среды Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="c1588-121">**To debug using the Visual Basic environment**</span></span>

1.  <span data-ttu-id="c1588-122">Откройте проект компонента в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c1588-122">Open the component project in Visual Basic.</span></span>

2.  <span data-ttu-id="c1588-123">Скомпилируйте компонент, а затем задайте в проекте двоичную совместимость для скомпилированного компонента.</span><span class="sxs-lookup"><span data-stu-id="c1588-123">Compile your component, and then set binary compatibility in your project to the compiled component.</span></span>

3.  <span data-ttu-id="c1588-124">Задайте для свойства Мтстрансактионмоде значение, отличное от 0-Нотанмтсобжект.</span><span class="sxs-lookup"><span data-stu-id="c1588-124">Set the MTSTransactionMode property to a value other than 0 - NotAnMTSObject.</span></span> <span data-ttu-id="c1588-125">При запуске проекта этот параметр запрашивает Visual Basic активации компонента в COM+.</span><span class="sxs-lookup"><span data-stu-id="c1588-125">When you start the project, this setting prompts Visual Basic to activate your component within COM+.</span></span>

4.  <span data-ttu-id="c1588-126">В меню **проект** выберите пункт **свойства**, а затем введите начальную программу на вкладке **Отладка** . Программа запуска — это клиентский исполняемый файл, вызывающий этот компонент.</span><span class="sxs-lookup"><span data-stu-id="c1588-126">From the **Project** menu, click **Properties**, and then enter the start program on the **Debugging** tab. The start program is the client executable that calls this component.</span></span>

    > [!Note]  
    > <span data-ttu-id="c1588-127">Начальная программа должна быть локальной для отлаживаемого компонента.</span><span class="sxs-lookup"><span data-stu-id="c1588-127">The start program must be local to the component you are debugging.</span></span>

     

5.  <span data-ttu-id="c1588-128">Нажмите клавишу F5, чтобы начать отладку компонента.</span><span class="sxs-lookup"><span data-stu-id="c1588-128">Press the F5 key to begin debugging the component.</span></span>

<span data-ttu-id="c1588-129">После нажатия клавиши F5 Visual Basic запускает клиентское приложение и запускает компонент в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="c1588-129">After you press F5, Visual Basic launches the client application and runs the component in debug mode.</span></span> <span data-ttu-id="c1588-130">Точки останова можно размещать в коде компонента и устанавливать контрольные значения для переменных.</span><span class="sxs-lookup"><span data-stu-id="c1588-130">You can place breakpoints in the component's code and set watches on variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1588-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c1588-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1588-132">Поддержка отладки Visual Basic COM+ отличается от MTS</span><span class="sxs-lookup"><span data-stu-id="c1588-132">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="c1588-133">Отладка скомпилированных компонентов Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c1588-133">Debugging Compiled Visual Basic Components</span></span>](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



