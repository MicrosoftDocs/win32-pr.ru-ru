---
description: В этом примере демонстрируются расширенные возможности программного интерфейса программирования (API) Микрософттаблет PC Automation, используемого для распознавания рукописного текста.
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: Пример использования нескольких распознавателей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a21d24001e3544be16dde4d288a8adc7ea0081f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656654"
---
# <a name="multiple-recognizers-sample"></a><span data-ttu-id="d7ca4-103">Пример использования нескольких распознавателей</span><span class="sxs-lookup"><span data-stu-id="d7ca4-103">Multiple Recognizers Sample</span></span>

<span data-ttu-id="d7ca4-104">В этом примере демонстрируются расширенные возможности программного интерфейса программирования (API) Микрософттаблет PC Automation, используемого для распознавания *рукописного текста* .</span><span class="sxs-lookup"><span data-stu-id="d7ca4-104">This sample demonstrates advanced features of the MicrosoftTablet PC Automation application programming interface (API) used for *handwriting* recognition.</span></span>

<span data-ttu-id="d7ca4-105">Он включает в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="d7ca4-105">It includes the following:</span></span>

-   <span data-ttu-id="d7ca4-106">Перечисление установленных распознавателей</span><span class="sxs-lookup"><span data-stu-id="d7ca4-106">Enumerating the installed recognizers</span></span>
-   <span data-ttu-id="d7ca4-107">Создание *контекста распознавателя* с помощью распознавателя определенного языка</span><span class="sxs-lookup"><span data-stu-id="d7ca4-107">Creating a *recognizer context* with a specific language recognizer</span></span>
-   <span data-ttu-id="d7ca4-108">Сериализация результатов распознавания с помощью коллекции штрихов</span><span class="sxs-lookup"><span data-stu-id="d7ca4-108">Serializing recognition results with a stroke collection</span></span>
-   <span data-ttu-id="d7ca4-109">Упорядочение коллекций штрихов в пользовательскую коллекцию в объекте [**инкдисп**](inkdisp-class.md)</span><span class="sxs-lookup"><span data-stu-id="d7ca4-109">Organizing stroke collections into a custom collection within the [**InkDisp**](inkdisp-class.md) object</span></span>
-   <span data-ttu-id="d7ca4-110">Сериализация объектов *рукописного ввода* и их извлечение из файла *сериализованного формата (ISF)*</span><span class="sxs-lookup"><span data-stu-id="d7ca4-110">Serializing *ink* objects to and retrieving them from an *ink serialized format (ISF)* file</span></span>
-   <span data-ttu-id="d7ca4-111">Настройка входных руководств распознавателя</span><span class="sxs-lookup"><span data-stu-id="d7ca4-111">Setting recognizer input guides</span></span>
-   <span data-ttu-id="d7ca4-112">Использование синхронного и асинхронного распознавания</span><span class="sxs-lookup"><span data-stu-id="d7ca4-112">Using synchronous and asynchronous recognition</span></span>

## <a name="ink-headers"></a><span data-ttu-id="d7ca4-113">Заголовки рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="d7ca4-113">Ink Headers</span></span>

<span data-ttu-id="d7ca4-114">Сначала включите заголовки для интерфейсов автоматизации планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-114">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="d7ca4-115">Они устанавливаются вместе с пакетом средств разработки программного обеспечения (SDK) Microsoft Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-115">These are installed with the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="d7ca4-116">В файле Евентсинкс. h определяются интерфейсы Иинкевентсимпл и Иинкрекогнитионевентсимпл.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-116">The EventSinks.h file defines the IInkEventsImpl and IInkRecognitionEventsImpl interfaces.</span></span>


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a><span data-ttu-id="d7ca4-117">Перечисление установленных распознавателей</span><span class="sxs-lookup"><span data-stu-id="d7ca4-117">Enumerating the Installed Recognizers</span></span>

