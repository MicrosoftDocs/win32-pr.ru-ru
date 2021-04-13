---
title: возможность, команда
description: Команда возможностей запрашивает сведения о конкретной возможности устройства. Все устройства MCI распознают эту команду.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- Команда возможностей мультимедиа Windows
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489600"
---
# <a name="capability-command"></a><span data-ttu-id="21cdc-105">возможность, команда</span><span class="sxs-lookup"><span data-stu-id="21cdc-105">capability command</span></span>

<span data-ttu-id="21cdc-106">Команда возможностей запрашивает сведения о конкретной возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="21cdc-106">The capability command requests information about a particular capability of a device.</span></span> <span data-ttu-id="21cdc-107">Все устройства MCI распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="21cdc-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="21cdc-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="21cdc-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="21cdc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="21cdc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21cdc-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="21cdc-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="21cdc-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="21cdc-111">Identifier of an MCI device.</span></span> <span data-ttu-id="21cdc-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="21cdc-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="21cdc-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*лпсзрекуест*</span><span class="sxs-lookup"><span data-stu-id="21cdc-113"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="21cdc-114">Флаг, определяющий возможность устройства.</span><span class="sxs-lookup"><span data-stu-id="21cdc-114">Flag that identifies a device capability.</span></span> <span data-ttu-id="21cdc-115">В следующей таблице перечислены типы устройств, которые распознают команду **возможности** и флаги, используемые каждым типом:</span><span class="sxs-lookup"><span data-stu-id="21cdc-115">The following table lists device types that recognize the **capability** command and the flags used by each type:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21cdc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="21cdc-116">Value</span></span></th>
<th><span data-ttu-id="21cdc-117">Тип</span><span class="sxs-lookup"><span data-stu-id="21cdc-117">Type</span></span></th>
<th><span data-ttu-id="21cdc-118">Тип</span><span class="sxs-lookup"><span data-stu-id="21cdc-118">Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21cdc-119">кдаудио</span><span class="sxs-lookup"><span data-stu-id="21cdc-119">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="21cdc-120">можно извлечь</span><span class="sxs-lookup"><span data-stu-id="21cdc-120">can eject</span></span></li>
<li><span data-ttu-id="21cdc-121">может играть</span><span class="sxs-lookup"><span data-stu-id="21cdc-121">can play</span></span></li>
<li><span data-ttu-id="21cdc-122">может записывать</span><span class="sxs-lookup"><span data-stu-id="21cdc-122">can record</span></span></li>
<li><span data-ttu-id="21cdc-123">можно сохранить</span><span class="sxs-lookup"><span data-stu-id="21cdc-123">can save</span></span></li>
<li><span data-ttu-id="21cdc-124">составное устройство</span><span class="sxs-lookup"><span data-stu-id="21cdc-124">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="21cdc-125">тип устройства</span><span class="sxs-lookup"><span data-stu-id="21cdc-125">device type</span></span></li>
<li><span data-ttu-id="21cdc-126">имеет звук</span><span class="sxs-lookup"><span data-stu-id="21cdc-126">has audio</span></span></li>
<li><span data-ttu-id="21cdc-127">содержит видео</span><span class="sxs-lookup"><span data-stu-id="21cdc-127">has video</span></span></li>
<li><span data-ttu-id="21cdc-128">использует файлы</span><span class="sxs-lookup"><span data-stu-id="21cdc-128">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-129">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="21cdc-129">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="21cdc-130">можно извлечь</span><span class="sxs-lookup"><span data-stu-id="21cdc-130">can eject</span></span></li>
<li><span data-ttu-id="21cdc-131">может заморозить</span><span class="sxs-lookup"><span data-stu-id="21cdc-131">can freeze</span></span></li>
<li><span data-ttu-id="21cdc-132">может блокировать</span><span class="sxs-lookup"><span data-stu-id="21cdc-132">can lock</span></span></li>
<li><span data-ttu-id="21cdc-133">может играть</span><span class="sxs-lookup"><span data-stu-id="21cdc-133">can play</span></span></li>
<li><span data-ttu-id="21cdc-134">может записывать</span><span class="sxs-lookup"><span data-stu-id="21cdc-134">can record</span></span></li>
<li><span data-ttu-id="21cdc-135">может быть обратным</span><span class="sxs-lookup"><span data-stu-id="21cdc-135">can reverse</span></span></li>
<li><span data-ttu-id="21cdc-136">можно сохранить</span><span class="sxs-lookup"><span data-stu-id="21cdc-136">can save</span></span></li>
<li><span data-ttu-id="21cdc-137">можно растянуть</span><span class="sxs-lookup"><span data-stu-id="21cdc-137">can stretch</span></span></li>
<li><span data-ttu-id="21cdc-138">может растягивать входные данные</span><span class="sxs-lookup"><span data-stu-id="21cdc-138">can stretch input</span></span></li>
<li><span data-ttu-id="21cdc-139">можно протестировать</span><span class="sxs-lookup"><span data-stu-id="21cdc-139">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="21cdc-140">составное устройство</span><span class="sxs-lookup"><span data-stu-id="21cdc-140">compound device</span></span></li>
<li><span data-ttu-id="21cdc-141">тип устройства</span><span class="sxs-lookup"><span data-stu-id="21cdc-141">device type</span></span></li>
<li><span data-ttu-id="21cdc-142">имеет звук</span><span class="sxs-lookup"><span data-stu-id="21cdc-142">has audio</span></span></li>
<li><span data-ttu-id="21cdc-143">по-прежнему</span><span class="sxs-lookup"><span data-stu-id="21cdc-143">has still</span></span></li>
<li><span data-ttu-id="21cdc-144">содержит видео</span><span class="sxs-lookup"><span data-stu-id="21cdc-144">has video</span></span></li>
<li><span data-ttu-id="21cdc-145">максимальная скорость воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21cdc-145">maximum play rate</span></span></li>
<li><span data-ttu-id="21cdc-146">Минимальная скорость воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21cdc-146">minimum play rate</span></span></li>
<li><span data-ttu-id="21cdc-147">использует файлы</span><span class="sxs-lookup"><span data-stu-id="21cdc-147">uses files</span></span></li>
<li><span data-ttu-id="21cdc-148">использует палитры</span><span class="sxs-lookup"><span data-stu-id="21cdc-148">uses palettes</span></span></li>
<li><span data-ttu-id="21cdc-149">Windows</span><span class="sxs-lookup"><span data-stu-id="21cdc-149">windows</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-150">overlay</span><span class="sxs-lookup"><span data-stu-id="21cdc-150">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="21cdc-151">можно извлечь</span><span class="sxs-lookup"><span data-stu-id="21cdc-151">can eject</span></span></li>
<li><span data-ttu-id="21cdc-152">может заморозить</span><span class="sxs-lookup"><span data-stu-id="21cdc-152">can freeze</span></span></li>
<li><span data-ttu-id="21cdc-153">может играть</span><span class="sxs-lookup"><span data-stu-id="21cdc-153">can play</span></span></li>
<li><span data-ttu-id="21cdc-154">может записывать</span><span class="sxs-lookup"><span data-stu-id="21cdc-154">can record</span></span></li>
<li><span data-ttu-id="21cdc-155">можно сохранить</span><span class="sxs-lookup"><span data-stu-id="21cdc-155">can save</span></span></li>
<li><span data-ttu-id="21cdc-156">можно растянуть</span><span class="sxs-lookup"><span data-stu-id="21cdc-156">can stretch</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="21cdc-157">составное устройство</span><span class="sxs-lookup"><span data-stu-id="21cdc-157">compound device</span></span></li>
<li><span data-ttu-id="21cdc-158">тип устройства</span><span class="sxs-lookup"><span data-stu-id="21cdc-158">device type</span></span></li>
<li><span data-ttu-id="21cdc-159">имеет звук</span><span class="sxs-lookup"><span data-stu-id="21cdc-159">has audio</span></span></li>
<li><span data-ttu-id="21cdc-160">содержит видео</span><span class="sxs-lookup"><span data-stu-id="21cdc-160">has video</span></span></li>
<li><span data-ttu-id="21cdc-161">использует файлы</span><span class="sxs-lookup"><span data-stu-id="21cdc-161">uses files</span></span></li>
<li><span data-ttu-id="21cdc-162">Windows</span><span class="sxs-lookup"><span data-stu-id="21cdc-162">windows</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-163">sequencer</span><span class="sxs-lookup"><span data-stu-id="21cdc-163">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="21cdc-164">можно извлечь</span><span class="sxs-lookup"><span data-stu-id="21cdc-164">can eject</span></span></li>
<li><span data-ttu-id="21cdc-165">может играть</span><span class="sxs-lookup"><span data-stu-id="21cdc-165">can play</span></span></li>
<li><span data-ttu-id="21cdc-166">может записывать</span><span class="sxs-lookup"><span data-stu-id="21cdc-166">can record</span></span></li>
<li><span data-ttu-id="21cdc-167">можно сохранить</span><span class="sxs-lookup"><span data-stu-id="21cdc-167">can save</span></span></li>
<li><span data-ttu-id="21cdc-168">составное устройство</span><span class="sxs-lookup"><span data-stu-id="21cdc-168">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="21cdc-169">тип устройства</span><span class="sxs-lookup"><span data-stu-id="21cdc-169">device type</span></span></li>
<li><span data-ttu-id="21cdc-170">имеет звук</span><span class="sxs-lookup"><span data-stu-id="21cdc-170">has audio</span></span></li>
<li><span data-ttu-id="21cdc-171">содержит видео</span><span class="sxs-lookup"><span data-stu-id="21cdc-171">has video</span></span></li>
<li><span data-ttu-id="21cdc-172">использует файлы</span><span class="sxs-lookup"><span data-stu-id="21cdc-172">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-173">видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="21cdc-173">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="21cdc-174">может обнаружить длину</span><span class="sxs-lookup"><span data-stu-id="21cdc-174">can detect length</span></span></li>
<li><span data-ttu-id="21cdc-175">можно извлечь</span><span class="sxs-lookup"><span data-stu-id="21cdc-175">can eject</span></span></li>
<li><span data-ttu-id="21cdc-176">может заморозить</span><span class="sxs-lookup"><span data-stu-id="21cdc-176">can freeze</span></span></li>
<li><span data-ttu-id="21cdc-177">может отслеживать источники</span><span class="sxs-lookup"><span data-stu-id="21cdc-177">can monitor sources</span></span></li>
<li><span data-ttu-id="21cdc-178">может играть</span><span class="sxs-lookup"><span data-stu-id="21cdc-178">can play</span></span></li>
<li><span data-ttu-id="21cdc-179">может предвернуть</span><span class="sxs-lookup"><span data-stu-id="21cdc-179">can preroll</span></span></li>
<li><span data-ttu-id="21cdc-180">Возможен предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="21cdc-180">can preview</span></span></li>
<li><span data-ttu-id="21cdc-181">может записывать</span><span class="sxs-lookup"><span data-stu-id="21cdc-181">can record</span></span></li>
<li><span data-ttu-id="21cdc-182">может быть обратным</span><span class="sxs-lookup"><span data-stu-id="21cdc-182">can reverse</span></span></li>
<li><span data-ttu-id="21cdc-183">можно сохранить</span><span class="sxs-lookup"><span data-stu-id="21cdc-183">can save</span></span></li>
<li><span data-ttu-id="21cdc-184">можно протестировать</span><span class="sxs-lookup"><span data-stu-id="21cdc-184">can test</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="21cdc-185">Частота приращения часов</span><span class="sxs-lookup"><span data-stu-id="21cdc-185">clock increment rate</span></span></li>
<li><span data-ttu-id="21cdc-186">составное устройство</span><span class="sxs-lookup"><span data-stu-id="21cdc-186">compound device</span></span></li>
<li><span data-ttu-id="21cdc-187">тип устройства</span><span class="sxs-lookup"><span data-stu-id="21cdc-187">device type</span></span></li>
<li><span data-ttu-id="21cdc-188">имеет звук</span><span class="sxs-lookup"><span data-stu-id="21cdc-188">has audio</span></span></li>
<li><span data-ttu-id="21cdc-189">имеет часы</span><span class="sxs-lookup"><span data-stu-id="21cdc-189">has clock</span></span></li>
<li><span data-ttu-id="21cdc-190">имеет код времени</span><span class="sxs-lookup"><span data-stu-id="21cdc-190">has timecode</span></span></li>
<li><span data-ttu-id="21cdc-191">содержит видео</span><span class="sxs-lookup"><span data-stu-id="21cdc-191">has video</span></span></li>
<li><span data-ttu-id="21cdc-192">число меток</span><span class="sxs-lookup"><span data-stu-id="21cdc-192">number of marks</span></span></li>
<li><span data-ttu-id="21cdc-193">точность поиска</span><span class="sxs-lookup"><span data-stu-id="21cdc-193">seek accuracy</span></span></li>
<li><span data-ttu-id="21cdc-194">использует файлы</span><span class="sxs-lookup"><span data-stu-id="21cdc-194">uses files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-195">видеодиск</span><span class="sxs-lookup"><span data-stu-id="21cdc-195">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="21cdc-196">можно извлечь</span><span class="sxs-lookup"><span data-stu-id="21cdc-196">can eject</span></span></li>
<li><span data-ttu-id="21cdc-197">может играть</span><span class="sxs-lookup"><span data-stu-id="21cdc-197">can play</span></span></li>
<li><span data-ttu-id="21cdc-198">может записывать</span><span class="sxs-lookup"><span data-stu-id="21cdc-198">can record</span></span></li>
<li><span data-ttu-id="21cdc-199">может быть обратным</span><span class="sxs-lookup"><span data-stu-id="21cdc-199">can reverse</span></span></li>
<li><span data-ttu-id="21cdc-200">можно сохранить</span><span class="sxs-lookup"><span data-stu-id="21cdc-200">can save</span></span></li>
<li><span data-ttu-id="21cdc-201">кав</span><span class="sxs-lookup"><span data-stu-id="21cdc-201">CAV</span></span></li>
<li><span data-ttu-id="21cdc-202">CLV</span><span class="sxs-lookup"><span data-stu-id="21cdc-202">CLV</span></span></li>
<li><span data-ttu-id="21cdc-203">составное устройство</span><span class="sxs-lookup"><span data-stu-id="21cdc-203">compound device</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="21cdc-204">тип устройства</span><span class="sxs-lookup"><span data-stu-id="21cdc-204">device type</span></span></li>
<li><span data-ttu-id="21cdc-205">скорость быстрого воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21cdc-205">fast play rate</span></span></li>
<li><span data-ttu-id="21cdc-206">имеет звук</span><span class="sxs-lookup"><span data-stu-id="21cdc-206">has audio</span></span></li>
<li><span data-ttu-id="21cdc-207">содержит видео</span><span class="sxs-lookup"><span data-stu-id="21cdc-207">has video</span></span></li>
<li><span data-ttu-id="21cdc-208">нормальная скорость воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21cdc-208">normal play rate</span></span></li>
<li><span data-ttu-id="21cdc-209">скорость снижения скорости воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21cdc-209">slow play rate</span></span></li>
<li><span data-ttu-id="21cdc-210">использует файлы</span><span class="sxs-lookup"><span data-stu-id="21cdc-210">uses files</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-211">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="21cdc-211">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="21cdc-212">можно извлечь</span><span class="sxs-lookup"><span data-stu-id="21cdc-212">can eject</span></span></li>
<li><span data-ttu-id="21cdc-213">может играть</span><span class="sxs-lookup"><span data-stu-id="21cdc-213">can play</span></span></li>
<li><span data-ttu-id="21cdc-214">может записывать</span><span class="sxs-lookup"><span data-stu-id="21cdc-214">can record</span></span></li>
<li><span data-ttu-id="21cdc-215">можно сохранить</span><span class="sxs-lookup"><span data-stu-id="21cdc-215">can save</span></span></li>
<li><span data-ttu-id="21cdc-216">составное устройство</span><span class="sxs-lookup"><span data-stu-id="21cdc-216">compound device</span></span></li>
<li><span data-ttu-id="21cdc-217">тип устройства</span><span class="sxs-lookup"><span data-stu-id="21cdc-217">device type</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="21cdc-218">имеет звук</span><span class="sxs-lookup"><span data-stu-id="21cdc-218">has audio</span></span></li>
<li><span data-ttu-id="21cdc-219">содержит видео</span><span class="sxs-lookup"><span data-stu-id="21cdc-219">has video</span></span></li>
<li><span data-ttu-id="21cdc-220">Ввод данных</span><span class="sxs-lookup"><span data-stu-id="21cdc-220">inputs</span></span></li>
<li><span data-ttu-id="21cdc-221">outputs</span><span class="sxs-lookup"><span data-stu-id="21cdc-221">outputs</span></span></li>
<li><span data-ttu-id="21cdc-222">использует файлы</span><span class="sxs-lookup"><span data-stu-id="21cdc-222">uses files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="21cdc-223">В следующей таблице перечислены флаги, которые можно указать в параметре *лпсзрекуест* , а также их значения.</span><span class="sxs-lookup"><span data-stu-id="21cdc-223">The following table lists the flags that can be specified in the *lpszRequest* parameter and their meanings:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21cdc-224">Флаги</span><span class="sxs-lookup"><span data-stu-id="21cdc-224">Flags</span></span></th>
<th><span data-ttu-id="21cdc-225">Значение</span><span class="sxs-lookup"><span data-stu-id="21cdc-225">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21cdc-226">может обнаружить длину</span><span class="sxs-lookup"><span data-stu-id="21cdc-226">can detect length</span></span></td>
<td><span data-ttu-id="21cdc-227">Возвращает <strong>значение true</strong> , если устройство может определить длину носителя.</span><span class="sxs-lookup"><span data-stu-id="21cdc-227">Returns <strong>TRUE</strong> if the device can detect the length of the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-228">можно извлечь</span><span class="sxs-lookup"><span data-stu-id="21cdc-228">can eject</span></span></td>
<td><span data-ttu-id="21cdc-229">Возвращает <strong>значение true</strong> , если устройство может извлечь носитель.</span><span class="sxs-lookup"><span data-stu-id="21cdc-229">Returns <strong>TRUE</strong> if the device can eject the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-230">может заморозить</span><span class="sxs-lookup"><span data-stu-id="21cdc-230">can freeze</span></span></td>
<td><span data-ttu-id="21cdc-231">Возвращает <strong>значение true</strong> , если устройство может заморозить данные в буфере кадров.</span><span class="sxs-lookup"><span data-stu-id="21cdc-231">Returns <strong>TRUE</strong> if the device can freeze data in the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-232">может блокировать</span><span class="sxs-lookup"><span data-stu-id="21cdc-232">can lock</span></span></td>
<td><span data-ttu-id="21cdc-233">Возвращает <strong>значение true</strong> , если устройство может блокировать данные.</span><span class="sxs-lookup"><span data-stu-id="21cdc-233">Returns <strong>TRUE</strong> if the device can lock data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-234">может отслеживать источники</span><span class="sxs-lookup"><span data-stu-id="21cdc-234">can monitor sources</span></span></td>
<td><span data-ttu-id="21cdc-235">Возвращает <strong>значение true</strong> , если устройство может передать входные данные (источник) отслеживаемому выходу, независимо от текущего выбора ввода.</span><span class="sxs-lookup"><span data-stu-id="21cdc-235">Returns <strong>TRUE</strong> if the device can pass an input (source) to the monitored output, independent of the current input selection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-236">может играть</span><span class="sxs-lookup"><span data-stu-id="21cdc-236">can play</span></span></td>
<td><span data-ttu-id="21cdc-237">Возвращает <strong>значение true</strong> , если устройство может играть.</span><span class="sxs-lookup"><span data-stu-id="21cdc-237">Returns <strong>TRUE</strong> if the device can play.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-238">может предвернуть</span><span class="sxs-lookup"><span data-stu-id="21cdc-238">can preroll</span></span></td>
<td><span data-ttu-id="21cdc-239">Возвращает <strong>значение true</strong> , если устройство поддерживает &quot; флаг превращение &quot; с помощью команды <a href="cue.md">подсказки</a> .</span><span class="sxs-lookup"><span data-stu-id="21cdc-239">Returns <strong>TRUE</strong> if the device supports the &quot;preroll&quot; flag with the <a href="cue.md">cue</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-240">Возможен предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="21cdc-240">can preview</span></span></td>
<td><span data-ttu-id="21cdc-241">Возвращает <strong>значение true</strong> , если устройство поддерживает предварительные версии.</span><span class="sxs-lookup"><span data-stu-id="21cdc-241">Returns <strong>TRUE</strong> if the device supports previews.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-242">может записывать</span><span class="sxs-lookup"><span data-stu-id="21cdc-242">can record</span></span></td>
<td><span data-ttu-id="21cdc-243">Возвращает <strong>значение true</strong> , если устройство поддерживает запись.</span><span class="sxs-lookup"><span data-stu-id="21cdc-243">Returns <strong>TRUE</strong> if the device supports recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-244">может быть обратным</span><span class="sxs-lookup"><span data-stu-id="21cdc-244">can reverse</span></span></td>
<td><span data-ttu-id="21cdc-245">Возвращает <strong>значение true</strong> , если устройство может воспроизводиться в обратную.</span><span class="sxs-lookup"><span data-stu-id="21cdc-245">Returns <strong>TRUE</strong> if the device can play in reverse.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-246">можно сохранить</span><span class="sxs-lookup"><span data-stu-id="21cdc-246">can save</span></span></td>
<td><span data-ttu-id="21cdc-247">Возвращает <strong>значение true</strong> , если устройство может сохранять данные.</span><span class="sxs-lookup"><span data-stu-id="21cdc-247">Returns <strong>TRUE</strong> if the device can save data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-248">можно растянуть</span><span class="sxs-lookup"><span data-stu-id="21cdc-248">can stretch</span></span></td>
<td><span data-ttu-id="21cdc-249">Возвращает <strong>значение true</strong> , если устройство может растянуть кадры для заполнения заданного прямоугольника экрана.</span><span class="sxs-lookup"><span data-stu-id="21cdc-249">Returns <strong>TRUE</strong> if the device can stretch frames to fill a given display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-250">может растягивать входные данные</span><span class="sxs-lookup"><span data-stu-id="21cdc-250">can stretch input</span></span></td>
<td><span data-ttu-id="21cdc-251">Возвращает <strong>значение true</strong> , если устройство может изменить размер изображения в процессе помещает его в буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="21cdc-251">Returns <strong>TRUE</strong> if the device can resize an image in the process of digitizing it into the frame buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-252">можно протестировать</span><span class="sxs-lookup"><span data-stu-id="21cdc-252">can test</span></span></td>
<td><span data-ttu-id="21cdc-253">Возвращает <strong>значение true</strong> , если устройство распознает ключевое слово теста.</span><span class="sxs-lookup"><span data-stu-id="21cdc-253">Returns <strong>TRUE</strong> if the device recognizes the test keyword.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-254">кав</span><span class="sxs-lookup"><span data-stu-id="21cdc-254">cav</span></span></td>
<td><span data-ttu-id="21cdc-255">При объединении с другими элементами этот флаг указывает, что возвращаемые сведения применяются к Кав формата видеодискс.</span><span class="sxs-lookup"><span data-stu-id="21cdc-255">When combined with other items, this flag specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="21cdc-256">Это значение по умолчанию, если видеодиск не вставлен.</span><span class="sxs-lookup"><span data-stu-id="21cdc-256">This is the default if no videodisc is inserted.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-257">Частота приращения часов</span><span class="sxs-lookup"><span data-stu-id="21cdc-257">clock increment rate</span></span></td>
<td><span data-ttu-id="21cdc-258">Возвращает число подразделений, поддерживаемых внешними часами, в секунду.</span><span class="sxs-lookup"><span data-stu-id="21cdc-258">Returns the number of subdivisions the external clock supports per second.</span></span> <span data-ttu-id="21cdc-259">Если внешние часы являются часами миллисекунд, возвращается значение 1000.</span><span class="sxs-lookup"><span data-stu-id="21cdc-259">If the external clock is a millisecond clock, the return value is 1000.</span></span> <span data-ttu-id="21cdc-260">Если возвращаемое значение равно 0, часы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="21cdc-260">If the return value is 0, no clock is supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-261">clv</span><span class="sxs-lookup"><span data-stu-id="21cdc-261">clv</span></span></td>
<td><span data-ttu-id="21cdc-262">При объединении с другими элементами этот флаг указывает, что возвращаемые сведения применяются к CLV формата видеодискс.</span><span class="sxs-lookup"><span data-stu-id="21cdc-262">When combined with other items, this flag specifies that the return information applies to CLV format videodiscs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-263">составное устройство</span><span class="sxs-lookup"><span data-stu-id="21cdc-263">compound device</span></span></td>
<td><span data-ttu-id="21cdc-264">Возвращает <strong>значение true</strong> , если устройство поддерживает имя элемента (filename).</span><span class="sxs-lookup"><span data-stu-id="21cdc-264">Returns <strong>TRUE</strong> if the device supports an element name (filename).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-265">тип устройства</span><span class="sxs-lookup"><span data-stu-id="21cdc-265">device type</span></span></td>
<td><span data-ttu-id="21cdc-266">Возвращает имя типа устройства, которое может принимать одно из следующих имен:</span><span class="sxs-lookup"><span data-stu-id="21cdc-266">Returns a device type name, which can be one of the following:</span></span>
<ul>
<li><span data-ttu-id="21cdc-267">кдаудио</span><span class="sxs-lookup"><span data-stu-id="21cdc-267">cdaudio</span></span></li>
<li><span data-ttu-id="21cdc-268">включая</span><span class="sxs-lookup"><span data-stu-id="21cdc-268">dat</span></span></li>
<li><span data-ttu-id="21cdc-269">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="21cdc-269">digitalvideo</span></span></li>
<li><span data-ttu-id="21cdc-270">др.</span><span class="sxs-lookup"><span data-stu-id="21cdc-270">other</span></span></li>
<li><span data-ttu-id="21cdc-271">overlay</span><span class="sxs-lookup"><span data-stu-id="21cdc-271">overlay</span></span></li>
<li><span data-ttu-id="21cdc-272">средство проверки</span><span class="sxs-lookup"><span data-stu-id="21cdc-272">scanner</span></span></li>
<li><span data-ttu-id="21cdc-273">sequencer</span><span class="sxs-lookup"><span data-stu-id="21cdc-273">sequencer</span></span></li>
<li><span data-ttu-id="21cdc-274">видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="21cdc-274">vcr</span></span></li>
<li><span data-ttu-id="21cdc-275">видеодиск</span><span class="sxs-lookup"><span data-stu-id="21cdc-275">videodisc</span></span></li>
<li><span data-ttu-id="21cdc-276">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="21cdc-276">waveaudio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-277">скорость быстрого воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21cdc-277">fast play rate</span></span></td>
<td><span data-ttu-id="21cdc-278">Возвращает скорость быстрого воспроизведения в кадрах в секунду или нуль, если устройство не может воспроизводиться быстро.</span><span class="sxs-lookup"><span data-stu-id="21cdc-278">Returns the fast play rate in frames per second, or zero if the device cannot play fast.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-279">имеет звук</span><span class="sxs-lookup"><span data-stu-id="21cdc-279">has audio</span></span></td>
<td><span data-ttu-id="21cdc-280">Возвращает <strong>значение true</strong> , если устройство поддерживает воспроизведение звука.</span><span class="sxs-lookup"><span data-stu-id="21cdc-280">Returns <strong>TRUE</strong> if the device supports audio playback.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-281">имеет часы</span><span class="sxs-lookup"><span data-stu-id="21cdc-281">has clock</span></span></td>
<td><span data-ttu-id="21cdc-282">Возвращает <strong>значение true</strong> , если устройство имеет часы.</span><span class="sxs-lookup"><span data-stu-id="21cdc-282">Returns <strong>TRUE</strong> if the device has a clock.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-283">по-прежнему</span><span class="sxs-lookup"><span data-stu-id="21cdc-283">has still</span></span></td>
<td><span data-ttu-id="21cdc-284">Возвращает <strong>значение true</strong> , если устройство обрабатывает файлы с одним изображением более эффективно, чем видеофайлы движения.</span><span class="sxs-lookup"><span data-stu-id="21cdc-284">Returns <strong>TRUE</strong> if the device treats files with a single image more efficiently than motion video files.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-285">имеет код времени</span><span class="sxs-lookup"><span data-stu-id="21cdc-285">has timecode</span></span></td>
<td><span data-ttu-id="21cdc-286">Возвращает <strong>значение true</strong> , если устройство может поддерживать код времени, или если оно неизвестно.</span><span class="sxs-lookup"><span data-stu-id="21cdc-286">Returns <strong>TRUE</strong> if the device is capable of supporting timecode, or if it is unknown.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-287">содержит видео</span><span class="sxs-lookup"><span data-stu-id="21cdc-287">has video</span></span></td>
<td><span data-ttu-id="21cdc-288">Возвращает <strong>значение true</strong> , если устройство поддерживает видео.</span><span class="sxs-lookup"><span data-stu-id="21cdc-288">Returns <strong>TRUE</strong> if the device supports video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-289">Ввод данных</span><span class="sxs-lookup"><span data-stu-id="21cdc-289">inputs</span></span></td>
<td><span data-ttu-id="21cdc-290">Возвращает общее число устройств ввода.</span><span class="sxs-lookup"><span data-stu-id="21cdc-290">Returns the total number of input devices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-291">максимальная скорость воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21cdc-291">maximum play rate</span></span></td>
<td><span data-ttu-id="21cdc-292">Возвращает максимальную скорость воспроизведения для устройства (в кадрах в секунду).</span><span class="sxs-lookup"><span data-stu-id="21cdc-292">Returns the maximum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-293">Минимальная скорость воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21cdc-293">minimum play rate</span></span></td>
<td><span data-ttu-id="21cdc-294">Возвращает минимальную скорость воспроизведения для устройства (в кадрах в секунду).</span><span class="sxs-lookup"><span data-stu-id="21cdc-294">Returns the minimum play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-295">нормальная скорость воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21cdc-295">normal play rate</span></span></td>
<td><span data-ttu-id="21cdc-296">Возвращает нормальную скорость воспроизведения для устройства (в кадрах в секунду).</span><span class="sxs-lookup"><span data-stu-id="21cdc-296">Returns the normal play rate, in frames per second, for the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-297">число меток</span><span class="sxs-lookup"><span data-stu-id="21cdc-297">number of marks</span></span></td>
<td><span data-ttu-id="21cdc-298">Возвращает максимальное число меток, которые могут быть использованы; ноль означает, что метки не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="21cdc-298">Returns the maximum number of marks that can be used; zero indicates that marks are unsupported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-299">outputs</span><span class="sxs-lookup"><span data-stu-id="21cdc-299">outputs</span></span></td>
<td><span data-ttu-id="21cdc-300">Возвращает общее число устройств вывода.</span><span class="sxs-lookup"><span data-stu-id="21cdc-300">Returns the total number of output devices.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-301">точность поиска</span><span class="sxs-lookup"><span data-stu-id="21cdc-301">seek accuracy</span></span></td>
<td><span data-ttu-id="21cdc-302">Возвращает ожидаемую точность поиска в кадрах; 0 означает, что устройство является точным для рамки, 1 означает, что устройство должно находиться в пределах одного кадра указанной точки поиска и т. д.</span><span class="sxs-lookup"><span data-stu-id="21cdc-302">Returns the expected accuracy of a search in frames; 0 indicates that the device is frame accurate, 1 indicates that the device expects to be within one frame of the indicated seek position, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-303">скорость снижения скорости воспроизведения</span><span class="sxs-lookup"><span data-stu-id="21cdc-303">slow play rate</span></span></td>
<td><span data-ttu-id="21cdc-304">Возвращает скорость медленного воспроизведения в кадрах в секунду или нуль, если устройство не может воспроизводиться медленно.</span><span class="sxs-lookup"><span data-stu-id="21cdc-304">Returns the slow play rate in frames per second, or zero if the device cannot play slowly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-305">использует файлы</span><span class="sxs-lookup"><span data-stu-id="21cdc-305">uses files</span></span></td>
<td><span data-ttu-id="21cdc-306">Возвращает <strong>значение true</strong> , если хранилище данных, используемое составным устройством, является файлом.</span><span class="sxs-lookup"><span data-stu-id="21cdc-306">Returns <strong>TRUE</strong> if the data storage used by a compound device is a file.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cdc-307">использует палитры</span><span class="sxs-lookup"><span data-stu-id="21cdc-307">uses palettes</span></span></td>
<td><span data-ttu-id="21cdc-308">Возвращает <strong>значение true</strong> , если устройство использует палитры.</span><span class="sxs-lookup"><span data-stu-id="21cdc-308">Returns <strong>TRUE</strong> if the device uses palettes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cdc-309">Windows</span><span class="sxs-lookup"><span data-stu-id="21cdc-309">windows</span></span></td>
<td><span data-ttu-id="21cdc-310">Возвращает число одновременно отображаемых окон, которые может поддерживать устройство.</span><span class="sxs-lookup"><span data-stu-id="21cdc-310">Returns the number of simultaneous display windows the device can support.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="21cdc-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="21cdc-311"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="21cdc-312">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="21cdc-312">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="21cdc-313">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="21cdc-313">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="21cdc-314">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="21cdc-314">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21cdc-315">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21cdc-315">Return Value</span></span>

