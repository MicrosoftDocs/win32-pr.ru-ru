---
description: используйте методы интерфейса ивиадататрансфер, чтобы передавать данные из устройства Windowsного получения изображений (WIA) 1,0 в приложение.
ms.assetid: 67fbf3d9-6965-4464-b04c-10989b2fd55d
title: Передача данных изображения в WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e2c1dfce551f105b0df1627f11e9b4ccb7ee8a420e395f3fd0cc1ba932f136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813674"
---
# <a name="transferring-image-data-in-wia-10"></a>Передача данных изображения в WIA 1,0

> [!Note]  
> это руководство предназначено для передачи данных изображений в приложения, которые будут работать Windows XP или более ранней версии. сведения о передаче данных изображений в приложениях, которые будут выполняться в Windows Vista или более поздней версии, см. [в разделе передача данных изображения в WIA 2,0](-wia-transferring-image-data-in-wia2.md) .

 

используйте методы интерфейса [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , чтобы передавать данные из устройства Windowsного получения изображений (WIA) 1,0 в приложение. Этот интерфейс поддерживает окно общей памяти для перемещения данных из объекта устройства в приложение и удаления ненужных копий данных во время маршалинга.

Приложения должны запрашивать элемент изображения, чтобы получить указатель на его интерфейс [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , как показано в следующем примере кода:


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



В приведенном выше коде предполагается, что **пвиаитем** является допустимым указателем на интерфейс [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . Вызов [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) заполняет **пвиадататрансфер** указателем на интерфейс [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) элемента, на который ссылается **пвиаитем**.

Затем приложение задает элементы структуры [стгмедиум](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) . Дополнительные сведения см. в разделе СТГМЕДИУМ и [тимед](/windows/win32/api/objidl/ne-objidl-tymed).


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



Если указать имя файла, оно должно содержать правильное расширение. WIA 1,0 не предоставляет расширения файлов. Если элемент **лпсзфиленаме** элемента **Стгмедиум** имеет **значение NULL**, то WIA 1,0 создает случайное имя файла и путь для передаваемых данных. Переместите или скопируйте этот файл перед вызовом Релеасестгмедиум, так как эта функция удалит файл.

Затем приложение вызывает метод [**ивиадататрансфер:: идтжетдата**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) для выполнения передаваемых данных:


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



В вызове [**ивиадататрансфер:: идтжетдата**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)второй параметр указывает указатель на интерфейс [**ивиадатакаллбакк**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) . Приложения должны реализовать этот интерфейс для получения обратных вызовов во время передачи данных. Дополнительные сведения о реализации этого интерфейса см. в разделе [**ивиадатакаллбакк:: бандеддатакаллбакк**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

Затем приложение освобождает указатели на интерфейс [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) и освобождает все данные, выделенные в структуре [стгмедиум](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .

Приложение также может передавать образ, используя передачу данных в памяти вместо передачи файлов. В этом случае приложение использует метод Идтжетбандеддата вместо метода Идтжетдата.

Ниже приведен полный пример с переносом данных.


```
HRESULT TransferWiaItem( IWiaItem *pWiaItem )
{
    //
    // Validate arguments
    //
    if (NULL == pWiaItem)
    {
        return E_INVALIDARG;
    }

    //
    // Get the IWiaPropertyStorage interface so you can set required properties.
    //
    IWiaPropertyStorage *pWiaPropertyStorage = NULL;
    HRESULT hr = pWiaItem->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaPropertyStorage );
    if (SUCCEEDED(hr))
    {
        //
        // Prepare PROPSPECs and PROPVARIANTs for setting the
        // media type and format
        //
        PROPSPEC PropSpec[2] = {0};
        PROPVARIANT PropVariant[2] = {0};
        const ULONG c_nPropCount = sizeof(PropVariant)/sizeof(PropVariant[0]);

        //
        // Use BMP as the output format
        //
        GUID guidOutputFormat = WiaImgFmt_BMP;

        //
        // Initialize the PROPSPECs
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_IPA_FORMAT;
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_IPA_TYMED;

        //
        // Initialize the PROPVARIANTs
        //
        PropVariant[0].vt = VT_CLSID;
        PropVariant[0].puuid = &guidOutputFormat;
        PropVariant[1].vt = VT_I4;
        PropVariant[1].lVal = TYMED_FILE;

        //
        // Set the properties
        //
        hr = pWiaPropertyStorage->WriteMultiple( c_nPropCount, PropSpec, PropVariant, WIA_IPA_FIRST );
        if (SUCCEEDED(hr))
        {
            //
            // Get the IWiaDataTransfer interface
            //
            IWiaDataTransfer *pWiaDataTransfer = NULL;
            hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
            if (SUCCEEDED(hr))
            {
                //
                // Create our callback class
                //
                CWiaDataCallback *pCallback = new CWiaDataCallback;
                if (pCallback)
                {
                    //
                    // Get the IWiaDataCallback interface from our callback class.
                    //
                    IWiaDataCallback *pWiaDataCallback = NULL;
                    hr = pCallback->QueryInterface( IID_IWiaDataCallback, (void**)&pWiaDataCallback );
                    if (SUCCEEDED(hr))
                    {
                        //
                        // Perform the transfer using default settings
                        //
                        STGMEDIUM stgMedium = {0};
                        StgMedium.tymed = TYMED_FILE;
                        hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
                        if (S_OK == hr)
                        {
                            //
                            // Print the filename (note that this filename is always
                            // a WCHAR string, not TCHAR).
                            //
                            _tprintf( TEXT("Transferred filename: %ws\n"), stgMedium.lpszFileName );

                            //
                            // Release any memory associated with the stgmedium
                            // This will delete the file stgMedium.lpszFileName.
                            //
                            ReleaseStgMedium( &stgMedium );
                        }

                        //
                        // Release the callback interface
                        //
                        pWiaDataCallback->Release();
                        pWiaDataCallback = NULL;
                    }

                    //
                    // Release our callback.  It should now delete itself.
                    //
                    pCallback->Release();
                    pCallback = NULL;
                }

                //
                // Release the IWiaDataTransfer
                //
                pWiaDataTransfer->Release();
                pWiaDataTransfer = NULL;
            }
        }

        //
        // Release the IWiaPropertyStorage
        //
        pWiaPropertyStorage->Release();
        pWiaPropertyStorage = NULL;
    }

    return hr;
}
```



 

 
