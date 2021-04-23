---
description: Восстановление после ошибки Invalid-Device (пространственный звук)
title: Восстановление после ошибки Invalid-Device (пространственный звук)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142412"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a><span data-ttu-id="825ca-103">Восстановление после ошибки Invalid-Device (пространственный звук)</span><span class="sxs-lookup"><span data-stu-id="825ca-103">Recovering from an Invalid-Device Error (Spatial Sound)</span></span>

<span data-ttu-id="825ca-104">Многие методы API-интерфейса пространственного звука (Майкрософт), такие как [испатиалаудиоклиент](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [испатиалаудиубжектрендерстреам](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)и [испатиалаудиубжект](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), возвращают коды ошибок, если устройство конечной точки аудио, используемое клиентским приложением, становится недопустимым или в конечной точке изменился формат пространственного звука.</span><span class="sxs-lookup"><span data-stu-id="825ca-104">Many of the methods of the Microsoft Spatial Audio API, such as [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream), and [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), return error codes if the audio endpoint device that the client application is using becomes invalid or the spatial audio rendering format is changed on the endpoint.</span></span> <span data-ttu-id="825ca-105">Эти коды ошибок указывают на то, что устройство конечной точки было отключено или перенастроено, отключено, удалено, режим пространственного звука или же недоступно для использования.</span><span class="sxs-lookup"><span data-stu-id="825ca-105">These error codes indicates that the endpoint device has been unplugged, or that the audio hardware or associated hardware resources have been reconfigured, disabled, removed, spatial audio mode is changed or otherwise made unavailable for use.</span></span> <span data-ttu-id="825ca-106">Часто приложение может восстановиться после этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="825ca-106">Frequently, the application can recover from this error.</span></span>

<span data-ttu-id="825ca-107">Коды ошибок, указывающие на ошибку недопустимого устройства, включают следующее:</span><span class="sxs-lookup"><span data-stu-id="825ca-107">Error codes that indicate an invalid-device error include the following:</span></span>

- <span data-ttu-id="825ca-108">SPTLAUDCLNT_E_DESTROYED</span><span class="sxs-lookup"><span data-stu-id="825ca-108">SPTLAUDCLNT_E_DESTROYED</span></span>
- <span data-ttu-id="825ca-109">AUDCLNT_E_DEVICE_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="825ca-109">AUDCLNT_E_DEVICE_INVALIDATED</span></span>
- <span data-ttu-id="825ca-110">AUDCLNT_E_RESOURCES_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="825ca-110">AUDCLNT_E_RESOURCES_INVALIDATED</span></span>
- <span data-ttu-id="825ca-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span><span class="sxs-lookup"><span data-stu-id="825ca-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span></span>
- <span data-ttu-id="825ca-112">SPTLAUDCLNT_E_INTERNAL</span><span class="sxs-lookup"><span data-stu-id="825ca-112">SPTLAUDCLNT_E_INTERNAL</span></span>

## <a name="strategies-for-handling-invalid-device-errors"></a><span data-ttu-id="825ca-113">Стратегии обработки недопустимых ошибок устройства</span><span class="sxs-lookup"><span data-stu-id="825ca-113">Strategies for handling invalid-device errors</span></span>

<span data-ttu-id="825ca-114">Рекомендуемая стратегия восстановления после ошибки недопустимого устройства зависит от того, будет ли приложение автоматически выбирать определенное устройство в соответствии с внутренними требованиями или пользователь может явно выбрать устройство из списка доступных устройств.</span><span class="sxs-lookup"><span data-stu-id="825ca-114">The recommended strategy for recovering from an invalid-device error depends on whether the application automatically selects a specific device based on internal requirements or it allows the user to explicitly select a device from a list of available devices.</span></span> 

### <a name="default-audio-device"></a><span data-ttu-id="825ca-115">Звуковое устройство по умолчанию</span><span class="sxs-lookup"><span data-stu-id="825ca-115">Default audio device</span></span>

<span data-ttu-id="825ca-116">Если приложение автоматически выбирает устройство по умолчанию, выполните следующие действия для восстановления.</span><span class="sxs-lookup"><span data-stu-id="825ca-116">If the application automatically selects the default device, use the following steps to recover.</span></span>

1. <span data-ttu-id="825ca-117">Освободите интерфейс [испатиалаудиубжектрендерстреам](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) и [испатиалаудиоклиент](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) и любые другие пространственные аудио интерфейсы, используемые для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="825ca-117">Release the [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) and [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interface and any other spatial audio interfaces that are used for rendering.</span></span> 
1. <span data-ttu-id="825ca-118">Вызовите [иммдевицеенумератор:: жетдефаултаудиоендпоинт](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , чтобы получить текущее звуковое устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="825ca-118">Call [IMMDeviceEnumerator::GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the current default audio device.</span></span>
1. <span data-ttu-id="825ca-119">Попытка активировать **испатиалаудиоклиент** на звуковом устройстве.</span><span class="sxs-lookup"><span data-stu-id="825ca-119">Attempt to activate **ISpatialAudioClient** on the audio device.</span></span>
1. <span data-ttu-id="825ca-120">Активация **испатиалаудиубжектрендерстреам**.</span><span class="sxs-lookup"><span data-stu-id="825ca-120">Activate **ISpatialAudioObjectRenderStream**.</span></span> 

### <a name="specifically-selected-audio-device"></a><span data-ttu-id="825ca-121">Конкретное выбранное звуковое устройство</span><span class="sxs-lookup"><span data-stu-id="825ca-121">Specifically selected audio device</span></span>

<span data-ttu-id="825ca-122">Если приложение выбирает определенное звуковое устройство, выполните следующие действия для восстановления.</span><span class="sxs-lookup"><span data-stu-id="825ca-122">If the application selects a specific audio device, use the following steps to recover.</span></span>

1. <span data-ttu-id="825ca-123">Освободите интерфейс Испатиалаудиубжектрендерстреам и любые другие пространственные аудио интерфейсы, которые используются для отрисовки, но не выпускайте **испатиалаудиоклиент**.</span><span class="sxs-lookup"><span data-stu-id="825ca-123">Release the ISpatialAudioObjectRenderStream interface and any other spatial audio interfaces that are used for rendering, but don't release **ISpatialAudioClient**.</span></span>
1. <span data-ttu-id="825ca-124">Используйте текущий экземпляр **испатиалаудиоклиент** для активации **испатиалаудиубжектрендерстреам**.</span><span class="sxs-lookup"><span data-stu-id="825ca-124">Use the current **ISpatialAudioClient** instance to activate **ISpatialAudioObjectRenderStream**.</span></span>

<span data-ttu-id="825ca-125">Обратите внимание, что для обеих стратегий, перечисленных выше, одни и те же действия можно применить к приложениям, использующим интерфейсы [испатиалаудиубжектрендерстреамформетадата](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) или [испатиалаудиубжектрендерстреамфорхртф](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) .</span><span class="sxs-lookup"><span data-stu-id="825ca-125">Note that for both strategies listed above, the same steps can be applied to applications that use the [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) or [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) interfaces.</span></span> <span data-ttu-id="825ca-126">Просто замените **испатиалаудиубжектрендерстреам** в описанных выше шагах на интерфейсы Metadata или хртф.</span><span class="sxs-lookup"><span data-stu-id="825ca-126">Simply replace **ISpatialAudioObjectRenderStream** in the above steps with the metadata or Hrtf interfaces.</span></span>


## <a name="related-topics"></a><span data-ttu-id="825ca-127">См. также</span><span class="sxs-lookup"><span data-stu-id="825ca-127">Related topics</span></span>

<dl> <span data-ttu-id="825ca-128"><dt>
[Восстановление после ошибки Invalid-Device](recovering-from-an-invalid-device-error.md) 
 [Управление потоками](stream-management.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="825ca-128"><dt>
[Recovering from an Invalid-Device Error](recovering-from-an-invalid-device-error.md)
[Stream Management](stream-management.md)
</dt> </span></span></dl>

 

 



