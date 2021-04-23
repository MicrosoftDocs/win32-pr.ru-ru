---
description: Внешние интерфейсы устройств для цифровых видеокамер
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Внешние интерфейсы устройств для цифровых видеокамер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e7106ec6e9b744da0d1f71958aeb895ec8df1a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909802"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="b0894-103">Внешние интерфейсы устройств для цифровых видеокамер</span><span class="sxs-lookup"><span data-stu-id="b0894-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="b0894-104">Фильтр [записи видео WDM](wdm-video-capture-filter.md) предоставляет три интерфейса для управления видеокамерой.</span><span class="sxs-lookup"><span data-stu-id="b0894-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



| <span data-ttu-id="b0894-105">Метка</span><span class="sxs-lookup"><span data-stu-id="b0894-105">Label</span></span> | <span data-ttu-id="b0894-106">Значение</span><span class="sxs-lookup"><span data-stu-id="b0894-106">Value</span></span> |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="b0894-107">**иамекстдевице**</span><span class="sxs-lookup"><span data-stu-id="b0894-107">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="b0894-108">Базовый интерфейс для внешнего управления устройством.</span><span class="sxs-lookup"><span data-stu-id="b0894-108">The base interface for external device control.</span></span> |
| [<span data-ttu-id="b0894-109">**иамексттранспорт**</span><span class="sxs-lookup"><span data-stu-id="b0894-109">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="b0894-110">Управляет функциями ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="b0894-110">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="b0894-111">**иамтимекодереадер**</span><span class="sxs-lookup"><span data-stu-id="b0894-111">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="b0894-112">Считывает код времени с устройства.</span><span class="sxs-lookup"><span data-stu-id="b0894-112">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="b0894-113">Чтобы использовать эти интерфейсы с драйвером видеокамеры МСДВ, включите в проект файл заголовка Кспртдефс. h.</span><span class="sxs-lookup"><span data-stu-id="b0894-113">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="b0894-114">После выбора устройства записи и создания экземпляра фильтра записи запросите фильтр для этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="b0894-114">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="b0894-115">В следующем примере объявляется пользовательская структура, содержащая указатели интерфейса, а также логические значения, определяющие доступность каждого интерфейса:</span><span class="sxs-lookup"><span data-stu-id="b0894-115">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b0894-116">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b0894-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0894-117">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="b0894-117">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



