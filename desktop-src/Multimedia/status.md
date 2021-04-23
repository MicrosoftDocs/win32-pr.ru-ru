---
title: Команда Status
description: Команда Status запрашивает сведения о состоянии устройства. Все устройства распознают эту команду.
ms.assetid: 39961bd7-866d-450d-9fbf-347a8f508481
keywords:
- Команда "состояние" мультимедиа Windows
topic_type:
- apiref
api_name:
- status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ab184ddaca16d0ea96b86a6b062f1e66e2eee2
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "105674509"
---
# <a name="status-command"></a><span data-ttu-id="b45ad-105">Команда Status</span><span class="sxs-lookup"><span data-stu-id="b45ad-105">status command</span></span>

> [!NOTE]
> <span data-ttu-id="b45ad-106">Обмен данными без смещения — Корпорация Майкрософт поддерживает различные и включенные среды.</span><span class="sxs-lookup"><span data-stu-id="b45ad-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="b45ad-107">В этом документе есть ссылки на слово "Slave".</span><span class="sxs-lookup"><span data-stu-id="b45ad-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="b45ad-108">В соответствии с руководством корпорации Майкрософт в [стиле Bias-Freeного обмена данными](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) это слово является исключаемым.</span><span class="sxs-lookup"><span data-stu-id="b45ad-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="b45ad-109">Это слово используется в том виде, в котором оно используется в командах.</span><span class="sxs-lookup"><span data-stu-id="b45ad-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="b45ad-110">Для обеспечения согласованности этот документ содержит это слово.</span><span class="sxs-lookup"><span data-stu-id="b45ad-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="b45ad-111">При изменении этого слова в командах будет исправлен этот документ в выравнивании.</span><span class="sxs-lookup"><span data-stu-id="b45ad-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="b45ad-112">Команда Status запрашивает сведения о состоянии устройства.</span><span class="sxs-lookup"><span data-stu-id="b45ad-112">The status command requests status information from a device.</span></span> <span data-ttu-id="b45ad-113">Все устройства распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="b45ad-113">All devices recognize this command.</span></span>

<span data-ttu-id="b45ad-114">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="b45ad-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("status %s %s %s"),
  lpszDeviceID,
  lpszRequest,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="b45ad-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="b45ad-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b45ad-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="b45ad-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b45ad-117">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="b45ad-117">Identifier of an MCI device.</span></span> <span data-ttu-id="b45ad-118">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="b45ad-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="b45ad-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*лпсзрекуест*</span><span class="sxs-lookup"><span data-stu-id="b45ad-119"><span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*</span></span>
</dt> <dd>

