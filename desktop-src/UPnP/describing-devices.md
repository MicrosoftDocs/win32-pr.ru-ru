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
# <a name="describing-devices"></a>Описание устройств

Существует два способа получения объектов устройств:

-   Использование интерфейса [**иупнпдескриптиондокумент**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . Интерфейс **иупнпдескриптиондокумент** является единственным интерфейсом, который является надежным для сценариев.
-   Использование интерфейса [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) для получения интерфейса [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .

Оба метода возвращают коллекции устройств. Затем приложения используют методы устройства для получения свойств устройств.

Приложения могут получать следующие типы данных:

-   Сведения об иерархии устройств, включая корневые устройства, родительские устройства и дочерние устройства.
-   Свойства устройства, включая Уднс, универсальные идентификаторы ресурсов (URI) и имена, доступные для чтения пользователем.
-   Сведения об изготовителе, включая имена и связанные с ними веб-страницы.
-   Сведения о модели, включая имя, число, UPC, серийные номера и описания устройств.
-   Отображение сведений, включая URL-адрес для управления устройством, и URL-адреса, с которых загружаются значки.
-   Службы, предоставляемые определенным устройством.

Приложения также получают URL-адрес документа описания устройства с помощью интерфейса [**иупнпдевицедокументакцесс**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) . Затем приложение загружает описание документа и работает со свойствами устройства и службы, которые не предоставляются интерфейсом [**иупнпдевице**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) . Этот интерфейс нельзя использовать в скриптах, поскольку он не является интерфейсом по умолчанию.

## <a name="visual-basic-example"></a>Пример Visual Basic

В следующем примере кода показано использование [**иупнпдевицедокументакцесс:: жетдокументурл**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).


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



## <a name="c-example"></a>Пример C++

В следующем примере кода показано использование [**иупнпдевицедокументакцесс:: жетдокументурл**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).


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



 

 