<span data-ttu-id="21cdc-316">Возвращает сведения в параметре *лпсзретурнстринг* функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="21cdc-316">Returns information in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="21cdc-317">Сведения зависят от типа запроса.</span><span class="sxs-lookup"><span data-stu-id="21cdc-317">The information is dependent on the request type.</span></span>

## <a name="examples"></a><span data-ttu-id="21cdc-318">Примеры</span><span class="sxs-lookup"><span data-stu-id="21cdc-318">Examples</span></span>

<span data-ttu-id="21cdc-319">Следующая команда возвращает тип устройства "мисаунд".</span><span class="sxs-lookup"><span data-stu-id="21cdc-319">The following command returns the device type of the "mysound" device.</span></span>

``` syntax
capability mysound device type
```

## <a name="requirements"></a><span data-ttu-id="21cdc-320">Требования</span><span class="sxs-lookup"><span data-stu-id="21cdc-320">Requirements</span></span>



| <span data-ttu-id="21cdc-321">Требование</span><span class="sxs-lookup"><span data-stu-id="21cdc-321">Requirement</span></span> | <span data-ttu-id="21cdc-322">Значение</span><span class="sxs-lookup"><span data-stu-id="21cdc-322">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="21cdc-323">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21cdc-323">Minimum supported client</span></span><br/> | <span data-ttu-id="21cdc-324">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="21cdc-324">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="21cdc-325">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21cdc-325">Minimum supported server</span></span><br/> | <span data-ttu-id="21cdc-326">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="21cdc-326">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="21cdc-327">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21cdc-327">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21cdc-328">MCI</span><span class="sxs-lookup"><span data-stu-id="21cdc-328">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="21cdc-329">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="21cdc-329">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="21cdc-330">cue</span><span class="sxs-lookup"><span data-stu-id="21cdc-330">cue</span></span>](cue.md)
</dt> </dl>

 