<span data-ttu-id="b45ad-120">Флаг для запроса сведений о состоянии.</span><span class="sxs-lookup"><span data-stu-id="b45ad-120">Flag for requesting status information.</span></span> <span data-ttu-id="b45ad-121">В следующей таблице перечислены типы устройств, которые распознают команду **Status** , и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="b45ad-121">The following table lists device types that recognize the **status** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b45ad-122">Тип устройства</span><span class="sxs-lookup"><span data-stu-id="b45ad-122">Device Type</span></span></th>
<th><span data-ttu-id="b45ad-123">Флаги запроса</span><span class="sxs-lookup"><span data-stu-id="b45ad-123">Request Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b45ad-124">кдаудио</span><span class="sxs-lookup"><span data-stu-id="b45ad-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="b45ad-125"><em>номер</em> направления для типа кдаудио</span><span class="sxs-lookup"><span data-stu-id="b45ad-125">cdaudio type track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-126">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-126">current track</span></span></li>
<li><span data-ttu-id="b45ad-127">length</span><span class="sxs-lookup"><span data-stu-id="b45ad-127">length</span></span></li>
<li><span data-ttu-id="b45ad-128"><em>номер</em> записи о длине</span><span class="sxs-lookup"><span data-stu-id="b45ad-128">length track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-129">носитель отсутствует</span><span class="sxs-lookup"><span data-stu-id="b45ad-129">media present</span></span></li>
<li><span data-ttu-id="b45ad-130">mode</span><span class="sxs-lookup"><span data-stu-id="b45ad-130">mode</span></span></li>
<li><span data-ttu-id="b45ad-131">число дорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-131">number of tracks</span></span></li>
<li><span data-ttu-id="b45ad-132">position</span><span class="sxs-lookup"><span data-stu-id="b45ad-132">position</span></span></li>
<li><span data-ttu-id="b45ad-133"><em>номер</em> отслеживания расположения</span><span class="sxs-lookup"><span data-stu-id="b45ad-133">position track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-134">всё</span><span class="sxs-lookup"><span data-stu-id="b45ad-134">ready</span></span></li>
<li><span data-ttu-id="b45ad-135">начальное расположение</span><span class="sxs-lookup"><span data-stu-id="b45ad-135">start position</span></span></li>
<li><span data-ttu-id="b45ad-136">формат времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-136">time format</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-137">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="b45ad-137">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="b45ad-138">звук</span><span class="sxs-lookup"><span data-stu-id="b45ad-138">audio</span></span></li>
<li><span data-ttu-id="b45ad-139">Выравнивание звука</span><span class="sxs-lookup"><span data-stu-id="b45ad-139">audio alignment</span></span></li>
<li><span data-ttu-id="b45ad-140">аудио битсперсампле</span><span class="sxs-lookup"><span data-stu-id="b45ad-140">audio bitspersample</span></span></li>
<li><span data-ttu-id="b45ad-141">обрывы звука</span><span class="sxs-lookup"><span data-stu-id="b45ad-141">audio breaks</span></span></li>
<li><span data-ttu-id="b45ad-142">аудио битесперсек</span><span class="sxs-lookup"><span data-stu-id="b45ad-142">audio bytespersec</span></span></li>
<li><span data-ttu-id="b45ad-143">звуковые входные данные</span><span class="sxs-lookup"><span data-stu-id="b45ad-143">audio input</span></span></li>
<li><span data-ttu-id="b45ad-144">звуковая запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-144">audio record</span></span></li>
<li><span data-ttu-id="b45ad-145">источник звука</span><span class="sxs-lookup"><span data-stu-id="b45ad-145">audio source</span></span></li>
<li><span data-ttu-id="b45ad-146">аудио самплесперсек</span><span class="sxs-lookup"><span data-stu-id="b45ad-146">audio samplespersec</span></span></li>
<li><span data-ttu-id="b45ad-147">аудиопоток</span><span class="sxs-lookup"><span data-stu-id="b45ad-147">audio stream</span></span></li>
<li><span data-ttu-id="b45ad-148">низким</span><span class="sxs-lookup"><span data-stu-id="b45ad-148">bass</span></span></li>
<li><span data-ttu-id="b45ad-149">битсперпел</span><span class="sxs-lookup"><span data-stu-id="b45ad-149">bitsperpel</span></span></li>
<li><span data-ttu-id="b45ad-150">brightness</span><span class="sxs-lookup"><span data-stu-id="b45ad-150">brightness</span></span></li>
<li><span data-ttu-id="b45ad-151">color</span><span class="sxs-lookup"><span data-stu-id="b45ad-151">color</span></span></li>
<li><span data-ttu-id="b45ad-152">контрастность</span><span class="sxs-lookup"><span data-stu-id="b45ad-152">contrast</span></span></li>
<li><span data-ttu-id="b45ad-153">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-153">current track</span></span></li>
<li><span data-ttu-id="b45ad-154"><em>дискового пространства</em></span><span class="sxs-lookup"><span data-stu-id="b45ad-154">disk space <em>drive</em></span></span></li>
<li><span data-ttu-id="b45ad-155">завершение файла</span><span class="sxs-lookup"><span data-stu-id="b45ad-155">file completion</span></span></li>
<li><span data-ttu-id="b45ad-156">формат файлов</span><span class="sxs-lookup"><span data-stu-id="b45ad-156">file format</span></span></li>
<li><span data-ttu-id="b45ad-157">файловый режим</span><span class="sxs-lookup"><span data-stu-id="b45ad-157">file mode</span></span></li>
<li><span data-ttu-id="b45ad-158">forward</span><span class="sxs-lookup"><span data-stu-id="b45ad-158">forward</span></span></li>
<li><span data-ttu-id="b45ad-159">пропущенные кадры</span><span class="sxs-lookup"><span data-stu-id="b45ad-159">frames skipped</span></span></li>
<li><span data-ttu-id="b45ad-160">gamma</span><span class="sxs-lookup"><span data-stu-id="b45ad-160">gamma</span></span></li>
<li><span data-ttu-id="b45ad-161">input</span><span class="sxs-lookup"><span data-stu-id="b45ad-161">input</span></span></li>
<li><span data-ttu-id="b45ad-162">левый том</span><span class="sxs-lookup"><span data-stu-id="b45ad-162">left volume</span></span></li>
<li><span data-ttu-id="b45ad-163">length</span><span class="sxs-lookup"><span data-stu-id="b45ad-163">length</span></span></li>
<li><span data-ttu-id="b45ad-164"><em>номер</em> записи о длине</span><span class="sxs-lookup"><span data-stu-id="b45ad-164">length track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-165">носитель отсутствует</span><span class="sxs-lookup"><span data-stu-id="b45ad-165">media present</span></span></li>
<li><span data-ttu-id="b45ad-166">mode</span><span class="sxs-lookup"><span data-stu-id="b45ad-166">mode</span></span></li>
<li><span data-ttu-id="b45ad-167">monitor</span><span class="sxs-lookup"><span data-stu-id="b45ad-167">monitor</span></span></li>
<li><span data-ttu-id="b45ad-168">метод Monitor</span><span class="sxs-lookup"><span data-stu-id="b45ad-168">monitor method</span></span></li>
<li><span data-ttu-id="b45ad-169">Функция</span><span class="sxs-lookup"><span data-stu-id="b45ad-169">nominal</span></span></li>
<li><span data-ttu-id="b45ad-170">Номинальная частота кадров</span><span class="sxs-lookup"><span data-stu-id="b45ad-170">nominal frame rate</span></span></li>
<li><span data-ttu-id="b45ad-171">Номинальная частота кадров записи</span><span class="sxs-lookup"><span data-stu-id="b45ad-171">nominal record frame rate</span></span></li>
<li><span data-ttu-id="b45ad-172">число дорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-172">number of tracks</span></span></li>
<li><span data-ttu-id="b45ad-173">output</span><span class="sxs-lookup"><span data-stu-id="b45ad-173">output</span></span></li>
<li><span data-ttu-id="b45ad-174">маркер палитры</span><span class="sxs-lookup"><span data-stu-id="b45ad-174">palette handle</span></span></li>
<li><span data-ttu-id="b45ad-175">режим приостановки</span><span class="sxs-lookup"><span data-stu-id="b45ad-175">pause mode</span></span></li>
<li><span data-ttu-id="b45ad-176">скорость воспроизведения</span><span class="sxs-lookup"><span data-stu-id="b45ad-176">play speed</span></span></li>
<li><span data-ttu-id="b45ad-177">position</span><span class="sxs-lookup"><span data-stu-id="b45ad-177">position</span></span></li>
<li><span data-ttu-id="b45ad-178"><em>номер</em> отслеживания расположения</span><span class="sxs-lookup"><span data-stu-id="b45ad-178">position track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-179">всё</span><span class="sxs-lookup"><span data-stu-id="b45ad-179">ready</span></span></li>
<li><span data-ttu-id="b45ad-180">Частота кадров записи</span><span class="sxs-lookup"><span data-stu-id="b45ad-180">record frame rate</span></span></li>
<li><span data-ttu-id="b45ad-181">Ссылочный <em>фрейм</em></span><span class="sxs-lookup"><span data-stu-id="b45ad-181">reference <em>frame</em></span></span></li>
<li><span data-ttu-id="b45ad-182">зарезервированный размер</span><span class="sxs-lookup"><span data-stu-id="b45ad-182">reserved size</span></span></li>
<li><span data-ttu-id="b45ad-183">правый том</span><span class="sxs-lookup"><span data-stu-id="b45ad-183">right volume</span></span></li>
<li><span data-ttu-id="b45ad-184">Поиск в точности</span><span class="sxs-lookup"><span data-stu-id="b45ad-184">seek exactly</span></span></li>
<li><span data-ttu-id="b45ad-185">четкость</span><span class="sxs-lookup"><span data-stu-id="b45ad-185">sharpness</span></span></li>
<li><span data-ttu-id="b45ad-186">SMPTE</span><span class="sxs-lookup"><span data-stu-id="b45ad-186">smpte</span></span></li>
<li><span data-ttu-id="b45ad-187">Скорость</span><span class="sxs-lookup"><span data-stu-id="b45ad-187">speed</span></span></li>
<li><span data-ttu-id="b45ad-188">начальное расположение</span><span class="sxs-lookup"><span data-stu-id="b45ad-188">start position</span></span></li>
<li><span data-ttu-id="b45ad-189">формат файла по-прежнему</span><span class="sxs-lookup"><span data-stu-id="b45ad-189">still file format</span></span></li>
<li><span data-ttu-id="b45ad-190">формат времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-190">time format</span></span></li>
<li><span data-ttu-id="b45ad-191">Интенсив</span><span class="sxs-lookup"><span data-stu-id="b45ad-191">tint</span></span></li>
<li><span data-ttu-id="b45ad-192">частот</span><span class="sxs-lookup"><span data-stu-id="b45ad-192">treble</span></span></li>
<li><span data-ttu-id="b45ad-193">несохраненные</span><span class="sxs-lookup"><span data-stu-id="b45ad-193">unsaved</span></span></li>
<li><span data-ttu-id="b45ad-194">видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-194">video</span></span></li>
<li><span data-ttu-id="b45ad-195">индекс ключа видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-195">video key index</span></span></li>
<li><span data-ttu-id="b45ad-196">цвет ключа видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-196">video key color</span></span></li>
<li><span data-ttu-id="b45ad-197">запись видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-197">video record</span></span></li>
<li><span data-ttu-id="b45ad-198">источник видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-198">video source</span></span></li>
<li><span data-ttu-id="b45ad-199">Исходный номер видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-199">video source number</span></span></li>
<li><span data-ttu-id="b45ad-200">поток видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-200">video stream</span></span></li>
<li><span data-ttu-id="b45ad-201">том</span><span class="sxs-lookup"><span data-stu-id="b45ad-201">volume</span></span></li>
<li><span data-ttu-id="b45ad-202">маркер окна</span><span class="sxs-lookup"><span data-stu-id="b45ad-202">window handle</span></span></li>
<li><span data-ttu-id="b45ad-203">видимое окно</span><span class="sxs-lookup"><span data-stu-id="b45ad-203">window visible</span></span></li>
<li><span data-ttu-id="b45ad-204">окно уменьшено</span><span class="sxs-lookup"><span data-stu-id="b45ad-204">window minimized</span></span></li>
<li><span data-ttu-id="b45ad-205">окно развернуто</span><span class="sxs-lookup"><span data-stu-id="b45ad-205">window maximized</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-206">overlay</span><span class="sxs-lookup"><span data-stu-id="b45ad-206">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="b45ad-207">носитель отсутствует</span><span class="sxs-lookup"><span data-stu-id="b45ad-207">media present</span></span></li>
<li><span data-ttu-id="b45ad-208">mode</span><span class="sxs-lookup"><span data-stu-id="b45ad-208">mode</span></span></li>
<li><span data-ttu-id="b45ad-209">число дорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-209">number of tracks</span></span></li>
<li><span data-ttu-id="b45ad-210">всё</span><span class="sxs-lookup"><span data-stu-id="b45ad-210">ready</span></span></li>
<li><span data-ttu-id="b45ad-211">растяжение</span><span class="sxs-lookup"><span data-stu-id="b45ad-211">stretch</span></span></li>
<li><span data-ttu-id="b45ad-212">маркер окна</span><span class="sxs-lookup"><span data-stu-id="b45ad-212">window handle</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-213">sequencer</span><span class="sxs-lookup"><span data-stu-id="b45ad-213">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="b45ad-214">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-214">current track</span></span></li>
<li><span data-ttu-id="b45ad-215">Тип деления</span><span class="sxs-lookup"><span data-stu-id="b45ad-215">division type</span></span></li>
<li><span data-ttu-id="b45ad-216">length</span><span class="sxs-lookup"><span data-stu-id="b45ad-216">length</span></span></li>
<li><span data-ttu-id="b45ad-217">образец <em>номера</em> записи о длине</span><span class="sxs-lookup"><span data-stu-id="b45ad-217">length track <em>number</em> master</span></span></li>
<li><span data-ttu-id="b45ad-218">носитель отсутствует</span><span class="sxs-lookup"><span data-stu-id="b45ad-218">media present</span></span></li>
<li><span data-ttu-id="b45ad-219">mode</span><span class="sxs-lookup"><span data-stu-id="b45ad-219">mode</span></span></li>
<li><span data-ttu-id="b45ad-220">число дорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-220">number of tracks</span></span></li>
<li><span data-ttu-id="b45ad-221">offset</span><span class="sxs-lookup"><span data-stu-id="b45ad-221">offset</span></span></li>
<li><span data-ttu-id="b45ad-222">порт</span><span class="sxs-lookup"><span data-stu-id="b45ad-222">port</span></span></li>
<li><span data-ttu-id="b45ad-223">position</span><span class="sxs-lookup"><span data-stu-id="b45ad-223">position</span></span></li>
<li><span data-ttu-id="b45ad-224"><em>номер</em> отслеживания расположения</span><span class="sxs-lookup"><span data-stu-id="b45ad-224">position track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-225">всё</span><span class="sxs-lookup"><span data-stu-id="b45ad-225">ready</span></span></li>
<li><span data-ttu-id="b45ad-226">подчинен</span><span class="sxs-lookup"><span data-stu-id="b45ad-226">slave</span></span></li>
<li><span data-ttu-id="b45ad-227">начальное расположение</span><span class="sxs-lookup"><span data-stu-id="b45ad-227">start position</span></span></li>
<li><span data-ttu-id="b45ad-228">темп</span><span class="sxs-lookup"><span data-stu-id="b45ad-228">tempo</span></span></li>
<li><span data-ttu-id="b45ad-229">формат времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-229">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-230">видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="b45ad-230">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="b45ad-231">собрать запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-231">assemble record</span></span></li>
<li><span data-ttu-id="b45ad-232">звуковой монитор</span><span class="sxs-lookup"><span data-stu-id="b45ad-232">audio monitor</span></span></li>
<li><span data-ttu-id="b45ad-233">номер звукового монитора</span><span class="sxs-lookup"><span data-stu-id="b45ad-233">audio monitor number</span></span></li>
<li><span data-ttu-id="b45ad-234">звуковая запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-234">audio record</span></span></li>
<li><span data-ttu-id="b45ad-235"><em>номер</em> дорожки записи звука</span><span class="sxs-lookup"><span data-stu-id="b45ad-235">audio record track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-236">источник звука</span><span class="sxs-lookup"><span data-stu-id="b45ad-236">audio source</span></span></li>
<li><span data-ttu-id="b45ad-237">номер источника аудио</span><span class="sxs-lookup"><span data-stu-id="b45ad-237">audio source number</span></span></li>
<li><span data-ttu-id="b45ad-238">channel</span><span class="sxs-lookup"><span data-stu-id="b45ad-238">channel</span></span></li>
<li><span data-ttu-id="b45ad-239"><em>номер</em> тюнера канала</span><span class="sxs-lookup"><span data-stu-id="b45ad-239">channel tuner <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-240">clock</span><span class="sxs-lookup"><span data-stu-id="b45ad-240">clock</span></span></li>
<li><span data-ttu-id="b45ad-241">Идентификатор часов</span><span class="sxs-lookup"><span data-stu-id="b45ad-241">clock id</span></span></li>
<li><span data-ttu-id="b45ad-242">Счетчик</span><span class="sxs-lookup"><span data-stu-id="b45ad-242">counter</span></span></li>
<li><span data-ttu-id="b45ad-243">Формат счетчика</span><span class="sxs-lookup"><span data-stu-id="b45ad-243">counter format</span></span></li>
<li><span data-ttu-id="b45ad-244">разрешение счетчиков</span><span class="sxs-lookup"><span data-stu-id="b45ad-244">counter resolution</span></span></li>
<li><span data-ttu-id="b45ad-245">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-245">current track</span></span></li>
<li><span data-ttu-id="b45ad-246">Частота кадров</span><span class="sxs-lookup"><span data-stu-id="b45ad-246">frame rate</span></span></li>
<li><span data-ttu-id="b45ad-247">index</span><span class="sxs-lookup"><span data-stu-id="b45ad-247">index</span></span></li>
<li><span data-ttu-id="b45ad-248">индекс по</span><span class="sxs-lookup"><span data-stu-id="b45ad-248">index on</span></span></li>
<li><span data-ttu-id="b45ad-249">length</span><span class="sxs-lookup"><span data-stu-id="b45ad-249">length</span></span></li>
<li><span data-ttu-id="b45ad-250"><em>номер</em> записи о длине</span><span class="sxs-lookup"><span data-stu-id="b45ad-250">length track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-251">носитель отсутствует</span><span class="sxs-lookup"><span data-stu-id="b45ad-251">media present</span></span></li>
<li><span data-ttu-id="b45ad-252">Тип носителя</span><span class="sxs-lookup"><span data-stu-id="b45ad-252">media type</span></span></li>
<li><span data-ttu-id="b45ad-253">mode</span><span class="sxs-lookup"><span data-stu-id="b45ad-253">mode</span></span></li>
<li><span data-ttu-id="b45ad-254">Число звуковых дорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-254">number of audio tracks</span></span></li>
<li><span data-ttu-id="b45ad-255">число дорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-255">number of tracks</span></span></li>
<li><span data-ttu-id="b45ad-256">число видеодорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-256">number of video tracks</span></span></li>
<li><span data-ttu-id="b45ad-257"><em>время ожидания</em> приостановки</span><span class="sxs-lookup"><span data-stu-id="b45ad-257">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="b45ad-258">Формат воспроизведения</span><span class="sxs-lookup"><span data-stu-id="b45ad-258">play format</span></span></li>
<li><span data-ttu-id="b45ad-259">position</span><span class="sxs-lookup"><span data-stu-id="b45ad-259">position</span></span></li>
<li><span data-ttu-id="b45ad-260">Начало должности</span><span class="sxs-lookup"><span data-stu-id="b45ad-260">position start</span></span></li>
<li><span data-ttu-id="b45ad-261"><em>номер</em> отслеживания расположения</span><span class="sxs-lookup"><span data-stu-id="b45ad-261">position track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-262"><em>Длительность</em> выкрутки</span><span class="sxs-lookup"><span data-stu-id="b45ad-262">postroll <em>duration</em></span></span></li>
<li><span data-ttu-id="b45ad-263">Включение</span><span class="sxs-lookup"><span data-stu-id="b45ad-263">power on</span></span></li>
<li><span data-ttu-id="b45ad-264"><em>Длительность</em> предпробного выполнения</span><span class="sxs-lookup"><span data-stu-id="b45ad-264">preroll <em>duration</em></span></span></li>
<li><span data-ttu-id="b45ad-265">всё</span><span class="sxs-lookup"><span data-stu-id="b45ad-265">ready</span></span></li>
<li><span data-ttu-id="b45ad-266">формат записи</span><span class="sxs-lookup"><span data-stu-id="b45ad-266">record format</span></span></li>
<li><span data-ttu-id="b45ad-267">Скорость</span><span class="sxs-lookup"><span data-stu-id="b45ad-267">speed</span></span></li>
<li><span data-ttu-id="b45ad-268">формат времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-268">time format</span></span></li>
<li><span data-ttu-id="b45ad-269">режим времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-269">time mode</span></span></li>
<li><span data-ttu-id="b45ad-270">тип времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-270">time type</span></span></li>
<li><span data-ttu-id="b45ad-271">код времени имеется</span><span class="sxs-lookup"><span data-stu-id="b45ad-271">timecode present</span></span></li>
<li><span data-ttu-id="b45ad-272">запись времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-272">timecode record</span></span></li>
<li><span data-ttu-id="b45ad-273">тип времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-273">timecode type</span></span></li>
<li><span data-ttu-id="b45ad-274">номер тюнера</span><span class="sxs-lookup"><span data-stu-id="b45ad-274">tuner number</span></span></li>
<li><span data-ttu-id="b45ad-275">монитор видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-275">video monitor</span></span></li>
<li><span data-ttu-id="b45ad-276">номер монитора видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-276">video monitor number</span></span></li>
<li><span data-ttu-id="b45ad-277">запись видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-277">video record</span></span></li>
<li><span data-ttu-id="b45ad-278"><em>номер</em> дорожки записи видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-278">video record track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-279">источник видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-279">video source</span></span></li>
<li><span data-ttu-id="b45ad-280">Исходный номер видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-280">video source number</span></span></li>
<li><span data-ttu-id="b45ad-281">защищено от записи</span><span class="sxs-lookup"><span data-stu-id="b45ad-281">write protected</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-282">видеодиск</span><span class="sxs-lookup"><span data-stu-id="b45ad-282">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="b45ad-283">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-283">current track</span></span></li>
<li><span data-ttu-id="b45ad-284">Размер диска</span><span class="sxs-lookup"><span data-stu-id="b45ad-284">disc size</span></span></li>
<li><span data-ttu-id="b45ad-285">forward</span><span class="sxs-lookup"><span data-stu-id="b45ad-285">forward</span></span></li>
<li><span data-ttu-id="b45ad-286">length</span><span class="sxs-lookup"><span data-stu-id="b45ad-286">length</span></span></li>
<li><span data-ttu-id="b45ad-287"><em>номер</em> записи о длине</span><span class="sxs-lookup"><span data-stu-id="b45ad-287">length track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-288">носитель отсутствует</span><span class="sxs-lookup"><span data-stu-id="b45ad-288">media present</span></span></li>
<li><span data-ttu-id="b45ad-289">Тип носителя</span><span class="sxs-lookup"><span data-stu-id="b45ad-289">media type</span></span></li>
<li><span data-ttu-id="b45ad-290">mode</span><span class="sxs-lookup"><span data-stu-id="b45ad-290">mode</span></span></li>
<li><span data-ttu-id="b45ad-291">число дорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-291">number of tracks</span></span></li>
<li><span data-ttu-id="b45ad-292">position</span><span class="sxs-lookup"><span data-stu-id="b45ad-292">position</span></span></li>
<li><span data-ttu-id="b45ad-293"><em>номер</em> отслеживания расположения</span><span class="sxs-lookup"><span data-stu-id="b45ad-293">position track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-294">всё</span><span class="sxs-lookup"><span data-stu-id="b45ad-294">ready</span></span></li>
<li><span data-ttu-id="b45ad-295">сбоку</span><span class="sxs-lookup"><span data-stu-id="b45ad-295">side</span></span></li>
<li><span data-ttu-id="b45ad-296">Скорость</span><span class="sxs-lookup"><span data-stu-id="b45ad-296">speed</span></span></li>
<li><span data-ttu-id="b45ad-297">начальное расположение</span><span class="sxs-lookup"><span data-stu-id="b45ad-297">start position</span></span></li>
<li><span data-ttu-id="b45ad-298">формат времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-298">time format</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-299">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="b45ad-299">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="b45ad-300">выравнивание</span><span class="sxs-lookup"><span data-stu-id="b45ad-300">alignment</span></span></li>
<li><span data-ttu-id="b45ad-301">битсперсампле</span><span class="sxs-lookup"><span data-stu-id="b45ad-301">bitspersample</span></span></li>
<li><span data-ttu-id="b45ad-302">битесперсек</span><span class="sxs-lookup"><span data-stu-id="b45ad-302">bytespersec</span></span></li>
<li><span data-ttu-id="b45ad-303">каналов</span><span class="sxs-lookup"><span data-stu-id="b45ad-303">channels</span></span></li>
<li><span data-ttu-id="b45ad-304">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-304">current track</span></span></li>
<li><span data-ttu-id="b45ad-305">Формат тега</span><span class="sxs-lookup"><span data-stu-id="b45ad-305">format tag</span></span></li>
<li><span data-ttu-id="b45ad-306">input</span><span class="sxs-lookup"><span data-stu-id="b45ad-306">input</span></span></li>
<li><span data-ttu-id="b45ad-307">length</span><span class="sxs-lookup"><span data-stu-id="b45ad-307">length</span></span></li>
<li><span data-ttu-id="b45ad-308"><em>номер</em> записи о длине</span><span class="sxs-lookup"><span data-stu-id="b45ad-308">length track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-309">уровень</span><span class="sxs-lookup"><span data-stu-id="b45ad-309">level</span></span></li>
<li><span data-ttu-id="b45ad-310">носитель отсутствует</span><span class="sxs-lookup"><span data-stu-id="b45ad-310">media present</span></span></li>
<li><span data-ttu-id="b45ad-311">mode</span><span class="sxs-lookup"><span data-stu-id="b45ad-311">mode</span></span></li>
<li><span data-ttu-id="b45ad-312">число дорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-312">number of tracks</span></span></li>
<li><span data-ttu-id="b45ad-313">output</span><span class="sxs-lookup"><span data-stu-id="b45ad-313">output</span></span></li>
<li><span data-ttu-id="b45ad-314">position</span><span class="sxs-lookup"><span data-stu-id="b45ad-314">position</span></span></li>
<li><span data-ttu-id="b45ad-315"><em>номер</em> отслеживания расположения</span><span class="sxs-lookup"><span data-stu-id="b45ad-315">position track <em>number</em></span></span></li>
<li><span data-ttu-id="b45ad-316">всё</span><span class="sxs-lookup"><span data-stu-id="b45ad-316">ready</span></span></li>
<li><span data-ttu-id="b45ad-317">самплесперсек</span><span class="sxs-lookup"><span data-stu-id="b45ad-317">samplespersec</span></span></li>
<li><span data-ttu-id="b45ad-318">начальное расположение</span><span class="sxs-lookup"><span data-stu-id="b45ad-318">start position</span></span></li>
<li><span data-ttu-id="b45ad-319">формат времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-319">time format</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b45ad-320">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсзрекуест** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="b45ad-320">The following table lists the flags that can be specified in the **lpszRequest** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b45ad-321">Значение</span><span class="sxs-lookup"><span data-stu-id="b45ad-321">Value</span></span></th>
<th><span data-ttu-id="b45ad-322">Значение</span><span class="sxs-lookup"><span data-stu-id="b45ad-322">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b45ad-323">выравнивание</span><span class="sxs-lookup"><span data-stu-id="b45ad-323">alignment</span></span></td>
<td><span data-ttu-id="b45ad-324">Возвращает выравнивание блока данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="b45ad-324">Returns the block alignment of data, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-325">собрать запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-325">assemble record</span></span></td>
<td><span data-ttu-id="b45ad-326">Возвращает <strong>значение true</strong> , если устройство настроено для записи в режиме сборки.</span><span class="sxs-lookup"><span data-stu-id="b45ad-326">Returns <strong>TRUE</strong> if the device is set to assemble mode recording.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-327">звук</span><span class="sxs-lookup"><span data-stu-id="b45ad-327">audio</span></span></td>
<td><span data-ttu-id="b45ad-328">Возвращает &quot; &quot; или &quot; отключает в &quot; зависимости от самой последней команды <a href="setaudio.md">сетаудио</a> &quot; On &quot; или &quot; Off &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-328">Returns &quot;on&quot; or &quot;off&quot; depending on the most recent <a href="setaudio.md">setaudio</a> &quot;on&quot; or &quot;off&quot; command.</span></span> <span data-ttu-id="b45ad-329">Он возвращает &quot; значение &quot; , если один или оба динамика включены, и &quot; &quot; в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b45ad-329">It returns &quot;on&quot; if either or both speakers are enabled, and &quot;off&quot; otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-330">Выравнивание звука</span><span class="sxs-lookup"><span data-stu-id="b45ad-330">audio alignment</span></span></td>
<td><span data-ttu-id="b45ad-331">Возвращает выравнивание блоков данных относительно начала входных аудио-данных.</span><span class="sxs-lookup"><span data-stu-id="b45ad-331">Returns the alignment of data blocks relative to the start of input waveform-audio data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-332">аудио битсперсампле</span><span class="sxs-lookup"><span data-stu-id="b45ad-332">audio bitspersample</span></span></td>
<td><span data-ttu-id="b45ad-333">Возвращает количество бит на выборку, используемое устройством для записи.</span><span class="sxs-lookup"><span data-stu-id="b45ad-333">Returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="b45ad-334">Этот флаг применяется только к устройствам, поддерживающим &quot; &quot; алгоритм PCM.</span><span class="sxs-lookup"><span data-stu-id="b45ad-334">This flag applies only to devices supporting the &quot;pcm&quot; algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-335">обрывы звука</span><span class="sxs-lookup"><span data-stu-id="b45ad-335">audio breaks</span></span></td>
<td><span data-ttu-id="b45ad-336">Возвращает, сколько раз была нарушена звуковая часть последней последовательности AVI.</span><span class="sxs-lookup"><span data-stu-id="b45ad-336">Returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="b45ad-337">Система подсчитывает разрыв звука при попытке записи звуковых данных в драйвер устройства и обнаруживает, что драйвер уже воспроизводил все доступные данные.</span><span class="sxs-lookup"><span data-stu-id="b45ad-337">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="b45ad-338">Этот флаг распознается только драйвером МЦИАВИ Digital-Video.</span><span class="sxs-lookup"><span data-stu-id="b45ad-338">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="b45ad-339">Он предназначен только для оценки производительности; Возвращаемое значение сложно интерпретировать.</span><span class="sxs-lookup"><span data-stu-id="b45ad-339">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-340">аудио битесперсек</span><span class="sxs-lookup"><span data-stu-id="b45ad-340">audio bytespersec</span></span></td>
<td><span data-ttu-id="b45ad-341">Возвращает среднее число байтов, используемых для записи в секунду.</span><span class="sxs-lookup"><span data-stu-id="b45ad-341">Returns the average number of bytes per second used for recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-342">звуковые входные данные</span><span class="sxs-lookup"><span data-stu-id="b45ad-342">audio input</span></span></td>
<td><span data-ttu-id="b45ad-343">Возвращает приблизительный моментальный звуковой сигнал аналогового входного звукового сигнала.</span><span class="sxs-lookup"><span data-stu-id="b45ad-343">Returns the approximate instantaneous audio level of the analog input audio signal.</span></span> <span data-ttu-id="b45ad-344">Значение больше 1000 означает вырезание искажений.</span><span class="sxs-lookup"><span data-stu-id="b45ad-344">A value greater than 1000 implies clipping distortion.</span></span> <span data-ttu-id="b45ad-345">Некоторые устройства могут возвращать это значение только при записи звука.</span><span class="sxs-lookup"><span data-stu-id="b45ad-345">Some devices can return this value only while recording audio.</span></span> <span data-ttu-id="b45ad-346">Значение не имеет связанной команды <a href="set.md">Set</a> или <a href="setaudio.md">сетаудио</a> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-346">The value has no associated <a href="set.md">set</a> or <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-347">звуковой монитор</span><span class="sxs-lookup"><span data-stu-id="b45ad-347">audio monitor</span></span></td>
<td><span data-ttu-id="b45ad-348">Возвращает &quot; выходные данные &quot; или один из допустимых входных типов источника.</span><span class="sxs-lookup"><span data-stu-id="b45ad-348">Returns &quot;output&quot;, or one of the valid source-input types.</span></span> <span data-ttu-id="b45ad-349">Дополнительные сведения см. в описании <strong></strong> &quot; команды Monitor сетаудио &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-349">For more information, see the <strong>setaudio</strong> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-350">номер звукового монитора</span><span class="sxs-lookup"><span data-stu-id="b45ad-350">audio monitor number</span></span></td>
<td><span data-ttu-id="b45ad-351">Возвращает номер отслеживаемого видео типа, указанный в мониторе <strong>состояния</strong> &quot; Audio &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-351">Returns the monitored-video number of the type specified by <strong>status</strong> &quot;audio monitor&quot;.</span></span> <span data-ttu-id="b45ad-352">Дополнительные сведения см. в описании команды <a href="setaudio.md">сетаудио</a> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-352">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-353">звуковая запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-353">audio record</span></span></td>
<td><span data-ttu-id="b45ad-354">Возвращает &quot; &quot; или &quot; отключает &quot; , отражая состояние, заданное записью <strong>сетаудио</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-354">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by <strong>setaudio</strong> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-355"><em>номер</em> дорожки записи звука</span><span class="sxs-lookup"><span data-stu-id="b45ad-355">audio record track <em>number</em></span></span></td>
<td><span data-ttu-id="b45ad-356">Возвращает <strong>значение true</strong> , если видеомагнитофон настроен для записи звука.</span><span class="sxs-lookup"><span data-stu-id="b45ad-356">Returns <strong>TRUE</strong> if the VCR is set to record audio.</span></span> <span data-ttu-id="b45ad-357">Если номер записи не указан, предполагается значение по умолчанию, равное 1.</span><span class="sxs-lookup"><span data-stu-id="b45ad-357">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-358">аудио самплесперсек</span><span class="sxs-lookup"><span data-stu-id="b45ad-358">audio samplespersec</span></span></td>
<td><span data-ttu-id="b45ad-359">Возвращает число записанных выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="b45ad-359">Returns the number of samples per second recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-360">источник звука</span><span class="sxs-lookup"><span data-stu-id="b45ad-360">audio source</span></span></td>
<td><span data-ttu-id="b45ad-361">Возвращает текущий источник аудио дигитайзера: &quot; левое &quot; , &quot; правое &quot; , &quot; Среднее &quot; или &quot; стерео &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-361">Returns the current audio digitizer source: &quot;left&quot;, &quot;right&quot;, &quot;average&quot;, or &quot;stereo&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-362">номер источника аудио</span><span class="sxs-lookup"><span data-stu-id="b45ad-362">audio source number</span></span></td>
<td><span data-ttu-id="b45ad-363">Возвращает номер источника звука для типа, возвращенного источником звука <strong>состояния</strong> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-363">Returns the audio-source number of the type returned by <strong>status</strong> &quot;audio source&quot;.</span></span> <span data-ttu-id="b45ad-364">Дополнительные сведения см. в описании команды <a href="setaudio.md">сетаудио</a> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-364">For more information, see the <a href="setaudio.md">setaudio</a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-365">аудиопоток</span><span class="sxs-lookup"><span data-stu-id="b45ad-365">audio stream</span></span></td>
<td><span data-ttu-id="b45ad-366">Возвращает текущий номер звукового потока.</span><span class="sxs-lookup"><span data-stu-id="b45ad-366">Returns the current audio-stream number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-367">низким</span><span class="sxs-lookup"><span data-stu-id="b45ad-367">bass</span></span></td>
<td><span data-ttu-id="b45ad-368">Возвращает текущий уровень громкости звука.</span><span class="sxs-lookup"><span data-stu-id="b45ad-368">Returns the current audio-bass level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-369">битсперпел</span><span class="sxs-lookup"><span data-stu-id="b45ad-369">bitsperpel</span></span></td>
<td><span data-ttu-id="b45ad-370">Возвращает число битов на пиксель для сохранения записанных или записанных данных.</span><span class="sxs-lookup"><span data-stu-id="b45ad-370">Returns the number of bits per pixel for saving captured or recorded data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-371">битсперсампле</span><span class="sxs-lookup"><span data-stu-id="b45ad-371">bitspersample</span></span></td>
<td><span data-ttu-id="b45ad-372">Возвращает биты на выборку.</span><span class="sxs-lookup"><span data-stu-id="b45ad-372">Returns the bits per sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-373">brightness</span><span class="sxs-lookup"><span data-stu-id="b45ad-373">brightness</span></span></td>
<td><span data-ttu-id="b45ad-374">Возвращает текущий уровень яркости видео.</span><span class="sxs-lookup"><span data-stu-id="b45ad-374">Returns the current video-brightness level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-375">битесперсек</span><span class="sxs-lookup"><span data-stu-id="b45ad-375">bytespersec</span></span></td>
<td><span data-ttu-id="b45ad-376">Возвращает среднее число воспроизводимых или записанных байт в секунду.</span><span class="sxs-lookup"><span data-stu-id="b45ad-376">Returns the average number of bytes per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-377"><em>номер</em> направления для типа кдаудио</span><span class="sxs-lookup"><span data-stu-id="b45ad-377">cdaudio type track <em>number</em></span></span></td>
<td><span data-ttu-id="b45ad-378">Возвращает тип указанного номера записи.</span><span class="sxs-lookup"><span data-stu-id="b45ad-378">Returns the type of the specified track number.</span></span> <span data-ttu-id="b45ad-379">Это может быть &quot; звук &quot; или &quot; другое.&quot;</span><span class="sxs-lookup"><span data-stu-id="b45ad-379">This can be &quot;audio&quot; or &quot;other.&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-380">channel</span><span class="sxs-lookup"><span data-stu-id="b45ad-380">channel</span></span></td>
<td><span data-ttu-id="b45ad-381">Возвращает целочисленное значение набора каналов, установленного на тюнере.</span><span class="sxs-lookup"><span data-stu-id="b45ad-381">Returns the integer value of the channel set on the tuner.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-382"><em>номер</em> тюнера канала</span><span class="sxs-lookup"><span data-stu-id="b45ad-382">channel tuner <em>number</em></span></span></td>
<td><span data-ttu-id="b45ad-383">Если &quot; задан &quot; <em>номер</em> тюнера, будет возвращен выбранный канал на логическом <em>номере</em> тюнера.</span><span class="sxs-lookup"><span data-stu-id="b45ad-383">If &quot;tuner&quot; <em>number</em> is given, then the currently selected channel on the logical tuner <em>number</em> will be returned.</span></span> <span data-ttu-id="b45ad-384">Обратите внимание, что может быть несколько логических тюнеров.</span><span class="sxs-lookup"><span data-stu-id="b45ad-384">Note that there can be several logical tuners.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-385">каналов</span><span class="sxs-lookup"><span data-stu-id="b45ad-385">channels</span></span></td>
<td><span data-ttu-id="b45ad-386">Возвращает число наборов каналов (1 для Mono, 2 для стерео).</span><span class="sxs-lookup"><span data-stu-id="b45ad-386">Returns the number of channels set (1 for mono, 2 for stereo).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-387">clock</span><span class="sxs-lookup"><span data-stu-id="b45ad-387">clock</span></span></td>
<td><span data-ttu-id="b45ad-388">Возвращает внешнее время.</span><span class="sxs-lookup"><span data-stu-id="b45ad-388">Returns the external time.</span></span> <span data-ttu-id="b45ad-389">Время должно быть длинным целым числом без знака, равным общему количеству приращений.</span><span class="sxs-lookup"><span data-stu-id="b45ad-389">The time must be an unsigned long integer expressing total increments.</span></span> <span data-ttu-id="b45ad-390">Дополнительные сведения см. в описании <a href="capability.md"></a> &quot; команды частота добавочных синхронизирующих импульсов возможностей &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-390">For more information, see the <a href="capability.md">capability</a> &quot;clock increment rate&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-391">Идентификатор часов</span><span class="sxs-lookup"><span data-stu-id="b45ad-391">clock id</span></span></td>
<td><span data-ttu-id="b45ad-392">Возвращает уникальное целое число, определяющее часы.</span><span class="sxs-lookup"><span data-stu-id="b45ad-392">Returns a unique integer identifying the clock.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-393">color</span><span class="sxs-lookup"><span data-stu-id="b45ad-393">color</span></span></td>
<td><span data-ttu-id="b45ad-394">Возвращает текущий уровень цвета.</span><span class="sxs-lookup"><span data-stu-id="b45ad-394">Returns the current color level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-395">контрастность</span><span class="sxs-lookup"><span data-stu-id="b45ad-395">contrast</span></span></td>
<td><span data-ttu-id="b45ad-396">Возвращает текущий уровень контрастности.</span><span class="sxs-lookup"><span data-stu-id="b45ad-396">Returns the current contrast level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-397">Счетчик</span><span class="sxs-lookup"><span data-stu-id="b45ad-397">counter</span></span></td>
<td><span data-ttu-id="b45ad-398">Возвращает расположение счетчика в текущем формате счетчика.</span><span class="sxs-lookup"><span data-stu-id="b45ad-398">Returns the counter position, in the current counter format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-399">Формат счетчика</span><span class="sxs-lookup"><span data-stu-id="b45ad-399">counter format</span></span></td>
<td><span data-ttu-id="b45ad-400">Возвращает текущий формат счетчика.</span><span class="sxs-lookup"><span data-stu-id="b45ad-400">Returns the current counter format.</span></span> <span data-ttu-id="b45ad-401">Дополнительные сведения см. в разделе команда <a href="set.md">задания</a> &quot; формата счетчика &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-401">For more information, see the <a href="set.md">set</a> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-402">разрешение счетчиков</span><span class="sxs-lookup"><span data-stu-id="b45ad-402">counter resolution</span></span></td>
<td><span data-ttu-id="b45ad-403">Возвращает &quot; кадры &quot; или &quot; секунды &quot; , указывающие на разрешение счетчика.</span><span class="sxs-lookup"><span data-stu-id="b45ad-403">Returns &quot;frames&quot; or &quot;seconds&quot;, indicating the counter's resolution.</span></span> <span data-ttu-id="b45ad-404">Это не то же самое, что и точность.</span><span class="sxs-lookup"><span data-stu-id="b45ad-404">This is not the same as accuracy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-405">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="b45ad-405">current track</span></span></td>
<td><span data-ttu-id="b45ad-406">Возвращает текущую запись. МЦИСЕК Sequencer возвращает значение 1.</span><span class="sxs-lookup"><span data-stu-id="b45ad-406">Returns the current track. The MCISEQ sequencer returns 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-407">Размер диска</span><span class="sxs-lookup"><span data-stu-id="b45ad-407">disc size</span></span></td>
<td><span data-ttu-id="b45ad-408">Возвращает значение 8 или 12, указывающее размер загруженного диска в дюймах.</span><span class="sxs-lookup"><span data-stu-id="b45ad-408">Returns either 8 or 12, indicating the size of the loaded disc in inches.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-409"><em>дискового пространства</em></span><span class="sxs-lookup"><span data-stu-id="b45ad-409">disk space <em>drive</em></span></span></td>
<td><span data-ttu-id="b45ad-410">Возвращает приблизительное дисковое пространство в текущем формате времени, которое может быть получено командой <a href="reserve.md">резервирования</a> для указанного диска <em>.</em></span><span class="sxs-lookup"><span data-stu-id="b45ad-410">Returns the approximate disk space, in the current time format, that can be obtained by a <a href="reserve.md">reserve</a> command for the specified disk <em>drive.</em></span></span> <span data-ttu-id="b45ad-411"><em>Диск</em> обычно указывается как одна буква или одна буква, за которыми следует двоеточие (:).</span><span class="sxs-lookup"><span data-stu-id="b45ad-411">The <em>drive</em> is usually specified as a single letter or a single letter followed by a colon (:).</span></span> <span data-ttu-id="b45ad-412">Однако некоторые устройства могут использовать путь.</span><span class="sxs-lookup"><span data-stu-id="b45ad-412">Some devices, however, might use a path.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-413">Тип деления</span><span class="sxs-lookup"><span data-stu-id="b45ad-413">division type</span></span></td>
<td><span data-ttu-id="b45ad-414">Возвращает один из следующих типов разделения файлов:</span><span class="sxs-lookup"><span data-stu-id="b45ad-414">Returns one of the following file division types:</span></span>
<ul>
<li><span data-ttu-id="b45ad-415">ппкн</span><span class="sxs-lookup"><span data-stu-id="b45ad-415">PPQN</span></span></li>
<li><span data-ttu-id="b45ad-416">SMPTE 24 кадра</span><span class="sxs-lookup"><span data-stu-id="b45ad-416">SMPTE 24 frame</span></span></li>
<li><span data-ttu-id="b45ad-417">Кадр SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="b45ad-417">SMPTE 25 frame</span></span></li>
<li><span data-ttu-id="b45ad-418">SMPTE рамка проекции 30</span><span class="sxs-lookup"><span data-stu-id="b45ad-418">SMPTE 30 drop frame</span></span></li>
<li><span data-ttu-id="b45ad-419">SMPTE 30 кадров</span><span class="sxs-lookup"><span data-stu-id="b45ad-419">SMPTE 30 frame</span></span></li>
</ul>
<br/> <span data-ttu-id="b45ad-420">Используйте эти сведения для определения формата файла MIDI и значения темп и сведений о положении.</span><span class="sxs-lookup"><span data-stu-id="b45ad-420">Use this information to determine the format of the MIDI file and the meaning of tempo and position information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-421">завершение файла</span><span class="sxs-lookup"><span data-stu-id="b45ad-421">file completion</span></span></td>
<td><span data-ttu-id="b45ad-422">Возвращает оценочный процент выполнения операции <a href="load.md">загрузки</a>, <a href="save.md">сохранения</a>, <a href="capture.md">записи</a>, <a href="cut.md">вырезания</a>, <a href="copy.md">копирования</a>, <a href="delete.md">удаления</a>, <a href="paste.md">вставки</a>или <a href="undo.md">отмены</a> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-422">Returns the estimated percentage a <a href="load.md">load</a>, <a href="save.md">save</a>, <a href="capture.md">capture</a>, <a href="cut.md">cut</a>, <a href="copy.md">copy</a>, <a href="delete.md">delete</a>, <a href="paste.md">paste</a>, or <a href="undo.md">undo</a> operation has progressed.</span></span> <span data-ttu-id="b45ad-423">(Приложения могут использовать это для предоставления визуального индикатора хода выполнения.)</span><span class="sxs-lookup"><span data-stu-id="b45ad-423">(Applications can use this to provide a visual indicator of progress.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-424">формат файлов</span><span class="sxs-lookup"><span data-stu-id="b45ad-424">file format</span></span></td>
<td><span data-ttu-id="b45ad-425">Возвращает текущий формат файла для команд <a href="record.md">записи</a> или <strong>сохранения</strong> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-425">Returns the current file format for <a href="record.md">record</a> or <strong>save</strong> commands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-426">файловый режим</span><span class="sxs-lookup"><span data-stu-id="b45ad-426">file mode</span></span></td>
<td><span data-ttu-id="b45ad-427">Возвращает &quot; загрузку &quot; , &quot; Сохранение &quot; , &quot; изменение &quot; или &quot; бездействие &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-427">Returns &quot;loading&quot;, &quot;saving&quot;, &quot;editing&quot;, or &quot;idle&quot;.</span></span> <span data-ttu-id="b45ad-428">Во время операции <a href="load.md"><strong>загрузки</strong></a> возвращается &quot; Загрузка &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-428">During a <a href="load.md"><strong>load</strong></a> operation, it returns &quot;loading&quot;.</span></span> <span data-ttu-id="b45ad-429">Во время операций <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>сохранения</strong></a> и <a href="capture.md"><strong>записи</strong></a> он возвращает &quot; Сохранение &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-429">During <a href="https://www.bing.com/search?q=<strong>save</strong>"><strong>save</strong></a> and <a href="capture.md"><strong>capture</strong></a> operations, it returns &quot;saving&quot;.</span></span> <span data-ttu-id="b45ad-430">Во время операций <a href="cut.md"><strong>вырезания</strong></a>, <a href="copy.md"><strong>копирования</strong></a>, <a href="delete.md"><strong>удаления</strong></a>, <a href="paste.md"><strong>вставки</strong></a>и <a href="undo.md"><strong>отмены</strong></a> она возвращает &quot; Редактирование &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-430">During <a href="cut.md"><strong>cut</strong></a>, <a href="copy.md"><strong>copy</strong></a>, <a href="delete.md"><strong>delete</strong></a>, <a href="paste.md"><strong>paste</strong></a>, or <a href="undo.md"><strong>undo</strong></a> operations, it returns &quot;editing&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-431">Формат тега</span><span class="sxs-lookup"><span data-stu-id="b45ad-431">format tag</span></span></td>
<td><span data-ttu-id="b45ad-432">Возвращает тег формата.</span><span class="sxs-lookup"><span data-stu-id="b45ad-432">Returns the format tag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-433">forward</span><span class="sxs-lookup"><span data-stu-id="b45ad-433">forward</span></span></td>
<td><span data-ttu-id="b45ad-434">Возвращает <strong>значение true</strong> , если направление воспроизведения передается вперед или устройство не воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="b45ad-434">Returns <strong>TRUE</strong> if the play direction is forward or if the device is not playing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-435">Частота кадров</span><span class="sxs-lookup"><span data-stu-id="b45ad-435">frame rate</span></span></td>
<td><span data-ttu-id="b45ad-436">Возвращает число кадров в секунду, которое устройство будет использовать по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b45ad-436">Returns the number of frames per second that the device will use by default.</span></span> <span data-ttu-id="b45ad-437">Устройства NTSC возвращают 30, PAL 25 и т. д.</span><span class="sxs-lookup"><span data-stu-id="b45ad-437">NTSC devices return 30, PAL 25, and so on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-438">пропущенные кадры</span><span class="sxs-lookup"><span data-stu-id="b45ad-438">frames skipped</span></span></td>
<td><span data-ttu-id="b45ad-439">Возвращает число кадров, которые не были выведены при воспроизведении последней последовательности AVI.</span><span class="sxs-lookup"><span data-stu-id="b45ad-439">Returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="b45ad-440">Этот флаг распознается только драйвером МЦИАВИ Digital-Video.</span><span class="sxs-lookup"><span data-stu-id="b45ad-440">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="b45ad-441">Он предназначен только для оценки производительности; Возвращаемое значение сложно интерпретировать.</span><span class="sxs-lookup"><span data-stu-id="b45ad-441">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-442">gamma</span><span class="sxs-lookup"><span data-stu-id="b45ad-442">gamma</span></span></td>
<td><span data-ttu-id="b45ad-443">Возвращает значение, заданное <a href="setvideo.md"><strong></strong></a> с помощью &quot; гаммы сетвидео &quot; <em></em>.</span><span class="sxs-lookup"><span data-stu-id="b45ad-443">Returns the value set with <a href="setvideo.md"><strong>setvideo</strong></a> &quot;gamma to&quot; <em>value</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-444">index</span><span class="sxs-lookup"><span data-stu-id="b45ad-444">index</span></span></td>
<td><span data-ttu-id="b45ad-445">Возвращает текущий отображаемый индекс.</span><span class="sxs-lookup"><span data-stu-id="b45ad-445">Returns the current index display.</span></span> <span data-ttu-id="b45ad-446">Дополнительные сведения см. в описании команды <a href="set.md"><strong>Set</strong></a> &quot; index &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-446">For more information, see the <a href="set.md"><strong>set</strong></a> &quot;index&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-447">индекс по</span><span class="sxs-lookup"><span data-stu-id="b45ad-447">index on</span></span></td>
<td><span data-ttu-id="b45ad-448">Возвращает <strong>значение true</strong> , если индекс включен.</span><span class="sxs-lookup"><span data-stu-id="b45ad-448">Returns <strong>TRUE</strong> if the index is on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-449">input</span><span class="sxs-lookup"><span data-stu-id="b45ad-449">input</span></span></td>
<td><span data-ttu-id="b45ad-450">Возвращает входной набор.</span><span class="sxs-lookup"><span data-stu-id="b45ad-450">Returns the input set.</span></span> <span data-ttu-id="b45ad-451">Если он не задан, то возвращенная ошибка указывает, что можно использовать любое устройство.</span><span class="sxs-lookup"><span data-stu-id="b45ad-451">If one is not set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="b45ad-452">Для устройств с цифровыми видео изменяет низкие частоты, &quot; &quot; &quot; высокие частоты, &quot; &quot; громкость, &quot; &quot; яркость &quot; , &quot; Цвет &quot; , &quot; контрастность &quot; , &quot; гамма &quot; , &quot; резкость &quot; или &quot; флаг оттенка, &quot; чтобы он применялся только к входным данным.</span><span class="sxs-lookup"><span data-stu-id="b45ad-452">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the input.</span></span> <span data-ttu-id="b45ad-453">Это значение по умолчанию при мониторинге входных данных.</span><span class="sxs-lookup"><span data-stu-id="b45ad-453">This is the default when monitoring the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-454">левый том</span><span class="sxs-lookup"><span data-stu-id="b45ad-454">left volume</span></span></td>
<td><span data-ttu-id="b45ad-455">Возвращает набор томов для левого канала звука.</span><span class="sxs-lookup"><span data-stu-id="b45ad-455">Returns the volume set for the left audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-456">length</span><span class="sxs-lookup"><span data-stu-id="b45ad-456">length</span></span></td>
<td><span data-ttu-id="b45ad-457">Возвращает общую длину носителя в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="b45ad-457">Returns the total length of the media, in the current time format.</span></span> <span data-ttu-id="b45ad-458">Для файлов ППКН длина возвращается в единицах указателя песни.</span><span class="sxs-lookup"><span data-stu-id="b45ad-458">For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="b45ad-459">Для файлов SMPTE он возвращается как <em>чч: мм: СС: FF</em>, где <em>чч</em> — часы, <em>mm</em> — минуты, <em>SS</em> — секунды, а <em>FF</em> — кадры.</span><span class="sxs-lookup"><span data-stu-id="b45ad-459">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="b45ad-460">Для устройств ВИДЕОМАГНИТОФОНА Длина составляет 2 часа (если длина не была явно изменена с помощью команды <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>Set</strong></a> ).</span><span class="sxs-lookup"><span data-stu-id="b45ad-460">For VCR devices, the length is 2 hours (unless the length has been explicitly changed using the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> command).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-461"><em>номер</em> записи о длине</span><span class="sxs-lookup"><span data-stu-id="b45ad-461">length track <em>number</em></span></span></td>
<td><span data-ttu-id="b45ad-462">Возвращает длину записи в единицах времени или кадрах, определяемую <em>номером</em>. Для файлов ППКН длина возвращается в единицах указателя песни.</span><span class="sxs-lookup"><span data-stu-id="b45ad-462">Returns the length of the track, in time or frames, specified by <em>number</em>.For PPQN files, the length is returned in song pointer units.</span></span> <span data-ttu-id="b45ad-463">Для файлов SMPTE он возвращается как <em>чч: мм: СС: FF</em>, где <em>чч</em> — часы, <em>mm</em> — минуты, <em>SS</em> — секунды, а <em>FF</em> — кадры.</span><span class="sxs-lookup"><span data-stu-id="b45ad-463">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-464">уровень</span><span class="sxs-lookup"><span data-stu-id="b45ad-464">level</span></span></td>
<td><span data-ttu-id="b45ad-465">Возвращает текущее значение звукового образца PCM.</span><span class="sxs-lookup"><span data-stu-id="b45ad-465">Returns the current PCM audio sample value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-466">master</span><span class="sxs-lookup"><span data-stu-id="b45ad-466">master</span></span></td>
<td><span data-ttu-id="b45ad-467">Возвращает &quot; MIDI &quot; , &quot; None &quot; или &quot; SMPTE в &quot; зависимости от типа набора синхронизации.</span><span class="sxs-lookup"><span data-stu-id="b45ad-467">Returns &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-468">носитель отсутствует</span><span class="sxs-lookup"><span data-stu-id="b45ad-468">media present</span></span></td>
<td><span data-ttu-id="b45ad-469">Возвращает <strong>значение true</strong> , если носитель вставлен в устройство, или <strong>значение false</strong> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b45ad-469">Returns <strong>TRUE</strong> if the media is inserted in the device or <strong>FALSE</strong> otherwise.</span></span> <span data-ttu-id="b45ad-470">Device Sequencer, наложение видео, цифровое видео и аудио-аудиоустройства возвращают <strong>значение true</strong>.</span><span class="sxs-lookup"><span data-stu-id="b45ad-470">Sequencer, video-overlay, digital-video, and waveform-audio devices return <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-471">Тип носителя</span><span class="sxs-lookup"><span data-stu-id="b45ad-471">media type</span></span></td>
<td><span data-ttu-id="b45ad-472">Возвращает тип носителя.</span><span class="sxs-lookup"><span data-stu-id="b45ad-472">Returns the type of the media.</span></span> <span data-ttu-id="b45ad-473">Для видеомагнитофонов это &quot; 8mm &quot; , &quot; ВХС &quot; , &quot; свхс &quot; , &quot; Beta &quot; , &quot; Hi8 &quot; , &quot; едбета &quot; или &quot; other &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-473">For VCRS, this is &quot;8mm&quot;, &quot;vhs&quot;, &quot;svhs&quot;, &quot;beta&quot;, &quot;Hi8&quot;, &quot;edbeta&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="b45ad-474">Для видеодискс это &quot; Кав &quot; , &quot; CLV &quot; или &quot; other в &quot; зависимости от типа видеодиск.</span><span class="sxs-lookup"><span data-stu-id="b45ad-474">For videodiscs, this is &quot;CAV&quot;, &quot;CLV&quot;, or &quot;other&quot;, depending on the type of videodisc.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-475">mode</span><span class="sxs-lookup"><span data-stu-id="b45ad-475">mode</span></span></td>
<td><span data-ttu-id="b45ad-476">Возвращает текущий режим устройства.</span><span class="sxs-lookup"><span data-stu-id="b45ad-476">Returns the current mode of the device.</span></span> <span data-ttu-id="b45ad-477">Все устройства могут возвращать &quot; значения "не готово", "приостановлено", " &quot; Воспроизведение" &quot; и " &quot; &quot; &quot; &quot; остановлено" &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-477">All devices can return the &quot;not ready&quot;, &quot;paused&quot;, &quot;playing&quot;, and &quot;stopped&quot; values.</span></span> <span data-ttu-id="b45ad-478">Некоторые устройства могут возвращать дополнительные &quot; открытые &quot; , &quot; приостановленные &quot; , &quot; записываемые &quot; и &quot; искомые &quot; значения.</span><span class="sxs-lookup"><span data-stu-id="b45ad-478">Some devices can return the additional &quot;open&quot;, &quot;parked&quot;, &quot;recording&quot;, and &quot;seeking&quot; values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-479">monitor</span><span class="sxs-lookup"><span data-stu-id="b45ad-479">monitor</span></span></td>
<td><span data-ttu-id="b45ad-480">Возвращает &quot; файл &quot; или &quot; входные данные &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-480">Returns &quot;file&quot; or &quot;input&quot;.</span></span> <span data-ttu-id="b45ad-481">Возвращаемое значение указывает текущий источник представления.</span><span class="sxs-lookup"><span data-stu-id="b45ad-481">The returned value indicates the current presentation source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-482">метод Monitor</span><span class="sxs-lookup"><span data-stu-id="b45ad-482">monitor method</span></span></td>
<td><span data-ttu-id="b45ad-483">Возвращает &quot; Pre &quot; , &quot; POST &quot; или &quot; Direct &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-483">Returns &quot;pre&quot;, &quot;post&quot;, or &quot;direct&quot;.</span></span> <span data-ttu-id="b45ad-484">Возвращаемое значение указывает метод, используемый для мониторинга ввода.</span><span class="sxs-lookup"><span data-stu-id="b45ad-484">The returned value indicates the method used for input monitoring.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-485">Функция</span><span class="sxs-lookup"><span data-stu-id="b45ad-485">nominal</span></span></td>
<td><span data-ttu-id="b45ad-486">Элемент изменяет &quot; &quot; &quot; &quot; номинальное значение на низкие значения, яркость, &quot; Цвет &quot; , &quot; контрастность &quot; , &quot; гамма, резкость, &quot; &quot; &quot; &quot; тон &quot; , &quot; высокие частоты, а также &quot; &quot; &quot; Флаги тома.</span><span class="sxs-lookup"><span data-stu-id="b45ad-486">The item modifies the &quot;bass&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, &quot;tint&quot;, &quot;treble,&quot; and &quot;volume&quot; flags to return the nominal value instead of the current setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-487">Номинальная частота кадров</span><span class="sxs-lookup"><span data-stu-id="b45ad-487">nominal frame rate</span></span></td>
<td><span data-ttu-id="b45ad-488">Возвращает номинальную частоту кадров, связанную с файлом.</span><span class="sxs-lookup"><span data-stu-id="b45ad-488">Returns the nominal frame rate associated with the file.</span></span> <span data-ttu-id="b45ad-489">Единицы измерения находятся в кадрах в секунду, умноженные на 1000.</span><span class="sxs-lookup"><span data-stu-id="b45ad-489">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-490">Номинальная частота кадров записи</span><span class="sxs-lookup"><span data-stu-id="b45ad-490">nominal record frame rate</span></span></td>
<td><span data-ttu-id="b45ad-491">Возвращает номинальную частоту кадров, связанную с входным видеосигналом.</span><span class="sxs-lookup"><span data-stu-id="b45ad-491">Returns the nominal frame rate associated with the input video signal.</span></span> <span data-ttu-id="b45ad-492">Единицы измерения находятся в кадрах в секунду, умноженные на 1000.</span><span class="sxs-lookup"><span data-stu-id="b45ad-492">The units are in frames per second multiplied by 1000.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-493">Число звуковых дорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-493">number of audio tracks</span></span></td>
<td><span data-ttu-id="b45ad-494">Возвращает число звуковых дорожек на носителе.</span><span class="sxs-lookup"><span data-stu-id="b45ad-494">Returns the number of audio tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-495">число дорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-495">number of tracks</span></span></td>
<td><span data-ttu-id="b45ad-496">Возвращает количество дорожек на носителе.</span><span class="sxs-lookup"><span data-stu-id="b45ad-496">Returns the number of tracks on the media.</span></span> <span data-ttu-id="b45ad-497">Устройства МЦИСЕК и МЦИВАВЕ возвращают 1, как и большинство устройств ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="b45ad-497">The MCISEQ and MCIWAVE devices return 1, as do most VCR devices.</span></span> <span data-ttu-id="b45ad-498">Устройство МЦИПИОНР не поддерживает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="b45ad-498">The MCIPIONR device does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-499">число видеодорожек</span><span class="sxs-lookup"><span data-stu-id="b45ad-499">number of video tracks</span></span></td>
<td><span data-ttu-id="b45ad-500">Возвращает число видеодорожек на носителе.</span><span class="sxs-lookup"><span data-stu-id="b45ad-500">Returns the number of video tracks on the media.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-501">offset</span><span class="sxs-lookup"><span data-stu-id="b45ad-501">offset</span></span></td>
<td><span data-ttu-id="b45ad-502">Возвращает смещение файла на основе SMPTE.</span><span class="sxs-lookup"><span data-stu-id="b45ad-502">Returns the offset of a SMPTE-based file.</span></span> <span data-ttu-id="b45ad-503">Смещение — это время начала последовательности на основе SMPTE.</span><span class="sxs-lookup"><span data-stu-id="b45ad-503">The offset is the start time of a SMPTE-based sequence.</span></span> <span data-ttu-id="b45ad-504">Время возвращается в формате <em>чч: мм: СС: FF</em>, где <em>чч</em> — часы, <em>mm</em> — минуты, <em>SS</em> — секунды, а <em>FF</em> — кадры.</span><span class="sxs-lookup"><span data-stu-id="b45ad-504">The time is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-505">output</span><span class="sxs-lookup"><span data-stu-id="b45ad-505">output</span></span></td>
<td><span data-ttu-id="b45ad-506">Возвращает текущий набор выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b45ad-506">Returns the currently set output.</span></span> <span data-ttu-id="b45ad-507">Если выходные данные не заданы, то возвращенная ошибка указывает, что можно использовать любое устройство.</span><span class="sxs-lookup"><span data-stu-id="b45ad-507">If no output is set, the error returned indicates that any device can be used.</span></span> <span data-ttu-id="b45ad-508">Для устройств с цифровыми видео изменяет низкие частоты, &quot; &quot; &quot; высокие частоты, &quot; &quot; громкость, &quot; &quot; яркость &quot; , &quot; Цвет &quot; , &quot; контрастность, &quot; &quot; гамма &quot; , &quot; резкость &quot; или &quot; флаг оттенка, &quot; чтобы он применялся только к выходным данным.</span><span class="sxs-lookup"><span data-stu-id="b45ad-508">For digital-video devices, modifies the &quot;bass&quot;, &quot;treble&quot;, &quot;volume&quot;, &quot;brightness&quot;, &quot;color&quot;, &quot;contrast&quot;, &quot;gamma&quot;, &quot;sharpness&quot;, or &quot;tint&quot; flag so that it applies only to the output.</span></span> <span data-ttu-id="b45ad-509">Это значение по умолчанию при мониторинге файла.</span><span class="sxs-lookup"><span data-stu-id="b45ad-509">This is the default when monitoring a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-510">режим приостановки</span><span class="sxs-lookup"><span data-stu-id="b45ad-510">pause mode</span></span></td>
<td><span data-ttu-id="b45ad-511">Возвращает &quot; запись &quot; , если устройство приостанавливается во время записи.</span><span class="sxs-lookup"><span data-stu-id="b45ad-511">Returns &quot;recording&quot; if the device is paused while recording.</span></span> <span data-ttu-id="b45ad-512">Он возвращает &quot; Воспроизведение &quot; , если устройство приостанавливается во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b45ad-512">It returns &quot;playing&quot; if the device is paused while playing.</span></span> <span data-ttu-id="b45ad-513">Если устройство не приостановлено, оно возвращает действие "ошибка", &quot; неприменимое в текущем режиме &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-513">It returns the error &quot;Action not applicable in current mode&quot; if the device is not paused.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-514">время ожидания приостановки</span><span class="sxs-lookup"><span data-stu-id="b45ad-514">pause timeout</span></span></td>
<td><span data-ttu-id="b45ad-515">Возвращает максимальную продолжительность команды <a href="pause.md"><strong>Pause</strong></a> в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="b45ad-515">Returns the maximum duration, in milliseconds, of a <a href="pause.md"><strong>pause</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-516">Формат воспроизведения</span><span class="sxs-lookup"><span data-stu-id="b45ad-516">play format</span></span></td>
<td><span data-ttu-id="b45ad-517">Возвращает код, указывающий формат, в котором будет воспроизводиться видеокассета, если он доступен для обнаружения: &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; или &quot; другое &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-517">Returns a code indicating the format that the videotape will be played back in, if detectable: &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="b45ad-518">Дополнительные сведения см. в разделе &quot; флаг формата записи &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-518">For more information, see the &quot;record format&quot; flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-519">скорость воспроизведения</span><span class="sxs-lookup"><span data-stu-id="b45ad-519">play speed</span></span></td>
<td><span data-ttu-id="b45ad-520">Возвращает значение, представляющее, насколько близко текущее время воспроизведения последней последовательности AVI соответствует целевому времени воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b45ad-520">Returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="b45ad-521">Значение 1000 указывает на то, что целевое время и фактическое время одинаковы.</span><span class="sxs-lookup"><span data-stu-id="b45ad-521">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="b45ad-522">Значение 2000, например, указывает на то, что последовательность AVI заняла бы вдвое больше времени, чтобы играть, как нужно.</span><span class="sxs-lookup"><span data-stu-id="b45ad-522">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="b45ad-523">Этот флаг распознается только драйвером МЦИАВИ Digital-Video.</span><span class="sxs-lookup"><span data-stu-id="b45ad-523">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="b45ad-524">Он предназначен только для оценки производительности; Возвращаемое значение сложно интерпретировать.</span><span class="sxs-lookup"><span data-stu-id="b45ad-524">It is meant for performance evaluation only; the return value is difficult to interpret.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-525">порт</span><span class="sxs-lookup"><span data-stu-id="b45ad-525">port</span></span></td>
<td><span data-ttu-id="b45ad-526">Возвращает номер порта MIDI, назначенный последовательности.</span><span class="sxs-lookup"><span data-stu-id="b45ad-526">Returns the MIDI port number assigned to the sequence.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-527">position</span><span class="sxs-lookup"><span data-stu-id="b45ad-527">position</span></span></td>
<td><span data-ttu-id="b45ad-528">Возвращает текущую точку. Для файлов ППКН значение позиции возвращается в единицах указателя песни.</span><span class="sxs-lookup"><span data-stu-id="b45ad-528">Returns the current position.For PPQN files, the position is returned in song pointer units.</span></span> <span data-ttu-id="b45ad-529">Для файлов SMPTE он возвращается как <em>чч: мм: СС: FF</em>, где <em>чч</em> — часы, <em>mm</em> — минуты, SS — секунды, а <em>FF</em> — кадры.</span><span class="sxs-lookup"><span data-stu-id="b45ad-529">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, ss is seconds, and <em>ff</em> is frames.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-530">Начало должности</span><span class="sxs-lookup"><span data-stu-id="b45ad-530">position start</span></span></td>
<td><span data-ttu-id="b45ad-531">Возвращает расположение начала пригодного к использованию носителя.</span><span class="sxs-lookup"><span data-stu-id="b45ad-531">Returns the position of the start of the usable media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-532"><em>номер</em> отслеживания расположения</span><span class="sxs-lookup"><span data-stu-id="b45ad-532">position track <em>number</em></span></span></td>
<td><span data-ttu-id="b45ad-533">Возвращает порядковый номер начала записи, указанной параметром <em>Number</em>.</span><span class="sxs-lookup"><span data-stu-id="b45ad-533">Returns the position of the start of the track specified by <em>number</em>.</span></span> <span data-ttu-id="b45ad-534">Для файлов ППКН формат времени возвращается в единицах указателя песни.</span><span class="sxs-lookup"><span data-stu-id="b45ad-534">For PPQN files, the time format is returned in song pointer units.</span></span> <span data-ttu-id="b45ad-535">Для файлов SMPTE он возвращается как <em>чч: мм: СС: FF</em>, где <em>чч</em> — часы, <em>mm</em> — минуты, <em>SS</em> — секунды, а <em>FF</em> — кадры.</span><span class="sxs-lookup"><span data-stu-id="b45ad-535">For SMPTE files, it is returned as <em>hh:mm:ss:ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span> <span data-ttu-id="b45ad-536">МЦИСЕК Sequencer возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b45ad-536">The MCISEQ sequencer returns zero.</span></span> <span data-ttu-id="b45ad-537">Устройство МЦИПИОНР не поддерживает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="b45ad-537">The MCIPIONR device does not support this flag.</span></span> <span data-ttu-id="b45ad-538">Устройство МЦИВАВЕ возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b45ad-538">The MCIWAVE device returns zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-539">Длительность выкрутки</span><span class="sxs-lookup"><span data-stu-id="b45ad-539">postroll duration</span></span></td>
<td><span data-ttu-id="b45ad-540">Возвращает длину видеоленты (в текущем формате времени), необходимую для переноса данных из ВИДЕОМАГНИТОФОНА при выполнении команды <a href="stop.md"><strong>остановки</strong></a> или <a href="pause.md"><strong>приостановки</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-540">Returns the length of videotape, in the current time format, needed to brake the VCR transport when a <a href="stop.md"><strong>stop</strong></a> or <a href="pause.md"><strong>pause</strong></a> command is issued.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-541">Включение</span><span class="sxs-lookup"><span data-stu-id="b45ad-541">power on</span></span></td>
<td><span data-ttu-id="b45ad-542">Возвращает <strong>значение true</strong> , если питание видеомагнитофона включено.</span><span class="sxs-lookup"><span data-stu-id="b45ad-542">Returns <strong>TRUE</strong> if the VCR's power is on.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-543">Длительность предпробного выполнения</span><span class="sxs-lookup"><span data-stu-id="b45ad-543">preroll duration</span></span></td>
<td><span data-ttu-id="b45ad-544">Возвращает длину видеокассеты в текущем формате времени, необходимую для стабилизации выходных данных ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="b45ad-544">Returns the length of videotape, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-545">всё</span><span class="sxs-lookup"><span data-stu-id="b45ad-545">ready</span></span></td>
<td><span data-ttu-id="b45ad-546">Возвращает <strong>значение true</strong> , если устройство готово принять другую команду.</span><span class="sxs-lookup"><span data-stu-id="b45ad-546">Returns <strong>TRUE</strong> if the device is ready to accept another command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-547">формат записи</span><span class="sxs-lookup"><span data-stu-id="b45ad-547">record format</span></span></td>
<td><span data-ttu-id="b45ad-548">Возвращает код, указывающий формат, в котором будет записана лента.</span><span class="sxs-lookup"><span data-stu-id="b45ad-548">Returns a code indicating the format that the videotape will be recorded in.</span></span> <span data-ttu-id="b45ad-549">Текущими типами возврата являются &quot; LP &quot; , &quot; EP &quot; , &quot; SP &quot; или &quot; other &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-549">The current return types are &quot;lp&quot;, &quot;ep&quot;, &quot;sp&quot;, or &quot;other&quot;.</span></span> <span data-ttu-id="b45ad-550">Эти форматы не ВХС для конкретного видеомагнитофона и могут применяться к видеомагнитофонам с несколькими выбираемыми форматами записи.</span><span class="sxs-lookup"><span data-stu-id="b45ad-550">These formats are not VHS specific and can be applied to any VCR that has multiple selectable recording formats.</span></span> <span data-ttu-id="b45ad-551">&quot;Тип SP &quot; — это самый быстрый и наивысший формат записи качества, используемый по умолчанию в одном формате.</span><span class="sxs-lookup"><span data-stu-id="b45ad-551">The &quot;sp&quot; type is the fastest, highest quality recording format and is used as default on single format VCRs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-552">Частота кадров записи</span><span class="sxs-lookup"><span data-stu-id="b45ad-552">record frame rate</span></span></td>
<td><span data-ttu-id="b45ad-553">Возвращает частоту кадров в кадрах в секунду, умноженную на 1000, используемую для сжатия.</span><span class="sxs-lookup"><span data-stu-id="b45ad-553">Returns the frame rate, in frames per second multiplied by 1000, used for compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-554">Ссылочный <em>фрейм</em></span><span class="sxs-lookup"><span data-stu-id="b45ad-554">reference <em>frame</em></span></span></td>
<td><span data-ttu-id="b45ad-555">Возвращает номер кадра для ближайшего изображения опорного кадра, предшествующего указанному <em>кадру</em>.</span><span class="sxs-lookup"><span data-stu-id="b45ad-555">Returns the frame number for the nearest key frame image that precedes the specified <em>frame</em>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-556">зарезервированный размер</span><span class="sxs-lookup"><span data-stu-id="b45ad-556">reserved size</span></span></td>
<td><span data-ttu-id="b45ad-557">Возвращает размер зарезервированной рабочей области в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="b45ad-557">Returns the size, in the current time format, of the reserved workspace.</span></span> <span data-ttu-id="b45ad-558">Размер соответствует приблизительному времени, которое потребуется для воспроизведения сжатых данных из полной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b45ad-558">The size corresponds to the approximate time it would take to play the compressed data from a full workspace.</span></span> <span data-ttu-id="b45ad-559">При отсутствии зарезервированного места на диске он возвращает нуль.</span><span class="sxs-lookup"><span data-stu-id="b45ad-559">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="b45ad-560">Этот флаг Возвращает приблизительный размер, так как точное место на диске для сжатых данных не может быть прогнозным до тех пор, пока данные не будут сжаты.</span><span class="sxs-lookup"><span data-stu-id="b45ad-560">This flag returns the approximate size because the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-561">правый том</span><span class="sxs-lookup"><span data-stu-id="b45ad-561">right volume</span></span></td>
<td><span data-ttu-id="b45ad-562">Возвращает набор томов для правильного канала звука.</span><span class="sxs-lookup"><span data-stu-id="b45ad-562">Returns the volume set for the right audio channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-563">самплесперсек</span><span class="sxs-lookup"><span data-stu-id="b45ad-563">samplespersec</span></span></td>
<td><span data-ttu-id="b45ad-564">Возвращает число воспроизводимых или записанных выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="b45ad-564">Returns the number of samples per second played or recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-565">Поиск в точности</span><span class="sxs-lookup"><span data-stu-id="b45ad-565">seek exactly</span></span></td>
<td><span data-ttu-id="b45ad-566">Возвращает &quot; &quot; или &quot; задает значение ON или OFF &quot; , указывающее, &quot; установлен ли флаг поиска в точности &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-566">Returns &quot;on&quot; or &quot;off&quot;, indicating whether or not the &quot;seek exactly&quot; flag is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-567">четкость</span><span class="sxs-lookup"><span data-stu-id="b45ad-567">sharpness</span></span></td>
<td><span data-ttu-id="b45ad-568">Возвращает текущий уровень резкости устройства.</span><span class="sxs-lookup"><span data-stu-id="b45ad-568">Returns the current sharpness level of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-569">сбоку</span><span class="sxs-lookup"><span data-stu-id="b45ad-569">side</span></span></td>
<td><span data-ttu-id="b45ad-570">Возвращает значение 1 или 2, указывающее, какая сторона видеодиск загружена.</span><span class="sxs-lookup"><span data-stu-id="b45ad-570">Returns 1 or 2 to indicate which side of the videodisc is loaded.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-571">подчинен</span><span class="sxs-lookup"><span data-stu-id="b45ad-571">slave</span></span></td>
<td><span data-ttu-id="b45ad-572">Возвращает &quot; файл &quot; , &quot; MIDI &quot; , &quot; None &quot; или &quot; SMPTE в &quot; зависимости от типа набора синхронизации.</span><span class="sxs-lookup"><span data-stu-id="b45ad-572">Returns &quot;file&quot; , &quot;midi&quot;, &quot;none&quot;, or &quot;smpte&quot; depending on the type of synchronization set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-573">SMPTE</span><span class="sxs-lookup"><span data-stu-id="b45ad-573">smpte</span></span></td>
<td><span data-ttu-id="b45ad-574">Возвращает временной код SMPTE, связанный с текущей позицией в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b45ad-574">Returns the SMPTE timecode associated with the current position in the workspace.</span></span> <span data-ttu-id="b45ad-575">Это строка в формате <em>DD: DD: DD: DD</em>, где каждая <em>d</em> обозначает цифру от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="b45ad-575">This is a string with the form <em>dd:dd:dd:dd</em>, where each <em>d</em> denotes a digit from 0 to 9.</span></span> <span data-ttu-id="b45ad-576">Если данные рабочей области не содержат данные времени, этот флаг возвращает значение 00:00:00:00.</span><span class="sxs-lookup"><span data-stu-id="b45ad-576">If the workspace data does not include timecode data, then this flag returns 00:00:00:00.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-577">Скорость</span><span class="sxs-lookup"><span data-stu-id="b45ad-577">speed</span></span></td>
<td><span data-ttu-id="b45ad-578">Возвращает текущую скорость устройства в кадрах в секунду (или в том же формате, который используется командой " <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>задать</strong></a> &quot; скорость" &quot; ).</span><span class="sxs-lookup"><span data-stu-id="b45ad-578">Returns the current speed of the device in frames per second (or in the same format used by the <a href="https://www.bing.com/search?q=<strong>set</strong>"><strong>set</strong></a> &quot;speed&quot; command).</span></span> <span data-ttu-id="b45ad-579">Проигрыватель МЦИПИОНР видеодиск не поддерживает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="b45ad-579">The MCIPIONR videodisc player does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-580">начальное расположение</span><span class="sxs-lookup"><span data-stu-id="b45ad-580">start position</span></span></td>
<td><span data-ttu-id="b45ad-581">Возвращает начальную точку носителя.</span><span class="sxs-lookup"><span data-stu-id="b45ad-581">Returns the starting position of the media.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-582">формат файла по-прежнему</span><span class="sxs-lookup"><span data-stu-id="b45ad-582">still file format</span></span></td>
<td><span data-ttu-id="b45ad-583">Возвращает текущий формат файла для команды <a href="capture.md"><strong>Capture</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-583">Returns the current file format for the <a href="capture.md"><strong>capture</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-584">растяжение</span><span class="sxs-lookup"><span data-stu-id="b45ad-584">stretch</span></span></td>
<td><span data-ttu-id="b45ad-585">Возвращает <strong>значение true</strong> , если растяжение включено.</span><span class="sxs-lookup"><span data-stu-id="b45ad-585">Returns <strong>TRUE</strong> if stretching is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-586">темп</span><span class="sxs-lookup"><span data-stu-id="b45ad-586">tempo</span></span></td>
<td><span data-ttu-id="b45ad-587">Возвращает текущий темп последовательности MIDI в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="b45ad-587">Returns the current tempo of a MIDI sequence in the current time format.</span></span> <span data-ttu-id="b45ad-588">Для файлов с форматом ППКН темп находится в некотором в минуту.</span><span class="sxs-lookup"><span data-stu-id="b45ad-588">For files with PPQN format, the tempo is in beats per minute.</span></span> <span data-ttu-id="b45ad-589">Для файлов с форматом SMPTE темп находится в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="b45ad-589">For files with SMPTE format, the tempo is in frames per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-590">формат времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-590">time format</span></span></td>
<td><span data-ttu-id="b45ad-591">Возвращает текущий формат времени.</span><span class="sxs-lookup"><span data-stu-id="b45ad-591">Returns the current time format.</span></span> <span data-ttu-id="b45ad-592">Дополнительные сведения см. в разделе форматы времени в команде <a href="set.md"><strong>Set</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-592">For more information, see the time formats in the <a href="set.md"><strong>set</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-593">режим времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-593">time mode</span></span></td>
<td><span data-ttu-id="b45ad-594">Возвращает текущий режим времени текущего позиционирования.</span><span class="sxs-lookup"><span data-stu-id="b45ad-594">Returns the current position time mode.</span></span> <span data-ttu-id="b45ad-595">Это может быть &quot; Обнаружение &quot; , код времени &quot; &quot; или &quot; Счетчик &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-595">It can be &quot;detect&quot;, &quot;timecode&quot;, or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-596">тип времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-596">time type</span></span></td>
<td><span data-ttu-id="b45ad-597">Возвращает текущее используемое время позиционирования: код &quot; времени &quot; или &quot; Счетчик &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-597">Returns the current position time in use: &quot;timecode&quot; or &quot;counter&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-598">код времени имеется</span><span class="sxs-lookup"><span data-stu-id="b45ad-598">timecode present</span></span></td>
<td><span data-ttu-id="b45ad-599">Возвращает <strong>значение true</strong> , если код времени записан в текущую точку на ленте.</span><span class="sxs-lookup"><span data-stu-id="b45ad-599">Returns <strong>TRUE</strong> if timecode has been recorded at the current position on the tape.</span></span> <span data-ttu-id="b45ad-600">Код времени должен перемещаться с текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="b45ad-600">The timecode must advance from the current position.</span></span> <span data-ttu-id="b45ad-601">Для проверки этого состояния может потребоваться воспроизвести ВИДЕОМАГНИТОФОН.</span><span class="sxs-lookup"><span data-stu-id="b45ad-601">A VCR might need to be played to check this condition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-602">запись времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-602">timecode record</span></span></td>
<td><span data-ttu-id="b45ad-603">Возвращает <strong>значение true</strong> , если видеомагнитофон настроен для записи времени.</span><span class="sxs-lookup"><span data-stu-id="b45ad-603">Returns <strong>TRUE</strong> if the VCR is set to record timecode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-604">тип времени</span><span class="sxs-lookup"><span data-stu-id="b45ad-604">timecode type</span></span></td>
<td><span data-ttu-id="b45ad-605">Возвращает &quot; SMPTE &quot; , &quot; SMPTE DROP &quot; , &quot; other &quot; или &quot; None &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-605">Returns &quot;smpte&quot;, &quot;smpte drop&quot;, &quot;other&quot;, or &quot;none&quot;.</span></span> <span data-ttu-id="b45ad-606">Обратите внимание, что количество кадров в секунду можно получить из &quot; команды частота кадров &quot; , а точность устройства может быть возвращена <a href="capability.md"><strong></strong></a> &quot; командой точность поиска возможностей &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-606">Note the frames per second can be obtained from the status &quot;frame rate&quot; command, and the accuracy of the device can be returned by the <a href="capability.md"><strong>capability</strong></a> &quot;seek accuracy&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-607">Интенсив</span><span class="sxs-lookup"><span data-stu-id="b45ad-607">tint</span></span></td>
<td><span data-ttu-id="b45ad-608">Возвращает текущий уровень оттенка видео.</span><span class="sxs-lookup"><span data-stu-id="b45ad-608">Returns the current video-tint level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-609">частот</span><span class="sxs-lookup"><span data-stu-id="b45ad-609">treble</span></span></td>
<td><span data-ttu-id="b45ad-610">Возвращает текущий уровень звуковых частот.</span><span class="sxs-lookup"><span data-stu-id="b45ad-610">Returns the current audio-treble level.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-611">номер тюнера</span><span class="sxs-lookup"><span data-stu-id="b45ad-611">tuner number</span></span></td>
<td><span data-ttu-id="b45ad-612">Возвращает текущий номер логического тюнера.</span><span class="sxs-lookup"><span data-stu-id="b45ad-612">Returns the current logical-tuner number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-613">несохраненные</span><span class="sxs-lookup"><span data-stu-id="b45ad-613">unsaved</span></span></td>
<td><span data-ttu-id="b45ad-614">Возвращает <strong>значение true</strong> , если в рабочей области записаны данные, которые могут быть потеряны в результате выполнения команды <a href="close.md"><strong>Close</strong></a>, <a href="load.md"><strong>Load</strong></a>, <a href="record.md"><strong>Record</strong></a>, <a href="reserve.md"><strong>резервировать</strong></a>, <a href="cut.md"><strong>Cut</strong></a>, <a href="delete.md"><strong>Delete</strong></a>или <a href="paste.md"><strong>Paste</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-614">Returns <strong>TRUE</strong> if there is recorded data in the workspace that might be lost as a result of a <a href="close.md"><strong>close</strong></a>, <a href="load.md"><strong>load</strong></a>, <a href="record.md"><strong>record</strong></a>, <a href="reserve.md"><strong>reserve</strong></a>, <a href="cut.md"><strong>cut</strong></a>, <a href="delete.md"><strong>delete</strong></a>, or <a href="paste.md"><strong>paste</strong></a> command.</span></span> <span data-ttu-id="b45ad-615">В противном случае возвращает <strong>false</strong> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-615">Returns <strong>FALSE</strong> otherwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-616">видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-616">video</span></span></td>
<td><span data-ttu-id="b45ad-617">Возвращает &quot; &quot; или &quot; отключает &quot; , отражая состояние, заданное командой <a href="setvideo.md"><strong>сетвидео</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-617">Returns &quot;on&quot; or &quot;off&quot;, reflecting the state set by the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-618">цвет ключа видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-618">video key color</span></span></td>
<td><span data-ttu-id="b45ad-619">Возвращает значение для цвета ключа.</span><span class="sxs-lookup"><span data-stu-id="b45ad-619">Returns the value for the key color.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-620">индекс ключа видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-620">video key index</span></span></td>
<td><span data-ttu-id="b45ad-621">Возвращает значение индекса ключа.</span><span class="sxs-lookup"><span data-stu-id="b45ad-621">Returns the value for the key index.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-622">монитор видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-622">video monitor</span></span></td>
<td><span data-ttu-id="b45ad-623">Возвращает &quot; выходные данные &quot; или один из допустимых входных типов источника.</span><span class="sxs-lookup"><span data-stu-id="b45ad-623">Returns &quot;output&quot; or one of the valid source-input types.</span></span> <span data-ttu-id="b45ad-624">Дополнительные сведения см. в описании <a href="setvideo.md"><strong></strong></a> &quot; команды Monitor сетвидео &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-624">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> &quot;monitor&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-625">номер монитора видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-625">video monitor number</span></span></td>
<td><span data-ttu-id="b45ad-626">Возвращает отслеживаемое видео-число типа, возвращенное &quot; монитором состояния &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-626">Returns the monitored-video number of the type returned by status &quot;video monitor&quot;.</span></span> <span data-ttu-id="b45ad-627">Дополнительные сведения см. в описании команды <a href="setvideo.md">сетвидео</a> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-627">For more information, see the <a href="setvideo.md">setvideo</a> command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-628">запись видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-628">video record</span></span></td>
<td><span data-ttu-id="b45ad-629">Возвращает &quot; &quot; или &quot; отключает &quot; , отражающий текущее состояние, установленное записью <a href="setvideo.md"><strong>сетвидео</strong></a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="b45ad-629">Returns &quot;on&quot; or &quot;off&quot;, reflecting the current state set by <a href="setvideo.md"><strong>setvideo</strong></a> &quot;record&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-630"><em>номер</em> дорожки записи видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-630">video record track <em>number</em></span></span></td>
<td><span data-ttu-id="b45ad-631">Возвращает <strong>значение true</strong> , если видеомагнитофон настроен для записи видео.</span><span class="sxs-lookup"><span data-stu-id="b45ad-631">Return <strong>TRUE</strong> if the VCR is set to record video.</span></span> <span data-ttu-id="b45ad-632">Если номер записи не указан, предполагается значение по умолчанию, равное 1.</span><span class="sxs-lookup"><span data-stu-id="b45ad-632">If no track number is given, the default value of 1 is assumed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-633">источник видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-633">video source</span></span></td>
<td><span data-ttu-id="b45ad-634">Возвращает тип видео-источника.</span><span class="sxs-lookup"><span data-stu-id="b45ad-634">Returns the video-source type.</span></span> <span data-ttu-id="b45ad-635">Дополнительные сведения см. в описании команды <a href="setvideo.md"><strong>сетвидео</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b45ad-635">For more information, see the <a href="setvideo.md"><strong>setvideo</strong></a> command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-636">Исходный номер видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-636">video source number</span></span></td>
<td><span data-ttu-id="b45ad-637">Возвращает число, соответствующее источнику видео используемого типа.</span><span class="sxs-lookup"><span data-stu-id="b45ad-637">Returns a number corresponding to the video source of the type in use.</span></span> <span data-ttu-id="b45ad-638">Например, возвращает значение 2, если используется Вторая входная система видео NTSC.</span><span class="sxs-lookup"><span data-stu-id="b45ad-638">For example, it returns 2 if the second NTSC video source input is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-639">поток видео</span><span class="sxs-lookup"><span data-stu-id="b45ad-639">video stream</span></span></td>
<td><span data-ttu-id="b45ad-640">Возвращает текущий номер видео-потока.</span><span class="sxs-lookup"><span data-stu-id="b45ad-640">Returns the current video-stream number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-641">том</span><span class="sxs-lookup"><span data-stu-id="b45ad-641">volume</span></span></td>
<td><span data-ttu-id="b45ad-642">Возвращает средний объем левого и правого докладчика.</span><span class="sxs-lookup"><span data-stu-id="b45ad-642">Returns the average volume to the left and right speaker.</span></span> <span data-ttu-id="b45ad-643">Это возвращает ошибку, если устройство не было воспроизведено или том не был задан.</span><span class="sxs-lookup"><span data-stu-id="b45ad-643">This returns an error if the device has not been played or volume has not been set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-644">маркер окна</span><span class="sxs-lookup"><span data-stu-id="b45ad-644">window handle</span></span></td>
<td><span data-ttu-id="b45ad-645">Возвращает десятичное значение ASCII для маркера окна в младшем слове возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="b45ad-645">Returns the ASCII decimal value for the window handle in the low-order word of the return value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-646">окно развернуто</span><span class="sxs-lookup"><span data-stu-id="b45ad-646">window maximized</span></span></td>
<td><span data-ttu-id="b45ad-647">Возвращает <strong>значение true</strong> , если окно развернуто.</span><span class="sxs-lookup"><span data-stu-id="b45ad-647">Returns <strong>TRUE</strong> if the window is maximized.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-648">окно уменьшено</span><span class="sxs-lookup"><span data-stu-id="b45ad-648">window minimized</span></span></td>
<td><span data-ttu-id="b45ad-649">Возвращает <strong>значение true</strong> , если окно является сведенным.</span><span class="sxs-lookup"><span data-stu-id="b45ad-649">Returns <strong>TRUE</strong> if the window is minimized.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b45ad-650">видимое окно</span><span class="sxs-lookup"><span data-stu-id="b45ad-650">window visible</span></span></td>
<td><span data-ttu-id="b45ad-651">Возвращает <strong>значение true</strong> , если окно не скрыто.</span><span class="sxs-lookup"><span data-stu-id="b45ad-651">Returns <strong>TRUE</strong> if the window is not hidden.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b45ad-652">защищено от записи</span><span class="sxs-lookup"><span data-stu-id="b45ad-652">write protected</span></span></td>
<td><span data-ttu-id="b45ad-653">Возвращает <strong>значение true</strong> , если устройство обнаруживает, что оно не может записать (то есть если включена защита записи).</span><span class="sxs-lookup"><span data-stu-id="b45ad-653">Returns <strong>TRUE</strong> if the device detects that it cannot record (that is, if the write protect is on).</span></span> <span data-ttu-id="b45ad-654">Если он может записать или не сможет определить, может ли он записывать (без фактической записи), драйвер возвращает <strong>значение false</strong>.</span><span class="sxs-lookup"><span data-stu-id="b45ad-654">If it can record, or if it is unable to determine whether or not it can record (without actually writing), the driver returns <strong>FALSE</strong>.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="b45ad-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="b45ad-655"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b45ad-656">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="b45ad-656">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="b45ad-657">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="b45ad-657">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="b45ad-658">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b45ad-658">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b45ad-659">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b45ad-659">Return Value</span></span>

