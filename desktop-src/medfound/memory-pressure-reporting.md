---
description: Отчеты о нехватке памяти позволяют приложению Direct3D определить, когда рабочий набор видеопамяти стал слишком большим.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Отчеты о нехватке памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dc0df8db30281c6f7225309bdca5edfdbd3759f21a9e61cdc848f534dcce41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723774"
---
# <a name="memory-pressure-reporting"></a>Отчеты о нехватке памяти

Отчеты о нехватке памяти позволяют приложению Direct3D определить, когда рабочий набор видеопамяти стал слишком большим.

*Нехватка памяти* — это требование, которое приложение помещает в подсистему памяти. Хотя любое приложение Direct3D может использовать отчеты о нехватке памяти, эта функция особенно полезна для приложений, которые визуализируют видео с помощью Direct3D. Воспроизведение видео обычно дает преимущества от больших объемов буферизации, что позволяет заранее декодировать кадры. В то время как буферизация обычно приводит к более гладкому воспроизведению, это может привести к снижению производительности, если рабочий набор растет слишком большой из-за следующих факторов:

-   Память может быть удалена из кэша. В худшем случае это может происходить на каждом кадре видео.
-   Выделения памяти могут размещаться в неоптимальных сегментах памяти.

начиная с Windows 7, Direct3D может сообщать о некоторых статистических данных о нехватке видеопамяти:

-   Число байтов, исключенных процессом за интервал времени.
-   Объем памяти, размещенной в неоптимальных сегментах памяти.
-   Приблизительная индикация общей эффективности выделения памяти, размещенной в неоптимальной памяти.

Эти сведения могут помочь приложению поддерживать приемлемый рабочий набор.

## <a name="using-memory-pressure-reporting"></a>Использование отчетов о нехватке памяти

Отчеты о нехватке памяти используют существующий интерфейс **IDirect3DQuery9** для запроса устройства. В перечисление **D3DQUERYTYPE** добавлен новый тип запроса.


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



Чтобы использовать этот запрос, выполните следующие действия.

1.  Вызовите **IDirect3DDevice9Ex:: CreateQuery** с флагом **D3DQUERYTYPE \_ меморипрессуре** . Этот метод возвращает указатель на интерфейс **IDirect3DQuery9** .
2.  Вызовите **IDirect3DQuery9:: Issue** с флагом **\_ Begin D3DISSUE** , чтобы начать интервал измерения.
3.  Вызовите **IDirect3DQuery9:: Issue** с флагом **\_ End D3DISSUE** .
4.  Вызовите метод **IDirect3DQuery9:: GetData** , чтобы получить результат запроса. Запрос возвращает структуру [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .

## <a name="example-code"></a>Пример кода

В следующем примере показаны две функции, измеряющие нехватку памяти. Первый начинает интервал измерения, а второй извлекает результаты измерения.


```C++
HRESULT BeginMemoryPressureQuery(
    IDirect3DDevice9Ex *pDevice, 
    IDirect3DQuery9 **ppQuery
    )
{
    HRESULT hr = pDevice->CreateQuery(D3DQUERYTYPE_MEMORYPRESSURE, ppQuery);

    if (SUCCEEDED(hr))
    {
        hr = (*ppQuery)->Issue(D3DISSUE_BEGIN);
        if (FAILED(hr))
        {
            (*ppQuery)->Release();
            *ppQuery = NULL;
        }
    }
    return hr;
}

HRESULT EndMemoryPressureQuery(
    IDirect3DQuery9 *pQuery, 
    D3DMEMORYPRESSURE *pResult
    )
{
    HRESULT hr = pQuery->Issue(D3DISSUE_END);
    if (SUCCEEDED(hr))
    {
        hr = pQuery->GetData(pResult, sizeof(*pResult), D3DGETDATA_FLUSH);
    }
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[API-интерфейсы видео Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 



