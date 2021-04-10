---
description: Выбор фильтра сжатия
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Выбор фильтра сжатия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140659"
---
# <a name="choosing-a-compression-filter"></a>Выбор фильтра сжатия

Несколько типов программных компонентов могут выполнять видео или аудио сжатие, например:

-   Собственные фильтры DirectShow
-   Кодеки для сжатия видео (ВКМ)
-   Кодеки диспетчера аудиосжатия (ACM)
-   Объекты мультимедиа DirectX (дмос)

В DirectShow кодеки ВКМ упаковываются с помощью [фильтра AVI компрессор](avi-compressor-filter.md), а ACM кодеки упаковываются [фильтром оболочки ACM](acm-wrapper-filter.md). Дмос упаковывается [фильтром оболочки DMO](dmo-wrapper-filter.md). Перечислитель системных устройств обеспечивает единообразный способ перечисления и создания любого из этих типов сжатия, не беспокоясь о базовой модели.

Дополнительные сведения о перечислителе системных устройств см. [в разделе Использование перечислителя системных устройств](using-the-system-device-enumerator.md). Вкратце, все фильтры DirectShow классифицируются по категориям, и каждая категория идентифицируется по идентификатору GUID. Для видео-компрессоров Категория GUID имеет значение CLSID \_ видеокомпрессоркатегори. Для звуковых компрессоров это CLSID \_ аудиокомпрессоркатегори. Чтобы перечислить определенную категорию, перечислитель системных устройств создает объект *перечислителя* , который поддерживает интерфейс [**иенуммоникер**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) . Приложение использует этот интерфейс для получения моникеров устройств, где каждый моникер устройства представляет экземпляр фильтра DirectShow. Можно использовать моникер для создания фильтра или для получения понятного имени устройства без создания фильтра.

Для перечисления видео или звуковых компрессоров, доступных в системе пользователя, выполните следующие действия.

1.  Вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать перечислитель системных устройств с идентификатором класса CLSID \_ системдевицеенум.
2.  Вызовите [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) с идентификатором GUID категории фильтра. Метод возвращает указатель интерфейса **иенуммоникер** .
3.  Используйте метод Иенуммоникер:: Next для перечисления моникеров устройств. Этот метод возвращает интерфейс [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) , который представляет моникер.

Чтобы получить понятное имя из моникера, выполните следующие действия.

1.  Вызовите метод **IMoniker:: биндтостораже** . Этот метод возвращает указатель интерфейса **ипропертибаг** .
2.  Используйте метод **ипропертибаг:: Read** для чтения свойства **FriendlyName** .

Как правило, в приложении отображается список компрессоров, чтобы пользователь мог выбрать один из них. Например, следующий код заполняет список именами доступных компрессоров видео.


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



Чтобы создать экземпляр фильтра из моникера, вызовите метод **IMoniker:: биндтубжект** . Метод возвращает указатель [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



Для кодеков ВКМ каждый моникер представляет один конкретный кодек, хотя все кодеки упаковываются одним и тем же фильтром сжатия AVI. При вызове **биндтубжект** создается экземпляр этого фильтра, инициализированный для этого кодека. По этой причине нельзя вызвать метод **CoCreateInstance** непосредственно в фильтре сжатия AVI. Необходимо пройти перечислитель системных устройств.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Повторное сжатие файла AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 