<span data-ttu-id="b45ad-660">Возвращает сведения в параметре *лпсзретурнстринг* объекта [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b45ad-660">Returns information in the *lpszReturnString* parameter of [**mciSendString**](/previous-versions//dd757161(v=vs.85)).</span></span> <span data-ttu-id="b45ad-661">Сведения зависят от типа запроса.</span><span class="sxs-lookup"><span data-stu-id="b45ad-661">The information is dependent on the request type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b45ad-662">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b45ad-662">Remarks</span></span>

<span data-ttu-id="b45ad-663">Перед выполнением команд, использующих значения позиций, необходимо задать требуемый формат времени с помощью команды [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="b45ad-663">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="b45ad-664">Примеры</span><span class="sxs-lookup"><span data-stu-id="b45ad-664">Examples</span></span>

<span data-ttu-id="b45ad-665">Следующая команда возвращает текущий режим устройства "мисаунд".</span><span class="sxs-lookup"><span data-stu-id="b45ad-665">The following command returns the current mode of the "mysound" device.</span></span>

``` syntax
status mysound mode
```

## <a name="requirements"></a><span data-ttu-id="b45ad-666">Требования</span><span class="sxs-lookup"><span data-stu-id="b45ad-666">Requirements</span></span>



| <span data-ttu-id="b45ad-667">Требование</span><span class="sxs-lookup"><span data-stu-id="b45ad-667">Requirement</span></span> | <span data-ttu-id="b45ad-668">Значение</span><span class="sxs-lookup"><span data-stu-id="b45ad-668">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b45ad-669">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b45ad-669">Minimum supported client</span></span><br/> | <span data-ttu-id="b45ad-670">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b45ad-670">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b45ad-671">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b45ad-671">Minimum supported server</span></span><br/> | <span data-ttu-id="b45ad-672">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b45ad-672">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b45ad-673">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b45ad-673">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b45ad-674">MCI</span><span class="sxs-lookup"><span data-stu-id="b45ad-674">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b45ad-675">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="b45ad-675">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

<span data-ttu-id="b45ad-676">[capability](capability.md);</span><span class="sxs-lookup"><span data-stu-id="b45ad-676">[capability](capability.md)</span></span>
</dt> <dt>

[<span data-ttu-id="b45ad-677">выделяем</span><span class="sxs-lookup"><span data-stu-id="b45ad-677">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="b45ad-678">close</span><span class="sxs-lookup"><span data-stu-id="b45ad-678">close</span></span>](close.md)
</dt> <dt>

[<span data-ttu-id="b45ad-679">бавьте</span><span class="sxs-lookup"><span data-stu-id="b45ad-679">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="b45ad-680">delete</span><span class="sxs-lookup"><span data-stu-id="b45ad-680">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="b45ad-681">загрузка</span><span class="sxs-lookup"><span data-stu-id="b45ad-681">load</span></span>](load.md)
</dt> <dt>

[<span data-ttu-id="b45ad-682">pause</span><span class="sxs-lookup"><span data-stu-id="b45ad-682">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="b45ad-683">авить</span><span class="sxs-lookup"><span data-stu-id="b45ad-683">paste</span></span>](paste.md)
</dt> <dt>

[<span data-ttu-id="b45ad-684">record</span><span class="sxs-lookup"><span data-stu-id="b45ad-684">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="b45ad-685">предназначен</span><span class="sxs-lookup"><span data-stu-id="b45ad-685">reserve</span></span>](reserve.md)
</dt> <dt>

[<span data-ttu-id="b45ad-686">сохранить</span><span class="sxs-lookup"><span data-stu-id="b45ad-686">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="b45ad-687">set</span><span class="sxs-lookup"><span data-stu-id="b45ad-687">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="b45ad-688">сетаудио</span><span class="sxs-lookup"><span data-stu-id="b45ad-688">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="b45ad-689">сетвидео</span><span class="sxs-lookup"><span data-stu-id="b45ad-689">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="b45ad-690">stop</span><span class="sxs-lookup"><span data-stu-id="b45ad-690">stop</span></span>](stop.md)
</dt> <dt>

[<span data-ttu-id="b45ad-691">отменить</span><span class="sxs-lookup"><span data-stu-id="b45ad-691">undo</span></span>](undo.md)
</dt> </dl>

 

