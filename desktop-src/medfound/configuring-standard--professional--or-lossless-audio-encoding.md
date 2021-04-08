---
description: Когда кодировщик Windows Media Audio перечисляет типы вывода, он определяет каждый перечислимый тип как стандартный, профессиональный или без потерь.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Настройка стандартной, профессиональной или без потерь звука в кодировке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e781c2c093b46a12fa4ad5434f97931a948ff9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808152"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a><span data-ttu-id="ab095-103">Настройка стандартной, профессиональной или без потерь звука в кодировке</span><span class="sxs-lookup"><span data-stu-id="ab095-103">Configuring Standard, Professional, or Lossless Audio Encoding</span></span>

<span data-ttu-id="ab095-104">Когда кодировщик Windows Media Audio перечисляет типы вывода, он определяет каждый перечислимый тип как стандартный, профессиональный или без потерь.</span><span class="sxs-lookup"><span data-stu-id="ab095-104">When the Windows Media Audio encoder enumerates output types, it identifies each enumerated type as either Standard, Professional, or Lossless.</span></span> <span data-ttu-id="ab095-105">Вы можете определить, является ли тип выходных данных стандартным, профессиональным или без потерь, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ab095-105">You can determine whether an output type is Standard, Professional, or Lossless by performing the following steps.</span></span>

1.  <span data-ttu-id="ab095-106">Вызовите метод [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , чтобы получить интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , представляющий тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ab095-106">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to obtain an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface that represents the output type.</span></span>
2.  <span data-ttu-id="ab095-107">Вызовите [**имфмедиатипе::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) an, чтобы получить структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , содержащую сведения о типе выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ab095-107">Call [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) to get an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains information about the output type.</span></span>
3.  <span data-ttu-id="ab095-108">Элемент **пбформат** структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) указывает на структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) , содержащую дополнительные сведения о типе выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ab095-108">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure points to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure that contains additional information about the output type.</span></span> <span data-ttu-id="ab095-109">Проверьте элемент **вформаттаг** структуры **вавеформатекс** .</span><span class="sxs-lookup"><span data-stu-id="ab095-109">Inspect the **wFormatTag** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="ab095-110">Значение 0x161 соответствует стандарту, значение 0x162 — Professional, а значение 0x163 — без потери данных.</span><span class="sxs-lookup"><span data-stu-id="ab095-110">A value of 0x161 indicates Standard, a value of 0x162 indicates Professional, and a value of 0x163 indicates Lossless.</span></span>

<span data-ttu-id="ab095-111">Если задать свойства кодировщика Windows Media Audio перед перечислением типов вывода, можно ограничить количество перечислений типов выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ab095-111">If you set properties on the Windows Media Audio encoder before you enumerate output types, you can limit the number of output types that are enumerated.</span></span> <span data-ttu-id="ab095-112">Например, если задать свойства VBR соответствующим образом, можно ограничить перечислимые типы вывода теми, которые находятся в категории без потерь.</span><span class="sxs-lookup"><span data-stu-id="ab095-112">For example, if you set the VBR properties appropriately, you can limit the enumerated output types to those that are in the Lossless category.</span></span>

## <a name="standard-audio-encoding"></a><span data-ttu-id="ab095-113">Стандартная звуковая кодировка</span><span class="sxs-lookup"><span data-stu-id="ab095-113">Standard Audio Encoding</span></span>

<span data-ttu-id="ab095-114">Чтобы настроить стандартную звуковую кодировку, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ab095-114">You can use the following steps to configure Standard audio encoding.</span></span>

