---
title: получение указателя на объект Reader (Windows пакет SDK для формата мультимедиа 11)
description: узнайте, как получить указатель на объект Reader пакета SDK Windows Media Format с помощью интерфейса IWMReaderAdvanced2.
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows Пакет SDK для формата мультимедиа, DirectShow
- Windows Пакет SDK для формата мультимедиа, объекты Reader
- Windows Пакет SDK для формата мультимедиа, интерфейс IWMReaderAdvanced2
- Расширенный формат систем (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный системный формат (ASF), объекты Reader
- ASF (Расширенный системный формат), объекты Reader
- Расширенный системный формат (ASF), интерфейс IWMReaderAdvanced2
- ASF (Расширенный системный формат), интерфейс IWMReaderAdvanced2
- DirectShow, объекты Reader
- DirectShow, указатели на объекты Reader
- DirectShow, интерфейс IWMReaderAdvanced2
- объекты Reader, получение указателей
- потоки, объекты Reader
- потоки, указатели на объекты Reader
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4b2829e56d08825234dcefdc4fb1012f48c894419e7c328f10afeb76cb6c4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808054"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a>получение указателя на объект Reader (Windows пакет SDK для формата мультимедиа 11)

в некоторых случаях, например при определении расширений модулей данных, установленных для данного потока, может потребоваться доступ к [объекту модуля чтения](reader-object.md) пакета SDK для Windows Media Format напрямую. Следующая функция показывает, как получить интерфейс [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) для самого объекта Reader:


```C++
HRESULT GetReaderAdvanced (IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
  // We use CComPtr's to avoid headaches at cleanup time
  CComPtr<IEnumFilters> pEnum;
  CComPtr<IBaseFilter> pFilter;
  ULONG cFetched;

  HRESULT hr = pGraph->EnumFilters(&pEnum);
  if (FAILED(hr)) 
  {
    return hr;
  }

  while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
  {
    IWMHeaderInfo *pHI = NULL;
    // Only the WM ASF Reader will have interface. This filter should be
    // the first one returned in this loop.
    hr = pFilter->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHI);
    if (SUCCEEDED(hr))
    {
      // We use the IWMDRMReader interface only as a way to get
      // a pointer to the Reader Object.
      CComPtr<IWMDRMReader> pWMDRMReader;
      CComQIPtr<IServiceProvider, &IID_IServiceProvider> pSP;

      hr = pHI->QueryInterface(__uuidof(IServiceProvider), (void**)&pSP);
      if (!pSP)
      {
        return E_NOINTERFACE;
      }
      
      hr = pSP->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader);
      if (FAILED(hr))
      {
        return hr;
      }

      CComQIPtr<IWMReaderAdvanced2, &IID_IWMReaderAdvanced2> pRA2(pWMDRMReader);
      if (pRA2)
      {
        *pReaderAdvanced2 = pRA2.Detach();
        return S_OK;
      }

    }
    pFilter.Release();
  }
  
  //if we get here, we didn't find the WM ASF Reader
  return E_FAIL;
}
```



 

 