<span data-ttu-id="d7ca4-118">Метод Лоадмену приложения заполняет меню создать новые штрихи доступными распознавателями.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-118">The application's LoadMenu method populates the Create New Strokes menu with the available recognizers.</span></span> <span data-ttu-id="d7ca4-119">Создается [**инкрекогнизерс**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d7ca4-119">An [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) is created.</span></span> <span data-ttu-id="d7ca4-120">Если свойство [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) объекта **инкрекогнизерс** не пусто, то распознаватель является *распознавательм текста*, а значение его свойства [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) добавляется в меню.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-120">If the [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) property of an **InkRecognizers** object is not empty, then the recognizer is a *text recognizer*, and the value of its [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) property is added to the menu.</span></span>


```C++
// Create the enumerator for the installed recognizers
hr = m_spIInkRecognizers.CoCreateInstance(CLSID_InkRecognizers);
...
    // Filter out non-language recognizers by checking for
    // the languages supported by the recognizer - there is not
    // any if it is a gesture or object recognizer.
    CComVariant vLanguages;
    if (SUCCEEDED(spIInkRecognizer->get_Languages(&vLanguages)))
    {
        if ((VT_ARRAY == (VT_ARRAY & vLanguages.vt))           // it should be an array
            && (NULL != vLanguages.parray)
            && (0 < vLanguages.parray->rgsabound[0].cElements)) // with at least one element
        {
            // This is a language recognizer. Add its name to the menu.
            CComBSTR bstrName;
            if (SUCCEEDED(spIInkRecognizer->get_Name(&bstrName)))
                ...
        }
    }
```



## <a name="creating-an-ink-collector"></a><span data-ttu-id="d7ca4-121">Создание сборщика рукописных данных</span><span class="sxs-lookup"><span data-stu-id="d7ca4-121">Creating an Ink Collector</span></span>

<span data-ttu-id="d7ca4-122">Метод onCreate приложения создает объект [**InkCollector**](inkcollector-class.md) , подключает его к источнику события и включает сбор рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-122">The application's OnCreate method creates an [**InkCollector**](inkcollector-class.md) object, connects it to its event source, and enables ink collection.</span></span>


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a><span data-ttu-id="d7ca4-123">Создание контекста распознавателя</span><span class="sxs-lookup"><span data-stu-id="d7ca4-123">Creating a Recognizer Context</span></span>

