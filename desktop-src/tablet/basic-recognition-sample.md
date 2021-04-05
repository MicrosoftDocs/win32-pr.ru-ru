---
description: Это приложение демонстрирует создание простого приложения для распознавания рукописного текста. Эта программа создает объект InkCollector для рукописного ввода, позволяя использовать окно и объект контекста распознавателя по умолчанию.
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: Пример базового распознавания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19679a6d1642a94ed813ba0428654b6e03009ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912356"
---
# <a name="basic-recognition-sample"></a><span data-ttu-id="3654f-103">Пример базового распознавания</span><span class="sxs-lookup"><span data-stu-id="3654f-103">Basic Recognition Sample</span></span>

<span data-ttu-id="3654f-104">Это приложение демонстрирует создание простого приложения для распознавания *рукописного текста* .</span><span class="sxs-lookup"><span data-stu-id="3654f-104">This application demonstrates how you can build a simple *handwriting* recognition application.</span></span>

<span data-ttu-id="3654f-105">Эта программа создает объект [**InkCollector**](inkcollector-class.md) для *рукописного ввода*, позволяя использовать окно и объект *контекста распознавателя* по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3654f-105">This program creates an [**InkCollector**](inkcollector-class.md) object to *ink*-enable the window and a default *recognizer context* object.</span></span> <span data-ttu-id="3654f-106">При получении «Recognize!»</span><span class="sxs-lookup"><span data-stu-id="3654f-106">Upon receiving the "Recognize!"</span></span> <span data-ttu-id="3654f-107">команда, запускаемая из меню приложения, собранные рукописные штрихи передаются в контекст распознавателя.</span><span class="sxs-lookup"><span data-stu-id="3654f-107">command, fired from the application's menu, the collected ink strokes are passed to the recognizer context.</span></span> <span data-ttu-id="3654f-108">Лучшая итоговая строка представлена в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="3654f-108">The best result string is presented in a message box.</span></span>

## <a name="creating-the-recognizercontext-object"></a><span data-ttu-id="3654f-109">Создание объекта Рекогнизерконтекст</span><span class="sxs-lookup"><span data-stu-id="3654f-109">Creating the RecognizerContext Object</span></span>

<span data-ttu-id="3654f-110">В процедуре WndProc приложения при \_ получении сообщения WM Create при запуске создается новый контекст распознавателя, использующий распознаватель по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3654f-110">In the WndProc procedure for the application, when the WM\_CREATE message is received on startup, a new recognizer context that uses the default recognizer is created.</span></span> <span data-ttu-id="3654f-111">Этот контекст используется для всех средств распознавания в приложении.</span><span class="sxs-lookup"><span data-stu-id="3654f-111">This context is used for all recognition in the application.</span></span>


```C++
case WM_CREATE:
{
    HRESULT hr;
    hr = CoCreateInstance(CLSID_InkRecognizerContext,
             NULL, CLSCTX_INPROC_SERVER, IID_IInkRecognizerContext,
             (void **) &g_pIInkRecoContext);
    if (FAILED(hr))
    {
        ::MessageBox(NULL, TEXT("There are no handwriting recognizers installed.\n"
            "You need to have at least one in order to run this sample.\nExiting."),
            gc_szAppName, MB_ICONERROR);
        return -1;
    }
  //...
```



## <a name="recognizing-the-strokes"></a><span data-ttu-id="3654f-112">Распознавание штрихов</span><span class="sxs-lookup"><span data-stu-id="3654f-112">Recognizing the Strokes</span></span>

<span data-ttu-id="3654f-113">Команда Recognize получается, когда пользователь щелкает Recognize!</span><span class="sxs-lookup"><span data-stu-id="3654f-113">The recognize command is received when the user clicks the Recognize!</span></span> <span data-ttu-id="3654f-114">.</span><span class="sxs-lookup"><span data-stu-id="3654f-114">menu item.</span></span> <span data-ttu-id="3654f-115">Код получает указатель на рукописный [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (пиинкстрокес) из объекта [**инкдисп**](inkdisp-class.md) , а затем передает **инкстрокес** в контекст распознавателя, используя вызов путреф \_ штрихов.</span><span class="sxs-lookup"><span data-stu-id="3654f-115">The code gets a pointer to the ink [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) off of the [**InkDisp**](inkdisp-class.md) object, and then passes the **InkStrokes** to the recognizer context using a call to putref\_Strokes.</span></span>


```C++
 case WM_COMMAND:
  //...
  else if (wParam == ID_RECOGNIZE)
  {
      // change cursor to the system's Hourglass
      HCURSOR hCursor = ::SetCursor(::LoadCursor(NULL, IDC_WAIT));
      // Get a pointer to the ink stroke collection
      // This collection is a snapshot of the entire ink object
      IInkStrokes* pIInkStrokes = NULL;
      HRESULT hr = g_pIInkDisp->get_Strokes(&pIInkStrokes);
      if (SUCCEEDED(hr)) 
      {
          // Pass the stroke collection to the recognizer context
          hr = g_pIInkRecoContext->putref_Strokes(pIInkStrokes);
          if (SUCCEEDED(hr)) 
          {
```



<span data-ttu-id="3654f-116">Затем код вызывает метод [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) объекта [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) , передавая указатель на объект [**иинкрекогнитионресулт**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) для хранения результатов.</span><span class="sxs-lookup"><span data-stu-id="3654f-116">The code then calls the [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object, passing in a pointer to an [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object to hold the results.</span></span>


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



<span data-ttu-id="3654f-117">Наконец, в коде используется свойство [**топстринг**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) объекта [**иинкрекогнитионресулт**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) , получающее верхний результат распознавания в строковую переменную, освобождает объект **иинкрекогнитионресулт** и отображает строку в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="3654f-117">Finally, the code uses the [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object's [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) property retrieve the top recognition result into a string variable, releases the **IInkRecognitionResult** object, and displays the string in a message box.</span></span>


```C++
                  // Get the best result of the recognition 
                  BSTR bstrBestResult = NULL;
                  hr = pIInkRecoResult->get_TopString(&bstrBestResult);
                  pIInkRecoResult->Release();
                  pIInkRecoResult = NULL;

                  // Show the result string
                  if (SUCCEEDED(hr) && bstrBestResult)
                  {
                      MessageBoxW(hwnd, bstrBestResult, 
                                  L"Recognition Results", MB_OK);
                      SysFreeString(bstrBestResult);
                  }  }
        
```



<span data-ttu-id="3654f-118">Не забудьте сбросить контекст распознавателя между использованием.</span><span class="sxs-lookup"><span data-stu-id="3654f-118">Be sure to reset the recognizer context between usages.</span></span>


```
              // Reset the recognizer context
              g_pIInkRecoContext->putref_Strokes(NULL);
          }
          pIInkStrokes->Release();
      }
      // restore the cursor
      ::SetCursor(hCursor);
  }
```



 

 
