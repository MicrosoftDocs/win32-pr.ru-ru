---
title: Описание устройств
description: Существует два способа получения объектов устройств.
ms.assetid: a83fbf21-586e-4b92-9875-476d820c377d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abc84f15f6b52328585e05abfd95503087124b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888880"
---
# <a name="describing-devices"></a><span data-ttu-id="5b60b-103">Описание устройств</span><span class="sxs-lookup"><span data-stu-id="5b60b-103">Describing Devices</span></span>

<span data-ttu-id="5b60b-104">Существует два способа получения объектов устройств:</span><span class="sxs-lookup"><span data-stu-id="5b60b-104">There are two ways to obtain device objects:</span></span>

-   <span data-ttu-id="5b60b-105">Использование интерфейса [**иупнпдескриптиондокумент**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) .</span><span class="sxs-lookup"><span data-stu-id="5b60b-105">Using the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) interface.</span></span> <span data-ttu-id="5b60b-106">Интерфейс **иупнпдескриптиондокумент** является единственным интерфейсом, который является надежным для сценариев.</span><span class="sxs-lookup"><span data-stu-id="5b60b-106">The **IUPnPDescriptionDocument** interface is the only interface that is safe for scripting.</span></span>
-   <span data-ttu-id="5b60b-107">Использование интерфейса [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) для получения интерфейса [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="5b60b-107">Using the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface to obtain an [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface.</span></span>

<span data-ttu-id="5b60b-108">Оба метода возвращают коллекции устройств.</span><span class="sxs-lookup"><span data-stu-id="5b60b-108">Both methods return Devices collections.</span></span> <span data-ttu-id="5b60b-109">Затем приложения используют методы устройства для получения свойств устройств.</span><span class="sxs-lookup"><span data-stu-id="5b60b-109">Applications then use the Device methods to retrieve properties about devices.</span></span>

<span data-ttu-id="5b60b-110">Приложения могут получать следующие типы данных:</span><span class="sxs-lookup"><span data-stu-id="5b60b-110">Applications are able to retrieve the following types of information:</span></span>

-   <span data-ttu-id="5b60b-111">Сведения об иерархии устройств, включая корневые устройства, родительские устройства и дочерние устройства.</span><span class="sxs-lookup"><span data-stu-id="5b60b-111">Device hierarchy information, including root devices, parent devices, and child devices.</span></span>
-   <span data-ttu-id="5b60b-112">Свойства устройства, включая Уднс, универсальные идентификаторы ресурсов (URI) и имена, доступные для чтения пользователем.</span><span class="sxs-lookup"><span data-stu-id="5b60b-112">Device properties, including UDNs, uniform resource identifiers (URIs), and user-readable names.</span></span>
-   <span data-ttu-id="5b60b-113">Сведения об изготовителе, включая имена и связанные с ними веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="5b60b-113">Manufacturer information, including names and related Web pages.</span></span>
-   <span data-ttu-id="5b60b-114">Сведения о модели, включая имя, число, UPC, серийные номера и описания устройств.</span><span class="sxs-lookup"><span data-stu-id="5b60b-114">Model information, including the name, number, UPC, serial numbers and device descriptions.</span></span>
-   <span data-ttu-id="5b60b-115">Отображение сведений, включая URL-адрес для управления устройством, и URL-адреса, с которых загружаются значки.</span><span class="sxs-lookup"><span data-stu-id="5b60b-115">Display information, including the URL to control the device, and URLs from which icons are downloaded.</span></span>
-   <span data-ttu-id="5b60b-116">Службы, предоставляемые определенным устройством.</span><span class="sxs-lookup"><span data-stu-id="5b60b-116">Services provided by a particular device.</span></span>

<span data-ttu-id="5b60b-117">Приложения также получают URL-адрес документа описания устройства с помощью интерфейса [**иупнпдевицедокументакцесс**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) .</span><span class="sxs-lookup"><span data-stu-id="5b60b-117">Applications also obtain the URL of the device description document using the [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) interface.</span></span> <span data-ttu-id="5b60b-118">Затем приложение загружает описание документа и работает со свойствами устройства и службы, которые не предоставляются интерфейсом [**иупнпдевице**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) .</span><span class="sxs-lookup"><span data-stu-id="5b60b-118">The application then load the description document and work with device and service properties that are not exposed by the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface.</span></span> <span data-ttu-id="5b60b-119">Этот интерфейс нельзя использовать в скриптах, поскольку он не является интерфейсом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b60b-119">This interface cannot be used in scripting, because it is not the default interface.</span></span>

## <a name="visual-basic-example"></a><span data-ttu-id="5b60b-120">Пример Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5b60b-120">Visual Basic Example</span></span>

<span data-ttu-id="5b60b-121">В следующем примере кода показано использование [**иупнпдевицедокументакцесс:: жетдокументурл**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="5b60b-121">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```VB
Sub GetDocumentURL()
Dim pDescDoc As IUPnPDeviceDocumentAccess
Dim strDescDocURL As String

'currentDevice is UPnPDevice object containing the current UPnP Device 
'We are trying to get IUPnPDeviceDocumentAccess interface in the UPnP Device object
Set pDescDoc = currentDevice

If Not (pDescDoc is Nothing) Then
  'Description Document URL is got from device
  strDescDocURL = pDescDoc.GetDocumentURL 
End If
```



## <a name="c-example"></a><span data-ttu-id="5b60b-122">Пример C++</span><span class="sxs-lookup"><span data-stu-id="5b60b-122">C++ Example</span></span>

<span data-ttu-id="5b60b-123">В следующем примере кода показано использование [**иупнпдевицедокументакцесс:: жетдокументурл**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="5b60b-123">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

int GetDeviceDocumentUrl () 
{
  HRESULT hr = S_OK;
  // List of interfaces needed
  IUPnPDeviceFinder *pDevFinder=NULL;
  IUPnPDevice *pDevice =NULL;
  IUPnPDeviceDocumentAccess* pDeviceDocument=NULL;
  BSTR bstrDeviceUDN =NULL;
  BSTR bstrDeviceDocumentURL = NULL; 

  bstrDeviceUDN = SysAllocString(L"uuid:234324234324");
  if(bstrDeviceUDN == NULL){
    printf("ERROR: Could not allocate memory\n");
    return -1;
  }  

  //CoInitialize the program so that we can create COM objects
  CoInitializeEx(NULL, COINIT_MULTITHREADED);

  //now try to instantiate the DeviceFinder object
  hr = CoCreateInstance(  CLSID_UPnPDeviceFinder, 
              NULL,
              CLSCTX_INPROC_SERVER,
              IID_IUPnPDeviceFinder,
              (LPVOID *) &pDevFinder); 

  if(!SUCCEEDED(hr)){
    printf("\nERROR: CoCreateInstance on IUPnPDeviceFinder returned HRESULT %x",hr);
    goto cleanup;
  }

  printf("\nGot a pointer to the IUPnPDeviceFinder Interface");

  printf("\n Finding the device of given UDN\n");
  hr =pDevFinder->FindByUDN(bstrDeviceUDN, &pDevice);
  if(hr!=S_OK)
  {
    printf("\nERROR: FindByUDN for %S returned HRESULT %x", bstrDeviceUDN, hr);
    goto cleanup;
  }

  printf("\n\tFindByUDN for device of UDN %S succeeded", bstrDeviceUDN);
  //Now query pDevice for IUPnPDeviceDocumentAccess
  hr = pDevice->QueryInterface(IID_IUPnPDeviceDocumentAccess, (VOID **)&pDeviceDocument);
  if(SUCCEEDED(hr)){
    // We have got a pointer to the IUPnPDeviceDocumentAccess interface.
    // GetDocumentURL is available only in Windows XP. 
    hr = pDeviceDocument->GetDocumentURL(&bstrDeviceDocumentURL);
    if(SUCCEEDED(hr))
      printf("\nThe Device Document URL is %S \n", bstrDeviceDocumentURL);
  }
    
cleanup:
  //release references to all interfaces 
  if(pDevFinder)
    pDevFinder->Release();
  if(pDevice)
    pDevice->Release();
  if(pDeviceDocument)
    pDeviceDocument->Release();
  
  // Free the bstr strings
  if(bstrDeviceDocumentURL)
    SysFreeString(bstrDeviceDocumentURL);
  if(bstrDeviceUDN)
    SysFreeString(bstrDeviceUDN);
  CoUninitialize();
  return 0;
}
```



 

 




