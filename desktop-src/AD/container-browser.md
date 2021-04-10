---
title: Обозреватель контейнеров
description: Приложение может использовать функцию Дсбровсефорконтаинер для вывода диалогового окна, которое можно использовать для просмотра контейнеров в службе домен Active Directory.
ms.assetid: aa88d565-ff25-4082-964a-9a230d2607f2
ms.tgt_platform: multiple
keywords:
- Active Directory в браузере контейнеров
- контейнеры Active Directory, браузер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964c67873cc7936a75e2b9c1cdf331d0fa1fdae1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069804"
---
# <a name="container-browser"></a><span data-ttu-id="16e7e-105">Обозреватель контейнеров</span><span class="sxs-lookup"><span data-stu-id="16e7e-105">Container Browser</span></span>

<span data-ttu-id="16e7e-106">Приложение может использовать функцию [**дсбровсефорконтаинер**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) для вывода диалогового окна, которое можно использовать для просмотра контейнеров в службе домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="16e7e-106">An application can use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to display a dialog box that can be used to browse through the containers in an Active Directory Domain Service.</span></span> <span data-ttu-id="16e7e-107">Диалоговое окно отображает контейнеры в формате дерева и позволяет пользователю перемещаться по дереву с помощью клавиатуры и мыши.</span><span class="sxs-lookup"><span data-stu-id="16e7e-107">The dialog box displays the containers in a tree format and enables the user to navigate through the tree using the keyboard and mouse.</span></span> <span data-ttu-id="16e7e-108">Когда пользователь выбирает элемент в диалоговом окне, предоставляется путь к контейнеру, выбранному пользователем.</span><span class="sxs-lookup"><span data-stu-id="16e7e-108">When the user selects an item in the dialog box, the ADsPath of the container selected by the user is provided.</span></span>

