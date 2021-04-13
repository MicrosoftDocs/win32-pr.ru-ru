---
description: Свойство PKEY \_ аудиоендпоинт \_ disable \_ сисфкс указывает, включены ли системные эффекты в потоке общего режима, который передается на устройство конечной точки аудио или с него.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142241"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a><span data-ttu-id="35721-103">PKEY \_ аудиоендпоинт \_ Отключить \_ сисфкс</span><span class="sxs-lookup"><span data-stu-id="35721-103">PKEY\_AudioEndpoint\_Disable\_SysFx</span></span>

<span data-ttu-id="35721-104">Свойство **PKEY \_ аудиоендпоинт \_ disable \_ сисфкс** указывает, включены ли системные эффекты в потоке общего режима, который передается на устройство конечной точки аудио или с него.</span><span class="sxs-lookup"><span data-stu-id="35721-104">The **PKEY\_AudioEndpoint\_Disable\_SysFx** property specifies whether system effects are enabled in the shared-mode stream that flows to or from the audio endpoint device.</span></span>

<span data-ttu-id="35721-105">Системные эффекты реализуются как объекты обработки звука (APOs), которые можно вставить в аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="35721-105">System effects are implemented as audio processing objects (APOs) that can be inserted into an audio stream.</span></span> <span data-ttu-id="35721-106">APOs — это программные модули, выполняющие функции обработки звука, такие как управление томами и преобразование форматов.</span><span class="sxs-lookup"><span data-stu-id="35721-106">APOs are software modules that perform audio processing functions such as volume control and format conversion.</span></span> <span data-ttu-id="35721-107">Отключение системных эффектов для устройства конечной точки позволяет соответствующему потоку проходить через узел «APOs без изменений».</span><span class="sxs-lookup"><span data-stu-id="35721-107">Disabling the system effects for an endpoint device enables the associated stream to pass through the APOs unmodified.</span></span>

<span data-ttu-id="35721-108">Дополнительные сведения о системных эффектах в Windows Vista см. в технических документах под названием "пользовательские звуковые эффекты в Windows Vista" и "повторное использование Windows Vista Audio System Effects" на веб-сайте [технологии аудио устройства для Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="35721-108">For more information about system effects in Windows Vista, see the white papers titled "Custom Audio Effects in Windows Vista" and "Reusing Windows Vista Audio System Effects" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="35721-109">Это свойство применимо только к локальным результатам и глобальным эффектам, которые были установлены с помощью INF-файла, установившего звуковой адаптер, к которому подключено устройство конечной точки.</span><span class="sxs-lookup"><span data-stu-id="35721-109">This property applies only to the local-effects and global-effects APOs that were installed by the .inf file that installed the audio adapter to which the endpoint device is connected.</span></span> <span data-ttu-id="35721-110">Кроме того, это свойство влияет только на целевое устройство конечной точки — оно не влияет на системные эффекты для других устройств конечных точек, даже если они подключаются к одному адаптеру.</span><span class="sxs-lookup"><span data-stu-id="35721-110">In addition, this property affects only the target endpoint device—it has no effect on the system effects for any other endpoint devices, even if they connect to the same adapter.</span></span>

<span data-ttu-id="35721-111">Элементу **VT** структуры **пропвариант** присвоено значение **VT \_ UI4**.</span><span class="sxs-lookup"><span data-stu-id="35721-111">The **vt** member of the **PROPVARIANT** structure is set to **VT\_UI4**.</span></span>

<span data-ttu-id="35721-112">Элемент **улвал** структуры **пропвариант** устанавливается в значение **Endpoint \_ сисфкс \_ включено** , если системные эффекты включены, или в **конечную точку \_ сисфкс \_ отключены** , если они отключены.</span><span class="sxs-lookup"><span data-stu-id="35721-112">The **ulVal** member of the **PROPVARIANT** structure is set to **ENDPOINT\_SYSFX\_ENABLED** if system effects are enabled or to **ENDPOINT\_SYSFX\_DISABLED** if they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="35721-113">Требования</span><span class="sxs-lookup"><span data-stu-id="35721-113">Requirements</span></span>



| <span data-ttu-id="35721-114">Требование</span><span class="sxs-lookup"><span data-stu-id="35721-114">Requirement</span></span> | <span data-ttu-id="35721-115">Значение</span><span class="sxs-lookup"><span data-stu-id="35721-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35721-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35721-116">Minimum supported client</span></span><br/> | <span data-ttu-id="35721-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35721-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="35721-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35721-118">Minimum supported server</span></span><br/> | <span data-ttu-id="35721-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35721-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="35721-120">Header</span><span class="sxs-lookup"><span data-stu-id="35721-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="35721-121"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="35721-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35721-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35721-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35721-123">**Свойства конечной точки аудио**</span><span class="sxs-lookup"><span data-stu-id="35721-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="35721-124">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="35721-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




