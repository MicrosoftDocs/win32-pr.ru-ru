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
# <a name="multiple-recognizers-sample"></a>Пример использования нескольких распознавателей

В этом примере демонстрируются расширенные возможности программного интерфейса программирования (API) Микрософттаблет PC Automation, используемого для распознавания *рукописного текста* .

Он включает в себя следующее:

-   Перечисление установленных распознавателей
-   Создание *контекста распознавателя* с помощью распознавателя определенного языка
-   Сериализация результатов распознавания с помощью коллекции штрихов
-   Упорядочение коллекций штрихов в пользовательскую коллекцию в объекте [**инкдисп**](inkdisp-class.md)
-   Сериализация объектов *рукописного ввода* и их извлечение из файла *сериализованного формата (ISF)*
-   Настройка входных руководств распознавателя
-   Использование синхронного и асинхронного распознавания

## <a name="ink-headers"></a>Заголовки рукописного ввода

Сначала включите заголовки для интерфейсов автоматизации планшетных ПК. Они устанавливаются вместе с пакетом средств разработки программного обеспечения (SDK) Microsoft Windows XP Tablet PC Edition.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



В файле Евентсинкс. h определяются интерфейсы Иинкевентсимпл и Иинкрекогнитионевентсимпл.


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a>Перечисление установленных распознавателей

Метод Лоадмену приложения заполняет меню создать новые штрихи доступными распознавателями. Создается [**инкрекогнизерс**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) . Если свойство [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) объекта **инкрекогнизерс** не пусто, то распознаватель является *распознавательм текста*, а значение его свойства [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) добавляется в меню.


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



## <a name="creating-an-ink-collector"></a>Создание сборщика рукописных данных

Метод onCreate приложения создает объект [**InkCollector**](inkcollector-class.md) , подключает его к источнику события и включает сбор рукописных данных.


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a>Создание контекста распознавателя

Метод Креатерекоконтекст приложения создает и инициализирует новый контекст распознавателя и настраивает направляющие, поддерживаемые соответствующим языком. Метод [**креатерекогнизерконтекст**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) объекта [**Иинкрекогнизер**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) создает объект [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) для языка. При необходимости заменяется старый контекст распознавателя. Контекст подключен к источнику события. Наконец, проверяется свойство [**capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) контекста распознавателя, для которого поддерживается контекст распознавателя.


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



## <a name="collecting-strokes-and-displaying-recognition-results"></a>Сбор штрихов и отображение результатов распознавания

Метод onstroke приложения обновляет [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) сборщика рукописных данных, отменяет существующие асинхронные запросы на распознавание и создает запрос на распознавание в контексте распознавателя.


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



`OnRecognition`Метод приложения отправляет результаты запроса на распознавание в метод окна вывода `UpdateString` .


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a>Удаление обводок и результатов распознавания

Метод OnClear приложения удаляет все росчерки и результаты распознавания из объекта [**инкдисп**](inkdisp-class.md) и очищает окна. Связь контекста распознавателя с коллекцией [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) удаляется.


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



## <a name="changing-recognizer-contexts"></a>Изменение контекстов распознавателя

Метод Онневстрокес приложения вызывается, когда пользователь выбирает распознаватель в меню создать новые штрихи. Текущий [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) сохраняется. Если выбран другой распознаватель языка, создается новый контекст распознавателя. Затем новый **инкстрокес** прикрепляется к новому контексту распознавателя.


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



Затем он вызывает Стартневстрокеколлектион, который создает пустой [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) и прикрепляет его к контексту распознавателя.

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a>Сохранение коллекции штрихов для контекста распознавателя

`SaveStrokeCollection`Метод приложения проверяет наличие существующего контекста распознавателя и завершает распознавание текущей коллекции штрихов. Затем Коллекция [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) добавляется в [**кустомстрокес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) объекта рукописного ввода.


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



 

 
