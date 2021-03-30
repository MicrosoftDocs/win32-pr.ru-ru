---
description: Загрузка графа из внешнего процесса
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Загрузка графа из внешнего процесса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104552961"
---
# <a name="loading-a-graph-from-an-external-process"></a><span data-ttu-id="98a2a-103">Загрузка графа из внешнего процесса</span><span class="sxs-lookup"><span data-stu-id="98a2a-103">Loading a Graph From an External Process</span></span>

<span data-ttu-id="98a2a-104">Графедит может загрузить граф фильтра, созданный внешним процессом.</span><span class="sxs-lookup"><span data-stu-id="98a2a-104">GraphEdit can load a filter graph created by an external process.</span></span> <span data-ttu-id="98a2a-105">С помощью этой функции можно увидеть, какой граф фильтра создает приложение, с минимальным объемом дополнительного кода в приложении.</span><span class="sxs-lookup"><span data-stu-id="98a2a-105">With this feature, you can see exactly what filter graph your application builds, with only a minimal amount of additional code in your application.</span></span>

> [!Note]  
> <span data-ttu-id="98a2a-106">Для этого компонента требуется Windows 2000, Windows XP или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="98a2a-106">This feature requires Windows 2000, Windows XP, or later.</span></span>

 

> [!Note]  
> <span data-ttu-id="98a2a-107">Начиная с Windows Vista, необходимо зарегистрировать proppage.dll, чтобы включить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="98a2a-107">Starting in Windows Vista, you must register proppage.dll to enable this feature.</span></span> <span data-ttu-id="98a2a-108">Proppage.dll входит в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="98a2a-108">Proppage.dll is included in the Windows SDK.</span></span>

 

<span data-ttu-id="98a2a-109">Приложение должно зарегистрировать экземпляр графа фильтра в запущенной таблице объектов (ROT).</span><span class="sxs-lookup"><span data-stu-id="98a2a-109">The application must register the filter graph instance in the Running Object Table (ROT).</span></span> <span data-ttu-id="98a2a-110">ROT — это глобально доступная Таблица поиска, которая отслеживает выполняемые объекты.</span><span class="sxs-lookup"><span data-stu-id="98a2a-110">The ROT is a globally accessible look-up table that keeps track of running objects.</span></span> <span data-ttu-id="98a2a-111">Объекты регистрируются в таблице ROT с помощью моникера.</span><span class="sxs-lookup"><span data-stu-id="98a2a-111">Objects are registered in the ROT by moniker.</span></span> <span data-ttu-id="98a2a-112">Чтобы подключиться к графу, Графедит выполняет поиск моникеров в таблице ROT, отображаемое имя которых соответствует определенному формату:</span><span class="sxs-lookup"><span data-stu-id="98a2a-112">To connect to the graph, GraphEdit searches the ROT for monikers whose display name matches a particular format:</span></span>


```C++
!FilterGraph X pid Y
```



<span data-ttu-id="98a2a-113">где *X* — шестнадцатеричный адрес диспетчера графа фильтров, а *Y* — идентификатор процесса, также в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="98a2a-113">where *X* is the hexadecimal address of the Filter Graph Manager, and *Y* is the process id, also in hexadecimal.</span></span>

<span data-ttu-id="98a2a-114">Когда приложение сначала создает граф фильтра, вызовите следующую функцию:</span><span class="sxs-lookup"><span data-stu-id="98a2a-114">When your application first creates the filter graph, call the following function:</span></span>


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



<span data-ttu-id="98a2a-115">Эта функция создает моникер и новую запись ROT для графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="98a2a-115">This function creates a moniker and a new ROT entry for the filter graph.</span></span> <span data-ttu-id="98a2a-116">Первый параметр — это указатель на граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="98a2a-116">The first parameter is a pointer to the filter graph.</span></span> <span data-ttu-id="98a2a-117">Второй параметр получает значение, идентифицирующее новую запись ROT.</span><span class="sxs-lookup"><span data-stu-id="98a2a-117">The second parameter receives a value that identifies the new ROT entry.</span></span> <span data-ttu-id="98a2a-118">Прежде чем приложение выпустит граф фильтра, вызовите следующую функцию, чтобы удалить запись ROT.</span><span class="sxs-lookup"><span data-stu-id="98a2a-118">Before the application releases the filter graph, call the following function to remove the ROT entry.</span></span> <span data-ttu-id="98a2a-119">Параметр *пдврегистер* — это идентификатор, возвращаемый функцией аддторот.</span><span class="sxs-lookup"><span data-stu-id="98a2a-119">The *pdwRegister* parameter is the identifier returned by the AddToRot function.</span></span>


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



<span data-ttu-id="98a2a-120">В следующем примере кода показано, как вызывать эти функции.</span><span class="sxs-lookup"><span data-stu-id="98a2a-120">The following code example shows how to call these functions.</span></span> <span data-ttu-id="98a2a-121">В этом примере код, который добавляет и удаляет записи ROT, компилируется условно, так что он включается только в отладочных сборках.</span><span class="sxs-lookup"><span data-stu-id="98a2a-121">In this example, the code that adds and removes ROT entries is conditionally compiled, so that it is included only in debug builds.</span></span>


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



