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
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a>Настройка стандартной, профессиональной или без потерь звука в кодировке

Когда кодировщик Windows Media Audio перечисляет типы вывода, он определяет каждый перечислимый тип как стандартный, профессиональный или без потерь. Вы можете определить, является ли тип выходных данных стандартным, профессиональным или без потерь, выполнив следующие действия.

1.  Вызовите метод [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , чтобы получить интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , представляющий тип выходных данных.
2.  Вызовите [**имфмедиатипе::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) an, чтобы получить структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , содержащую сведения о типе выходных данных.
3.  Элемент **пбформат** структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) указывает на структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) , содержащую дополнительные сведения о типе выходных данных. Проверьте элемент **вформаттаг** структуры **вавеформатекс** . Значение 0x161 соответствует стандарту, значение 0x162 — Professional, а значение 0x163 — без потери данных.

Если задать свойства кодировщика Windows Media Audio перед перечислением типов вывода, можно ограничить количество перечислений типов выходных данных. Например, если задать свойства VBR соответствующим образом, можно ограничить перечислимые типы вывода теми, которые находятся в категории без потерь.

## <a name="standard-audio-encoding"></a>Стандартная звуковая кодировка

Чтобы настроить стандартную звуковую кодировку, выполните следующие действия.

1.  Задайте свойства по своему усмотрению в кодировщике.
2.  Перечисление возможных типов вывода.
3.  Проверьте перечислимые типы и выберите один из них с тегом Audio Format (0x161).
4.  Задайте тип вывода для выбранного типа, вызвав [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="professional-audio-encoding"></a>Профессиональная звуковая кодировка

Чтобы настроить профессиональную звуковую кодировку, выполните следующие действия.

1.  Задайте свойства по своему усмотрению в кодировщике.
2.  Перечисление возможных типов вывода.
3.  Проверьте перечислимые типы и выберите один из них с тегом Audio Format (0x162).
4.  Задайте тип вывода для выбранного типа, вызвав [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="lossless-audio-encoding"></a>Кодирование звука без потерь

Для настройки кодирования звука без потерь можно использовать следующие шаги.

1.  Присвойте свойству [**\_ вбренаблед Мфпкэй**](mfpkey-vbrenabledproperty.md) значение **Variant \_ true**.
2.  Задайте для свойства [**мфпкэй \_ ограничение \_ перечисления \_ вбркуалити**](mfpkey-constrain-enumerated-vbrqualityproperty.md) значение **Variant \_ true**.
3.  Задайте для [**свойства \_ требуемое \_ вбркуалити мфпкэй**](mfpkey-desired-vbrqualityproperty.md) значение 100.
4.  Перечисляет типы выходных данных.
5.  Установите тип выходных данных в один из типов, перечисленных на шаге 4, вызвав [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

Следующий код перечисляет все типы выходных данных без потерь для кодировщика Windows Media Audio. Код выводит значение тега audio Format для каждого перечислимого типа. Так как все перечислимые типы без потерь, все эти теги формата имеют значение 0x163. Предположим, что Пимт является указателем на интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) в объекте кодировщика Windows Media Audio и что pStore является указателем на интерфейс **ипропертисторе** в том же объекте. Также предположим, что HR является переменной типа **HRESULT** , которая была объявлена ранее в коде.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка кодирования звука](configuringaudioencoding.md)
</dt> </dl>

 

 
