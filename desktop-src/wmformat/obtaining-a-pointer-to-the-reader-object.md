---
title: Получение указателя на объект Reader (пакет SDK для Windows Media Format 11)
description: Получение указателя на объект Reader
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Пакет SDK для Windows Media Format, DirectShow
- Windows Media Format SDK, объекты Reader
- Windows Media Format SDK, интерфейс IWMReaderAdvanced2
- Расширенный системный формат (ASF), DirectShow
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
ms.openlocfilehash: 63e0bb6611ba1d4e3c41fb2c00a68dd9c898505f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340105"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a>Получение указателя на объект Reader (пакет SDK для Windows Media Format 11)

В некоторых случаях, например при определении расширений единиц обработки данных, установленных для данного потока, может потребоваться доступ к [объекту Reader](reader-object.md) пакета SDK формата Windows Media напрямую. Следующая функция показывает, как получить интерфейс [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) для самого объекта Reader:


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



 

 




