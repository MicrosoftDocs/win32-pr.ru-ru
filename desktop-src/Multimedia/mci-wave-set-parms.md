---
title: Структура MCI_WAVE_SET_PARMS (МЦиапи. h)
description: '\_ \_ \_ Структура пармс набора звукозаписи MCI содержит сведения для команды MCI \_ Set для устройств аудио-Audio.'
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- MCI_WAVE_SET_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11446eda931da1a645b9bb6218c93898862b59bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892578"
---
# <a name="mci_wave_set_parms-structure"></a><span data-ttu-id="74473-104">\_ \_ Структура пармс набора ЗВУКОзаписи MCI \_</span><span class="sxs-lookup"><span data-stu-id="74473-104">MCI\_WAVE\_SET\_PARMS structure</span></span>

<span data-ttu-id="74473-105">Структура **\_ \_ \_ Пармс набора** звукозаписи MCI содержит сведения для команды [**MCI \_ Set**](mci-set.md) для устройств аудио-Audio.</span><span class="sxs-lookup"><span data-stu-id="74473-105">The **MCI\_WAVE\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="74473-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74473-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="74473-107">Члены</span><span class="sxs-lookup"><span data-stu-id="74473-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="74473-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="74473-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="74473-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="74473-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="74473-110">**двтимеформат**</span><span class="sxs-lookup"><span data-stu-id="74473-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="74473-111">Формат времени устройства.</span><span class="sxs-lookup"><span data-stu-id="74473-111">Device's time format.</span></span>

</dd> <dt>

<span data-ttu-id="74473-112">**дваудио**</span><span class="sxs-lookup"><span data-stu-id="74473-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="74473-113">Номер канала для выходных данных звука.</span><span class="sxs-lookup"><span data-stu-id="74473-113">Channel number for audio output.</span></span> <span data-ttu-id="74473-114">Обычно используется при включении или отключении канала.</span><span class="sxs-lookup"><span data-stu-id="74473-114">Typically used when turning a channel on or off.</span></span>

</dd> <dt>

<span data-ttu-id="74473-115">**винпут**</span><span class="sxs-lookup"><span data-stu-id="74473-115">**wInput**</span></span>
</dt> <dd>

<span data-ttu-id="74473-116">Входной канал звука.</span><span class="sxs-lookup"><span data-stu-id="74473-116">Audio input channel.</span></span>

</dd> <dt>

<span data-ttu-id="74473-117">**ваутпут**</span><span class="sxs-lookup"><span data-stu-id="74473-117">**wOutput**</span></span>
</dt> <dd>

<span data-ttu-id="74473-118">Используемое устройство вывода.</span><span class="sxs-lookup"><span data-stu-id="74473-118">Output device to use.</span></span> <span data-ttu-id="74473-119">Например, это значение может быть равно 2, если в системе имеется две установленные звуковые карты.</span><span class="sxs-lookup"><span data-stu-id="74473-119">For example, this value could be 2 if a system had two installed sound cards.</span></span>

</dd> <dt>

<span data-ttu-id="74473-120">**вформаттаг**</span><span class="sxs-lookup"><span data-stu-id="74473-120">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="74473-121">Формат данных звуковой волны, например \_ Формат \_ PCM.</span><span class="sxs-lookup"><span data-stu-id="74473-121">Format of the waveform-audio data, such as WAVE\_FORMAT\_PCM.</span></span> <span data-ttu-id="74473-122">Возможные значения определены в Ммрег. h.</span><span class="sxs-lookup"><span data-stu-id="74473-122">Possible values are defined in Mmreg.h.</span></span>

</dd> <dt>

<span data-ttu-id="74473-123">**wReserved2**</span><span class="sxs-lookup"><span data-stu-id="74473-123">**wReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="74473-124">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="74473-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="74473-125">**нчаннелс**</span><span class="sxs-lookup"><span data-stu-id="74473-125">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="74473-126">Моно (1) или стерео (2).</span><span class="sxs-lookup"><span data-stu-id="74473-126">Mono (1) or stereo (2).</span></span>

</dd> <dt>

<span data-ttu-id="74473-127">**wReserved3**</span><span class="sxs-lookup"><span data-stu-id="74473-127">**wReserved3**</span></span>
</dt> <dd>

<span data-ttu-id="74473-128">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="74473-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="74473-129">**нсамплесперсек**</span><span class="sxs-lookup"><span data-stu-id="74473-129">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="74473-130">Выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="74473-130">Samples per second.</span></span>

</dd> <dt>

<span data-ttu-id="74473-131">**навгбитесперсек**</span><span class="sxs-lookup"><span data-stu-id="74473-131">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="74473-132">Частота выборки в байтах в секунду.</span><span class="sxs-lookup"><span data-stu-id="74473-132">Sample rate in bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="74473-133">**нблоккалигн**</span><span class="sxs-lookup"><span data-stu-id="74473-133">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="74473-134">Заблокируйте выравнивание данных.</span><span class="sxs-lookup"><span data-stu-id="74473-134">Block alignment of the data.</span></span>

</dd> <dt>

<span data-ttu-id="74473-135">**wReserved4**</span><span class="sxs-lookup"><span data-stu-id="74473-135">**wReserved4**</span></span>
</dt> <dd>

<span data-ttu-id="74473-136">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="74473-136">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="74473-137">**вбитсперсампле**</span><span class="sxs-lookup"><span data-stu-id="74473-137">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="74473-138">Бит на выборку.</span><span class="sxs-lookup"><span data-stu-id="74473-138">Bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="74473-139">**wReserved5**</span><span class="sxs-lookup"><span data-stu-id="74473-139">**wReserved5**</span></span>
</dt> <dd>

<span data-ttu-id="74473-140">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="74473-140">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74473-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74473-141">Remarks</span></span>

<span data-ttu-id="74473-142">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="74473-142">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="74473-143">Требования</span><span class="sxs-lookup"><span data-stu-id="74473-143">Requirements</span></span>



| <span data-ttu-id="74473-144">Требование</span><span class="sxs-lookup"><span data-stu-id="74473-144">Requirement</span></span> | <span data-ttu-id="74473-145">Значение</span><span class="sxs-lookup"><span data-stu-id="74473-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74473-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74473-146">Minimum supported client</span></span><br/> | <span data-ttu-id="74473-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="74473-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="74473-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74473-148">Minimum supported server</span></span><br/> | <span data-ttu-id="74473-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="74473-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74473-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="74473-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="74473-151"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="74473-151"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74473-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74473-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74473-153">**MCI**</span><span class="sxs-lookup"><span data-stu-id="74473-153">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="74473-154">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="74473-154">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="74473-155">**\_набор MCI**</span><span class="sxs-lookup"><span data-stu-id="74473-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="74473-156">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74473-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

