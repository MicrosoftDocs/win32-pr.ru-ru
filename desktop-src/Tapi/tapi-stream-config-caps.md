---
description: '\_ \_ Структура Cap в настройках потока TAPI \_ содержит сведения о конфигурации видео или звукового потока.'
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: Структура TAPI_STREAM_CONFIG_CAPS (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675673"
---
# <a name="tapi_stream_config_caps-structure"></a><span data-ttu-id="8494b-103">\_ \_ Структура Caps конфигурации потока TAPI \_</span><span class="sxs-lookup"><span data-stu-id="8494b-103">TAPI\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="8494b-104">\[ Эта структура недоступна для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8494b-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8494b-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="8494b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8494b-106">Структура **\_ Cap в \_ настройках \_ потока TAPI** содержит сведения о конфигурации видео или звукового потока.</span><span class="sxs-lookup"><span data-stu-id="8494b-106">The **TAPI\_STREAM\_CONFIG\_CAPS** structure contains either video or audio stream configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8494b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8494b-107">Syntax</span></span>


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="8494b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8494b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8494b-109">**капстипе**</span><span class="sxs-lookup"><span data-stu-id="8494b-109">**CapsType**</span></span>
</dt> <dd>

<span data-ttu-id="8494b-110">Определяет, содержит ли член объединения данные видео или аудио.</span><span class="sxs-lookup"><span data-stu-id="8494b-110">Defines whether the union member contains video or audio information.</span></span>

</dd> <dt>

<span data-ttu-id="8494b-111">**видеокап**</span><span class="sxs-lookup"><span data-stu-id="8494b-111">**VideoCap**</span></span>
</dt> <dd>

<span data-ttu-id="8494b-112">Структура [**\_ \_ \_ \_ Caps конфигурации потока видео TAPI**](tapi-video-stream-config-caps.md) , содержащая возможности потокового видео.</span><span class="sxs-lookup"><span data-stu-id="8494b-112">A [**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**](tapi-video-stream-config-caps.md) structure containing the video stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="8494b-113">**аудиокап**</span><span class="sxs-lookup"><span data-stu-id="8494b-113">**AudioCap**</span></span>
</dt> <dd>

<span data-ttu-id="8494b-114">Структура [**\_ \_ \_ \_ Caps конфигурации аудио-потока TAPI**](tapi-audio-stream-config-caps.md) , содержащая возможности аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="8494b-114">A [**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**](tapi-audio-stream-config-caps.md) structure containing the audio stream capabilities.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8494b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8494b-115">Requirements</span></span>



| <span data-ttu-id="8494b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8494b-116">Requirement</span></span> | <span data-ttu-id="8494b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8494b-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8494b-118">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8494b-118">TAPI version</span></span><br/> | <span data-ttu-id="8494b-119">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="8494b-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="8494b-120">Header</span><span class="sxs-lookup"><span data-stu-id="8494b-120">Header</span></span><br/>       | <dl> <span data-ttu-id="8494b-121"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8494b-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8494b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8494b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8494b-123">**Итформатконтрол:: Жетстреамкапс**</span><span class="sxs-lookup"><span data-stu-id="8494b-123">**ITFormatControl::GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[<span data-ttu-id="8494b-124">**стреамконфигкапстипе**</span><span class="sxs-lookup"><span data-stu-id="8494b-124">**StreamConfigCapsType**</span></span>](streamconfigcapstype.md)
</dt> <dt>

[<span data-ttu-id="8494b-125">**\_ \_ \_ политики настройки потока видео \_ TAPI**</span><span class="sxs-lookup"><span data-stu-id="8494b-125">**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-video-stream-config-caps.md)
</dt> <dt>

[<span data-ttu-id="8494b-126">**\_ \_ \_ ограничения конфигурации аудио потока \_ TAPI**</span><span class="sxs-lookup"><span data-stu-id="8494b-126">**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




