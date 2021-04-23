---
title: Пример управления касанием Windows (Мтманипулатион)
description: В этом разделе описывается пример манипуляции с касанием Windows.
ms.assetid: 59b9279c-ffa3-42c3-a01f-3ea7aca8f235
keywords:
- Windows Touch, примеры кода
- Windows Touch, пример кода
- Касание Windows, манипуляции
- Пример манипуляции с Windows Touch
- манипуляции, пример кода
- манипуляции, примеры кода
- Пример манипуляции
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: b93ac4d7cd6724d5475c919c74b90eaf106d2803
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412500"
---
# <a name="windows-touch-manipulation-sample-mtmanipulation"></a><span data-ttu-id="24e71-110">Пример управления касанием Windows (Мтманипулатион)</span><span class="sxs-lookup"><span data-stu-id="24e71-110">Windows Touch Manipulation Sample (MTManipulation)</span></span>

<span data-ttu-id="24e71-111">В этом разделе описывается пример манипуляции с касанием Windows.</span><span class="sxs-lookup"><span data-stu-id="24e71-111">This section describes the Windows Touch Manipulation sample.</span></span>

<span data-ttu-id="24e71-112">В образце манипулирования Windows показано, как преобразовать, повернуть и масштабировать объект с помощью интерфейса [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) и реализации приемника событий [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) .</span><span class="sxs-lookup"><span data-stu-id="24e71-112">The Windows Touch Manipulation sample demonstrates how to translate, rotate, and scale an object using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface and implementing an [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) event sink.</span></span> <span data-ttu-id="24e71-113">На следующем снимке экрана показано, как выглядит пример при его выполнении.</span><span class="sxs-lookup"><span data-stu-id="24e71-113">The following screen shot shows how the sample looks when it is running.</span></span>

![снимок экрана с примером "Сенсорная манипуляция Windows" с повернутым синим цветом прямоугольника с синей линией, нарисованными из противоположных углов](images/mtmanipulation.png)

