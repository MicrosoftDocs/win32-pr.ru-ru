---
description: Требования к приложениям DRM-Enabled Windows Media
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Требования к приложениям DRM-Enabled Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713295"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a><span data-ttu-id="e6845-103">Требования к приложениям DRM-Enabled Windows Media</span><span class="sxs-lookup"><span data-stu-id="e6845-103">Requirements for Windows Media DRM-Enabled Applications</span></span>

<span data-ttu-id="e6845-104">Чтобы создать приложение с поддержкой цифровых Rights Management Windows Media (DRM), необходимо иметь заголовки и библиотеки, описанные в разделе [Общие требования для разработки приложений](general-requirements-for-application-development.md) этого документа.</span><span class="sxs-lookup"><span data-stu-id="e6845-104">To create a Windows Media Digital Rights Management (DRM)-enabled application, you must have the headers and libraries described in the [General Requirements for Application Development](general-requirements-for-application-development.md) section of this document.</span></span> <span data-ttu-id="e6845-105">Кроме того, при открытии устройства приложению потребуется предоставить дополнительные свойства в сведениях о клиенте.</span><span class="sxs-lookup"><span data-stu-id="e6845-105">In addition, the application will need to supply additional properties in the client information when opening the device.</span></span>

<span data-ttu-id="e6845-106">В следующей таблице описаны два дополнительных свойства, необходимые для включения передачи содержимого, защищенного с помощью DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e6845-106">The two additional properties that are required to enable Windows Media DRM-protected content transfers are described in the following table.</span></span>



| <span data-ttu-id="e6845-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="e6845-107">Property</span></span>                                      | <span data-ttu-id="e6845-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e6845-108">Description</span></span>                              |
|-----------------------------------------------|------------------------------------------|
| <span data-ttu-id="e6845-109">\_ \_ \_ \_ закрытый ключ клиентского приложения WPD с цифровыми правами \_</span><span class="sxs-lookup"><span data-stu-id="e6845-109">WPD\_CLIENT\_WMDRM\_APPLICATION\_PRIVATE\_KEY</span></span> | <span data-ttu-id="e6845-110">Указывает закрытый ключ приложения.</span><span class="sxs-lookup"><span data-stu-id="e6845-110">Specifies the application's private key.</span></span> |
| <span data-ttu-id="e6845-111">\_сертификат приложения WPD клиента для \_ WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="e6845-111">WPD\_CLIENT\_WMDRM\_APPLICATION\_CERTIFICATE</span></span>  | <span data-ttu-id="e6845-112">Указывает сертификат приложения.</span><span class="sxs-lookup"><span data-stu-id="e6845-112">Specifies the application's certificate.</span></span> |



 

<span data-ttu-id="e6845-113">Эти свойства должны быть заданы в клиентской информации приложения при открытии устройства с помощью метода [**ипортабледевице:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) .</span><span class="sxs-lookup"><span data-stu-id="e6845-113">These properties must be supplied in the application's client information when the device is opened with the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.</span></span> <span data-ttu-id="e6845-114">При предоставлении этих свойств API-интерфейс WPD позволяет передавать защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="e6845-114">When these properties are supplied, the WPD API allows protected content transfers.</span></span> <span data-ttu-id="e6845-115">Если приложение предоставил сертификат и закрытый ключ, API создаст защищенный канал для передачи защищенного WMDRM-содержимого на устройство.</span><span class="sxs-lookup"><span data-stu-id="e6845-115">If the application has provided a certificate and private key, the API will create a secure channel to transfer protected WMDRM content to the device.</span></span>

