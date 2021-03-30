---
description: Внешние интерфейсы устройств для цифровых видеокамер
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Внешние интерфейсы устройств для цифровых видеокамер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52b6d0fe00ff91ff87e9c810bbe7ecc319e9bfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895233"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="bf45f-103">Внешние интерфейсы устройств для цифровых видеокамер</span><span class="sxs-lookup"><span data-stu-id="bf45f-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="bf45f-104">Фильтр [записи видео WDM](wdm-video-capture-filter.md) предоставляет три интерфейса для управления видеокамерой.</span><span class="sxs-lookup"><span data-stu-id="bf45f-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



|                                                |                                                 |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="bf45f-105">**иамекстдевице**</span><span class="sxs-lookup"><span data-stu-id="bf45f-105">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="bf45f-106">Базовый интерфейс для внешнего управления устройством.</span><span class="sxs-lookup"><span data-stu-id="bf45f-106">The base interface for external device control.</span></span> |
| [<span data-ttu-id="bf45f-107">**иамексттранспорт**</span><span class="sxs-lookup"><span data-stu-id="bf45f-107">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="bf45f-108">Управляет функциями ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="bf45f-108">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="bf45f-109">**иамтимекодереадер**</span><span class="sxs-lookup"><span data-stu-id="bf45f-109">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="bf45f-110">Считывает код времени с устройства.</span><span class="sxs-lookup"><span data-stu-id="bf45f-110">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="bf45f-111">Чтобы использовать эти интерфейсы с драйвером видеокамеры МСДВ, включите в проект файл заголовка Кспртдефс. h.</span><span class="sxs-lookup"><span data-stu-id="bf45f-111">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="bf45f-112">После выбора устройства записи и создания экземпляра фильтра записи запросите фильтр для этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="bf45f-112">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="bf45f-113">В следующем примере объявляется пользовательская структура, содержащая указатели интерфейса, а также логические значения, определяющие доступность каждого интерфейса:</span><span class="sxs-lookup"><span data-stu-id="bf45f-113">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


```C++
struct _MyDevCap
{
    IAMExtDevice       *pDevice;
    IAMExtTransport    *pTransport;
    IAMTimecodeReader  *pTimecode;
    BOOL                bHasDevice;
    BOOL                bHasTransport;
    BOOL                bHasTimecode;
} MyDevCap;

HRESULT hr;
IBaseFilter *pDVCam;  // Pointer to the capture filter.

// Create an instance of the capture filter (not shown).

hr = pDVCam->QueryInterface(IID_IAMExtDevice, (void **)&MyDevCap.pDevice);
MyDevCap.bHasDevice = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMExtTransport, (void **)&MyDevCap.pTransport);
MyDevCap.bHasTransport = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMTimecodeReader, (void **)&MyDevCap.pTimecode);
MyDevCap.bHasTimecode = (SUCCEEDED(hr));
```



## <a name="related-topics"></a><span data-ttu-id="bf45f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="bf45f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf45f-115">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="bf45f-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