<span data-ttu-id="d7ca4-124">Метод Креатерекоконтекст приложения создает и инициализирует новый контекст распознавателя и настраивает направляющие, поддерживаемые соответствующим языком.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-124">The application's CreateRecoContext method creates and initializes a new recognizer context, and sets up the guides supported by the associated language.</span></span> <span data-ttu-id="d7ca4-125">Метод [**креатерекогнизерконтекст**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) объекта [**Иинкрекогнизер**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) создает объект [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) для языка.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-125">The [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object's [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) method creates a [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) object for the language.</span></span> <span data-ttu-id="d7ca4-126">При необходимости заменяется старый контекст распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-126">If necessary, the old recognizer context is replaced.</span></span> <span data-ttu-id="d7ca4-127">Контекст подключен к источнику события.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-127">The context is connected to its event source.</span></span> <span data-ttu-id="d7ca4-128">Наконец, проверяется свойство [**capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) контекста распознавателя, для которого поддерживается контекст распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-128">Finally, the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the recognizer context is checked for which guides the recognizer context supports.</span></span>


```C++
// Create a recognizer context
CComPtr<IInkRecognizerContext2> spNewContext;
if (FAILED(pIInkRecognizer2->CreateRecognizerContext(&spNewContext)))
    return false;

// Replace the current context with the new one
if (m_spIInkRecoContext != NULL)
{
    // Close the connection to the recognition events source
    IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventUnadvise(m_spIInkRecoContext);
}
m_spIInkRecoContext.Attach(spNewContext.Detach());

// Establish a connection with the recognizer context's event source
if (FAILED(IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkRecoContext)))
    ...

// Set the guide if it's supported by the recognizer and has been created 
int cRows = 0, cColumns = 0;
InkRecognizerCapabilities dwCapabilities = IRC_DontCare;
if (SUCCEEDED(pIInkRecognizer->get_Capabilities(&dwCapabilities)))
    ...
```



## <a name="collecting-strokes-and-displaying-recognition-results"></a><span data-ttu-id="d7ca4-129">Сбор штрихов и отображение результатов распознавания</span><span class="sxs-lookup"><span data-stu-id="d7ca4-129">Collecting Strokes and Displaying Recognition Results</span></span>

<span data-ttu-id="d7ca4-130">Метод onstroke приложения обновляет [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) сборщика рукописных данных, отменяет существующие асинхронные запросы на распознавание и создает запрос на распознавание в контексте распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-130">The application's OnStroke method updates the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) of the ink collector, cancels existing asynchronous recognition requests, and creates a recognition request on the recognizer context.</span></span>


```C++
// Add the new stroke to the current collection
hr = m_spIInkStrokes->Add(pIInkStroke);

if (SUCCEEDED(hr))
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();

    // Ask the context to update the recognition results with newly added strokes
    // When the results are ready, the recognizer context returns them
    // through the corresponding event RecognitionWithAlternates
    CComVariant vCustomData;
    m_spIInkRecoContext->BackgroundRecognize(vCustomData);
}
```



<span data-ttu-id="d7ca4-131">`OnRecognition`Метод приложения отправляет результаты запроса на распознавание в метод окна вывода `UpdateString` .</span><span class="sxs-lookup"><span data-stu-id="d7ca4-131">The application's `OnRecognition` method sends the results of the recognition request to the output window's `UpdateString` method.</span></span>


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a><span data-ttu-id="d7ca4-132">Удаление обводок и результатов распознавания</span><span class="sxs-lookup"><span data-stu-id="d7ca4-132">Deleting Strokes and Recognition Results</span></span>

<span data-ttu-id="d7ca4-133">Метод OnClear приложения удаляет все росчерки и результаты распознавания из объекта [**инкдисп**](inkdisp-class.md) и очищает окна.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-133">The application's OnClear method deletes all strokes and recognition results from the [**InkDisp**](inkdisp-class.md) object and clears the windows.</span></span> <span data-ttu-id="d7ca4-134">Связь контекста распознавателя с коллекцией [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) удаляется.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-134">The recognizer context's association with its [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is removed.</span></span>


```C++
// Detach the current stroke collection from the recognizer context and release it
if (m_spIInkRecoContext != NULL)
    m_spIInkRecoContext->putref_Strokes(NULL);

m_spIInkStrokes.Release();

// Clear the custom strokes collection
if (m_spIInkCustomStrokes != NULL)
    m_spIInkCustomStrokes->Clear();

// Delete all strokes from the Ink object
// Passing NULL as a stroke collection pointer means asking to delete all strokes
m_spIInkDisp->DeleteStrokes(NULL);

// Get a new stroke collection from the ink object
...
// Ask for an empty collection by passing an empty variant 
if (SUCCEEDED(m_spIInkDisp->CreateStrokes(v, &m_spIInkStrokes)))
{
    // Attach it to the recognizer context
    if (FAILED(m_spIInkRecoContext->putref_Strokes(m_spIInkStrokes)))
        ...
}
```



## <a name="changing-recognizer-contexts"></a><span data-ttu-id="d7ca4-135">Изменение контекстов распознавателя</span><span class="sxs-lookup"><span data-stu-id="d7ca4-135">Changing Recognizer Contexts</span></span>

<span data-ttu-id="d7ca4-136">Метод Онневстрокес приложения вызывается, когда пользователь выбирает распознаватель в меню создать новые штрихи.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-136">The application's OnNewStrokes method is called when the user selects a recognizer in the Create New Strokes menu.</span></span> <span data-ttu-id="d7ca4-137">Текущий [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) сохраняется.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-137">The current [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) is saved.</span></span> <span data-ttu-id="d7ca4-138">Если выбран другой распознаватель языка, создается новый контекст распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-138">If a different language recognizer was selected, a new recognizer context is created.</span></span> <span data-ttu-id="d7ca4-139">Затем новый **инкстрокес** прикрепляется к новому контексту распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-139">Then, a new **InkStrokes** is attached to the new recognizer context.</span></span>


```C++
// Save the current stroke collection if there is any
if (m_spIInkRecoContext != NULL)
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();
    
    // Let the context know that there'll be no more input 
    // for the attached stroke collection
    m_spIInkRecoContext->EndInkInput();

    // Add the stroke collection to the Ink object's CustomStrokes collection
    SaveStrokeCollection();
}
...
// If a different recognizer was selected, create a new recognizer context
// Else, reuse the same recognizer context
if (wID != m_nCmdRecognizer)
{
    // Get a pointer to the recognizer object from the recognizer collection  
    CComPtr<IInkRecognizer> spIInkRecognizer;
    if ((m_spIInkRecognizers == NULL)
        || FAILED(m_spIInkRecognizers->Item(wID - ID_RECOGNIZER_FIRST,
                                             &spIInkRecognizer))
        || (false == CreateRecoContext(spIInkRecognizer)))
    {
        // restore the cursor
        ::SetCursor(hCursor);
        return 0;
    }

    // Update the status bar
    m_bstrCurRecoName.Empty();
    spIInkRecognizer->get_Name(&m_bstrCurRecoName);
    UpdateStatusBar();

    // Store the selected recognizer's command id
    m_nCmdRecognizer = wID;
}
```



<span data-ttu-id="d7ca4-140">Затем он вызывает Стартневстрокеколлектион, который создает пустой [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) и прикрепляет его к контексту распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-140">It then calls StartNewStrokeCollection, which creates an empty [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) and attaches it to the recognizer context.</span></span>

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a><span data-ttu-id="d7ca4-141">Сохранение коллекции штрихов для контекста распознавателя</span><span class="sxs-lookup"><span data-stu-id="d7ca4-141">Saving the Strokes Collection for a Recognizer Context</span></span>

<span data-ttu-id="d7ca4-142">`SaveStrokeCollection`Метод приложения проверяет наличие существующего контекста распознавателя и завершает распознавание текущей коллекции штрихов.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-142">The application's `SaveStrokeCollection` method checks for an existing recognizer context, and finalizes the recognition of the current strokes collection.</span></span> <span data-ttu-id="d7ca4-143">Затем Коллекция [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) добавляется в [**кустомстрокес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) объекта рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="d7ca4-143">Then the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is added to the [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) of the ink object.</span></span>


```C++
if (m_spIInkRecoContext != NULL)
{
    if (SUCCEEDED(m_spIInkStrokes->get_Count(&lCount)) && 0 != lCount)
    {
        CComPtr<IInkRecognitionResult> spIInkRecoResult;
        InkRecognitionStatus RecognitionStatus;
        if (SUCCEEDED(m_spIInkRecoContext->Recognize(&RecognitionStatus, &spIInkRecoResult)))
        {
            if (SUCCEEDED(spIInkRecoResult->SetResultOnStrokes()))
            {
                CComBSTR bstr;
                spIInkRecoResult->get_TopString(&bstr);
                m_wndResults.UpdateString(bstr);
            }
            ...
        }
    }
    // Detach the stroke collection from the old recognizer context
    m_spIInkRecoContext->putref_Strokes(NULL);
}

// Now add it to the ink's custom strokes collection
// Each item (stroke collection) of the custom strokes must be identified
// by a unique string. Here we generate a GUID for this.
if ((0 != lCount) && (m_spIInkCustomStrokes != NULL))
{
    GUID guid;
    WCHAR szGuid[40]; // format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"
    if (SUCCEEDED(::CoCreateGuid(&guid)) 
        && (::StringFromGUID2(guid, szGuid, countof(szGuid)) != 0))
    {
        CComBSTR bstrGuid(szGuid);
        if (FAILED(m_spIInkCustomStrokes->Add(bstrGuid, m_spIInkStrokes)))
            ...
```



 

 
