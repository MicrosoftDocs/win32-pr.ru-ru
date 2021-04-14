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
# <a name="using-the-com-library"></a><span data-ttu-id="74ba7-103">Использование библиотеки COM</span><span class="sxs-lookup"><span data-stu-id="74ba7-103">Using the COM Library</span></span>

<span data-ttu-id="74ba7-104">Справочник по управляемой библиотеке Tablet PC теперь можно найти в разделе Справочник по библиотеке классов Windows Vista SDK.</span><span class="sxs-lookup"><span data-stu-id="74ba7-104">The Tablet PC managed library reference can now be found in the regular Windows Vista SDK Class Library reference section.</span></span> <span data-ttu-id="74ba7-105">Он предоставляет объектную модель для Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="74ba7-105">It provides an object model for Microsoft Visual C++.</span></span> <span data-ttu-id="74ba7-106">Большинство объектов в библиотеке COM идентичны тем, которые находятся в управляемом API-интерфейсе Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="74ba7-106">The majority of the objects in the COM Library are identical to those found in the Tablet PC Managed API.</span></span>

<span data-ttu-id="74ba7-107">Однако API COM содержит некоторые элементы в дополнение к тем, которые находятся в управляемом API, из-за различий между стандартной средой Microsoft Win32 и средой Microsoft .NET Фрамеворксофтваре Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="74ba7-107">However, the COM API contains some members in addition to those found in the Managed API because of differences between the standard Microsoft Win32 environment and the Microsoft .NET Frameworksoftware development kit (SDK) environment.</span></span> <span data-ttu-id="74ba7-108">Например, объекты Инкректангле и Инктрансформ используются в COM, но Фрамеворксдк предоставляет собственную реализацию для [**класса инкректангле**](inkrectangle-class.md) и [**класса инктрансформ**](inktransform-class.md) , которая устраняет необходимость в работе этих объектов в управляемом API платформы Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="74ba7-108">For example, the InkRectangle and InkTransform objects are used in COM, but the FrameworkSDK provides native implementation for [**InkRectangle Class**](inkrectangle-class.md) and [**InkTransform Class**](inktransform-class.md) that eliminates the need for these objects in the Tablet PC platform Managed API.</span></span>

> [!Note]  
> <span data-ttu-id="74ba7-109">Объекты в API COM и элементы управления рукописным вводом не предназначены для использования в Active Server страницах (ASP).</span><span class="sxs-lookup"><span data-stu-id="74ba7-109">The objects in the COM API and the ink controls are not designed for use in Active Server Pages (ASP).</span></span>

 

## <a name="working-with-collections"></a><span data-ttu-id="74ba7-110">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="74ba7-110">Working with Collections</span></span>

<span data-ttu-id="74ba7-111">Если в качестве индекса для любого из объектов коллекции в библиотеке COM передать значение **null** , то будет получен первый элемент в коллекции, так как значения этих аргументов приводятся к 0 при вызове метода.</span><span class="sxs-lookup"><span data-stu-id="74ba7-111">If you pass in a **NULL** value as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

<span data-ttu-id="74ba7-112">Свойство **\_ NewEnum** помечено как ограниченное в определении языка определения интерфейса (IDL) для интерфейсов коллекции.</span><span class="sxs-lookup"><span data-stu-id="74ba7-112">The **\_NewEnum** property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces.</span></span>

<span data-ttu-id="74ba7-113">В C++ используйте `For...` цикл для прохода по коллекции, сначала получив длину коллекции.</span><span class="sxs-lookup"><span data-stu-id="74ba7-113">In C++, use a `For...` loop to iterate through a collection by first obtaining the collection's length.</span></span> <span data-ttu-id="74ba7-114">В приведенном ниже примере показано, как выполнить итерацию по штрихам объекта [**инкдисп**](inkdisp-class.md) `pInk` .</span><span class="sxs-lookup"><span data-stu-id="74ba7-114">The example below shows how to iterate through the strokes of an [**InkDisp**](inkdisp-class.md) object, `pInk`.</span></span>


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



## <a name="parameters"></a><span data-ttu-id="74ba7-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="74ba7-115">Parameters</span></span>

<span data-ttu-id="74ba7-116">Если вы передаете VT \_ Empty или VT \_ null в качестве индекса для любого из объектов коллекции в библиотеке COM, вы получаете первый элемент в коллекции, так как значения этих аргументов приводятся к 0 при вызове метода.</span><span class="sxs-lookup"><span data-stu-id="74ba7-116">If you pass in VT\_EMPTY or VT\_NULL as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

