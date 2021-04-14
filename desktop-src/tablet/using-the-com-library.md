---
description: Общие сведения о библиотеке COM и примечания по использованию технологии планшетных ПК пакета SDK для Windows Vista.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Использование библиотеки COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82671b198114cf45b334e8c4e07146a91964e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343282"
---
# <a name="using-the-com-library"></a>Использование библиотеки COM

Справочник по управляемой библиотеке Tablet PC теперь можно найти в разделе Справочник по библиотеке классов Windows Vista SDK. Он предоставляет объектную модель для Microsoft Visual C++. Большинство объектов в библиотеке COM идентичны тем, которые находятся в управляемом API-интерфейсе Tablet PC.

Однако API COM содержит некоторые элементы в дополнение к тем, которые находятся в управляемом API, из-за различий между стандартной средой Microsoft Win32 и средой Microsoft .NET Фрамеворксофтваре Development Kit (SDK). Например, объекты Инкректангле и Инктрансформ используются в COM, но Фрамеворксдк предоставляет собственную реализацию для [**класса инкректангле**](inkrectangle-class.md) и [**класса инктрансформ**](inktransform-class.md) , которая устраняет необходимость в работе этих объектов в управляемом API платформы Tablet PC.

> [!Note]  
> Объекты в API COM и элементы управления рукописным вводом не предназначены для использования в Active Server страницах (ASP).

 

## <a name="working-with-collections"></a>Работа с коллекциями

Если в качестве индекса для любого из объектов коллекции в библиотеке COM передать значение **null** , то будет получен первый элемент в коллекции, так как значения этих аргументов приводятся к 0 при вызове метода.

Свойство **\_ NewEnum** помечено как ограниченное в определении языка определения интерфейса (IDL) для интерфейсов коллекции.

В C++ используйте `For...` цикл для прохода по коллекции, сначала получив длину коллекции. В приведенном ниже примере показано, как выполнить итерацию по штрихам объекта [**инкдисп**](inkdisp-class.md) `pInk` .


```C++
IInkStrokes* pStrokes;
HRESULT result = pInk->get_Strokes(&pStrokes);
if (SUCCEEDED(result))
{
    // Loop over strokes
    long nStrokes;
    result = pStrokes->get_Count(&nStrokes);
    if (SUCCEEDED(result))
    {
        for (int i =0; i < nStrokes; i++)
        {
            IInkStrokeDisp* pStroke;
            result = pStrokes->Item(i, &pStroke);
            if (SUCCEEDED(result))
            {
              // Code that uses pStroke
              // ...
            }
        }
    }
}
```



## <a name="parameters"></a>Параметры

Если вы передаете VT \_ Empty или VT \_ null в качестве индекса для любого из объектов коллекции в библиотеке COM, вы получаете первый элемент в коллекции, так как значения этих аргументов приводятся к 0 при вызове метода.

## <a name="using-idispatch"></a>Использование IDispatch

Для повышения производительности программный интерфейс COM (API) платформы Tablet PC не поддерживает вызов `IDispatchImpl::Invoke` со структурой DISPPARAMS с именованными аргументами. `IDispatchImpl::GetIDsOfNames`Также не поддерживается. Вместо этого вызывайте `Invoke` с идентификаторами DISPID, переданными в заголовках пакета SDK.

## <a name="waiting-for-events"></a>Ожидание событий

Среда планшетного ПК является многопоточной. Дополнительные сведения о многопоточности см. в документации по COM.

## <a name="support-for-aggregation"></a>Поддержка агрегирования

Статистическая обработка была протестирована только для элемента управления [InkEdit](inkedit-control-reference.md) , элемента управления [InkPicture](inkpicture-control-reference.md) , объекта [**инкдисп**](inkdisp-class.md) и объекта [**InkOverlay**](inkoverlay-class.md) . Статистическая обработка не была протестирована для других элементов управления и объектов в библиотеке.

## <a name="c"></a>C++

Использование пакета SDK для планшетных ПК в C++ требует использования некоторых концепций COM, таких как VARIANT, SAFEARRAY и BSTR. В этом разделе описывается, как использовать их.

