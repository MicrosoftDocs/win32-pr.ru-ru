---
description: Так как передача данных изображения выполняется в потоковом режиме при получении образа Windows (WIA) 2,0, указывать тип назначения не требуется (например,
ms.assetid: ebb9fce5-9450-4ffe-b480-b21670b60f90
title: Передача данных изображения в WIA 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ded5c6cd8fb94b1beccd86c3cd8aef3018aed0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343655"
---
# <a name="transferring-image-data-in-wia-20"></a>Передача данных изображения в WIA 2,0

> [!Note]  
> В этом учебнике показано, как передавать данные образа в приложения, работающие под управлением Windows Vista или более поздней версии. Сведения о передаче данных изображений в приложениях, работающих под управлением Windows XP или более ранних версий, см. [в разделе Передача данных изображения в WIA 1,0](-wia-transferring-image-data.md) .

 

Поскольку передача данных изображения в потоковой передаче выполняется в режиме получения изображений Windows (WIA) 2,0, указывать целевой тип (например, память или файл) не нужно. Приложение просто предоставляет WIA 2,0 для использования в потоке, а драйвер считывает или выполняет запись в поток. Поток может быть файловым потоком, потоком памяти или любым другим типом потока, а также прозрачным для драйвера. Использование потоков также обеспечивает простую интеграцию с фильтром обработки изображений.

Используйте методы интерфейса [**ивиатрансфер**](-wia-iwiatransfer.md) для перемещения данных с устройства WIA 2,0 в приложение. Этот интерфейс доступен через интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) . Интерфейс **ивиатрансфер** имеет методы для запроса передачи или загрузки данных с устройства. Эти методы принимают обратный вызов, предоставляемый приложением, и используют [IStream](/windows/win32/api/objidl/nn-objidl-istream) , предоставленный приложением, для фактического назначения передаваемых данных.

Приложения должны запрашивать элемент изображения, чтобы получить указатель на его интерфейс [**ивиатрансфер**](-wia-iwiatransfer.md) , как показано в следующем примере кода:


```
    // Get the IWiaTransfer interface
    //
    IWiaTransfer *pWiaTransfer = NULL;
    hr = pIWiaItem2->QueryInterface(IID_IWiaTransfer,(void**)&pWiaTransfer);
```



В приведенном выше коде предполагается, что **pWiaItem2** является допустимым указателем на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) . Вызов [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) заполняет **пвиатрансфер** указателем на интерфейс [**ивиатрансфер**](-wia-iwiatransfer.md) элемента, на который ссылается **pWiaItem2**.

Затем приложение создает экземпляр объекта обратного вызова, как показано ниже.


```
    //   Instantiate the object which receives the callbacks
    //
    CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
```



Затем приложение устанавливает свойства с помощью интерфейса [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) элемента [**IWiaItem2**](-wia-iwiaitem2.md) и выполняет перенос.

Загружаем


```
    // Download   
    hr = pWiaTransfer->Download(0,pWiaClassCallback);
```



Отправка


```
    //Create child item which eventually will be the uploaded image 
    IWiaItem2* pWiaItemChild = NULL;
    HRESULT hr = pIWiaItem2->CreateChildItem(WiaItemTypeImage|WiaItemTypeFile,0,bzUploadFileName,&pWiaItemChild);
    
    if(SUCCEEDED(hr))
    {
                
        //Set the format for the child item as BMP 
        IWiaPropertyStorage* pWiaChildPropertyStorage = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaChildPropertyStorage );
        if(SUCCEEDED(hr))
        {
            WritePropertyGuid(pWiaChildPropertyStorage,WIA_IPA_FORMAT,WiaImgFmt_BMP );

            //release pWiaChildPropertyStorage
            pWiaChildPropertyStorage->Release();
            pWiaChildPropertyStorage = NULL;
        }
        

        //Get the IWiaTransfer interface of the child
        IWiaTransfer* pWiaTransferChild = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransferChild );
        if(SUCCEEDED(hr)){
            IStream* pUploadStream = NULL;
                                        
            //Create stream on test.BMP file
            hr = SHCreateStreamOnFile(L"test.BMP",STGM_READ, &pUploadStream);
            if(SUCCEEDED(hr)){
                pWiaTransferChild->Upload(0,pUploadStream,pWiaClassCallback);
                
            }
         }
   
      }
```