## <a name="using-idispatch"></a><span data-ttu-id="74ba7-117">Использование IDispatch</span><span class="sxs-lookup"><span data-stu-id="74ba7-117">Using IDispatch</span></span>

<span data-ttu-id="74ba7-118">Для повышения производительности программный интерфейс COM (API) платформы Tablet PC не поддерживает вызов `IDispatchImpl::Invoke` со структурой DISPPARAMS с именованными аргументами.</span><span class="sxs-lookup"><span data-stu-id="74ba7-118">To increase performance, the Tablet PC Platform COM application programming interface (API) does not support calling `IDispatchImpl::Invoke` with a DISPPARAMS structure with named arguments.</span></span> <span data-ttu-id="74ba7-119">`IDispatchImpl::GetIDsOfNames`Также не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="74ba7-119">The `IDispatchImpl::GetIDsOfNames` is also not supported.</span></span> <span data-ttu-id="74ba7-120">Вместо этого вызывайте `Invoke` с идентификаторами DISPID, переданными в заголовках пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="74ba7-120">Instead, call `Invoke` with the DISPIDs supplied in the SDK headers.</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="74ba7-121">Ожидание событий</span><span class="sxs-lookup"><span data-stu-id="74ba7-121">Waiting for Events</span></span>

<span data-ttu-id="74ba7-122">Среда планшетного ПК является многопоточной.</span><span class="sxs-lookup"><span data-stu-id="74ba7-122">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="74ba7-123">Дополнительные сведения о многопоточности см. в документации по COM.</span><span class="sxs-lookup"><span data-stu-id="74ba7-123">Refer to COM documentation for multi-threading.</span></span>

## <a name="support-for-aggregation"></a><span data-ttu-id="74ba7-124">Поддержка агрегирования</span><span class="sxs-lookup"><span data-stu-id="74ba7-124">Support for Aggregation</span></span>

