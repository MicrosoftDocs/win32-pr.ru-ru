---
title: Предоставление безоконного редактирования элементов управления с помощью функций окна
description: Функциональные возможности окна включают возможность получения сообщений и владение контекстом устройства для рисования. Элементы управления Rich Edit без оконного редактирования получают эту функцию посредством пары интерфейсов Итекстсервицес и Итекссост.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce987630c21b1e15a2237066b39dd264125a857
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2020
ms.locfileid: "103987291"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a><span data-ttu-id="62906-104">Предоставление безоконного редактирования элементов управления с помощью функций окна</span><span class="sxs-lookup"><span data-stu-id="62906-104">How to Provide Windowless Rich Edit Controls with Window Functionality</span></span>

<span data-ttu-id="62906-105">Функциональные возможности окна включают возможность получения сообщений и владение контекстом устройства для рисования.</span><span class="sxs-lookup"><span data-stu-id="62906-105">Window functionality includes the ability to receive messages and the ownership of a device context into which to draw.</span></span> <span data-ttu-id="62906-106">Элементы управления Rich Edit без оконного редактирования получают эту функцию посредством пары интерфейсов: [**итекстсервицес**](/windows/desktop/api/Textserv/nl-textserv-itextservices) и [**итекссост**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="62906-106">Windowless rich edit controls receive this functionality by way of a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="62906-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="62906-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="62906-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="62906-108">Technologies</span></span>

-   [<span data-ttu-id="62906-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="62906-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="62906-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="62906-110">Prerequisites</span></span>

-   <span data-ttu-id="62906-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="62906-111">C/C++</span></span>
-   <span data-ttu-id="62906-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="62906-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="62906-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="62906-113">Instructions</span></span>

### <a name="establish-the-window-functionality"></a><span data-ttu-id="62906-114">Установить функциональные возможности окна</span><span class="sxs-lookup"><span data-stu-id="62906-114">Establish the Window Functionality</span></span>

<span data-ttu-id="62906-115">В следующем примере кода показано, как создать текстовый узел и текстовые службы.</span><span class="sxs-lookup"><span data-stu-id="62906-115">The following example code demonstrates how to create the text host and text services.</span></span>


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a><span data-ttu-id="62906-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62906-116">Remarks</span></span>

<span data-ttu-id="62906-117">Параметр *хмодричедит* в примере кода является обработчиком для модуля Msftedit.dll, и предполагается, что этот обработчик уже был извлечен вызовом функции **Ошибка GetModuleHandle** .</span><span class="sxs-lookup"><span data-stu-id="62906-117">The *hmodRichEdit* parameter in the code example is a handle to the Msftedit.dll module, and it is assumed that this handle has already been retrieved by a call to the **GetModuleHandle** function.</span></span>

## <a name="complete-example"></a><span data-ttu-id="62906-118">Полный пример</span><span class="sxs-lookup"><span data-stu-id="62906-118">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="62906-119">См. также</span><span class="sxs-lookup"><span data-stu-id="62906-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62906-120">Использование безоконных элементов управления "поле ввода"</span><span class="sxs-lookup"><span data-stu-id="62906-120">Using Windowless Rich Edit Controls</span></span>](using-windowless-rich-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="62906-121">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="62906-121">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="62906-122">[Демонстрация стандартных элементов управления Windows (Кппвиндовскоммонконтролс)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="62906-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




