---
description: Настройка параметров чередования
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Настройка параметров чередования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805206"
---
# <a name="setting-deinterlace-preferences"></a>Настройка параметров чередования

Устройство микширования видео (VMR) поддерживает дечередование с аппаратным ускорением, что улучшает качество отображения для чередования видео. Конкретные доступные функции зависят от базового оборудования. Приложение может запрашивать возможности дечередования оборудования и задавать параметры разбора с помощью интерфейса [**ивмрдеинтерлацеконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) или [**IVMRDEINTERLACECONTROL9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) Interface (VMR-9). Дечередование выполняется отдельно для каждого потока.

Существует одно важное различие в поведении чередования между VMR-7 и VMR-9. В системах, где графическое оборудование не поддерживает расширенное чередование, фильтр VMR-7 может вернуться к наложение оборудования и поручить его использовать для дечередования в стиле Боба. В этом случае, несмотря на то, что VMR сообщает о 30fps, на самом деле видео отображается в 60 отражения в секунду.

За исключением VMR-7 с использованием наложения оборудования, это происходит с помощью микшера VMR. Для выполнения дечередования микшер использует ускорение видео DirectX (ДКСВА) с помощью интерфейса драйвера устройства (DDI). Эта DDI не может быть вызвана приложениями, и приложения не могут заменить функцию разчередования VMR. Однако приложение может выбрать нужный режим разчередования, как описано в этом разделе.

> [!Note]  
> В этом разделе описываются методы **IVMRDeinterlaceControl9** , но версии VMR-7 практически идентичны.

 

Чтобы получить возможность разчередования видео для видеопотока, выполните следующие действия.

1.  Заполните структуру [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) с описанием видеопотока. Подробные сведения о том, как заполнять эту структуру, приведены далее.
2.  Передайте структуру в метод [**IVMRDeinterlaceControl9:: жетнумберофдеинтерлацемодес**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) . Вызовите метод дважды. Первый вызов возвращает число режимов с чередованием, поддерживаемое оборудованием, для указанного формата. Выделите массив GUID этого размера и снова вызовите метод, передав адрес массива. Второй вызов заполняет массив идентификаторами GUID. Каждый идентификатор GUID определяет один режим разчередования.
3.  Чтобы получить возможности в определенном режиме, вызовите метод [**IVMRDeinterlaceControl9:: жетдеинтерлацемодекапс**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) . Передайте ту же структуру **VMR9VideoDesc** вместе с одним из идентификаторов GUID из массива. Метод заполняет структуру [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) с помощью возможностей режима.

В следующем коде показаны следующие шаги.


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



Теперь приложение может задать режим разчередования для потока с помощью следующих методов:

-   Метод [**сетдеинтерлацемоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) задает предпочтительный режим. Используйте GUID \_ null, чтобы отключить дечередование.
-   Метод [**сетдеинтерлацепрефс**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) задает поведение, если запрошенный режим недоступен.
-   Метод [**жетдеинтерлацемоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) Возвращает предпочтительный режим, который был задан.
-   Метод [**жетактуалдеинтерлацемоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) возвращает фактически используемый режим, который может быть резервным режимом, если предпочтительный режим недоступен.

Дополнительные сведения см. на страницах справочника по методам.

**Использование структуры VMR9VideoDesc**

В процедуре, заданной ранее, первым шагом является заполнение структуры **VMR9VideoDesc** с описанием видеопотока. Начните с получения типа мультимедиа потока видео. Это можно сделать, вызвав [**Ипин:: коннектионмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) в закрепление ввода фильтра VMR. Затем проверьте, является ли видеопоток чередованием. Чередование можно выполнять только в форматах [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Если используется формат формата \_ видеоинфо, он должен быть последовательным кадром. Если используется формат формата \_ VideoInfo2, проверьте поле **двинтерлацефлагс** для \_ флага аминтерлаце с чередованием. Наличие этого флага означает, что видео чередуются.

Предположим, что переменная **пбми** является указателем на структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) в блоке format. Задайте следующие значения в структуре **VMR9VideoDesc** :

-   **двсизе**: задайте для этого поля значение `sizeof(VMR9VideoDesc)` .
-   **двсамплевидс**: задайте для этого поля значение `pBMI->biWidth` .
-   **двсамплехеигхт**: задайте для этого поля значение `abs(pBMI->biHeight)` .
-   **Самплеформат**. это поле описывает характеристики развертки типа мультимедиа. Проверьте поле **двинтерлацефлагс** в структуре **VIDEOINFOHEADER2** и установите **самплеформат** равным эквивалентному флагу [**VMR9 \_ самплеформат**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) . Ниже приведен вспомогательная функция для этого.
-   **Инпутсамплефрек**: в этом поле содержится входная частота, которую можно вычислить из поля **Авгтимеперфраме** в структуре **VIDEOINFOHEADER2** . В общем случае установите для **двнумератор** значение 10000000 и задайте для **двденоминатор** значение **авгтимеперфраме**. Однако можно также проверить наличие некоторых известных ставок кадров:

    | Среднее время на кадр | Частота кадров (кадров/с) | Числитель | Подробно |
    |------------------------|------------------|-----------|-------------|
    | 166833                 | 59,94 (NTSC)     | 60 000     | 1001        |
    | 333667                 | 29,97 (NTSC)     | 30 000     | 1001        |
    | 417188                 | 23,97 (NTSC)     | 24 000     | 1001        |
    | 200 000                 | 50,00 (PAL)      | 50        | 1           |
    | 400000                 | 25,00 (PAL)      | 25        | 1           |
    | 416667                 | 24,00 (пленка)     | 24        | 1           |

    

     

-   **Аутпутфрамефрек**: это поле содержит частоту вывода, которую можно вычислить на основе значения **инпутсамплефрек** и характеристик появления входного потока:
    -   Задайте **аутпутфрамефрек. двденоминатор** равным **инпутсамплефрек. двденоминатор**.
    -   Если входное видео находится под чередованием, установите **аутпутфрамефрек. двнумератор** в значение 2 x **инпутсамплефрек. двнумератор**. (После дечередования частота кадров удваивается.) В противном случае установите значение **инпутсамплефрек. двнумератор**.
-   **двфауркк**: задайте для этого поля значение `pBMI->biCompression` .

Следующая вспомогательная функция преобразует \_ Флаги аминтерлаце *X* в значения [**VMR9 \_ самплеформат**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) :


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



