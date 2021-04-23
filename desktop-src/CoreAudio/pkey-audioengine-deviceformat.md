---
description: Свойство PKEY \_ аудиоенгине \_ девицеформат определяет формат устройства, который является форматом, выбранным пользователем для потока, который передается между обработчиком аудио и устройством конечной точки аудио, когда устройство работает в режиме общего доступа.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807828"
---
# <a name="pkey_audioengine_deviceformat"></a><span data-ttu-id="9f1dd-103">PKEY \_ аудиоенгине \_ девицеформат</span><span class="sxs-lookup"><span data-stu-id="9f1dd-103">PKEY\_AudioEngine\_DeviceFormat</span></span>

<span data-ttu-id="9f1dd-104">Свойство **PKEY \_ аудиоенгине \_ девицеформат** определяет формат устройства, который является форматом, выбранным пользователем для потока, который передается между обработчиком аудио и устройством конечной точки аудио, когда устройство работает в режиме общего доступа.</span><span class="sxs-lookup"><span data-stu-id="9f1dd-104">The **PKEY\_AudioEngine\_DeviceFormat** property specifies the device format, which is the format that the user has selected for the stream that flows between the audio engine and the audio endpoint device when the device operates in shared mode.</span></span> <span data-ttu-id="9f1dd-105">Этот формат может быть не лучшим форматом по умолчанию для использования в приложениях с монопольным режимом.</span><span class="sxs-lookup"><span data-stu-id="9f1dd-105">This format might not be the best default format for an exclusive-mode application to use.</span></span> <span data-ttu-id="9f1dd-106">Как правило, приложение с монопольным режимом находит подходящий формат устройства, выполнив некоторое количество вызовов метода [**иаудиоклиент:: исформатсуппортед**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="9f1dd-106">Typically, an exclusive-mode application finds a suitable device format by making some number of calls to the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method.</span></span> <span data-ttu-id="9f1dd-107">Дополнительные сведения см. в разделе [форматы устройств](device-formats.md).</span><span class="sxs-lookup"><span data-stu-id="9f1dd-107">For more information, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="9f1dd-108">Элементу **VT** структуры **пропвариант** задано значение VT \_ BLOB.</span><span class="sxs-lookup"><span data-stu-id="9f1dd-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="9f1dd-109">Членом **большого двоичного объекта** структуры **пропвариант** является структура типа **BLOB** , содержащая два члена.</span><span class="sxs-lookup"><span data-stu-id="9f1dd-109">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="9f1dd-110">Member **BLOB. кбсизе** — это **DWORD** , указывающий число байтов в описании формата.</span><span class="sxs-lookup"><span data-stu-id="9f1dd-110">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="9f1dd-111">Member **BLOB. пблобдата** указывает на структуру **вавеформатекс** , содержащую описание формата.</span><span class="sxs-lookup"><span data-stu-id="9f1dd-111">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="9f1dd-112">Дополнительные сведения о **большом двоичном объекте** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9f1dd-112">For more information about **BLOB**, see the Windows SDK documentation.</span></span> <span data-ttu-id="9f1dd-113">Дополнительные сведения о **вавеформатекс** см. в документации по Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="9f1dd-113">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f1dd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9f1dd-114">Requirements</span></span>



| <span data-ttu-id="9f1dd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9f1dd-115">Requirement</span></span> | <span data-ttu-id="9f1dd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9f1dd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f1dd-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f1dd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9f1dd-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f1dd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9f1dd-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f1dd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9f1dd-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9f1dd-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9f1dd-121">Header</span><span class="sxs-lookup"><span data-stu-id="9f1dd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f1dd-122"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f1dd-122"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f1dd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f1dd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f1dd-124">**Свойства конечной точки аудио**</span><span class="sxs-lookup"><span data-stu-id="9f1dd-124">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="9f1dd-125">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="9f1dd-125">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




