---
description: Использование дмос в DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Использование дмос в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d056d22e5e9b42795cbe95ce676ac293605453200e0a691d4f0d00374e94cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078654"
---
# <a name="using-dmos-in-directshow"></a>Использование дмос в DirectShow

приложения на основе DirectShow могут использовать дмос в графе фильтров с помощью фильтра [оболочки DMO](dmo-wrapper-filter.md) . этот фильтр объединяет DMO и обрабатывает все сведения об использовании DMO, например передачу данных в DMO, выделение объектов [**имедиабуффер**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) и т. д.

поскольку DMO статистической обработки по фильтру, приложение может запросить фильтр для любых COM-интерфейсов, предоставляемых DMO. Однако приложение должно позволить фильтру выполнять все операции потоковой передачи на DMO. например, не следует задавать типы носителей, обрабатывать любые буферы, сбрасывать DMO, блокировать DMO, включать или отключать контроль качества, а также устанавливать оптимизации видео.

если вы знакомы с идентификатором класса (CLSID) определенного DMO, который вы хотите использовать, можно инициализировать фильтр оболочки DMO с этим DMO следующим образом:

1.  вызовите **cocreateinstance** , чтобы создать фильтр оболочки DMO.
2.  запросите фильтр оболочки DMO для интерфейса [**идмоврапперфилтер**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .
3.  Вызовите метод [**идмоврапперфилтер:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) . укажите идентификатор CLSID DMO и идентификатор GUID категории DMO. список категорий DMO см. в разделе [DMO guids](dmo-guids.md).

Следующий код показывает эти действия.


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



Функция [**дмоенум**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) перечисляет дмос в реестре. эта функция использует другой набор идентификаторов guid категорий из тех, которые используются для DirectShow фильтров.

**Использование перечислителя системных устройств с дмос**

вместо того, чтобы создавать DMO напрямую, можно использовать [перечислитель системных устройств](system-device-enumerator.md), который может перечислить любую категорию DMO, поддерживаемую методом **дмоенум** . перечислитель системных устройств также включает дмос при перечислении определенных категорий фильтров DirectShow. в следующей таблице показано сопоставление между категориями DMO и категориями DirectShow.



| Метка | Значение |
|-----------------------------|--------------------------------|
| DMO Категори                | DirectShow Друг          |
| \_КОДИРОВЩИК дмокатегори Audio \_ | \_АУДИОКОМПРЕССОРКАТЕГОРИ CLSID |
| \_декодер дмокатегори Audio \_ | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID  |
| \_кодировщик видео \_ дмокатегори | \_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID |
| \_декодер видео \_ дмокатегори | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID  |



 

Перечислитель системных устройств возвращает список объектов моникера. если моникер представляет DMO, метод **IMoniker:: биндтубжект** автоматически создает фильтр оболочки DMO и инициализирует его с этим DMO. таким же, тот факт, что DMO участвует в прозрачности приложения. Дополнительные сведения об использовании перечислителя системных устройств см. в разделе [Использование перечислителя системных устройств](using-the-system-device-enumerator.md).

**Ограничения**

Существуют некоторые ограничения при использовании дмос в DirectShow.

-   фильтр оболочки DMO не поддерживает дмос с нулевым числом входов, несколькими входами или нулевыми выходами.
-   все соединения пин-кода в фильтре оболочки DMO используют интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   DirectShow службы редактирования не поддерживают эффекты или переходы на основе DMO.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование дмос](using-dmos.md)
</dt> </dl>

 

 



