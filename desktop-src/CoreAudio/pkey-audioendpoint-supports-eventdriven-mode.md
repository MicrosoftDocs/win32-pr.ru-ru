---
description: Свойство PKEY \_ аудиоендпоинт \_ поддерживает режим \_ EventDriven, указывающее, \_ поддерживает ли конечная точка в режиме, управляемом событиями.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990723"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a><span data-ttu-id="c79f9-103">PKEY \_ аудиоендпоинт \_ поддерживает \_ \_ режим EventDriven</span><span class="sxs-lookup"><span data-stu-id="c79f9-103">PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode</span></span>

<span data-ttu-id="c79f9-104">Свойство **PKEY \_ аудиоендпоинт \_ поддерживает \_ режим \_ EventDriven** , указывающее, поддерживает ли конечная точка в режиме, управляемом событиями.</span><span class="sxs-lookup"><span data-stu-id="c79f9-104">The **PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode** property indicates whether the endpoint supports the event-driven mode.</span></span>

<span data-ttu-id="c79f9-105">Элементу **VT** структуры **пропвариант** присвоено значение VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="c79f9-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="c79f9-106">Элемент **уинтвал** структуры **Пропвариант** — это **DWORD** , указывающий, поддерживает ли конечная точка режим, управляемый событиями.</span><span class="sxs-lookup"><span data-stu-id="c79f9-106">The **uintVal** member of the **PROPVARIANT** structure is a **DWORD** that indicates if the endpoint supports the event-driven mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="c79f9-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c79f9-107">Remarks</span></span>

<span data-ttu-id="c79f9-108">Это значение свойства заполняется аудио-ПРОИЗВОДИТЕЛем в INF-файле, чтобы указать, что оборудование Хдаудио поддерживает режим, управляемый событиями, согласно требованию WHQL.</span><span class="sxs-lookup"><span data-stu-id="c79f9-108">This property value is populated by an audio OEM in an .inf file to indicate that the HDAudio hardware supports event driven mode as per the WHQL requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="c79f9-109">Требования</span><span class="sxs-lookup"><span data-stu-id="c79f9-109">Requirements</span></span>



| <span data-ttu-id="c79f9-110">Требование</span><span class="sxs-lookup"><span data-stu-id="c79f9-110">Requirement</span></span> | <span data-ttu-id="c79f9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c79f9-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c79f9-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c79f9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c79f9-113">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c79f9-113">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c79f9-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c79f9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c79f9-115">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c79f9-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c79f9-116">Header</span><span class="sxs-lookup"><span data-stu-id="c79f9-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c79f9-117"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c79f9-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c79f9-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c79f9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c79f9-119">**Свойства конечной точки аудио**</span><span class="sxs-lookup"><span data-stu-id="c79f9-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="c79f9-120">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="c79f9-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