<span data-ttu-id="e6845-116">Сведения о создании и распространении приложений Windows, которые поддерживают Windows Media DRM, см. в следующем разделе [Лицензирование приложений на основе Windows](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e6845-116">For information about creating and distributing Windows-based applications that support Windows Media DRM, see the following [Licensing Windows-based Applications](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) topic.</span></span>

## <a name="transferring-content"></a><span data-ttu-id="e6845-117">Передача содержимого</span><span class="sxs-lookup"><span data-stu-id="e6845-117">Transferring Content</span></span>

<span data-ttu-id="e6845-118">Чтобы переместить защищенное WMDRM содержимое, используйте [**ипортабледевицеконтент:: креатеобжектвиспропертиесанддата**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="e6845-118">To transfer WMDRM protected content, use [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="e6845-119">Этот метод можно использовать как для защищенного, так и для открытого содержимого без дополнительных параметров.</span><span class="sxs-lookup"><span data-stu-id="e6845-119">This method can be used for both protected and clear content without additional options.</span></span> <span data-ttu-id="e6845-120">API-интерфейс WPD автоматически выбирает защищенный или сброшенный канал в зависимости от того, является ли содержимое защищенным или открытым.</span><span class="sxs-lookup"><span data-stu-id="e6845-120">The WPD API will automatically select the protected or clear channel depending on whether the content is protected or clear.</span></span> <span data-ttu-id="e6845-121">Он взаимодействует с поставщиком безопасного содержимого WMDRM для обработки лицензий WMDRM.</span><span class="sxs-lookup"><span data-stu-id="e6845-121">It interfaces with the WMDRM Secure Content Provider to process the WMDRM licenses.</span></span>

## <a name="transferring-known-clear-content"></a><span data-ttu-id="e6845-122">Передача известного открытого содержимого</span><span class="sxs-lookup"><span data-stu-id="e6845-122">Transferring Known Clear Content</span></span>

<span data-ttu-id="e6845-123">Если вы включили приложение для обработки защищенного содержимого, но знаете, что конкретный файл не защищен, вы можете сообщить WPD, что он пропускает обработку DRM, установив **\_ параметр API \_ - \_ \_ \_ \_ интерфейса WPD** в поле входные **ипортабледевицевалуес** при вызове [**ипортабледевицеконтент:: креатеобжектвиспропертиесанддата**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) для очистки содержимого.</span><span class="sxs-lookup"><span data-stu-id="e6845-123">If you've enabled your application to handle protected content, but you know that a specific file is not protected, you can tell WPD to skip the DRM processing by setting **WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM** option to TRUE in the input **IPortableDeviceValues** when calling [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) for clear content.</span></span>

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a><span data-ttu-id="e6845-124">Доступ к операциям отслеживания использования с помощью Ивмдрмдевицеапп</span><span class="sxs-lookup"><span data-stu-id="e6845-124">Accessing Metering Operations using IWMDRMDeviceApp</span></span>

<span data-ttu-id="e6845-125">Средство WPD предоставляет механизм доступа к API **ивмдрмдевицеапп** для обновлений лицензий и получения данных контроля использования.</span><span class="sxs-lookup"><span data-stu-id="e6845-125">WPD provides a mechanism to access the **IWMDRMDeviceApp** APIs for license updates and metering data retrieval.</span></span> <span data-ttu-id="e6845-126">Чтобы получить доступ к этому API через WPD, вызовите **QueryInterface** для **IID \_ ивмдрмдевицеапп** из **IStream** , возвращенного из [**ипортабледевицеконтент:: креатеобжектвиспропертиесанддата**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="e6845-126">To access this API through WPD, call **QueryInterface** on **IID\_IWMDRMDeviceApp** from the **IStream** returned from [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="e6845-127">Этот экземпляр **ивмдрмдевицеапп** связан с подключением **ипортабледевице** к устройству, совместимому с WMDRM, а не с конкретным содержимым, в котором был получен объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="e6845-127">This **IWMDRMDeviceApp** instance tied to the **IPortableDevice** connection to your WMDRM-compatible device, and not the specific content where the **IStream** was obtained.</span></span> <span data-ttu-id="e6845-128">WPD внутренне заключает в оболочку API отслеживания использования и делает его доступным для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="e6845-128">WPD internally wraps the metering APIs and makes it accessible to your application.</span></span> <span data-ttu-id="e6845-129">Для параметра Ивмдмдевице в приложении следует \_ использовать \_ \_ \_ константу PTR для устройства  WPD вмдрмдевицеапп \* .</span><span class="sxs-lookup"><span data-stu-id="e6845-129">Your application should use the WMDRMDEVICEAPP\_USE\_WPD\_DEVICE\_PTR constant for the *IWMDMDevice*\* parameter.</span></span>

<span data-ttu-id="e6845-130">Это показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="e6845-130">The following code snippet demonstrates this.</span></span>


```C++
IStream*               pDataStream = NULL;

IWMDRMDeviceApp*       pWMDRMApp   = NULL;

  

// ... Initialization 

 

hr = pPortableDeviceContent->CreateObjectWithPropertiesAndData(pValues,

                              &pDataStream,

                              &dwOptimalWriteBufferSize,

                              NULL);

 

// ... Transfer the protected WMDRM content 

pDataStream->Write(pData, cbData, &cbWritten);

 

pDataStream->Commit(0);

 

hr = pDataStream->QueryInterface(IID_IWMDRMDeviceApp, 

                                 (void**)&pWMDRMApp);

 

if (SUCCEEDED(hr))

{

   DWORD dwStatus = 0;

 

   // Call metering operations on the current device using the WPD device pointer

   hr = pWMDRMApp->QueryDeviceStatus((IWMDMDevice *)WMDRMDEVICEAPP_USE_WPD_DEVICE_PTR, 

                                     &dwStatus);

}

```



<span data-ttu-id="e6845-131">Также применяется тот же самый предварительный компонент с закрытым ключом приложения и сертификатом.</span><span class="sxs-lookup"><span data-stu-id="e6845-131">The same pre-requisite with the application private key and certificate applies here as well.</span></span> <span data-ttu-id="e6845-132">Если ключ или сертификат недействительны или не удается инициализировать систему WMDRM, вызов **куеринферфаце** завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e6845-132">If the key/certificate is invalid or if the WMDRM system fails to initialize, the **QueryInferface** call will fail.</span></span>

<span data-ttu-id="e6845-133">Приведенный выше метод получения интерфейса **ивмдрмдевицеапп** из указателя **IStream** является просто удобным, если приложение уже выполняет предыдущий защищенный перенос содержимого, прежде чем продолжать выполнение операций отслеживания и синхронизации лицензий.</span><span class="sxs-lookup"><span data-stu-id="e6845-133">The above method to acquire the **IWMDRMDeviceApp** interface from the **IStream** pointer is just a convenience if your application is already doing a prior protected content transfer, before proceeding on to do metering and license synchronization operations.</span></span>

<span data-ttu-id="e6845-134">Наша рекомендация для большинства приложений, которым требуется доступ к **ивмдрмдевицеапп** , — это инициализация **ивмдрмдевицеапп** напрямую, так как это не требует от приложения передавать защищенное содержимое или хранить их в интерфейсах перемещения, чтобы обеспечить отслеживание устройств и синхронизацию лицензий. Для этого метода потребуется использование интерфейсов API Windows Media диспетчер устройств (ВМДМ).</span><span class="sxs-lookup"><span data-stu-id="e6845-134">Our recommendation for most applications that need to access **IWMDRMDeviceApp** is to initialize **IWMDRMDeviceApp** directly as this does not require your application to transfer protected content or hold on to the transfer interfaces in order to do device metering and license sync. This method will require usage of Windows Media Device Manager (WMDM) APIs.</span></span> <span data-ttu-id="e6845-135">Дополнительные сведения и примеры кода см. в техническом документе о [приложении WPD](../windows-portable-devices.md) на сайте вхдк.</span><span class="sxs-lookup"><span data-stu-id="e6845-135">For details and sample code, refer to the [Accessing WMDRM APIs from a WPD Application](../windows-portable-devices.md) whitepaper on the WHDC site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6845-136">См. также</span><span class="sxs-lookup"><span data-stu-id="e6845-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6845-137">**Портативные устройства Windows**</span><span class="sxs-lookup"><span data-stu-id="e6845-137">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
