---
title: Получение указателя на объект Reader (пакет SDK для Windows Media Format 11)
description: Узнайте, как получить указатель на объект Reader пакета SDK Windows Media Format с помощью интерфейса IWMReaderAdvanced2.
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
ms.openlocfilehash: 6dd31bd868365b87b38eefd0c0c81e8beafef51c
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989139"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a><span data-ttu-id="07fb4-119">Получение указателя на объект Reader (пакет SDK для Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="07fb4-119">Obtaining a Pointer to the Reader Object (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="07fb4-120">В некоторых случаях, например при определении расширений единиц обработки данных, установленных для данного потока, может потребоваться доступ к [объекту Reader](reader-object.md) пакета SDK формата Windows Media напрямую.</span><span class="sxs-lookup"><span data-stu-id="07fb4-120">In certain cases, for example when determining which data unit extensions are set on a given stream, you may need to access the [Reader Object](reader-object.md) of the Windows Media Format SDK directly.</span></span> <span data-ttu-id="07fb4-121">Следующая функция показывает, как получить интерфейс [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) для самого объекта Reader:</span><span class="sxs-lookup"><span data-stu-id="07fb4-121">The following function shows how to obtain the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface on the Reader Object itself:</span></span>


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



 

 




