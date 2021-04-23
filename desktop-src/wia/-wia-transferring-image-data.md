---
description: Используйте методы интерфейса Ивиадататрансфер, чтобы передавать данные из устройства Windows для получения образа (WIA) 1,0 в приложение.
ms.assetid: 67fbf3d9-6965-4464-b04c-10989b2fd55d
title: Передача данных изображения в WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00fc7ff76576b6c140358f9af3a0f9d17d4b180e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145370"
---
# <a name="transferring-image-data-in-wia-10"></a><span data-ttu-id="19322-103">Передача данных изображения в WIA 1,0</span><span class="sxs-lookup"><span data-stu-id="19322-103">Transferring Image Data in WIA 1.0</span></span>

> [!Note]  
> <span data-ttu-id="19322-104">Это руководство предназначено для передачи данных образа в приложения, которые будут работать под управлением Windows XP или более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="19322-104">This tutorial is about transferring image data in applications that will run Windows XP or earlier.</span></span> <span data-ttu-id="19322-105">Сведения о передаче данных изображений в приложениях, которые будут выполняться в Windows Vista или более поздней версии, см. [в разделе Передача данных изображения в WIA 2,0](-wia-transferring-image-data-in-wia2.md) .</span><span class="sxs-lookup"><span data-stu-id="19322-105">See [Transferring Image Data in WIA 2.0](-wia-transferring-image-data-in-wia2.md) for information about transferring image data in applications that will run on Windows Vista or later.</span></span>

 

<span data-ttu-id="19322-106">Используйте методы интерфейса [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , чтобы передавать данные из устройства Windows для получения образа (WIA) 1,0 в приложение.</span><span class="sxs-lookup"><span data-stu-id="19322-106">Use the methods of the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface to transfer data from a Windows Image Acquisition (WIA) 1.0 device to an application.</span></span> <span data-ttu-id="19322-107">Этот интерфейс поддерживает окно общей памяти для перемещения данных из объекта устройства в приложение и удаления ненужных копий данных во время маршалинга.</span><span class="sxs-lookup"><span data-stu-id="19322-107">This interface supports a shared memory window to transfer data from the device object to the application and eliminate unnecessary data copies during marshalling.</span></span>

<span data-ttu-id="19322-108">Приложения должны запрашивать элемент изображения, чтобы получить указатель на его интерфейс [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="19322-108">Applications must query an image item to obtain a pointer to its [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface, as in the following code sample:</span></span>


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



<span data-ttu-id="19322-109">В приведенном выше коде предполагается, что **пвиаитем** является допустимым указателем на интерфейс [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="19322-109">In the previous code, it is assumed that **pWiaItem** is a valid pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface.</span></span> <span data-ttu-id="19322-110">Вызов [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) заполняет **пвиадататрансфер** указателем на интерфейс [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) элемента, на который ссылается **пвиаитем**.</span><span class="sxs-lookup"><span data-stu-id="19322-110">The call to [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) fills **pWiaDataTransfer** with a pointer to the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface of the item referred to by **pWiaItem**.</span></span>

<span data-ttu-id="19322-111">Затем приложение задает элементы структуры [стгмедиум](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .</span><span class="sxs-lookup"><span data-stu-id="19322-111">The application then sets the [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure members.</span></span> <span data-ttu-id="19322-112">Дополнительные сведения см. в разделе СТГМЕДИУМ и [тимед](/windows/win32/api/objidl/ne-objidl-tymed).</span><span class="sxs-lookup"><span data-stu-id="19322-112">For information, see STGMEDIUM and [TYMED](/windows/win32/api/objidl/ne-objidl-tymed).</span></span>


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



<span data-ttu-id="19322-113">Если указать имя файла, оно должно содержать правильное расширение. WIA 1,0 не предоставляет расширения файлов.</span><span class="sxs-lookup"><span data-stu-id="19322-113">If you supply a filename, it should include the proper file extension; WIA 1.0 does not provide file extensions.</span></span> <span data-ttu-id="19322-114">Если элемент **лпсзфиленаме** элемента **Стгмедиум** имеет **значение NULL**, то WIA 1,0 создает случайное имя файла и путь для передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="19322-114">If the **lpszFileName** member of **StgMedium** is **NULL**, WIA 1.0 generates a random file name and path for the transferred data.</span></span> <span data-ttu-id="19322-115">Переместите или скопируйте этот файл перед вызовом Релеасестгмедиум, так как эта функция удалит файл.</span><span class="sxs-lookup"><span data-stu-id="19322-115">Move or copy this file before calling ReleaseStgMedium, because this function will delete the file.</span></span>

<span data-ttu-id="19322-116">Затем приложение вызывает метод [**ивиадататрансфер:: идтжетдата**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) для выполнения передаваемых данных:</span><span class="sxs-lookup"><span data-stu-id="19322-116">The application then calls the [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) method to run the data transfer:</span></span>


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



<span data-ttu-id="19322-117">В вызове [**ивиадататрансфер:: идтжетдата**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)второй параметр указывает указатель на интерфейс [**ивиадатакаллбакк**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) .</span><span class="sxs-lookup"><span data-stu-id="19322-117">In the call to [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata), the second parameter specifies a pointer to the [**IWiaDataCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) interface.</span></span> <span data-ttu-id="19322-118">Приложения должны реализовать этот интерфейс для получения обратных вызовов во время передачи данных.</span><span class="sxs-lookup"><span data-stu-id="19322-118">Applications must implement this interface to receive callbacks during data transfers.</span></span> <span data-ttu-id="19322-119">Дополнительные сведения о реализации этого интерфейса см. в разделе [**ивиадатакаллбакк:: бандеддатакаллбакк**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="19322-119">For information about implementing this interface, see [**IWiaDataCallback::BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

<span data-ttu-id="19322-120">Затем приложение освобождает указатели на интерфейс [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) и освобождает все данные, выделенные в структуре [стгмедиум](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .</span><span class="sxs-lookup"><span data-stu-id="19322-120">The application then releases the pointers to the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface and frees any data allocated in the [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure.</span></span>

<span data-ttu-id="19322-121">Приложение также может передавать образ, используя передачу данных в памяти вместо передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="19322-121">The application can also transfer the image using in-memory data transfers instead of file transfers.</span></span> <span data-ttu-id="19322-122">В этом случае приложение использует метод Идтжетбандеддата вместо метода Идтжетдата.</span><span class="sxs-lookup"><span data-stu-id="19322-122">In this case, the application uses the idtGetBandedData method in place of the idtGetData method.</span></span>

<span data-ttu-id="19322-123">Ниже приведен полный пример с переносом данных.</span><span class="sxs-lookup"><span data-stu-id="19322-123">Here is the complete data transfer sample:</span></span>


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



 

 
