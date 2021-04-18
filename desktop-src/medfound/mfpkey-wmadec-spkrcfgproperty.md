---
description: Указывает конфигурацию динамика на клиентском компьютере.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: Свойство MFPKEY_WMADEC_SPKRCFG (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544783"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a><span data-ttu-id="77e42-103">МФПКЭЙ \_ вмадек \_ Спкркфг, свойство</span><span class="sxs-lookup"><span data-stu-id="77e42-103">MFPKEY\_WMADEC\_SPKRCFG Property</span></span>

<span data-ttu-id="77e42-104">Указывает конфигурацию динамика на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="77e42-104">Specifies the speaker configuration on the client computer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="77e42-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="77e42-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="77e42-106">g \_ всзвмакспеакерконфиг</span><span class="sxs-lookup"><span data-stu-id="77e42-106">g\_wszWMACSpeakerConfig</span></span>

## <a name="data-type"></a><span data-ttu-id="77e42-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="77e42-107">Data Type</span></span>

<span data-ttu-id="77e42-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="77e42-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="77e42-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="77e42-109">Default Value</span></span>

<span data-ttu-id="77e42-110">Никакой конкретной конфигурации докладчика не предполагается.</span><span class="sxs-lookup"><span data-stu-id="77e42-110">No specific speaker configuration is assumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="77e42-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77e42-111">Remarks</span></span>

<span data-ttu-id="77e42-112">Это значение следует присвоить одной из констант или значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="77e42-112">You should set this value to one of the constants or values in the following table.</span></span> <span data-ttu-id="77e42-113">Константы определены в Microsoft DirectSound и перечислены здесь для удобства.</span><span class="sxs-lookup"><span data-stu-id="77e42-113">The constants are defined in Microsoft DirectSound, and are listed here for convenience.</span></span> <span data-ttu-id="77e42-114">Чтобы разрешить эти константные имена для компилятора, необходимо включить дсаунд. h.</span><span class="sxs-lookup"><span data-stu-id="77e42-114">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="77e42-115">Константа</span><span class="sxs-lookup"><span data-stu-id="77e42-115">Constant</span></span>             | <span data-ttu-id="77e42-116">Значение</span><span class="sxs-lookup"><span data-stu-id="77e42-116">Value</span></span>      | <span data-ttu-id="77e42-117">Описание</span><span class="sxs-lookup"><span data-stu-id="77e42-117">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="77e42-118">ДССПЕАКЕР \_</span><span class="sxs-lookup"><span data-stu-id="77e42-118">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="77e42-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77e42-119">0x00000000</span></span> | <span data-ttu-id="77e42-120">Звук передается напрямую, без настройки для динамиков.</span><span class="sxs-lookup"><span data-stu-id="77e42-120">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="77e42-121">\_наушники дсспеакер</span><span class="sxs-lookup"><span data-stu-id="77e42-121">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="77e42-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="77e42-122">0x00000001</span></span> | <span data-ttu-id="77e42-123">Клиентский компьютер оснащен наушниками.</span><span class="sxs-lookup"><span data-stu-id="77e42-123">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="77e42-124">ДССПЕАКЕР \_ Mono</span><span class="sxs-lookup"><span data-stu-id="77e42-124">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="77e42-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="77e42-125">0x00000002</span></span> | <span data-ttu-id="77e42-126">Клиентский компьютер оснащен моноауралным докладчиком.</span><span class="sxs-lookup"><span data-stu-id="77e42-126">The client computer is equipped with a monoaural speaker.</span></span>                    |
| <span data-ttu-id="77e42-127">ДССПЕАКЕР \_ Quad</span><span class="sxs-lookup"><span data-stu-id="77e42-127">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="77e42-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="77e42-128">0x00000003</span></span> | <span data-ttu-id="77e42-129">Клиентский компьютер оснащен куадрафоник колонками.</span><span class="sxs-lookup"><span data-stu-id="77e42-129">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="77e42-130">\_стерео дсспеакер</span><span class="sxs-lookup"><span data-stu-id="77e42-130">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="77e42-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="77e42-131">0x00000004</span></span> | <span data-ttu-id="77e42-132">Клиентский компьютер оснащен стереодинамиками.</span><span class="sxs-lookup"><span data-stu-id="77e42-132">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="77e42-133">ДССПЕАКЕР \_ вокруг</span><span class="sxs-lookup"><span data-stu-id="77e42-133">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="77e42-134">0x00000005</span><span class="sxs-lookup"><span data-stu-id="77e42-134">0x00000005</span></span> | <span data-ttu-id="77e42-135">Клиентский компьютер оснащен динамиками с четырьмя каналами.</span><span class="sxs-lookup"><span data-stu-id="77e42-135">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="77e42-136">ДССПЕАКЕР \_ 5POINT1</span><span class="sxs-lookup"><span data-stu-id="77e42-136">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="77e42-137">0x00000006</span><span class="sxs-lookup"><span data-stu-id="77e42-137">0x00000006</span></span> | <span data-ttu-id="77e42-138">Клиентский компьютер оснащен пятью динамиками и сабвуфером.</span><span class="sxs-lookup"><span data-stu-id="77e42-138">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="77e42-139">ДССПЕАКЕР \_ 7POINT1</span><span class="sxs-lookup"><span data-stu-id="77e42-139">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="77e42-140">0x00000007</span><span class="sxs-lookup"><span data-stu-id="77e42-140">0x00000007</span></span> | <span data-ttu-id="77e42-141">Клиентский компьютер оснащен семью динамиками и сабвуфером.</span><span class="sxs-lookup"><span data-stu-id="77e42-141">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="77e42-142">Значение, заданное для этого свойства, определяет форматы вывода, перечисленные кодеком для многоканального аудио.</span><span class="sxs-lookup"><span data-stu-id="77e42-142">The value set for this property determines the output formats enumerated by the codec for multichannel audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="77e42-143">Требования</span><span class="sxs-lookup"><span data-stu-id="77e42-143">Requirements</span></span>



| <span data-ttu-id="77e42-144">Требование</span><span class="sxs-lookup"><span data-stu-id="77e42-144">Requirement</span></span> | <span data-ttu-id="77e42-145">Значение</span><span class="sxs-lookup"><span data-stu-id="77e42-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77e42-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77e42-146">Minimum supported client</span></span><br/> | <span data-ttu-id="77e42-147">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="77e42-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="77e42-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77e42-148">Minimum supported server</span></span><br/> | <span data-ttu-id="77e42-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77e42-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77e42-150">Header</span><span class="sxs-lookup"><span data-stu-id="77e42-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="77e42-151"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="77e42-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77e42-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77e42-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e42-153">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="77e42-153">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




