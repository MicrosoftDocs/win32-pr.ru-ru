---
description: .
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Проверка поддерживаемых форматов ДКСВА-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7560d574cee5fca21ab8de78b01b87af1de5a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496845"
---
# <a name="checking-supported-dxva-hd-formats"></a><span data-ttu-id="4e4b8-103">Проверка поддерживаемых форматов ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="4e4b8-103">Checking Supported DXVA-HD Formats</span></span>

## <a name="checking-supported-input-formats"></a><span data-ttu-id="4e4b8-104">Проверка поддерживаемых форматов входных данных</span><span class="sxs-lookup"><span data-stu-id="4e4b8-104">Checking Supported Input Formats</span></span>

<span data-ttu-id="4e4b8-105">Чтобы получить список форматов входных данных, поддерживаемых устройством Microsoft DirectX Video ускорение High Definition (ДКСВА-HD), выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-105">To get a list of the input formats that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports, do the following:</span></span>

1.  <span data-ttu-id="4e4b8-106">Вызовите [**идксвахд \_ Device:: жетвидеопроцессордевицекапс**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) , чтобы получить возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-106">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="4e4b8-107">Проверьте элемент **инпутформаткаунт** структуры [**дксвахд \_ впдевкапс**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="4e4b8-107">Check the **InputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="4e4b8-108">Этот член предоставляет количество поддерживаемых входных форматов.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-108">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="4e4b8-109">Выделите массив значений **D3DFORMAT** размером **инпутформаткаунт**.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-109">Allocate an array of **D3DFORMAT** values, of size **InputFormatCount**.</span></span>
4.  <span data-ttu-id="4e4b8-110">Передайте этот массив в метод [**идксвахд \_ устройства:: жетвидеопроцессоринпутформатс**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) .</span><span class="sxs-lookup"><span data-stu-id="4e4b8-110">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) method.</span></span> <span data-ttu-id="4e4b8-111">Методы заполняют массив списком входных форматов.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-111">The methods fills the array with a list of input formats.</span></span>

<span data-ttu-id="4e4b8-112">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-112">The following code shows these steps:</span></span>


```C++
// Checks whether a DXVA-HD device supports a specified input format.

HRESULT CheckInputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[ caps.InputFormatCount ];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorInputFormats(
        caps.InputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.InputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.InputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="checking-supported-output-formats"></a><span data-ttu-id="4e4b8-113">Проверка поддерживаемых форматов выходных данных</span><span class="sxs-lookup"><span data-stu-id="4e4b8-113">Checking Supported Output Formats</span></span>

<span data-ttu-id="4e4b8-114">Чтобы получить список форматов вывода, поддерживаемых устройством ДКСВА-HD, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-114">To get a list of the output formats that the DXVA-HD device supports, do the following:</span></span>

1.  <span data-ttu-id="4e4b8-115">Вызовите [**идксвахд \_ Device:: жетвидеопроцессордевицекапс**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) , чтобы получить возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-115">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="4e4b8-116">Проверьте элемент **аутпутформаткаунт** структуры [**дксвахд \_ впдевкапс**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="4e4b8-116">Check the **OutputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="4e4b8-117">Этот член предоставляет количество поддерживаемых входных форматов.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-117">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="4e4b8-118">Выделите массив значений **D3DFORMAT** размером **аутпутформаткаунт**.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-118">Allocate an array of **D3DFORMAT** values, of size **OutputFormatCount**.</span></span>
4.  <span data-ttu-id="4e4b8-119">Передайте этот массив в метод [**идксвахд \_ устройства:: жетвидеопроцессораутпутформатс**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) .</span><span class="sxs-lookup"><span data-stu-id="4e4b8-119">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) method.</span></span> <span data-ttu-id="4e4b8-120">Методы заполняют массив списком выходных форматов.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-120">The methods fills the array with a list of output formats.</span></span>

<span data-ttu-id="4e4b8-121">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="4e4b8-121">The following code shows these steps:</span></span>


```C++
// Checks whether a DXVA-HD device supports a specified output format.

HRESULT CheckOutputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[caps.OutputFormatCount];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorOutputFormats(
        caps.OutputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.OutputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.OutputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4e4b8-122">См. также</span><span class="sxs-lookup"><span data-stu-id="4e4b8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e4b8-123">ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="4e4b8-123">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