<span data-ttu-id="24e71-115">В этом примере создается класс **кдравингобжект** , который можно программно переводить, поворачивать или масштабировать.</span><span class="sxs-lookup"><span data-stu-id="24e71-115">For this sample, a **CDrawingObject** class is created that can be programmatically translated, rotated, or scaled.</span></span> <span data-ttu-id="24e71-116">Создается экземпляр интерфейса [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="24e71-116">An [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface is instantiated.</span></span> <span data-ttu-id="24e71-117">Создается приемник событий манипуляции, который принимает указатель на класс **кдравингобжект** и интерфейс **IManipulationProcessor** в своем конструкторе.</span><span class="sxs-lookup"><span data-stu-id="24e71-117">A manipulation event sink is created that accepts a pointer to the **CDrawingObject** class and the **IManipulationProcessor** interface on its constructor.</span></span> <span data-ttu-id="24e71-118">Точка соединения с IManipulationProcessor создается в реализации приемника событий манипуляции, чтобы события, вызванные **IManipulationProcessor** , получались приемником событий.</span><span class="sxs-lookup"><span data-stu-id="24e71-118">A connection point to the IManipulationProcessor is created in the manipulation event sink implementation so that events raised by the **IManipulationProcessor** are received by the event sink.</span></span> <span data-ttu-id="24e71-119">Сенсорные данные подаются в интерфейс **IManipulationProcessor** , а интерфейс порождает [**_IManipulationEvent**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) событий.</span><span class="sxs-lookup"><span data-stu-id="24e71-119">Touch data is fed to the **IManipulationProcessor** interface and the interface will then raise [**_IManipulationEvent**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) events.</span></span> <span data-ttu-id="24e71-120">Обработчики событий в классе **кманипулатионевентсинк** будут обновлять ориентацию **кдравингобжект** путем вызова методов доступа в указателе на **кдравингобжект**.</span><span class="sxs-lookup"><span data-stu-id="24e71-120">The event handlers in the **CManipulationEventSink** class will update the orientation of the **CDrawingObject** by calling accessors on the pointer to the **CDrawingObject**.</span></span>

<span data-ttu-id="24e71-121">В следующем коде показано, как окно настраивается для сенсорного ввода и как создаются экземпляры **кдравингобжект** и [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) и передаются в конструктор **кманипулатионевентсинк** .</span><span class="sxs-lookup"><span data-stu-id="24e71-121">The following code shows how the window is set up for touch and how the **CDrawingObject** and [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) are instantiated and passed to the **CManipulationEventSink** constructor.</span></span>

```C++
CDrawingObject g_cRect; // CDrawingObject class holds information about the rectangle
                        // and it is responsible for painting the rectangle.

(...)

BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
(...)
    // Register application window for receiving multi-touch input. Use default settings.
    if (!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multi-touch input", L"Error", MB_OK);
        return FALSE;
    }
    ASSERT(IsTouchWindow(hWnd, NULL));

    // Instantiate the ManipulationProcessor object
    HRESULT hr = CoCreateInstance(__uuidof(ManipulationProcessor), NULL, CLSCTX_ALL, IID_PPV_ARGS(&g_pIManipProc));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"InitInstance: failed to instantiate the ManipulationProcessor object");
        return FALSE;
    }

    // Instantiate the event sink with the manipulation processor and pointer to the rectangle object
    g_pManipulationEventSink = new CManipulationEventSink(&g_cRect);
    if (g_pManipulationEventSink == NULL)
    {
        ASSERT(g_pManipulationEventSink && L"InitInstance: failed to instantiate the CManipulationEventSink class");
        g_pIManipProc->Release();
        g_pIManipProc = NULL;
        return FALSE;
    }

    // Establish the link between ManipulationEventSink and ManipulationProcessor
    if (!g_pManipulationEventSink->Connect(g_pIManipProc))
    {
        ASSERT(FALSE && L"InitInstance: failed to connect ManipulationEventSink and ManipulationProcessor");
        g_pIManipProc->Release();
        g_pIManipProc = NULL;
        g_pManipulationEventSink->Release();
        g_pManipulationEventSink = NULL;
        return FALSE;
    }
```

<span data-ttu-id="24e71-122">В следующем коде показан конструктор для приемника событий манипуляции **кманипулатионевентсинк**.</span><span class="sxs-lookup"><span data-stu-id="24e71-122">The following code shows the constructor for the manipulation event sink, **CManipulationEventSink**.</span></span>

```C++
CManipulationEventSink::CManipulationEventSink(CDrawingObject* pcDrawingObject)
:   m_cRefCount(1),
    m_pConnection(NULL),
    m_dwCookie(0),
    m_pcDrawingObject(pcDrawingObject)
{
    ASSERT((pcDrawingObject != NULL) && L"CManipulationEventSink constructor: incorrect argument");
}
```

<span data-ttu-id="24e71-123">В следующем коде показано, как приемник событий подключен к обработчику манипуляции.</span><span class="sxs-lookup"><span data-stu-id="24e71-123">The following code shows how the event sink is connected to the manipulation processor.</span></span>

```C++
bool CManipulationEventSink::Connect(IManipulationProcessor* pManipulationProcessor)
{
    // Check input arguments
    if (pManipulationProcessor == NULL)
    {
        ASSERT((pManipulationProcessor != NULL) && L"CManipulationEventSink::Create : incorrect arguments");
        return false;
    }

    // Check object state
    if ((m_dwCookie != 0) || (m_pConnection != NULL))
    {
        ASSERT((m_dwCookie == 0) && (m_pConnection == NULL) && L"CManipulationEventSink::Connect : connection already established");
        return false;
    }

    // Get the container with the connection points.
    IConnectionPointContainer* pConnectionContainer = NULL;
    HRESULT hr = pManipulationProcessor->QueryInterface(&pConnectionContainer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CManipulationEventSink::Connect : failed to get the container with the connection points");
        return false;
    }

    // Get a connection point.
    hr = pConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnection);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CManipulationEventSink::Connect : failed to get a connection point");
        pConnectionContainer->Release();
        return false;
    }

    // Release the connection container.
    pConnectionContainer->Release();

    // Advise. Establishes an advisory connection between the connection point and the
    // caller's sink object.
    hr = m_pConnection->Advise(this, &m_dwCookie);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CManipulationEventSink::Connect : failed to Advise");
        m_pConnection->Release();
        m_pConnection = NULL;
        return false;
    }

    return true;
}
```

<span data-ttu-id="24e71-124">В следующем коде показано, как сенсорные данные передаются в приемник событий манипуляции.</span><span class="sxs-lookup"><span data-stu-id="24e71-124">The following code shows how touch data is passed to the manipulation event sink.</span></span>

```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
(...)

    switch (message)
    {
 (...)
    // WM_TOUCH message handlers
    case WM_TOUCH:
        {
            // WM_TOUCH message can contain several messages from different contacts
            // packed together.
            // Message parameters need to be decoded:
            UINT  cInputs  = (int) wParam;      // Number of actual per-contact messages
            TOUCHINPUT* pInputs = new TOUCHINPUT[cInputs]; // Allocate the storage for the parameters of the per-contact messages
            if (pInputs == NULL)
            {
                break;
            }
            // Unpack message parameters into the array of TOUCHINPUT structures, each
            // representing a message for one single contact.
            if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT)))
            {
                // For each contact, dispatch the message to the appropriate message
                // handler.
                for (unsigned int i = 0; i < cInputs; i++)
                {
                    if (pInputs[i].dwFlags & TOUCHEVENTF_DOWN)
                    {
                        g_pIManipProc->ProcessDown(pInputs[i].dwID, (FLOAT)pInputs[i].x, (FLOAT)pInputs[i].y);
                    }
                    else if (pInputs[i].dwFlags & TOUCHEVENTF_MOVE)
                    {
                        g_pIManipProc->ProcessMove(pInputs[i].dwID, (FLOAT)pInputs[i].x, (FLOAT)pInputs[i].y);
                    }
                    else if (pInputs[i].dwFlags & TOUCHEVENTF_UP)
                    {
                        g_pIManipProc->ProcessUp(pInputs[i].dwID, (FLOAT)pInputs[i].x, (FLOAT)pInputs[i].y);
                    }
                }
            }
            else
            {
                // error handling, presumably out of memory
                ASSERT(FALSE && L"Error: failed to execute GetTouchInputInfo");
                delete [] pInputs;
                break;
            }
            if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
            {
                // error handling, presumably out of memory
                ASSERT(FALSE && L"Error: failed to execute CloseTouchInputHandle");
                delete [] pInputs;
                break;
            }
            delete [] pInputs;

            // Force redraw of the rectangle
            InvalidateRect(hWnd, NULL, TRUE);
        }
        break;
```

<span data-ttu-id="24e71-125">В следующем коде показано, как обработчики событий обновляют ориентацию и размер объекта при манипуляциях с разностными событиями.</span><span class="sxs-lookup"><span data-stu-id="24e71-125">The following code shows how the event handlers update the object orientation and size on manipulation delta events.</span></span>

```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta(
    /* [in] */ FLOAT /* x */,
    /* [in] */ FLOAT /* y */,
    /* [in] */ FLOAT translationDeltaX,
    /* [in] */ FLOAT translationDeltaY,
    /* [in] */ FLOAT scaleDelta,
    /* [in] */ FLOAT /* expansionDelta */,
    /* [in] */ FLOAT rotationDelta,
    /* [in] */ FLOAT /* cumulativeTranslationX */,
    /* [in] */ FLOAT /* cumulativeTranslationY */,
    /* [in] */ FLOAT /* cumulativeScale */,
    /* [in] */ FLOAT /* cumulativeExpansion */,
    /* [in] */ FLOAT /* cumulativeRotation */)
{
    m_pcDrawingObject->ApplyManipulationDelta(translationDeltaX,translationDeltaY,scaleDelta,rotationDelta);

    return S_OK;
}
```

<span data-ttu-id="24e71-126">Следующий код является реализацией **апплиманипулатионделта** в классе **кдравингобжект** .</span><span class="sxs-lookup"><span data-stu-id="24e71-126">The following code is the implementation of **ApplyManipulationDelta** in the **CDrawingObject** class.</span></span>

```C++
// This function is responsible for manipulation of the rectangle.
// It is called from CManipulationEventSink class.
// in:
//      translationDeltaX - shift of the x-coordinate (1/100 of pixel units)
//      translationDeltaY - shift of the y-coordinate (1/100 of pixel units)
//             scaleDelta - scale factor (zoom in/out)
//          rotationDelta - rotation angle in radians
void CDrawingObject::ApplyManipulationDelta(
    const FLOAT translationDeltaX,
    const FLOAT translationDeltaY,
    const FLOAT scaleDelta,
    const FLOAT rotationDelta
)
{
    _ptCenter.x += (LONG) (translationDeltaX / 100.0);
    _ptCenter.y += (LONG) (translationDeltaY / 100.0);

    _dScalingFactor *= scaleDelta;

    _dRotationAngle -= rotationDelta; // we are substracting because Y-axis is down
}
```

<span data-ttu-id="24e71-127">После обновления центральных точек **кдравингобжект**, коэффициента масштабирования и угла вращения объект будет рисовать сам.</span><span class="sxs-lookup"><span data-stu-id="24e71-127">After the **CDrawingObject**'s center points, scale factor, and rotation angle are updated, the object will draw itself transformed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24e71-128">См. также</span><span class="sxs-lookup"><span data-stu-id="24e71-128">Related topics</span></span>

<span data-ttu-id="24e71-129">[Приложение для управления несколькими касаниями](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [пример манипуляции и инерции](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [примеры для Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="24e71-129">[Multi-touch Manipulation Application](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [Manipulation and Inertia Sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