Ниже приведен полный пример с переносом данных.


```
HRESULT TransferWiaItem( IWiaItem2 *pIWiaItem2)
{
    // Validate arguments
    if (NULL == pIWiaItem2)
    {
        _tprintf(TEXT("\nInvalid parameters passed"));
        return E_INVALIDARG;
    }
    
    // Get the IWiaTransfer interface
    IWiaTransfer *pWiaTransfer = NULL;
    HRESULT hr = pIWiaItem2->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransfer );
    if (SUCCEEDED(hr))
    {
        // Create our callback class
        CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
        if (pWiaClassCallback)
        {
            
              LONG lItemType = 0;
              hr = pIWiaItem2->GetItemType( &lItemType );

              //download all items which have WiaItemTypeTransfer flag set
              if(lItemType & WiaItemTypeTransfer)
              {

                  // If it is a folder, do folder download . Hence with one API call, all the leaf nodes of this folder 
                  // will be transferred
                  if ((lItemType & WiaItemTypeFolder))
                  {
                        _tprintf ( L"\nI am a folder item");
                        hr = pWiaTransfer->Download(WIA_TRANSFER_ACQUIRE_CHILDREN, pWiaClassCallback);
                        if(S_OK == hr)
                        {
                            _tprintf(TEXT("\npWiaTransfer->Download() on folder item SUCCEEDED"));
                        }
                        else if(S_FALSE == hr)
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item returned S_FALSE. Folder may not be having child items"),hr);
                        }
                        else if(FAILED(hr))
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item failed"),hr);
                        }
                   }

                  
                  // If this is an file type, do file download
                  else if (lItemType & WiaItemTypeFile )
                  {
                      hr = pWiaTransfer->Download(0,pWiaClassCallback);
                      if(S_OK == hr)
                      {
                          _tprintf(TEXT("\npWiaTransfer->Download() on file item SUCCEEDED"));
                      }
                      else if(S_FALSE == hr)
                      {
                          ReportError(TEXT("\npWiaTransfer->Download() on file item returned S_FALSE. File may be empty"),hr);
                      }
                      else if(FAILED(hr))
                      {
                         ReportError(TEXT("\npWiaTransfer->Download() on file item failed"),hr);
                      }
                  }                     
                }
                
                // Release our callback.  It should now delete itself.
                pWiaClassCallback->Release();
                pWiaClassCallback = NULL;
        }
        else
        {
            ReportError( TEXT("\nUnable to create CWiaTransferCallback class instance") );
        }
            
        // Release the IWiaTransfer
        pWiaTransfer->Release();
        pWiaTransfer = NULL;
    }
    else
    {
        ReportError( TEXT("\npIWiaItem2->QueryInterface failed on IID_IWiaTransfer"), hr );
    }
    return hr;
}

// Callback Class should be something like this:

class CWiaTransferCallback : public IWiaTransferCallback
{
public: // Constructors, destructor
    CWiaTransferCallback () : m_cRef(1) {};
    ~ CWiaTransferCallback () {};

public: // IWiaTransferCallback
    HRESULT __stdcall TransferCallback(
        LONG                lFlags,
        WiaTransferParams   *pWiaTransferParams)
    {
        HRESULT hr = S_OK;

        switch (pWiaTransferParams->lMessage)
        {
            case WIA_TRANSFER_MSG_STATUS:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_STREAM:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_TRANSFER:
                ...
                break;
            default:
                break;
        }

        return hr;
    }

    HRESULT __stdcall GetNextStream(
        LONG    lFlags,
        BSTR    bstrItemName,
        BSTR    bstrFullItemName,
        IStream **ppDestination)
    {

        HRESULT hr = S_OK;

        //  Return a new stream for this item's data.
        //
        hr = CreateDestinationStream(bstrItemName, ppDestination);
        return hr;
    }

public: // IUnknown
        .
        .
        . // Etc.

private:
    /// For ref counting implementation
    LONG                m_cRef;
};

```



 

 