<span data-ttu-id="16e7e-109">[**Дсбровсефорконтаинер**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) принимает указатель на структуру [**дсбровсеинфо**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) , содержащую данные о диалоговом окне, и возвращает путь к выбранному элементу.</span><span class="sxs-lookup"><span data-stu-id="16e7e-109">[**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) takes a pointer to a [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure that contains data about the dialog box and returns the ADsPath of the selected item.</span></span>

<span data-ttu-id="16e7e-110">Элемент **псзрут** является указателем на строку в Юникоде, содержащую корневой контейнер дерева.</span><span class="sxs-lookup"><span data-stu-id="16e7e-110">The **pszRoot** member is a pointer to a Unicode string that contains the root container of the tree.</span></span> <span data-ttu-id="16e7e-111">Если **псзрут** имеет **значение NULL**, дерево будет содержать все дерево.</span><span class="sxs-lookup"><span data-stu-id="16e7e-111">If **pszRoot** is **NULL**, the tree will contain the entire tree.</span></span>

<span data-ttu-id="16e7e-112">Элемент **псзпас** получает путь к выбранному объекту.</span><span class="sxs-lookup"><span data-stu-id="16e7e-112">The **pszPath** member receives the ADsPath of the selected object.</span></span> <span data-ttu-id="16e7e-113">Можно указать конкретный контейнер, который должен быть видимым и выбранным при первом отображении диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="16e7e-113">It is possible to specify a particular container to be visible and selected when the dialog box is first displayed.</span></span> <span data-ttu-id="16e7e-114">Это достигается путем установки для **псзпас** значения ADsPath для выбранного элемента и установки флага **\_ експандонопен ДСБИ** в **dwFlags**.</span><span class="sxs-lookup"><span data-stu-id="16e7e-114">This is accomplished by setting **pszPath** to the ADsPath of the item to be selected and setting the **DSBI\_EXPANDONOPEN** flag in **dwFlags**.</span></span>

<span data-ttu-id="16e7e-115">Содержимое и поведение диалогового окна также можно контролировать во время выполнения путем реализации функции [**бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="16e7e-115">The contents and behavior of the dialog box can also be controlled at runtime by implementing a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="16e7e-116">Функция **бффкаллбакк** реализуется приложением и вызывается при возникновении определенных событий.</span><span class="sxs-lookup"><span data-stu-id="16e7e-116">The **BFFCallBack** function is implemented by the application and is called when certain events occur.</span></span> <span data-ttu-id="16e7e-117">Приложение может использовать эти события для управления отображением элементов диалогового окна, а также фактическим содержимым диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="16e7e-117">An application can use these events to control how the items in the dialog box are displayed as well as the actual contents of the dialog box.</span></span> <span data-ttu-id="16e7e-118">Например, приложение может отфильтровать элементы, отображаемые в диалоговом окне, путем реализации функции **бффкаллбакк** , которая может управлять уведомлением **\_ куеринсерт ДСБМ** .</span><span class="sxs-lookup"><span data-stu-id="16e7e-118">For example, an application can filter the items displayed in the dialog box by implementing a **BFFCallBack** function that can handle the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="16e7e-119">При получении уведомления **ДСБМ \_ куеринсерт** используйте элемент **псзадспас** структуры [**дсбитем**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) , чтобы определить, какой элемент будет вставлен.</span><span class="sxs-lookup"><span data-stu-id="16e7e-119">When a **DSBM\_QUERYINSERT** notification is received, use the **pszADsPath** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure to determine which item is about to be inserted.</span></span> <span data-ttu-id="16e7e-120">Если приложение определяет, что элемент не должен отображаться, он может скрыть элемент, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="16e7e-120">If the application determines that the item should not be displayed, it can hide the item by performing the following steps.</span></span>

1.  <span data-ttu-id="16e7e-121">Добавьте флаг **\_ состояния дсбф** в элемент **двмаск** структуры [**дсбитем**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="16e7e-121">Add the **DSBF\_STATE** flag to the **dwMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
2.  <span data-ttu-id="16e7e-122">Добавьте флаг **дсбс \_ Hidden** в элемент **двстатемаск** структуры [**дсбитем**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="16e7e-122">Add the **DSBS\_HIDDEN** flag to the **dwStateMask** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
3.  <span data-ttu-id="16e7e-123">Добавьте флаг **дсбс \_ Hidden** в элемент **двстате** структуры [**дсбитем**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) .</span><span class="sxs-lookup"><span data-stu-id="16e7e-123">Add the **DSBS\_HIDDEN** flag to the **dwState** member of the [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema) structure.</span></span>
4.  <span data-ttu-id="16e7e-124">Возврат ненулевого значения из функции [**бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="16e7e-124">Return a nonzero value from the [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span>

<span data-ttu-id="16e7e-125">В дополнение к скрытию определенных элементов приложение может изменить текст и значок, отображаемые для элемента, обрабатывая уведомление **ДСБМ \_ куеринсерт** .</span><span class="sxs-lookup"><span data-stu-id="16e7e-125">In addition to hiding certain items, an application can modify the text and icon displayed for the item by handling the **DSBM\_QUERYINSERT** notification.</span></span> <span data-ttu-id="16e7e-126">Дополнительные сведения см. в разделе [**дсбитем**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span><span class="sxs-lookup"><span data-stu-id="16e7e-126">For more information, see [**DSBITEM**](/windows/desktop/api/Dsclient/ns-dsclient-dsbitema).</span></span>

<span data-ttu-id="16e7e-127">Функция [**бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) может использовать **\_ инициализированное уведомление бффм** для получения маркера диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="16e7e-127">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function can use the **BFFM\_INITIALIZED** notification to obtain the handle of the dialog box.</span></span> <span data-ttu-id="16e7e-128">Приложение может использовать этот обработчик для отправки сообщений, например **бффм \_ енаблеок**, в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="16e7e-128">The application can use this handle to send messages, such as **BFFM\_ENABLEOK**, to the dialog box.</span></span> <span data-ttu-id="16e7e-129">Дополнительные сведения о сообщениях, которые могут быть отправлены в диалоговое окно, см. в разделе [**бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span><span class="sxs-lookup"><span data-stu-id="16e7e-129">For more information about the messages that can be sent to the dialog box, see [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback).</span></span>

<span data-ttu-id="16e7e-130">Чтобы получить прямой доступ к элементам управления в диалоговом окне, можно также использовать обработчик диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="16e7e-130">The dialog box handle can also be used to gain direct access to the controls in the dialog box.</span></span> <span data-ttu-id="16e7e-131">**Дсбид \_ БАННЕР** — это идентификатор элемента управления "статический текст", в котором отображается элемент **Псзтитле** структуры [**дсбровсеинфо**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) .</span><span class="sxs-lookup"><span data-stu-id="16e7e-131">**DSBID\_BANNER** is the identifier for the static text control that the **pszTitle** member of the [**DSBROWSEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dsbrowseinfoa) structure is displayed in.</span></span> <span data-ttu-id="16e7e-132">**Дсбид \_ КОНТАИНЕРЛИСТ** — это идентификатор элемента управления иерархического представления, используемого для отображения содержимого дерева.</span><span class="sxs-lookup"><span data-stu-id="16e7e-132">**DSBID\_CONTAINERLIST** is the identifier of the tree view control used to display the tree contents.</span></span> <span data-ttu-id="16e7e-133">По возможности следует избегать использования этих элементов, чтобы предотвратить будущие проблемы совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="16e7e-133">Use of these items should be avoided, if possible, to prevent future application compatibility problems.</span></span>

<span data-ttu-id="16e7e-134">В следующем примере кода C++ показано, как использовать функцию [**дсбровсефорконтаинер**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) для создания диалогового окна "Обозреватель контейнеров" и реализации функции [**бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) .</span><span class="sxs-lookup"><span data-stu-id="16e7e-134">The following C++ code example shows how to use the [**DsBrowseForContainer**](/windows/desktop/api/Dsclient/nf-dsclient-dsbrowseforcontainera) function to create the container browser dialog box and implement a [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) function.</span></span> <span data-ttu-id="16e7e-135">[**Бффкаллбакк**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) использует уведомление **\_ куеринсерт ДСБМ** , чтобы изменить отображаемое имя каждого элемента на различающееся имя элемента.</span><span class="sxs-lookup"><span data-stu-id="16e7e-135">The [**BFFCallBack**](/windows/win32/api/shlobj_core/nc-shlobj_core-bffcallback) uses the **DSBM\_QUERYINSERT** notification to change the display name for each item to the distinguished name of the item.</span></span>


```C++
#include <shlobj.h>
#include <dsclient.h>
#include <atlbase.h>

/**********

    WideCharToLocal()
   
***********/

int WideCharToLocal(LPTSTR pLocal, LPWSTR pWide, DWORD dwChars)
{
    *pLocal = NULL;
    size_t nWideLength = 0;
    wchar_t *pwszSubstring;

    nWideLength = wcslen(pWide);

#ifdef UNICODE
    if(nWideLength < dwChars)
    {
        wcsncpy_s(pLocal, pWide, dwChars);
    }
    else
    {
        wcsncpy_s(pLocal, pWide, dwChars-1);
        pLocal[dwChars-1] = NULL;
    }
#else
    if(nWideLength < dwChars)
    {
        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pWide, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);
    }
    else
    {
        pwszSubstring = new WCHAR[dwChars];
        wcsncpy_s(pwszSubstring,pWide,dwChars-1);
        pwszSubstring[dwChars-1] = NULL;

        WideCharToMultiByte(    CP_ACP, 
                                0, 
                                pwszSubstring, 
                                -1, 
                                pLocal, 
                                dwChars, 
                                NULL, 
                                NULL);

    delete [] pwszSubstring;
    }
#endif

    return lstrlen(pLocal);
}

/**********

    BrowseCallback()

***********/

int CALLBACK BrowseCallback(HWND hWnd, 
                            UINT uMsg, 
                            LPARAM lParam, 
                            LPARAM lpData)
{
    switch(uMsg)
    {
    case DSBM_QUERYINSERT:
        {
            BOOL fReturn = FALSE;
            DSBITEM *pItem = (DSBITEM*)lParam;

            /*
            If this is to the root item, get the distinguished name 
            for the object and set the display name to the 
            distinguished name.
            */
            if(!(pItem->dwState & DSBS_ROOT))
            {
                HRESULT hr;
                IADs    *pads;

                hr = ADsGetObject(pItem->pszADsPath , 
                    IID_IADs, (LPVOID*)&pads);
                if(SUCCEEDED(hr))
                {
                    VARIANT var;

                    VariantInit(&var);
                    hr = pads->Get(CComBSTR("distinguishedName"), 
                        &var);
                    if(SUCCEEDED(hr))
                    {
                        if(VT_BSTR == var.vt)
                        {
                            WideCharToLocal(pItem->szDisplayName, 
                                var.bstrVal, 
                                DSB_MAX_DISPLAYNAME_CHARS);
                            pItem->dwMask |= DSBF_DISPLAYNAME;
                            fReturn = TRUE;
                        }
                        
                        VariantClear(&var);
                    }
                    
                    pads->Release();
                }
            }

            return fReturn;
        }

        break;
    }
    
    return FALSE;
}

/***********

    BrowseForContainer()

************/

HRESULT BrowseForContainer(HWND hwndParent, 
    LPOLESTR *ppContainerADsPath)
{
    HRESULT hr = E_FAIL;
    DSBROWSEINFO dsbi;
    OLECHAR wszPath[MAX_PATH * 2];
    DWORD result;
 
    if(!ppContainerADsPath)
    {
        return E_INVALIDARG;
    }
 
    ZeroMemory(&dsbi, sizeof(dsbi));
    dsbi.hwndOwner = hwndParent;
    dsbi.cbStruct = sizeof (DSBROWSEINFO);
    dsbi.pszCaption = TEXT("Browse for a Container");
    dsbi.pszTitle = TEXT("Select an Active Directory container.");
    dsbi.pszRoot = NULL;
    dsbi.pszPath = wszPath;
    dsbi.cchPath = sizeof(wszPath)/sizeof(OLECHAR);
    dsbi.dwFlags = DSBI_INCLUDEHIDDEN |
                    DSBI_IGNORETREATASLEAF|
                    DSBI_RETURN_FORMAT;
    dsbi.pfnCallback = BrowseCallback;
    dsbi.lParam = 0;
    dsbi.dwReturnFormat = ADS_FORMAT_X500;
 
    // Display the browse dialog box.
    // Returns -1, 0, IDOK, or IDCANCEL.
    result = DsBrowseForContainer(&dsbi); 
    if(IDOK == result)
    {
        // Allocate memory for the string.
        *ppContainerADsPath = (OLECHAR*)CoTaskMemAlloc(
            sizeof(OLECHAR)*(wcslen(wszPath) + 1));
        if(*ppContainerADsPath)
        {
            wcscpy_s(*ppContainerADsPath, wszPath);
            // Caller must free using CoTaskMemFree. 
            hr = S_OK;
        }
        else
        {
            hr = E_FAIL;
        }
    }
    else
    {
        hr = E_FAIL;
    }
 
    return hr;
}
```



 

 