### <a name="variant-and-safearray"></a>VARIANT и SAFEARRAY

Структура VARIANT используется для обмена данными между COM-объектами. По сути, структура VARIANT — это контейнер для большого объединения, который содержит много типов данных.

Значение в первом члене структуры, VT, описывает, какое из членов Union является допустимым. При получении сведений в структуре варианта проверьте элемент VT, чтобы узнать, какой элемент содержит допустимые данные. Аналогично, при отправке данных с использованием структуры VARIANT всегда задавайте VT для отражения члена объединения, содержащего эти сведения.

Перед использованием структуры инициализируйте ее, вызвав функцию COM Вариантинит. После завершения работы со структурой очистите ее, прежде чем память, содержащая вариант, освобождается путем вызова Вариантклеар.

Дополнительные сведения о структуре вариантов см. в разделе [типы данных Variant и VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

Структура SAFEARRAY предоставляется как способ безопасной работы с массивами в COM. Поле паррай варианта является указателем на SAFEARRAY. Используйте такие функции, как Сафеаррайкреатевектор, Сафеаррайакцессдата и Сафеаррайунакцессдата, чтобы создать и заполнить SAFEARRAY в ВАРИАНТе.

Дополнительные сведения о типе данных SAFEARRAY см. в разделе [тип данных SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray).

Этот пример C++ создает [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp` в объекте [**инкдисп**](inkdisp-class.md) , `pInk` из массива данных Point.


```C++
VARIANT   var, varPK;
LONG*   plongArray=NULL;
POINT   ptArray[2]={0};
long   lSize=0;
IInkStrokeDisp* pInkStrokeDisp;

IInkDisp*   pInk;   // the object should be created correctly 
                    // elsewhere and assigned here.
HRESULT   hr=E_FAIL;

ptArray[0].x = 20;
ptArray[0].y = 100;
ptArray[1].x = 30;
ptArray[1].y = 110;
lSize = 2;   // two points

VariantInit( &var );
VariantInit( &varPK );
SAFEARRAY* psa = SafeArrayCreateVector( VT_I4, 0, lSize*2 );
if( psa )
{
  if( SUCCEEDED( hr = SafeArrayAccessData( psa, (void**)&plongArray) ))
   {
      for( long i = 0; i < lSize; i++ ) 
      {
         plongArray[2*i] = ptArray[i].x;
         plongArray[2*i+1] = ptArray[i].y;
      }
      hr = SafeArrayUnaccessData( psa );

      if ( SUCCEEDED( hr ) ) 
      {
         var.vt     = VT_ARRAY | VT_I4;
         var.parray = psa;

        // varPK (packet description) is currently reserved, so it is
        // just empty variant for now.
         pInk->CreateStroke( var, varPK, &pInkStrokeDisp );   
      }
   }
}
VariantClear( &var );
VariantClear( &varPK );
```



### <a name="bstr"></a>BSTR

Поддерживаемый формат строки для COM — BSTR. BSTR имеет указатель на строку, завершающуюся нулем, но также содержит длину строки (в байтах, не считая Терминатор), которая хранится в 4 байтах непосредственно перед первым символом строки.

Дополнительные сведения о BSTR см. в разделе [тип данных BSTR](/previous-versions/windows/desktop/automat/bstr).

В этом примере C++ показано, как задать фактоид для [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) с помощью BSTR.


```C++
IInkRecognizerContext* pRecognizerContext = NULL;
result = CoCreateInstance(CLSID_InkRecognizerContext, 
    NULL, CLSCTX_INPROC_SERVER,
    IID_IInkRecognizerContext, 
    (void **) &pRecognizerContext);
if SUCCEEDED(result)
{
    BSTR bstrFactoid = SysAllocString(FACTOID_DATE);
    result = pRecognizerContext->put_Factoid(bstrFactoid);
    if SUCCEEDED(result)
    {
      // Use recognizer context...
      // ...
    }
    SysFreeString(bstrFactoid);
}
```



 

 
