---
description: Это приложение демонстрирует создание простого приложения для распознавания рукописного текста. Эта программа создает объект InkCollector для рукописного ввода, позволяя использовать окно и объект контекста распознавателя по умолчанию.
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: Пример базового распознавания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf45aa7695866e1cf413ea42b7c377b07ea84984ecf2cc3f44da93ff868072d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111144"
---
# <a name="basic-recognition-sample"></a>Пример базового распознавания

Это приложение демонстрирует создание простого приложения для распознавания *рукописного текста* .

Эта программа создает объект [**InkCollector**](inkcollector-class.md) для *рукописного ввода*, позволяя использовать окно и объект *контекста распознавателя* по умолчанию. При получении «Recognize!» команда, запускаемая из меню приложения, собранные рукописные штрихи передаются в контекст распознавателя. Лучшая итоговая строка представлена в окне сообщения.

## <a name="creating-the-recognizercontext-object"></a>Создание объекта Рекогнизерконтекст

В процедуре WndProc приложения при \_ получении сообщения WM Create при запуске создается новый контекст распознавателя, использующий распознаватель по умолчанию. Этот контекст используется для всех средств распознавания в приложении.


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



## <a name="recognizing-the-strokes"></a>Распознавание штрихов

Команда Recognize получается, когда пользователь щелкает Recognize! . Код получает указатель на рукописный [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (пиинкстрокес) из объекта [**инкдисп**](inkdisp-class.md) , а затем передает **инкстрокес** в контекст распознавателя, используя вызов путреф \_ штрихов.


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



Затем код вызывает метод [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) объекта [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) , передавая указатель на объект [**иинкрекогнитионресулт**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) для хранения результатов.


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



Наконец, в коде используется свойство [**топстринг**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) объекта [**иинкрекогнитионресулт**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) , получающее верхний результат распознавания в строковую переменную, освобождает объект **иинкрекогнитионресулт** и отображает строку в окне сообщения.


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



Не забудьте сбросить контекст распознавателя между использованием.


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



 

 