<span data-ttu-id="98a2a-122">Чтобы просмотреть граф фильтра в Графедит, запустите приложение и Графедит в то же время.</span><span class="sxs-lookup"><span data-stu-id="98a2a-122">To view the filter graph in GraphEdit, run your application and GraphEdit at the same time.</span></span> <span data-ttu-id="98a2a-123">В меню **файл** графедит выберите пункт **подключиться к удаленной диаграмме...** В диалоговом окне **Подключение к графу** выберите идентификатор процесса (PID) приложения и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="98a2a-123">In the GraphEdit **File** menu, click **Connect to Remote Graph...** In the **Connect To Graph** dialog box, select the process id (pid) of your application and click **OK**.</span></span> <span data-ttu-id="98a2a-124">Графедит загружает граф фильтра и отображает его.</span><span class="sxs-lookup"><span data-stu-id="98a2a-124">GraphEdit loads the filter graph and displays it.</span></span> <span data-ttu-id="98a2a-125">Не используйте другие функции Графедит на этом графе — это может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="98a2a-125">Don't use any other GraphEdit features on this graph—it might cause unexpected results.</span></span> <span data-ttu-id="98a2a-126">Например, не добавляйте и не удаляйте фильтры, а также приостанавливаете и запускаете граф.</span><span class="sxs-lookup"><span data-stu-id="98a2a-126">For example, don't add or remove filters, or stop and start the graph.</span></span> <span data-ttu-id="98a2a-127">Перед выходом из приложения закройте Графедит.</span><span class="sxs-lookup"><span data-stu-id="98a2a-127">Close GraphEdit before exiting your application.</span></span>

> [!Note]  
> <span data-ttu-id="98a2a-128">Приложение может столкнуться с различными утверждениями при его выходе.</span><span class="sxs-lookup"><span data-stu-id="98a2a-128">Your application might hit various asserts when it exits.</span></span> <span data-ttu-id="98a2a-129">На них можно не обращать внимания.</span><span class="sxs-lookup"><span data-stu-id="98a2a-129">You can ignore these.</span></span>

 

<span data-ttu-id="98a2a-130">На следующем рисунке показано диалоговое окно « **соединение с диаграммой** ».</span><span class="sxs-lookup"><span data-stu-id="98a2a-130">The following illustration shows the **Connect To Graph** dialog box.</span></span>

![подключение к графу](images/gedit-spy.png)

<span data-ttu-id="98a2a-132">Когда Графедит загружает граф, он выполняется в контексте целевого приложения.</span><span class="sxs-lookup"><span data-stu-id="98a2a-132">When GraphEdit loads the graph, it executes in the context of the target application.</span></span> <span data-ttu-id="98a2a-133">Таким образом, Графедит может блокироваться, так как ожидает поток.</span><span class="sxs-lookup"><span data-stu-id="98a2a-133">Therefore, GraphEdit might block because it is waiting for the thread.</span></span> <span data-ttu-id="98a2a-134">Например, это может произойти при пошаговом выполнении кода в отладчике.</span><span class="sxs-lookup"><span data-stu-id="98a2a-134">For example, this can occur if you are stepping through your code in the debugger.</span></span>

<span data-ttu-id="98a2a-135">Эта функция должна использоваться только в отладочных сборках приложения, а не в розничных сборках, так как позволяет другим приложениям просматривать граф фильтра и управлять им.</span><span class="sxs-lookup"><span data-stu-id="98a2a-135">This feature should be used only in debug builds of your application, not retail builds, because it enables other applications to view or control the filter graph.</span></span>

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a><span data-ttu-id="98a2a-136">Подключение к удаленному графу из командной строки</span><span class="sxs-lookup"><span data-stu-id="98a2a-136">Connecting to a Remote Graph from the Command Line</span></span>

<span data-ttu-id="98a2a-137">Графедит поддерживает параметр командной строки для автоматической загрузки удаленного графа при запуске.</span><span class="sxs-lookup"><span data-stu-id="98a2a-137">GraphEdit supports a command-line option to load a remote graph automatically on startup.</span></span> <span data-ttu-id="98a2a-138">Синтаксис выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="98a2a-138">The syntax is:</span></span>


```C++
GraphEdt -a moniker
```



<span data-ttu-id="98a2a-139">где *моникер* — моникер, созданный с помощью функции аддторот, описанной выше.</span><span class="sxs-lookup"><span data-stu-id="98a2a-139">where *moniker* is a moniker created using the AddToRot function, described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98a2a-140">См. также</span><span class="sxs-lookup"><span data-stu-id="98a2a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98a2a-141">Имитация построения графа с помощью Графедит</span><span class="sxs-lookup"><span data-stu-id="98a2a-141">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



