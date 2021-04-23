---
title: Использование OLE в элементах управления Rich Edit
description: В этом разделе содержатся сведения об использовании связывания и внедрения объектов (OLE) в элементах управления Rich Edit.
ms.assetid: bfcecbf5-cc35-47b8-a713-7e5fd03f60cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7868bd62044c87765a25f6033499460ed044e57
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "104133614"
---
# <a name="how-to-use-ole-in-rich-edit-controls"></a><span data-ttu-id="cd74d-103">Использование OLE в элементах управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="cd74d-103">How to Use OLE in Rich Edit Controls</span></span>

<span data-ttu-id="cd74d-104">В этом разделе содержатся сведения об использовании связывания и внедрения объектов (OLE) в элементах управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="cd74d-104">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cd74d-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="cd74d-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cd74d-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="cd74d-106">Technologies</span></span>

-   [<span data-ttu-id="cd74d-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="cd74d-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cd74d-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="cd74d-108">Prerequisites</span></span>

-   <span data-ttu-id="cd74d-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="cd74d-109">C/C++</span></span>
-   <span data-ttu-id="cd74d-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="cd74d-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cd74d-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="cd74d-111">Instructions</span></span>

### <a name="use-a-rich-edit-interface"></a><span data-ttu-id="cd74d-112">Использование расширенного интерфейса редактирования</span><span class="sxs-lookup"><span data-stu-id="cd74d-112">Use a Rich Edit Interface</span></span>

<span data-ttu-id="cd74d-113">Элементы управления Rich Edit предоставляют некоторые из своих функций через интерфейсы модели COM.</span><span class="sxs-lookup"><span data-stu-id="cd74d-113">Rich edit controls expose some of their functionality through Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="cd74d-114">Получая интерфейс из элемента управления, вы получаете возможность работать с другими объектами в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="cd74d-114">By obtaining an interface from a control, you gain the ability to work with other objects within the control.</span></span> <span data-ttu-id="cd74d-115">Этот интерфейс можно получить, отправив сообщение [**EM \_ жетолеинтерфаце**](em-getoleinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="cd74d-115">You can obtain this interface by sending the [**EM\_GETOLEINTERFACE**](em-getoleinterface.md) message.</span></span> <span data-ttu-id="cd74d-116">В интерфейсе [**иричедитоле**](/windows/desktop/api/Richole/nn-richole-iricheditole) можно получить интерфейсы, используемые в [объектной модели текста](text-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="cd74d-116">From the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface, you can then obtain interfaces used in the [Text Object Model](text-object-model.md).</span></span>

<span data-ttu-id="cd74d-117">Другой интерфейс, [**иричедитолекаллбакк**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), реализуется приложениями для определения поведения элемента управления, когда он взаимодействует с объектами.</span><span class="sxs-lookup"><span data-stu-id="cd74d-117">Another interface, [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback), is implemented by applications to define the behavior of the control when it interacts with objects.</span></span>

### <a name="insert-an-object-into-a-rich-edit-control"></a><span data-ttu-id="cd74d-118">Вставка объекта в элемент управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="cd74d-118">Insert an Object into a Rich Edit Control</span></span>

<span data-ttu-id="cd74d-119">В следующем примере кода объект File вставляется в форматируемый элемент управления Edit.</span><span class="sxs-lookup"><span data-stu-id="cd74d-119">The following code example inserts a file object into a rich edit control.</span></span> <span data-ttu-id="cd74d-120">Если программа связана с типом файлов на компьютере пользователя (например, Microsoft Excel для XLS-файла), содержимое файла отображается в элементе управления. в противном случае отображается значок.</span><span class="sxs-lookup"><span data-stu-id="cd74d-120">If a program is associated with the file type on the user's machine (for example, Microsoft Excel for an .xls file), the contents of the file display in the control; otherwise, an icon appears.</span></span>

1.  <span data-ttu-id="cd74d-121">Получите интерфейс [**иричедитоле**](/windows/desktop/api/Richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="cd74d-121">Get the [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) interface.</span></span>

    ```
    BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
    {
        HRESULT hr;

        LPRICHEDITOLE pRichEditOle;
        SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);
        
        ...
    ```

    

2.  <span data-ttu-id="cd74d-122">Создайте структурированное хранилище.</span><span class="sxs-lookup"><span data-stu-id="cd74d-122">Create structured storage.</span></span>

    ```
        LPLOCKBYTES pLockBytes = NULL;
        hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);
        
        LPSTORAGE pStorage;
        hr = StgCreateDocfileOnILockBytes(pLockBytes, 
                                          STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
                                          0, &pStorage);
        ...
    ```

    

3.  <span data-ttu-id="cd74d-123">Настройте формат данных.</span><span class="sxs-lookup"><span data-stu-id="cd74d-123">Set up the data format.</span></span>

    ```
        FORMATETC formatEtc;
        
        formatEtc.cfFormat = 0;
        formatEtc.ptd      = NULL;
        formatEtc.dwAspect = DVASPECT_CONTENT;
        formatEtc.lindex   = -1;
        formatEtc.tymed    = TYMED_NULL;
        
        ...
    ```

    

4.  <span data-ttu-id="cd74d-124">Получение указателя на сайт для просмотра.</span><span class="sxs-lookup"><span data-stu-id="cd74d-124">Get a pointer to the display site.</span></span>

    ```
        LPOLECLIENTSITE pClientSite;
        hr = pRichEditOle->GetClientSite(&pClientSite);
        
        ...
    ```

    

5.  <span data-ttu-id="cd74d-125">Создайте объект и извлеките его интерфейс **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="cd74d-125">Create the object and retrieve its **IUnknown** interface.</span></span>

    ```
        LPUNKNOWN pUnk;
        CLSID clsid = CLSID_NULL;
        
        hr = OleCreateFromFile(clsid, 
                               pszFileName, 
                               IID_IUnknown, 
                               OLERENDER_DRAW, 
                               &formatEtc, 
                               pClientSite, 
                               pStorage, 
                               (void**)&pUnk);
        
        pClientSite->Release();
                  
        ...
    ```

    

6.  <span data-ttu-id="cd74d-126">Получите интерфейс Иолеобжект для объекта.</span><span class="sxs-lookup"><span data-stu-id="cd74d-126">Get the IOleObject interface to the object.</span></span>

    ```
        LPOLEOBJECT pObject;
        
        hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
        
        pUnk->Release();

        ...
    ```

    

7.  <span data-ttu-id="cd74d-127">Чтобы обеспечить правильную инвентаризацию ссылок, уведомите объект, который он содержит.</span><span class="sxs-lookup"><span data-stu-id="cd74d-127">To ensure that references are counted correctly, notify the object that it is contained.</span></span>

    ```
        OleSetContainedObject(pObject, TRUE);

        ...
    ```

    

8.  <span data-ttu-id="cd74d-128">Настройка сведений об объекте.</span><span class="sxs-lookup"><span data-stu-id="cd74d-128">Set up object info.</span></span>

    ```
        REOBJECT reobject = { sizeof(REOBJECT)};
        
        hr = pObject->GetUserClassID(&clsid);
        
        reobject.clsid    = clsid;
        reobject.cp       = REO_CP_SELECTION;
        reobject.dvaspect = DVASPECT_CONTENT;
        reobject.dwFlags  = REO_RESIZABLE | REO_BELOWBASELINE;
        reobject.dwUser   = 0;
        reobject.poleobj  = pObject;
        reobject.polesite = pClientSite;
        reobject.pstg     = pStorage;
        
        SIZEL sizel       = { 0 };
        reobject.sizel    = sizel;

        ...
    ```

    

9.  <span data-ttu-id="cd74d-129">Переместить курсор в конец текста и добавить символ возврата каретки.</span><span class="sxs-lookup"><span data-stu-id="cd74d-129">Move the caret to the end of the text and add a carriage return.</span></span>

    ```
        SendMessage(hRichEdit, EM_SETSEL, 0, -1);
        
        DWORD dwStart, dwEnd;
        
        SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
        SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
        SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

        ...
    ```

    

10. <span data-ttu-id="cd74d-130">Вставьте объект.</span><span class="sxs-lookup"><span data-stu-id="cd74d-130">Insert the object.</span></span>

    ```
        hr = pRichEditOle->InsertObject(&reobject);

        ...
    ```

    

11. <span data-ttu-id="cd74d-131">Очистка.</span><span class="sxs-lookup"><span data-stu-id="cd74d-131">Clean up.</span></span>

    ```
        pObject->Release();
        
        pRichEditOle->Release();

        return TRUE;
        
    }
    ```

    

### <a name="using-iricheditolecallback"></a><span data-ttu-id="cd74d-132">Использование Иричедитолекаллбакк</span><span class="sxs-lookup"><span data-stu-id="cd74d-132">Using IRichEditOleCallback</span></span>

<span data-ttu-id="cd74d-133">Приложения реализуют интерфейс [**иричедитолекаллбакк**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) для реагирования на запросы, связанные с OLE, или действия, выполняемые элементом управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="cd74d-133">Applications implement the [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) interface to respond to OLE-related queries or actions that are performed by a rich edit control.</span></span> <span data-ttu-id="cd74d-134">Вы связываете реализацию интерфейса с элементом управления, отправляя сообщение [**EM \_ сетолекаллбакк**](em-setolecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="cd74d-134">You associate your implementation of the interface with the control by sending an [**EM\_SETOLECALLBACK**](em-setolecallback.md) message.</span></span> <span data-ttu-id="cd74d-135">Затем элемент управления вызывает методы в вашей реализации интерфейса, если это уместно.</span><span class="sxs-lookup"><span data-stu-id="cd74d-135">The control then calls methods on your implementation of the interface as appropriate.</span></span>

<span data-ttu-id="cd74d-136">Например, [**куерякцептдата**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) вызывается, когда пользователь пытается перетащить или вставить объект в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="cd74d-136">For example, [**QueryAcceptData**](/windows/desktop/api/Richole/nf-richole-iricheditolecallback-queryacceptdata) is called when the user attempts to drag or paste an object into the control.</span></span> <span data-ttu-id="cd74d-137">Если приложение может принимать данные, реализация метода возвращает значение S \_ ОК. в противном случае возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="cd74d-137">If your application can accept the data, your implementation of the method returns S\_OK; otherwise, it returns an error code.</span></span> <span data-ttu-id="cd74d-138">Метод также может выполнить некоторое другое действие, например предупреждение о том, что файлы этого типа не могут быть помещены в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="cd74d-138">The method might also take some other action, such as warning the user that files of that type cannot be placed in the control.</span></span>

## <a name="complete-insertobject-example-function"></a><span data-ttu-id="cd74d-139">Пример функции Complete Инсертобжект</span><span class="sxs-lookup"><span data-stu-id="cd74d-139">Complete InsertObject Example Function</span></span>

<span data-ttu-id="cd74d-140">В следующем примере кода показаны предыдущие фрагменты кода, Объединенные в одну полную функцию, которая включает в себя обработку ошибок.</span><span class="sxs-lookup"><span data-stu-id="cd74d-140">The following code example demonstrates the previous code snippets combined into one complete function that includes error handling.</span></span>


```C++
BOOL InsertObject(HWND hRichEdit, LPCTSTR pszFileName)
{
    HRESULT hr;

    LPRICHEDITOLE pRichEditOle;
    SendMessage(hRichEdit, EM_GETOLEINTERFACE, 0, (LPARAM)&pRichEditOle);

    if (pRichEditOle == NULL)
    {
        return FALSE;
    }

    LPLOCKBYTES pLockBytes = NULL;
    hr = CreateILockBytesOnHGlobal(NULL, TRUE, &pLockBytes);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPSTORAGE pStorage;
    hr = StgCreateDocfileOnILockBytes(pLockBytes, 
           STGM_SHARE_EXCLUSIVE | STGM_CREATE | STGM_READWRITE, 
           0, &pStorage);

    if (FAILED(hr))
    {
        return FALSE;
    }

    FORMATETC formatEtc;
    formatEtc.cfFormat = 0;
    formatEtc.ptd = NULL;
    formatEtc.dwAspect = DVASPECT_CONTENT;
    formatEtc.lindex = -1;
    formatEtc.tymed = TYMED_NULL;

    LPOLECLIENTSITE pClientSite;
    hr = pRichEditOle->GetClientSite(&pClientSite);

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPUNKNOWN pUnk;
    CLSID clsid = CLSID_NULL;

    hr = OleCreateFromFile(clsid, pszFileName, IID_IUnknown, OLERENDER_DRAW, 
           &formatEtc, pClientSite, pStorage, (void**)&pUnk);

    pClientSite->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    LPOLEOBJECT pObject;
    hr = pUnk->QueryInterface(IID_IOleObject, (void**)&pObject);
    pUnk->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }

    OleSetContainedObject(pObject, TRUE);
    REOBJECT reobject = { sizeof(REOBJECT)};
    hr = pObject->GetUserClassID(&clsid);

    if (FAILED(hr))
    {
        pObject->Release();
        return FALSE;
    }

    reobject.clsid = clsid;
    reobject.cp = REO_CP_SELECTION;
    reobject.dvaspect = DVASPECT_CONTENT;
    reobject.dwFlags = REO_RESIZABLE | REO_BELOWBASELINE;
    reobject.dwUser = 0;
    reobject.poleobj = pObject;
    reobject.polesite = pClientSite;
    reobject.pstg = pStorage;
    SIZEL sizel = { 0 };
    reobject.sizel = sizel;

    SendMessage(hRichEdit, EM_SETSEL, 0, -1);
    DWORD dwStart, dwEnd;
    SendMessage(hRichEdit, EM_GETSEL, (WPARAM)&dwStart, (LPARAM)&dwEnd);
    SendMessage(hRichEdit, EM_SETSEL, dwEnd+1, dwEnd+1);
    SendMessage(hRichEdit, EM_REPLACESEL, TRUE, (WPARAM)L"\n"); 

    hr = pRichEditOle->InsertObject(&reobject);
    pObject->Release();
    pRichEditOle->Release();

    if (FAILED(hr))
    {
        return FALSE;
    }
    
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="cd74d-141">См. также</span><span class="sxs-lookup"><span data-stu-id="cd74d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd74d-142">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="cd74d-142">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="cd74d-143">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="cd74d-143">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




