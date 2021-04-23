---
title: Структура MCI_VCR_SET_PARMS (видеомагнитофон. h)
description: '\_ \_ Структура ПАРМС видеомагнитофона MCI Set \_ содержит параметры для \_ команды MCI Set для устройств записи видеокассет.'
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- MCI_VCR_SET_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416013"
---
# <a name="mci_vcr_set_parms-structure"></a><span data-ttu-id="1bf45-104">\_ \_ Структура пармс набора видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="1bf45-104">MCI\_VCR\_SET\_PARMS structure</span></span>

<span data-ttu-id="1bf45-105">Структура **\_ \_ \_ пармс видеомагнитофона MCI Set** содержит параметры для команды [**MCI \_ Set**](mci-set.md) для устройств записи видеокассет.</span><span class="sxs-lookup"><span data-stu-id="1bf45-105">The **MCI\_VCR\_SET\_PARMS** structure contains parameters for the [**MCI\_SET**](mci-set.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf45-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bf45-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="1bf45-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1bf45-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1bf45-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="1bf45-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="1bf45-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-110">**двтимеформат**</span><span class="sxs-lookup"><span data-stu-id="1bf45-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-111">Текущий формат времени.</span><span class="sxs-lookup"><span data-stu-id="1bf45-111">Current time format.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-112">**дваудио**</span><span class="sxs-lookup"><span data-stu-id="1bf45-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1bf45-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-114">**двтимемоде**</span><span class="sxs-lookup"><span data-stu-id="1bf45-114">**dwTimeMode**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-115">Константа, указывающая источник времени, используемый устройством.</span><span class="sxs-lookup"><span data-stu-id="1bf45-115">Constant that specifies the timing source used by the device.</span></span> <span data-ttu-id="1bf45-116">Источник времени — это либо время, записанное на видеокассете, либо счетчики на устройстве, которые имеют смысл перемещения видеокассет.</span><span class="sxs-lookup"><span data-stu-id="1bf45-116">The timing source is either a timecode recorded on videotape, or the counters in the device that sense videotape movement.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-117">**дврекордформат**</span><span class="sxs-lookup"><span data-stu-id="1bf45-117">**dwRecordFormat**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-118">Скорость записи.</span><span class="sxs-lookup"><span data-stu-id="1bf45-118">Recording rate.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-119">**двкаунтерформат**</span><span class="sxs-lookup"><span data-stu-id="1bf45-119">**dwCounterFormat**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-120">Формат нового значения времени счетчика.</span><span class="sxs-lookup"><span data-stu-id="1bf45-120">Format of a new counter time value.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-121">**двиндекс**</span><span class="sxs-lookup"><span data-stu-id="1bf45-121">**dwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-122">Содержимое экрана.</span><span class="sxs-lookup"><span data-stu-id="1bf45-122">Contents of on-screen display.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-123">**двтраккинг**</span><span class="sxs-lookup"><span data-stu-id="1bf45-123">**dwTracking**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-124">Корректировка скорости, используемая при отслеживании скорости воспроизведения ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="1bf45-124">Speed adjustment used when tracking the VCR playback rate.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-125">**двспид**</span><span class="sxs-lookup"><span data-stu-id="1bf45-125">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-126">Скорость воспроизведения, используемая устройством в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="1bf45-126">Playback speed used by the device as an integer.</span></span> <span data-ttu-id="1bf45-127">Нормальная скорость воспроизведения составляет 1000, двойная скорость — 2000, а половина — 500.</span><span class="sxs-lookup"><span data-stu-id="1bf45-127">Normal playback speed is 1000, double speed is 2000, and half speed is 500.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-128">**двленгс**</span><span class="sxs-lookup"><span data-stu-id="1bf45-128">**dwLength**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-129">Длина видеокассеты, если на устройстве не обнаружена длина.</span><span class="sxs-lookup"><span data-stu-id="1bf45-129">Videotape length when the length is undetectable by the device.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-130">**двкаунтер**</span><span class="sxs-lookup"><span data-stu-id="1bf45-130">**dwCounter**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-131">Новое значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="1bf45-131">New counter value.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-132">**двклокк**</span><span class="sxs-lookup"><span data-stu-id="1bf45-132">**dwClock**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-133">Новое время.</span><span class="sxs-lookup"><span data-stu-id="1bf45-133">New clock time.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-134">**двпаусетимеаут**</span><span class="sxs-lookup"><span data-stu-id="1bf45-134">**dwPauseTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-135">Новое значение времени ожидания для команды Pause.</span><span class="sxs-lookup"><span data-stu-id="1bf45-135">New timeout value for pause command.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-136">**двпрероллдуратион**</span><span class="sxs-lookup"><span data-stu-id="1bf45-136">**dwPrerollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-137">Длина видеокассеты, необходимая для стабилизации выходных данных ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="1bf45-137">Videotape length needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="1bf45-138">**двпостроллдуратион**</span><span class="sxs-lookup"><span data-stu-id="1bf45-138">**dwPostrollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-139">Длина видеокассеты, необходимая для переноса данных из ВИДЕОМАГНИТОФОНА [**при \_ остановке MCI**](mci-stop.md) или при выполнении команды [**MCI \_ Pause**](mci-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="1bf45-139">Videotape length needed to brake the VCR transport when a [**MCI\_STOP**](mci-stop.md) or [**MCI\_PAUSE**](mci-pause.md) command is issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bf45-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1bf45-140">Remarks</span></span>

<span data-ttu-id="1bf45-141">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="1bf45-141">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf45-142">Требования</span><span class="sxs-lookup"><span data-stu-id="1bf45-142">Requirements</span></span>



| <span data-ttu-id="1bf45-143">Требование</span><span class="sxs-lookup"><span data-stu-id="1bf45-143">Requirement</span></span> | <span data-ttu-id="1bf45-144">Значение</span><span class="sxs-lookup"><span data-stu-id="1bf45-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1bf45-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1bf45-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf45-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1bf45-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1bf45-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1bf45-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf45-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1bf45-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1bf45-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1bf45-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bf45-150"><dt>Видеомагнитофон. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bf45-150"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bf45-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bf45-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf45-152">**MCI**</span><span class="sxs-lookup"><span data-stu-id="1bf45-152">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1bf45-153">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="1bf45-153">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="1bf45-154">**Приостановка MCI \_**</span><span class="sxs-lookup"><span data-stu-id="1bf45-154">**MCI\_PAUSE**</span></span>](mci-pause.md)
</dt> <dt>

[<span data-ttu-id="1bf45-155">**\_набор MCI**</span><span class="sxs-lookup"><span data-stu-id="1bf45-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="1bf45-156">**\_прерывание MCI**</span><span class="sxs-lookup"><span data-stu-id="1bf45-156">**MCI\_STOP**</span></span>](mci-stop.md)
</dt> <dt>

<span data-ttu-id="1bf45-157">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bf45-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

