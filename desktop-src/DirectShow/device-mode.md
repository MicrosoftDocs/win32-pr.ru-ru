---
description: Режим устройства
ms.assetid: d56021be-616b-41cd-8cf0-9e0d314f62cd
title: Режим устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4657fbb49e2619d75911c18185109805116b9647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495780"
---
# <a name="device-mode"></a><span data-ttu-id="a0cf3-103">Режим устройства</span><span class="sxs-lookup"><span data-stu-id="a0cf3-103">Device Mode</span></span>

<span data-ttu-id="a0cf3-104">IEEE 1394 и USB-видеокамеры могут переключаться между режимами камеры и видеомагнитофона (Втр).</span><span class="sxs-lookup"><span data-stu-id="a0cf3-104">IEEE 1394 and USB camcorders can switch between camera mode and video tape recorder (VTR) mode.</span></span> <span data-ttu-id="a0cf3-105">При переключении в режим видеокамеры IEEE 1394 устройство сбрасывается, и приложение должно повторно перечислить его.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-105">When an IEEE 1394 camcorder switches modes, the device resets and the application must enumerate it again.</span></span> <span data-ttu-id="a0cf3-106">Приложение не может переключать режим программным способом.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-106">There is no way for an application to switch the mode programmatically.</span></span> <span data-ttu-id="a0cf3-107">USB-видеокамеры, с другой стороны, могут переключаться между режимами Camera и Втр без сброса, а приложение может изменить режим.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-107">USB camcorders, on the other hand, can switch between camera and VTR modes without resetting, and the application can change the mode.</span></span>

<span data-ttu-id="a0cf3-108">**Драйвер МСДВ**</span><span class="sxs-lookup"><span data-stu-id="a0cf3-108">**MSDV Driver**</span></span>

<span data-ttu-id="a0cf3-109">Чтобы получить текущий режим на устройстве IEEE 1394, вызовите метод [**иамекстдевице:: capability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) с \_ типом устройства value ED девкап \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a0cf3-109">To get the current mode on an IEEE 1394 device, call the [**IAMExtDevice::GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) method with the value ED\_DEVCAP\_DEVICE\_TYPE.</span></span> <span data-ttu-id="a0cf3-110">Если метод возвращает значение ED \_ девтипе \_ видеомагнитофона, устройство находится в режиме Втр и имеет такие функции, как пауза, остановка, перемотка вперед и назад.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-110">If the method returns the value ED\_DEVTYPE\_VCR, the device is in VTR mode and has functions such as pause, stop, fast-forward, and rewind.</span></span> <span data-ttu-id="a0cf3-111">В противном случае, если метод \_ возвращает \_ камеру девтипе, устройство находится в режиме камеры.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-111">Otherwise, if the method returns ED\_DEVTYPE\_CAMERA, the device is in camera mode.</span></span> <span data-ttu-id="a0cf3-112">В следующем примере кода показано, как запросить тип устройства.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-112">The following code example shows how to query the device type:</span></span>


```C++
if (MyDevCap.bHasDevice) 
{
    LONG lDeviceType = 0;
    MyDevCap.pDevice->GetCapability(ED_DEVCAP_DEVICE_TYPE, &lDeviceType, 0);

    if (lDeviceType == ED_DEVTYPE_VCR) 
    {
        // Device is a VTR. Enable all VTR functions.
    }
    else 
    {
        // Device is a camera. 
        // Enable record and record-pause; disable other functions.
    }
}
```



<span data-ttu-id="a0cf3-113">Если видеокамера переходит в автономный режим, следует запросить ее снова, когда она станет доступной.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-113">If the camcorder goes offline, you should query it again when it next becomes available.</span></span> <span data-ttu-id="a0cf3-114">При удалении устройства диспетчер графа фильтров отправляет событие [**EC об \_ \_ потере устройства**](ec-device-lost.md) .</span><span class="sxs-lookup"><span data-stu-id="a0cf3-114">The filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event when the device is removed.</span></span>

<span data-ttu-id="a0cf3-115">**Драйвер УВК**</span><span class="sxs-lookup"><span data-stu-id="a0cf3-115">**UVC Driver**</span></span>

<span data-ttu-id="a0cf3-116">Так как видеоустройства USB могут переключать режимы без сброса, код, приведенный в предыдущих примерах, не может быть надежным для USB-устройств.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-116">Because USB video devices can switch modes without resetting, the code shown in the previous examples is not reliable for USB devices.</span></span> <span data-ttu-id="a0cf3-117">Вместо этого [**используйте интерфейс,**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) чтобы получить текущий режим.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-117">Instead, use the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface to get the current mode.</span></span> <span data-ttu-id="a0cf3-118">Этот интерфейс также можно использовать для переключения режимов программным способом, если устройство поддерживает его.</span><span class="sxs-lookup"><span data-stu-id="a0cf3-118">You can also use this interface to switch modes programmatically if the device supports it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0cf3-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a0cf3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0cf3-120">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="a0cf3-120">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