<span data-ttu-id="74ba7-125">Статистическая обработка была протестирована только для элемента управления [InkEdit](inkedit-control-reference.md) , элемента управления [InkPicture](inkpicture-control-reference.md) , объекта [**инкдисп**](inkdisp-class.md) и объекта [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="74ba7-125">Aggregation has been tested for only the [InkEdit](inkedit-control-reference.md) control, the [InkPicture](inkpicture-control-reference.md) control, the [**InkDisp**](inkdisp-class.md) object, and the [**InkOverlay**](inkoverlay-class.md) object.</span></span> <span data-ttu-id="74ba7-126">Статистическая обработка не была протестирована для других элементов управления и объектов в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="74ba7-126">Aggregation has not been tested for other controls and objects in the library.</span></span>

## <a name="c"></a><span data-ttu-id="74ba7-127">C++</span><span class="sxs-lookup"><span data-stu-id="74ba7-127">C++</span></span>

<span data-ttu-id="74ba7-128">Использование пакета SDK для планшетных ПК в C++ требует использования некоторых концепций COM, таких как VARIANT, SAFEARRAY и BSTR.</span><span class="sxs-lookup"><span data-stu-id="74ba7-128">Using the Tablet PC SDK in C++ requires the use of some COM concepts, such as VARIANT, SAFEARRAY, and BSTR.</span></span> <span data-ttu-id="74ba7-129">В этом разделе описывается, как использовать их.</span><span class="sxs-lookup"><span data-stu-id="74ba7-129">This section describes how to use them.</span></span>

### <a name="variant-and-safearray"></a><span data-ttu-id="74ba7-130">VARIANT и SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="74ba7-130">VARIANT and SAFEARRAY</span></span>

<span data-ttu-id="74ba7-131">Структура VARIANT используется для обмена данными между COM-объектами.</span><span class="sxs-lookup"><span data-stu-id="74ba7-131">The VARIANT structure is used for communication between COM objects.</span></span> <span data-ttu-id="74ba7-132">По сути, структура VARIANT — это контейнер для большого объединения, который содержит много типов данных.</span><span class="sxs-lookup"><span data-stu-id="74ba7-132">Essentially, the VARIANT structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="74ba7-133">Значение в первом члене структуры, VT, описывает, какое из членов Union является допустимым.</span><span class="sxs-lookup"><span data-stu-id="74ba7-133">The value in the first member of the structure, vt, describes which of the union members is valid.</span></span> <span data-ttu-id="74ba7-134">При получении сведений в структуре варианта проверьте элемент VT, чтобы узнать, какой элемент содержит допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="74ba7-134">When you receive information in a VARIANT structure, check the vt member to find out which member contains valid data.</span></span> <span data-ttu-id="74ba7-135">Аналогично, при отправке данных с использованием структуры VARIANT всегда задавайте VT для отражения члена объединения, содержащего эти сведения.</span><span class="sxs-lookup"><span data-stu-id="74ba7-135">Similarly, when you send information using a VARIANT structure, always set vt to reflect the union member that contains the information.</span></span>

<span data-ttu-id="74ba7-136">Перед использованием структуры инициализируйте ее, вызвав функцию COM Вариантинит.</span><span class="sxs-lookup"><span data-stu-id="74ba7-136">Before using the structure, initialize it by calling the VariantInit COM function.</span></span> <span data-ttu-id="74ba7-137">После завершения работы со структурой очистите ее, прежде чем память, содержащая вариант, освобождается путем вызова Вариантклеар.</span><span class="sxs-lookup"><span data-stu-id="74ba7-137">When finished with the structure, clear it before the memory that contains the VARIANT is freed by calling VariantClear.</span></span>

<span data-ttu-id="74ba7-138">Дополнительные сведения о структуре вариантов см. в разделе [типы данных Variant и VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="74ba7-138">For more information on the VARIANT structure, see [VARIANT and VARIANTARG Data Types](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="74ba7-139">Структура SAFEARRAY предоставляется как способ безопасной работы с массивами в COM.</span><span class="sxs-lookup"><span data-stu-id="74ba7-139">The SAFEARRAY structure is provided as a way to safely work with arrays in COM.</span></span> <span data-ttu-id="74ba7-140">Поле паррай варианта является указателем на SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="74ba7-140">The VARIANT's parray field is a pointer to a SAFEARRAY.</span></span> <span data-ttu-id="74ba7-141">Используйте такие функции, как Сафеаррайкреатевектор, Сафеаррайакцессдата и Сафеаррайунакцессдата, чтобы создать и заполнить SAFEARRAY в ВАРИАНТе.</span><span class="sxs-lookup"><span data-stu-id="74ba7-141">Use functions such as SafeArrayCreateVector, SafeArrayAccessData, and SafeArrayUnaccessData to create and fill a SAFEARRAY in a VARIANT.</span></span>

<span data-ttu-id="74ba7-142">Дополнительные сведения о типе данных SAFEARRAY см. в разделе [тип данных SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="74ba7-142">For more information on the SAFEARRAY data type, see [SafeArray Data Type](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

<span data-ttu-id="74ba7-143">Этот пример C++ создает [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp` в объекте [**инкдисп**](inkdisp-class.md) , `pInk` из массива данных Point.</span><span class="sxs-lookup"><span data-stu-id="74ba7-143">This C++ example creates an [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp`, in an [**InkDisp**](inkdisp-class.md) object, `pInk`, from an array of point data.</span></span>


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



### <a name="bstr"></a><span data-ttu-id="74ba7-144">BSTR</span><span class="sxs-lookup"><span data-stu-id="74ba7-144">BSTR</span></span>

<span data-ttu-id="74ba7-145">Поддерживаемый формат строки для COM — BSTR.</span><span class="sxs-lookup"><span data-stu-id="74ba7-145">The supported string format for COM is BSTR.</span></span> <span data-ttu-id="74ba7-146">BSTR имеет указатель на строку, завершающуюся нулем, но также содержит длину строки (в байтах, не считая Терминатор), которая хранится в 4 байтах непосредственно перед первым символом строки.</span><span class="sxs-lookup"><span data-stu-id="74ba7-146">A BSTR has a pointer to a zero-terminated string, but it also contains the length of the string (in bytes, not counting the terminator), which is stored in the 4 bytes immediately preceding the first character of the string.</span></span>

<span data-ttu-id="74ba7-147">Дополнительные сведения о BSTR см. в разделе [тип данных BSTR](/previous-versions/windows/desktop/automat/bstr).</span><span class="sxs-lookup"><span data-stu-id="74ba7-147">For more information on BSTR, see [BSTR Data Type](/previous-versions/windows/desktop/automat/bstr).</span></span>

<span data-ttu-id="74ba7-148">В этом примере C++ показано, как задать фактоид для [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) с помощью BSTR.</span><span class="sxs-lookup"><span data-stu-id="74ba7-148">This C++ sample shows how to set the factoid on an [**InkRecognizerContext**](inkrecognizercontext-class.md) using a BSTR.</span></span>


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



 

 
