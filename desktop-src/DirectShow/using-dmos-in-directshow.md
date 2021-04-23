---
description: Использование дмос в DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Использование дмос в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdddc643d39798dc09807e9ecfa15c38a6e0c2cf
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908692"
---
# <a name="using-dmos-in-directshow"></a>Использование дмос в DirectShow

Приложения, основанные на DirectShow, могут использовать дмос в графе фильтров с помощью фильтра [оболочки DMO](dmo-wrapper-filter.md) . Этот фильтр объединяет DMO и обрабатывает все детали использования DMO, такие как передача данных в DMO, выделение объектов [**имедиабуффер**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) и т. д.

Поскольку объекты DMO объединяются фильтром, приложение может запросить фильтр для любых COM-интерфейсов, предоставляемых DMO. Однако приложение должно позволить фильтру выполнять все операции потоковой передачи на DMO. Например, не следует задавать типы носителей, обрабатывать любые буферы, сбрасывать объекты DMO, блокировать объекты DMO, включать или отключать контроль качества, а также устанавливать оптимизации видео.

Если вы знакомы с идентификатором класса (CLSID) конкретного DMO, который вы хотите использовать, можно инициализировать фильтр оболочки DMO с этим DMO следующим образом:

1.  Вызовите **CoCreateInstance** , чтобы создать фильтр оболочки DMO.
2.  Запросите фильтр оболочки DMO для интерфейса [**идмоврапперфилтер**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .
3.  Вызовите метод [**идмоврапперфилтер:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) . Укажите идентификатор CLSID DMO и идентификатор GUID категории DMO. Список категорий DMO см. в разделе [идентификаторы GUID DMO](dmo-guids.md).

В следующем коде показаны следующие шаги.


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



Функция [**дмоенум**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) перечисляет дмос в реестре. Эта функция использует другой набор идентификаторов GUID категорий из тех, которые используются для фильтров DirectShow.

**Использование перечислителя системных устройств с дмос**

Вместо непосредственного создания DMO можно использовать [перечислитель системных устройств](system-device-enumerator.md), который позволяет перечислить любую категорию DMO, поддерживаемую методом **дмоенум** . Перечислитель системных устройств также включает дмос, когда он перечисляет определенные категории фильтров DirectShow. В следующей таблице показано сопоставление между категориями DMO и категориями DirectShow.



| Метка | Значение |
|-----------------------------|--------------------------------|
| Категория DMO                | Эквивалент DirectShow          |
| \_КОДИРОВЩИК дмокатегори Audio \_ | \_АУДИОКОМПРЕССОРКАТЕГОРИ CLSID |
| \_декодер дмокатегори Audio \_ | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID  |
| \_кодировщик видео \_ дмокатегори | \_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID |
| \_декодер видео \_ дмокатегори | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID  |



 

Перечислитель системных устройств возвращает список объектов моникера. Если моникер представляет DMO, метод **IMoniker:: биндтубжект** автоматически создает фильтр оболочки DMO и инициализирует его с этим DMO. Таким же, тот факт, что задействован DMO, прозрачен для приложения. Дополнительные сведения об использовании перечислителя системных устройств см. в разделе [Использование перечислителя системных устройств](using-the-system-device-enumerator.md).

**Ограничения**

При использовании дмос в DirectShow существуют некоторые ограничения:

-   Фильтр оболочки DMO не поддерживает дмос с нулевым числом входов, несколькими входами или нулевыми выходами.
-   Все соединения ПИН-кода в фильтре оболочки DMO используют интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Службы редактирования DirectShow не поддерживают эффекты и переходы на основе DMO.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование дмос](using-dmos.md)
</dt> </dl>

 

 