1.  <span data-ttu-id="ab095-115">Задайте свойства по своему усмотрению в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="ab095-115">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="ab095-116">Перечисление возможных типов вывода.</span><span class="sxs-lookup"><span data-stu-id="ab095-116">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="ab095-117">Проверьте перечислимые типы и выберите один из них с тегом Audio Format (0x161).</span><span class="sxs-lookup"><span data-stu-id="ab095-117">Inspect the enumerated types and choose one that has an audio format tag of 0x161.</span></span>
4.  <span data-ttu-id="ab095-118">Задайте тип вывода для выбранного типа, вызвав [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="ab095-118">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="professional-audio-encoding"></a><span data-ttu-id="ab095-119">Профессиональная звуковая кодировка</span><span class="sxs-lookup"><span data-stu-id="ab095-119">Professional Audio Encoding</span></span>

<span data-ttu-id="ab095-120">Чтобы настроить профессиональную звуковую кодировку, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ab095-120">You can use the following steps to configure Professional audio encoding.</span></span>

1.  <span data-ttu-id="ab095-121">Задайте свойства по своему усмотрению в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="ab095-121">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="ab095-122">Перечисление возможных типов вывода.</span><span class="sxs-lookup"><span data-stu-id="ab095-122">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="ab095-123">Проверьте перечислимые типы и выберите один из них с тегом Audio Format (0x162).</span><span class="sxs-lookup"><span data-stu-id="ab095-123">Inspect the enumerated types and choose one that has an audio format tag of 0x162.</span></span>
4.  <span data-ttu-id="ab095-124">Задайте тип вывода для выбранного типа, вызвав [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="ab095-124">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="lossless-audio-encoding"></a><span data-ttu-id="ab095-125">Кодирование звука без потерь</span><span class="sxs-lookup"><span data-stu-id="ab095-125">Lossless Audio Encoding</span></span>

<span data-ttu-id="ab095-126">Для настройки кодирования звука без потерь можно использовать следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="ab095-126">You can use the following steps to configure Lossless audio encoding.</span></span>

1.  <span data-ttu-id="ab095-127">Присвойте свойству [**\_ вбренаблед Мфпкэй**](mfpkey-vbrenabledproperty.md) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="ab095-127">Set the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to **VARIANT\_TRUE**.</span></span>
2.  <span data-ttu-id="ab095-128">Задайте для свойства [**мфпкэй \_ ограничение \_ перечисления \_ вбркуалити**](mfpkey-constrain-enumerated-vbrqualityproperty.md) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="ab095-128">Set the [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) property to **VARIANT\_TRUE**.</span></span>
3.  <span data-ttu-id="ab095-129">Задайте для [**свойства \_ требуемое \_ вбркуалити мфпкэй**](mfpkey-desired-vbrqualityproperty.md) значение 100.</span><span class="sxs-lookup"><span data-stu-id="ab095-129">Set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property to 100.</span></span>
4.  <span data-ttu-id="ab095-130">Перечисляет типы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ab095-130">Enumerate output types.</span></span>
5.  <span data-ttu-id="ab095-131">Установите тип выходных данных в один из типов, перечисленных на шаге 4, вызвав [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="ab095-131">Set the output type to one of the types enumerated in step 4 by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="ab095-132">Следующий код перечисляет все типы выходных данных без потерь для кодировщика Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="ab095-132">The following code enumerates all of the lossless output types for the Windows Media Audio encoder.</span></span> <span data-ttu-id="ab095-133">Код выводит значение тега audio Format для каждого перечислимого типа.</span><span class="sxs-lookup"><span data-stu-id="ab095-133">The code prints the value of the audio format tag for each enumerated type.</span></span> <span data-ttu-id="ab095-134">Так как все перечислимые типы без потерь, все эти теги формата имеют значение 0x163.</span><span class="sxs-lookup"><span data-stu-id="ab095-134">Because all of the enumerated types are lossless, all of those format tags have a value of 0x163.</span></span> <span data-ttu-id="ab095-135">Предположим, что Пимт является указателем на интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) в объекте кодировщика Windows Media Audio и что pStore является указателем на интерфейс **ипропертисторе** в том же объекте.</span><span class="sxs-lookup"><span data-stu-id="ab095-135">Assume that pIMT is a pointer to an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a Windows Media Audio encoder object and that pStore is a pointer to an **IPropertyStore** interface on the same object.</span></span> <span data-ttu-id="ab095-136">Также предположим, что HR является переменной типа **HRESULT** , которая была объявлена ранее в коде.</span><span class="sxs-lookup"><span data-stu-id="ab095-136">Also assume that hr is a variable of type **HRESULT** that was declared previously in the code.</span></span>


```
PROPVARIANT prop;
prop.vt = VT_BOOL;
prop.boolVal = VARIANT_TRUE;
hr = pStore->SetValue(MFPKEY_VBRENABLED, prop);

if(SUCCEEDED(hr))
{
   hr = pStore->SetValue(MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY, prop);

   if(SUCCEEDED(hr))
   {
      prop.vt = VT_UI4;
      prop.ulVal = 100;
      hr = pStore->SetValue(MFPKEY_DESIRED_VBRQUALITY, prop);
      
      if(SUCCEEDED(hr))
      {           
         HRESULT hrAvailableType = S_OK;
         LONG j = 0;
         while(MF_E_NO_MORE_TYPES != hrAvailableType)
         {
            IMFMediaType* pOutputType = NULL;     
            hrAvailableType = pIMFT->GetOutputAvailableType(
               0, j, &pOutputType);

            if(SUCCEEDED(hrAvailableType))
            {
               AM_MEDIA_TYPE* pTypeRep = NULL;
               hr = pOutputType->GetRepresentation(
                  AM_MEDIA_TYPE_REPRESENTATION, (VOID**)&pTypeRep); 
                     
               if(SUCCEEDED(hr))
               {
                  WAVEFORMATEX* pwfex = (WAVEFORMATEX*)pTypeRep->pbFormat;
                  printf_s("%x\n", pwfex->wFormatTag);
                  pOutputType->FreeRepresentation(
                     AM_MEDIA_TYPE_REPRESENTATION, (VOID*)pTypeRep);
               }

               pOutputType->Release();
               ++j;
            }                                                                  
         } // while                 
      }                                
   } 
}
```



## <a name="related-topics"></a><span data-ttu-id="ab095-137">См. также</span><span class="sxs-lookup"><span data-stu-id="ab095-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab095-138">Настройка кодирования звука</span><span class="sxs-lookup"><span data-stu-id="ab095-138">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> </dl>

 

 
