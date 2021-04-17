---
title: команда Set
description: Команда Set устанавливает параметры управления для устройства. Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, ВИДЕОМАГНИТОФОН, видеодиск, наложение видео и аудио-файлы.
ms.assetid: 1ec4d84e-372a-4b6d-b694-f5afb41f90b2
keywords:
- Задание команд мультимедиа Windows
topic_type:
- apiref
api_name:
- set
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914743db038b0cae32b53fa79b7696ddba1ad05b
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "105674510"
---
# <a name="set-command"></a><span data-ttu-id="34704-105">команда Set</span><span class="sxs-lookup"><span data-stu-id="34704-105">set command</span></span>

> [!NOTE]
> <span data-ttu-id="34704-106">Обмен данными без смещения — Корпорация Майкрософт поддерживает различные и включенные среды.</span><span class="sxs-lookup"><span data-stu-id="34704-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="34704-107">В этом документе есть ссылки на слово "Slave".</span><span class="sxs-lookup"><span data-stu-id="34704-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="34704-108">В соответствии с руководством корпорации Майкрософт в [стиле Bias-Freeного обмена данными](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) это слово является исключаемым.</span><span class="sxs-lookup"><span data-stu-id="34704-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="34704-109">Это слово используется в том виде, в котором оно используется в командах.</span><span class="sxs-lookup"><span data-stu-id="34704-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="34704-110">Для обеспечения согласованности этот документ содержит это слово.</span><span class="sxs-lookup"><span data-stu-id="34704-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="34704-111">При изменении этого слова в командах будет исправлен этот документ в выравнивании.</span><span class="sxs-lookup"><span data-stu-id="34704-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>


<span data-ttu-id="34704-112">Команда Set устанавливает параметры управления для устройства.</span><span class="sxs-lookup"><span data-stu-id="34704-112">The set command establishes control settings for the device.</span></span> <span data-ttu-id="34704-113">Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, ВИДЕОМАГНИТОФОН, видеодиск, наложение видео и аудио-файлы.</span><span class="sxs-lookup"><span data-stu-id="34704-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="34704-114">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="34704-114">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand,
  TEXT("set %s %s %s"),
  lpszDeviceID,
  lpszSetting,
  lpszFlags
);
      
```

## <a name="parameters"></a><span data-ttu-id="34704-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="34704-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34704-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="34704-116"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="34704-117">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="34704-117">Identifier of an MCI device.</span></span> <span data-ttu-id="34704-118">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="34704-118">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="34704-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*лпсзсеттинг*</span><span class="sxs-lookup"><span data-stu-id="34704-119"><span id="lpszSetting"></span><span id="lpszsetting"></span><span id="LPSZSETTING"></span>*lpszSetting*</span></span>
</dt> <dd>

<span data-ttu-id="34704-120">Флаг для установки параметров управления.</span><span class="sxs-lookup"><span data-stu-id="34704-120">Flag for establishing control settings.</span></span> <span data-ttu-id="34704-121">В следующей таблице перечислены типы устройств, которые распознают команду **Set** и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="34704-121">The following table lists device types that recognize the **set** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34704-122">Тип устройства</span><span class="sxs-lookup"><span data-stu-id="34704-122">Device Type</span></span></th>
<th><span data-ttu-id="34704-123">Флаги команд</span><span class="sxs-lookup"><span data-stu-id="34704-123">Command Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34704-124">кдаудио</span><span class="sxs-lookup"><span data-stu-id="34704-124">cdaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="34704-125">Звук выкл.</span><span class="sxs-lookup"><span data-stu-id="34704-125">audio all off</span></span></li>
<li><span data-ttu-id="34704-126">звук включен</span><span class="sxs-lookup"><span data-stu-id="34704-126">audio all on</span></span></li>
<li><span data-ttu-id="34704-127">звук отключен</span><span class="sxs-lookup"><span data-stu-id="34704-127">audio left off</span></span></li>
<li><span data-ttu-id="34704-128">звук остался на</span><span class="sxs-lookup"><span data-stu-id="34704-128">audio left on</span></span></li>
<li><span data-ttu-id="34704-129">звуковое право</span><span class="sxs-lookup"><span data-stu-id="34704-129">audio right off</span></span></li>
<li><span data-ttu-id="34704-130">аудио справа</span><span class="sxs-lookup"><span data-stu-id="34704-130">audio right on</span></span></li>
<li><span data-ttu-id="34704-131">дверца закрыта</span><span class="sxs-lookup"><span data-stu-id="34704-131">door closed</span></span></li>
<li><span data-ttu-id="34704-132">Дверца открыта</span><span class="sxs-lookup"><span data-stu-id="34704-132">door open</span></span></li>
<li><span data-ttu-id="34704-133">формат времени (МС)</span><span class="sxs-lookup"><span data-stu-id="34704-133">time format milliseconds</span></span></li>
<li><span data-ttu-id="34704-134">формат времени, MSF</span><span class="sxs-lookup"><span data-stu-id="34704-134">time format msf</span></span></li>
<li><span data-ttu-id="34704-135">формат времени тмсф</span><span class="sxs-lookup"><span data-stu-id="34704-135">time format tmsf</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-136">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="34704-136">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="34704-137">Звук выкл.</span><span class="sxs-lookup"><span data-stu-id="34704-137">audio all off</span></span></li>
<li><span data-ttu-id="34704-138">звук включен</span><span class="sxs-lookup"><span data-stu-id="34704-138">audio all on</span></span></li>
<li><span data-ttu-id="34704-139">звук отключен</span><span class="sxs-lookup"><span data-stu-id="34704-139">audio left off</span></span></li>
<li><span data-ttu-id="34704-140">звук остался на</span><span class="sxs-lookup"><span data-stu-id="34704-140">audio left on</span></span></li>
<li><span data-ttu-id="34704-141">звуковое право</span><span class="sxs-lookup"><span data-stu-id="34704-141">audio right off</span></span></li>
<li><span data-ttu-id="34704-142">аудио справа</span><span class="sxs-lookup"><span data-stu-id="34704-142">audio right on</span></span></li>
<li><span data-ttu-id="34704-143">дверца закрыта</span><span class="sxs-lookup"><span data-stu-id="34704-143">door closed</span></span></li>
<li><span data-ttu-id="34704-144">Дверца открыта</span><span class="sxs-lookup"><span data-stu-id="34704-144">door open</span></span></li>
<li><span data-ttu-id="34704-145"><em>Формат</em> формата файла</span><span class="sxs-lookup"><span data-stu-id="34704-145">file format <em>format</em></span></span></li>
<li><span data-ttu-id="34704-146">Поиск в точности</span><span class="sxs-lookup"><span data-stu-id="34704-146">seek exactly on</span></span></li>
<li><span data-ttu-id="34704-147">Поиск в точности</span><span class="sxs-lookup"><span data-stu-id="34704-147">seek exactly off</span></span></li>
<li><span data-ttu-id="34704-148"><em>Коэффициент</em> скорости</span><span class="sxs-lookup"><span data-stu-id="34704-148">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="34704-149"><em>Формат</em> файла по-прежнему</span><span class="sxs-lookup"><span data-stu-id="34704-149">still file format <em>format</em></span></span></li>
<li><span data-ttu-id="34704-150">кадры формата времени</span><span class="sxs-lookup"><span data-stu-id="34704-150">time format frames</span></span></li>
<li><span data-ttu-id="34704-151">формат времени (МС)</span><span class="sxs-lookup"><span data-stu-id="34704-151">time format milliseconds</span></span></li>
<li><span data-ttu-id="34704-152">видео отключено</span><span class="sxs-lookup"><span data-stu-id="34704-152">video off</span></span></li>
<li><span data-ttu-id="34704-153">видео вкл.</span><span class="sxs-lookup"><span data-stu-id="34704-153">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-154">overlay</span><span class="sxs-lookup"><span data-stu-id="34704-154">overlay</span></span></td>
<td><ul>
<li><span data-ttu-id="34704-155">Звук выкл.</span><span class="sxs-lookup"><span data-stu-id="34704-155">audio all off</span></span></li>
<li><span data-ttu-id="34704-156">звук включен</span><span class="sxs-lookup"><span data-stu-id="34704-156">audio all on</span></span></li>
<li><span data-ttu-id="34704-157">звук отключен</span><span class="sxs-lookup"><span data-stu-id="34704-157">audio left off</span></span></li>
<li><span data-ttu-id="34704-158">звук остался на</span><span class="sxs-lookup"><span data-stu-id="34704-158">audio left on</span></span></li>
<li><span data-ttu-id="34704-159">звуковое право</span><span class="sxs-lookup"><span data-stu-id="34704-159">audio right off</span></span></li>
<li><span data-ttu-id="34704-160">аудио справа</span><span class="sxs-lookup"><span data-stu-id="34704-160">audio right on</span></span></li>
<li><span data-ttu-id="34704-161">дверца закрыта</span><span class="sxs-lookup"><span data-stu-id="34704-161">door closed</span></span></li>
<li><span data-ttu-id="34704-162">Дверца открыта</span><span class="sxs-lookup"><span data-stu-id="34704-162">door open</span></span></li>
<li><span data-ttu-id="34704-163">видео отключено</span><span class="sxs-lookup"><span data-stu-id="34704-163">video off</span></span></li>
<li><span data-ttu-id="34704-164">видео вкл.</span><span class="sxs-lookup"><span data-stu-id="34704-164">video on</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-165">sequencer</span><span class="sxs-lookup"><span data-stu-id="34704-165">sequencer</span></span></td>
<td><ul>
<li><span data-ttu-id="34704-166">Звук выкл.</span><span class="sxs-lookup"><span data-stu-id="34704-166">audio all off</span></span></li>
<li><span data-ttu-id="34704-167">звук включен</span><span class="sxs-lookup"><span data-stu-id="34704-167">audio all on</span></span></li>
<li><span data-ttu-id="34704-168">звук отключен</span><span class="sxs-lookup"><span data-stu-id="34704-168">audio left off</span></span></li>
<li><span data-ttu-id="34704-169">звук остался на</span><span class="sxs-lookup"><span data-stu-id="34704-169">audio left on</span></span></li>
<li><span data-ttu-id="34704-170">звуковое право</span><span class="sxs-lookup"><span data-stu-id="34704-170">audio right off</span></span></li>
<li><span data-ttu-id="34704-171">аудио справа</span><span class="sxs-lookup"><span data-stu-id="34704-171">audio right on</span></span></li>
<li><span data-ttu-id="34704-172">дверца закрыта</span><span class="sxs-lookup"><span data-stu-id="34704-172">door closed</span></span></li>
<li><span data-ttu-id="34704-173">Дверца открыта</span><span class="sxs-lookup"><span data-stu-id="34704-173">door open</span></span></li>
<li><span data-ttu-id="34704-174">основной MIDI</span><span class="sxs-lookup"><span data-stu-id="34704-174">master MIDI</span></span></li>
<li><span data-ttu-id="34704-175">нет главного сервера</span><span class="sxs-lookup"><span data-stu-id="34704-175">master none</span></span></li>
<li><span data-ttu-id="34704-176">Главный SMPTE</span><span class="sxs-lookup"><span data-stu-id="34704-176">master SMPTE</span></span></li>
<li><span data-ttu-id="34704-177"><em>время</em> смещения</span><span class="sxs-lookup"><span data-stu-id="34704-177">offset <em>time</em></span></span></li>
<li><span data-ttu-id="34704-178">сопоставитель портов</span><span class="sxs-lookup"><span data-stu-id="34704-178">port mapper</span></span></li>
<li><span data-ttu-id="34704-179">порт отсутствует</span><span class="sxs-lookup"><span data-stu-id="34704-179">port none</span></span></li>
<li><span data-ttu-id="34704-180"><em>port_number</em> порта</span><span class="sxs-lookup"><span data-stu-id="34704-180">port <em>port_number</em></span></span></li>
<li><span data-ttu-id="34704-181">ведомый файл</span><span class="sxs-lookup"><span data-stu-id="34704-181">slave file</span></span></li>
<li><span data-ttu-id="34704-182">ведомый MIDI</span><span class="sxs-lookup"><span data-stu-id="34704-182">slave MIDI</span></span></li>
<li><span data-ttu-id="34704-183">подчиненный нет</span><span class="sxs-lookup"><span data-stu-id="34704-183">slave none</span></span></li>
<li><span data-ttu-id="34704-184">Ведомая SMPTE</span><span class="sxs-lookup"><span data-stu-id="34704-184">slave SMPTE</span></span></li>
<li><span data-ttu-id="34704-185">темп <em>tempo_value</em></span><span class="sxs-lookup"><span data-stu-id="34704-185">tempo <em>tempo_value</em></span></span></li>
<li><span data-ttu-id="34704-186">формат времени (МС)</span><span class="sxs-lookup"><span data-stu-id="34704-186">time format milliseconds</span></span></li>
<li><span data-ttu-id="34704-187">формат времени SMPTE <em>кадров/</em> с</span><span class="sxs-lookup"><span data-stu-id="34704-187">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="34704-188">формат времени SMPTE 30 Drop</span><span class="sxs-lookup"><span data-stu-id="34704-188">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="34704-189">Указатель песни формата времени</span><span class="sxs-lookup"><span data-stu-id="34704-189">time format song pointer</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-190"><strong>видеомагнитофон</strong></span><span class="sxs-lookup"><span data-stu-id="34704-190"><strong>vcr</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="34704-191">собрать запись на</span><span class="sxs-lookup"><span data-stu-id="34704-191">assemble record on</span></span></li>
<li><span data-ttu-id="34704-192">собрать запись</span><span class="sxs-lookup"><span data-stu-id="34704-192">assemble record off</span></span></li>
<li><span data-ttu-id="34704-193">Звук выкл.</span><span class="sxs-lookup"><span data-stu-id="34704-193">audio all off</span></span></li>
<li><span data-ttu-id="34704-194">звук включен</span><span class="sxs-lookup"><span data-stu-id="34704-194">audio all on</span></span></li>
<li><span data-ttu-id="34704-195">звук отключен</span><span class="sxs-lookup"><span data-stu-id="34704-195">audio left off</span></span></li>
<li><span data-ttu-id="34704-196">звук остался на</span><span class="sxs-lookup"><span data-stu-id="34704-196">audio left on</span></span></li>
<li><span data-ttu-id="34704-197">звуковое право</span><span class="sxs-lookup"><span data-stu-id="34704-197">audio right off</span></span></li>
<li><span data-ttu-id="34704-198">аудио справа</span><span class="sxs-lookup"><span data-stu-id="34704-198">audio right on</span></span></li>
<li><span data-ttu-id="34704-199"><em>время</em> в часах</span><span class="sxs-lookup"><span data-stu-id="34704-199">clock <em>time</em></span></span></li>
<li><span data-ttu-id="34704-200">Формат счетчика</span><span class="sxs-lookup"><span data-stu-id="34704-200">counter format</span></span></li>
<li><span data-ttu-id="34704-201"><em>значение</em> счетчика</span><span class="sxs-lookup"><span data-stu-id="34704-201">counter <em>value</em></span></span></li>
<li><span data-ttu-id="34704-202">дверца закрыта</span><span class="sxs-lookup"><span data-stu-id="34704-202">door closed</span></span></li>
<li><span data-ttu-id="34704-203">Дверца открыта</span><span class="sxs-lookup"><span data-stu-id="34704-203">door open</span></span></li>
<li><span data-ttu-id="34704-204">Счетчик индекса</span><span class="sxs-lookup"><span data-stu-id="34704-204">index counter</span></span></li>
<li><span data-ttu-id="34704-205">Дата индекса</span><span class="sxs-lookup"><span data-stu-id="34704-205">index date</span></span></li>
<li><span data-ttu-id="34704-206">время индекса</span><span class="sxs-lookup"><span data-stu-id="34704-206">index time</span></span></li>
<li><span data-ttu-id="34704-207">время индекса</span><span class="sxs-lookup"><span data-stu-id="34704-207">index time</span></span></li>
<li><span data-ttu-id="34704-208">коделенгс <em>Длительность</em></span><span class="sxs-lookup"><span data-stu-id="34704-208">codelength <em>duration</em></span></span></li>
<li><span data-ttu-id="34704-209"><em>время ожидания</em> приостановки</span><span class="sxs-lookup"><span data-stu-id="34704-209">pause <em>timeout</em></span></span></li>
<li><span data-ttu-id="34704-210">Длительность выкрутки —</span><span class="sxs-lookup"><span data-stu-id="34704-210">postroll duration -</span></span></li>
<li><span data-ttu-id="34704-211"><em>duration</em></span><span class="sxs-lookup"><span data-stu-id="34704-211"><em>duration</em></span></span></li>
<li><span data-ttu-id="34704-212">Включение</span><span class="sxs-lookup"><span data-stu-id="34704-212">power on</span></span></li>
<li><span data-ttu-id="34704-213">выключение питания</span><span class="sxs-lookup"><span data-stu-id="34704-213">power off</span></span></li>
<li><span data-ttu-id="34704-214"><em>Длительность</em> преддействия</span><span class="sxs-lookup"><span data-stu-id="34704-214">preroll duration <em>duration</em></span></span></li>
<li><span data-ttu-id="34704-215">формат записи SP</span><span class="sxs-lookup"><span data-stu-id="34704-215">record format SP</span></span></li>
<li><span data-ttu-id="34704-216">формат записи LP</span><span class="sxs-lookup"><span data-stu-id="34704-216">record format LP</span></span></li>
<li><span data-ttu-id="34704-217">формат записи EP</span><span class="sxs-lookup"><span data-stu-id="34704-217">record format EP</span></span></li>
<li><span data-ttu-id="34704-218"><em>Коэффициент</em> скорости</span><span class="sxs-lookup"><span data-stu-id="34704-218">speed <em>factor</em></span></span></li>
<li><span data-ttu-id="34704-219">кадры формата времени</span><span class="sxs-lookup"><span data-stu-id="34704-219">time format frames</span></span></li>
<li><span data-ttu-id="34704-220">формат времени ХМс</span><span class="sxs-lookup"><span data-stu-id="34704-220">time format hms</span></span></li>
<li><span data-ttu-id="34704-221">формат времени (МС)</span><span class="sxs-lookup"><span data-stu-id="34704-221">time format milliseconds</span></span></li>
<li><span data-ttu-id="34704-222">формат времени, MSF</span><span class="sxs-lookup"><span data-stu-id="34704-222">time format msf</span></span></li>
<li><span data-ttu-id="34704-223">формат времени SMPTE <em>кадров/</em> с</span><span class="sxs-lookup"><span data-stu-id="34704-223">time format SMPTE <em>fps</em></span></span></li>
<li><span data-ttu-id="34704-224">формат времени SMPTE 30 Drop</span><span class="sxs-lookup"><span data-stu-id="34704-224">time format SMPTE 30 drop</span></span></li>
<li><span data-ttu-id="34704-225">формат времени тмсф</span><span class="sxs-lookup"><span data-stu-id="34704-225">time format tmsf</span></span></li>
<li><span data-ttu-id="34704-226">Счетчик режима времени</span><span class="sxs-lookup"><span data-stu-id="34704-226">time mode counter</span></span></li>
<li><span data-ttu-id="34704-227">Обнаружение режима времени</span><span class="sxs-lookup"><span data-stu-id="34704-227">time mode detect</span></span></li>
<li><span data-ttu-id="34704-228">временной код режима времени</span><span class="sxs-lookup"><span data-stu-id="34704-228">time mode timecode</span></span></li>
<li><span data-ttu-id="34704-229">Отслеживание и</span><span class="sxs-lookup"><span data-stu-id="34704-229">tracking plus</span></span></li>
<li><span data-ttu-id="34704-230">Отслеживание минус</span><span class="sxs-lookup"><span data-stu-id="34704-230">tracking minus</span></span></li>
<li><span data-ttu-id="34704-231">Отслеживание сброса</span><span class="sxs-lookup"><span data-stu-id="34704-231">tracking reset</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-232">видеодиск</span><span class="sxs-lookup"><span data-stu-id="34704-232">videodisc</span></span></td>
<td><ul>
<li><span data-ttu-id="34704-233">Звук выкл.</span><span class="sxs-lookup"><span data-stu-id="34704-233">audio all off</span></span></li>
<li><span data-ttu-id="34704-234">звук включен</span><span class="sxs-lookup"><span data-stu-id="34704-234">audio all on</span></span></li>
<li><span data-ttu-id="34704-235">звук отключен</span><span class="sxs-lookup"><span data-stu-id="34704-235">audio left off</span></span></li>
<li><span data-ttu-id="34704-236">звук остался на</span><span class="sxs-lookup"><span data-stu-id="34704-236">audio left on</span></span></li>
<li><span data-ttu-id="34704-237">звуковое право</span><span class="sxs-lookup"><span data-stu-id="34704-237">audio right off</span></span></li>
<li><span data-ttu-id="34704-238">аудио справа</span><span class="sxs-lookup"><span data-stu-id="34704-238">audio right on</span></span></li>
<li><span data-ttu-id="34704-239">дверца закрыта</span><span class="sxs-lookup"><span data-stu-id="34704-239">door closed</span></span></li>
<li><span data-ttu-id="34704-240">Дверца открыта</span><span class="sxs-lookup"><span data-stu-id="34704-240">door open</span></span></li>
<li><span data-ttu-id="34704-241">кадры формата времени</span><span class="sxs-lookup"><span data-stu-id="34704-241">time format frames</span></span></li>
<li><span data-ttu-id="34704-242">формат времени ХМс</span><span class="sxs-lookup"><span data-stu-id="34704-242">time format hms</span></span></li>
<li><span data-ttu-id="34704-243">формат времени (МС)</span><span class="sxs-lookup"><span data-stu-id="34704-243">time format milliseconds</span></span></li>
<li><span data-ttu-id="34704-244">формат времени</span><span class="sxs-lookup"><span data-stu-id="34704-244">time format track</span></span></li>
<li><span data-ttu-id="34704-245">видео отключено</span><span class="sxs-lookup"><span data-stu-id="34704-245">video off</span></span></li>
<li><span data-ttu-id="34704-246">видео вкл.</span><span class="sxs-lookup"><span data-stu-id="34704-246">video on</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-247">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="34704-247">waveaudio</span></span></td>
<td><ul>
<li><span data-ttu-id="34704-248">Выравнивание по <em>целому</em> краю</span><span class="sxs-lookup"><span data-stu-id="34704-248">alignment <em>integer</em></span></span></li>
<li><span data-ttu-id="34704-249">любые входные данные</span><span class="sxs-lookup"><span data-stu-id="34704-249">any input</span></span></li>
<li><span data-ttu-id="34704-250">любые выходные данные</span><span class="sxs-lookup"><span data-stu-id="34704-250">any output</span></span></li>
<li><span data-ttu-id="34704-251">Звук выкл.</span><span class="sxs-lookup"><span data-stu-id="34704-251">audio all off</span></span></li>
<li><span data-ttu-id="34704-252">звук включен</span><span class="sxs-lookup"><span data-stu-id="34704-252">audio all on</span></span></li>
<li><span data-ttu-id="34704-253">звук отключен</span><span class="sxs-lookup"><span data-stu-id="34704-253">audio left off</span></span></li>
<li><span data-ttu-id="34704-254">звук остался на</span><span class="sxs-lookup"><span data-stu-id="34704-254">audio left on</span></span></li>
<li><span data-ttu-id="34704-255">звуковое право</span><span class="sxs-lookup"><span data-stu-id="34704-255">audio right off</span></span></li>
<li><span data-ttu-id="34704-256">аудио справа</span><span class="sxs-lookup"><span data-stu-id="34704-256">audio right on</span></span></li>
<li><span data-ttu-id="34704-257">битсперсампле <em>bit_count</em></span><span class="sxs-lookup"><span data-stu-id="34704-257">bitspersample <em>bit_count</em></span></span></li>
<li><span data-ttu-id="34704-258">битесперсек <em>byte_rate</em></span><span class="sxs-lookup"><span data-stu-id="34704-258">bytespersec <em>byte_rate</em></span></span></li>
<li><span data-ttu-id="34704-259">каналы <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="34704-259">channels <em>channel_count</em></span></span></li>
<li><span data-ttu-id="34704-260">дверца закрыта</span><span class="sxs-lookup"><span data-stu-id="34704-260">door closed</span></span></li>
<li><span data-ttu-id="34704-261">Дверца открыта</span><span class="sxs-lookup"><span data-stu-id="34704-261">door open</span></span></li>
<li><span data-ttu-id="34704-262">формат PCM тега</span><span class="sxs-lookup"><span data-stu-id="34704-262">format tag pcm</span></span></li>
<li><span data-ttu-id="34704-263">формат <em>тега</em> тега</span><span class="sxs-lookup"><span data-stu-id="34704-263">format tag <em>tag</em></span></span></li>
<li><span data-ttu-id="34704-264">Входное <em>целое число</em></span><span class="sxs-lookup"><span data-stu-id="34704-264">input <em>integer</em></span></span></li>
<li><span data-ttu-id="34704-265">Выходное <em>целое число</em></span><span class="sxs-lookup"><span data-stu-id="34704-265">output <em>integer</em></span></span></li>
<li><span data-ttu-id="34704-266">самплесперсек <em>целое число</em></span><span class="sxs-lookup"><span data-stu-id="34704-266">samplespersec <em>integer</em></span></span></li>
<li><span data-ttu-id="34704-267">байты формата времени</span><span class="sxs-lookup"><span data-stu-id="34704-267">time format bytes</span></span></li>
<li><span data-ttu-id="34704-268">формат времени (МС)</span><span class="sxs-lookup"><span data-stu-id="34704-268">time format milliseconds</span></span></li>
<li><span data-ttu-id="34704-269">Примеры форматов времени</span><span class="sxs-lookup"><span data-stu-id="34704-269">time format samples</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="34704-270">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсзсеттинг** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="34704-270">The following table lists the flags that can be specified in the **lpszSetting** parameter and their meanings.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34704-271">Значение</span><span class="sxs-lookup"><span data-stu-id="34704-271">Value</span></span></th>
<th><span data-ttu-id="34704-272">Значение</span><span class="sxs-lookup"><span data-stu-id="34704-272">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34704-273">Выравнивание по <em>целому</em> краю</span><span class="sxs-lookup"><span data-stu-id="34704-273">alignment <em>integer</em></span></span></td>
<td><span data-ttu-id="34704-274">Задает выравнивание блоков данных относительно начала данных, передаваемых устройству аудио-аудио.</span><span class="sxs-lookup"><span data-stu-id="34704-274">Sets the alignment of data blocks relative to the start of data passed to the waveform-audio device.</span></span> <span data-ttu-id="34704-275">Файл сохраняется в этом формате.</span><span class="sxs-lookup"><span data-stu-id="34704-275">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-276">любые входные данные</span><span class="sxs-lookup"><span data-stu-id="34704-276">any input</span></span></td>
<td><span data-ttu-id="34704-277">Используйте любые входные данные, которые поддерживают текущий формат при записи.</span><span class="sxs-lookup"><span data-stu-id="34704-277">Use any input that supports the current format when recording.</span></span> <span data-ttu-id="34704-278">Это параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="34704-278">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-279">любые выходные данные</span><span class="sxs-lookup"><span data-stu-id="34704-279">any output</span></span></td>
<td><span data-ttu-id="34704-280">Используйте любые выходные данные, которые поддерживают текущий формат при воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="34704-280">Use any output that supports the current format when playing.</span></span> <span data-ttu-id="34704-281">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="34704-281">This is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-282">собрать запись на</span><span class="sxs-lookup"><span data-stu-id="34704-282">assemble record on</span></span> <br/> <span data-ttu-id="34704-283">собрать запись</span><span class="sxs-lookup"><span data-stu-id="34704-283">assemble record off</span></span> <br/></td>
<td><span data-ttu-id="34704-284">В режиме сборки все дорожки записываются как определенные устройством.</span><span class="sxs-lookup"><span data-stu-id="34704-284">In assemble mode, all tracks are recorded as defined by the device.</span></span> <span data-ttu-id="34704-285">По умолчанию большинство видеомагнитофонов находятся в режиме сборки.</span><span class="sxs-lookup"><span data-stu-id="34704-285">Most VCRs are in assemble mode by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-286">Звук выкл.</span><span class="sxs-lookup"><span data-stu-id="34704-286">audio all off</span></span> <br/> <span data-ttu-id="34704-287">звук включен</span><span class="sxs-lookup"><span data-stu-id="34704-287">audio all on</span></span> <br/></td>
<td><span data-ttu-id="34704-288">Отключает или включает звуковые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="34704-288">Disables or enables audio output.</span></span> <span data-ttu-id="34704-289">Устройства с наложением видео, МЦИСЕК и МЦИВАВЕ волна-Audio не поддерживают этот флаг.</span><span class="sxs-lookup"><span data-stu-id="34704-289">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-290">звук отключен</span><span class="sxs-lookup"><span data-stu-id="34704-290">audio left off</span></span> <br/> <span data-ttu-id="34704-291">звук остался на</span><span class="sxs-lookup"><span data-stu-id="34704-291">audio left on</span></span> <br/> <span data-ttu-id="34704-292">звуковое право</span><span class="sxs-lookup"><span data-stu-id="34704-292">audio right off</span></span> <br/> <span data-ttu-id="34704-293">аудио справа</span><span class="sxs-lookup"><span data-stu-id="34704-293">audio right on</span></span> <br/></td>
<td><span data-ttu-id="34704-294">Отключает или включает вывод для левого или правого канала звука.</span><span class="sxs-lookup"><span data-stu-id="34704-294">Disables or enables output to either the left or the right audio channel.</span></span> <span data-ttu-id="34704-295">Устройства с наложением видео, МЦИСЕК и МЦИВАВЕ волна-Audio не поддерживают этот флаг.</span><span class="sxs-lookup"><span data-stu-id="34704-295">Video-overlay devices, the MCISEQ sequencer, and the MCIWAVE waveform-audio device do not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-296">битсперсампле <em>bit_count</em></span><span class="sxs-lookup"><span data-stu-id="34704-296">bitspersample <em>bit_count</em></span></span></td>
<td><span data-ttu-id="34704-297">Задает количество записываемых или записанных битов на PCM (модуляция импульсного кода).</span><span class="sxs-lookup"><span data-stu-id="34704-297">Sets the number of bits per PCM (Pulse Code Modulation) sample played or recorded.</span></span> <span data-ttu-id="34704-298">Файл сохраняется в этом формате.</span><span class="sxs-lookup"><span data-stu-id="34704-298">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-299">битесперсек <em>byte_rate</em></span><span class="sxs-lookup"><span data-stu-id="34704-299">bytespersec <em>byte_rate</em></span></span></td>
<td><span data-ttu-id="34704-300">Задает среднее число воспроизводимых или записанных байт в секунду.</span><span class="sxs-lookup"><span data-stu-id="34704-300">Sets the average number of bytes per second played or recorded.</span></span> <span data-ttu-id="34704-301">Файл сохраняется в этом формате.</span><span class="sxs-lookup"><span data-stu-id="34704-301">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-302">каналы <em>channel_count</em></span><span class="sxs-lookup"><span data-stu-id="34704-302">channels <em>channel_count</em></span></span></td>
<td><span data-ttu-id="34704-303">Задает каналы для воспроизведения и записи.</span><span class="sxs-lookup"><span data-stu-id="34704-303">Sets the channels for playing and recording.</span></span> <span data-ttu-id="34704-304">Файл сохраняется в этом формате.</span><span class="sxs-lookup"><span data-stu-id="34704-304">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-305"><em>время</em> в часах</span><span class="sxs-lookup"><span data-stu-id="34704-305">clock <em>time</em></span></span></td>
<td><span data-ttu-id="34704-306">Задает время для внешних часов <em>.</em></span><span class="sxs-lookup"><span data-stu-id="34704-306">Sets time on the external clock to <em>time.</em></span></span> <span data-ttu-id="34704-307">Формат указывается как длинное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="34704-307">The format is specified as a long unsigned integer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-308">Формат счетчика</span><span class="sxs-lookup"><span data-stu-id="34704-308">counter format</span></span></td>
<td><span data-ttu-id="34704-309">Задайте формат времени для счетчика, возвращенного счетчиком <a href="status.md">состояния</a> &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="34704-309">Set the time format for the counter, as returned by <a href="status.md">status</a> &quot;counter&quot;.</span></span> <span data-ttu-id="34704-310">Дополнительные сведения о применимых типах см. в описании команды " <strong>задать</strong> &quot; Формат времени" &quot; .</span><span class="sxs-lookup"><span data-stu-id="34704-310">For information about applicable types, see the <strong>set</strong> &quot;time format&quot; command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-311"><em>значение</em> счетчика</span><span class="sxs-lookup"><span data-stu-id="34704-311">counter <em>value</em></span></span></td>
<td><span data-ttu-id="34704-312">Устанавливает для счетчика ВИДЕОМАГНИТОФОНА указанное значение.</span><span class="sxs-lookup"><span data-stu-id="34704-312">Sets the VCR counter to the specified value.</span></span> <span data-ttu-id="34704-313">Значение должно быть указано в текущем формате счетчика.</span><span class="sxs-lookup"><span data-stu-id="34704-313">The value must be specified in the current counter format.</span></span> <span data-ttu-id="34704-314">Дополнительные сведения см. в разделе команда <strong>задания</strong> &quot; формата счетчика &quot; .</span><span class="sxs-lookup"><span data-stu-id="34704-314">For more information, see the <strong>set</strong> &quot;counter format&quot; command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-315">дверца закрыта</span><span class="sxs-lookup"><span data-stu-id="34704-315">door closed</span></span></td>
<td><span data-ttu-id="34704-316">Отзывает область и закрывает дверцу, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="34704-316">Retracts the tray and closes the door, if possible.</span></span> <span data-ttu-id="34704-317">Для видеомагнитофона загружает ленту автоматически.</span><span class="sxs-lookup"><span data-stu-id="34704-317">For VCRs, loads the tape automatically.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-318">Дверца открыта</span><span class="sxs-lookup"><span data-stu-id="34704-318">door open</span></span></td>
<td><span data-ttu-id="34704-319">Открывает дверцу и извлекает лоток или ленту, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="34704-319">Opens the door and ejects the tray or tape, if possible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-320"><em>Формат</em> формата файла</span><span class="sxs-lookup"><span data-stu-id="34704-320">file format <em>format</em></span></span></td>
<td><span data-ttu-id="34704-321">Указывает формат файла, используемый для <a href="save.md">сохранения</a> или <a href="capture.md">записи</a> команд.</span><span class="sxs-lookup"><span data-stu-id="34704-321">Specifies a file format that is used for <a href="save.md">save</a> or <a href="capture.md">capture</a> commands.</span></span> <span data-ttu-id="34704-322">Если этот параметр опущен, то по умолчанию может быть задан формат драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="34704-322">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="34704-323">Если указанный формат файла конфликтует с текущим выбранным алгоритмом и качеством, то они будут заменены на значения по умолчанию для формата файла.</span><span class="sxs-lookup"><span data-stu-id="34704-323">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="34704-324">Определены следующие форматы файлов:</span><span class="sxs-lookup"><span data-stu-id="34704-324">The following file formats are defined:</span></span>
<ul>
<li><span data-ttu-id="34704-325">AVI: указывает формат AVI.</span><span class="sxs-lookup"><span data-stu-id="34704-325">avi: Specifies AVI format.</span></span></li>
<li><span data-ttu-id="34704-326">авсс: указывает формат АВСС.</span><span class="sxs-lookup"><span data-stu-id="34704-326">avss: Specifies AVSS format.</span></span></li>
<li><span data-ttu-id="34704-327">DIB: задает формат DIB.</span><span class="sxs-lookup"><span data-stu-id="34704-327">dib: Specifies DIB format.</span></span></li>
<li><span data-ttu-id="34704-328">JFIF: указывает формат JFIF.</span><span class="sxs-lookup"><span data-stu-id="34704-328">jfif: Specifies JFIF format.</span></span></li>
<li><span data-ttu-id="34704-329">JPEG: определяет формат JPEG.</span><span class="sxs-lookup"><span data-stu-id="34704-329">jpeg: Specifies JPEG format.</span></span></li>
<li><span data-ttu-id="34704-330">MPEG: указывает формат MPEG.</span><span class="sxs-lookup"><span data-stu-id="34704-330">mpeg: Specifies MPEG format.</span></span></li>
<li><span data-ttu-id="34704-331">рдиб: указывает формат RLE DIB.</span><span class="sxs-lookup"><span data-stu-id="34704-331">rdib: Specifies RLE DIB format.</span></span></li>
<li><span data-ttu-id="34704-332">ржпег: указывает формат РЖПЕГ.</span><span class="sxs-lookup"><span data-stu-id="34704-332">rjpeg: Specifies RJPEG format.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-333">формат PCM тега</span><span class="sxs-lookup"><span data-stu-id="34704-333">format tag pcm</span></span></td>
<td><span data-ttu-id="34704-334">Задает тип формата PCM для воспроизведения и записи.</span><span class="sxs-lookup"><span data-stu-id="34704-334">Sets the format type to PCM for playing and recording.</span></span> <span data-ttu-id="34704-335">Файл сохраняется в этом формате.</span><span class="sxs-lookup"><span data-stu-id="34704-335">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-336">формат <em>тега</em> тега</span><span class="sxs-lookup"><span data-stu-id="34704-336">format tag <em>tag</em></span></span></td>
<td><span data-ttu-id="34704-337">Задает тип формата для воспроизведения и записи.</span><span class="sxs-lookup"><span data-stu-id="34704-337">Sets the format type for playing and recording.</span></span> <span data-ttu-id="34704-338">Файл сохраняется в этом формате.</span><span class="sxs-lookup"><span data-stu-id="34704-338">The file is saved in this format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-339">временной код индекса</span><span class="sxs-lookup"><span data-stu-id="34704-339">index timecode</span></span> <br/> <span data-ttu-id="34704-340">Счетчик индекса</span><span class="sxs-lookup"><span data-stu-id="34704-340">index counter</span></span> <br/> <span data-ttu-id="34704-341">Дата индекса</span><span class="sxs-lookup"><span data-stu-id="34704-341">index date</span></span> <br/> <span data-ttu-id="34704-342">время индекса</span><span class="sxs-lookup"><span data-stu-id="34704-342">index time</span></span> <br/></td>
<td><span data-ttu-id="34704-343">Задает текущий экран отображения на ВИДЕОМАГНИТОФОН.</span><span class="sxs-lookup"><span data-stu-id="34704-343">Sets the current display screen on the VCR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-344">Входное <em>целое число</em></span><span class="sxs-lookup"><span data-stu-id="34704-344">input <em>integer</em></span></span></td>
<td><span data-ttu-id="34704-345">Задает канал звука, используемый в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="34704-345">Sets the audio channel used as the input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-346"><em>Длительность</em> длины</span><span class="sxs-lookup"><span data-stu-id="34704-346">length <em>duration</em></span></span></td>
<td><span data-ttu-id="34704-347">Задает указанную пользователем длину ленты в ВИДЕОМАГНИТОФОН.</span><span class="sxs-lookup"><span data-stu-id="34704-347">Sets the user-specified length of the tape in the VCR.</span></span> <span data-ttu-id="34704-348">Эта длина возвращается командой "длина <a href="status.md">состояния</a> &quot; " &quot; и предоставляется для совместимости с приложениями, для которых эта команда должна возвращать допустимую длину.</span><span class="sxs-lookup"><span data-stu-id="34704-348">This length is returned by the <a href="status.md">status</a> &quot;length&quot; command and is provided for compatibility with applications that require this command to return a valid length.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-349">основной MIDI</span><span class="sxs-lookup"><span data-stu-id="34704-349">master midi</span></span></td>
<td><span data-ttu-id="34704-350">Задает секвенсор MIDI в качестве источника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="34704-350">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="34704-351">Данные синхронизации отправляются в формате MIDI.</span><span class="sxs-lookup"><span data-stu-id="34704-351">Synchronization data is sent in MIDI format.</span></span> <span data-ttu-id="34704-352">МЦИСЕК Sequencer не поддерживает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="34704-352">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-353">нет главного сервера</span><span class="sxs-lookup"><span data-stu-id="34704-353">master none</span></span></td>
<td><span data-ttu-id="34704-354">Запрещает секвенсору MIDI отправку данных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="34704-354">Inhibits the MIDI sequencer from sending synchronization data.</span></span> <span data-ttu-id="34704-355">МЦИСЕК Sequencer не поддерживает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="34704-355">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-356">Главный SMPTE</span><span class="sxs-lookup"><span data-stu-id="34704-356">master smpte</span></span></td>
<td><span data-ttu-id="34704-357">Задает секвенсор MIDI в качестве источника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="34704-357">Sets the MIDI sequencer as the synchronization source.</span></span> <span data-ttu-id="34704-358">Данные синхронизации отправляются в SMPTE (общество разработчиков изображений и телевизионных телевидения).</span><span class="sxs-lookup"><span data-stu-id="34704-358">Synchronization data is sent in SMPTE (Society of Motion Picture and Television Engineers) format.</span></span> <span data-ttu-id="34704-359">МЦИСЕК Sequencer не поддерживает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="34704-359">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-360"><em>время</em> смещения</span><span class="sxs-lookup"><span data-stu-id="34704-360">offset <em>time</em></span></span></td>
<td><span data-ttu-id="34704-361">Задает <em>время</em>смещения SMPTE.</span><span class="sxs-lookup"><span data-stu-id="34704-361">Sets the SMPTE offset <em>time</em>.</span></span> <span data-ttu-id="34704-362">Смещение — это время начала последовательности на основе SMPTE.</span><span class="sxs-lookup"><span data-stu-id="34704-362">The offset is the beginning time of a SMPTE based sequence.</span></span> <span data-ttu-id="34704-363"><em>Время</em> выражается в <em>формате чч</em>: <em>мм</em>: <em>СС</em>: <em>FF</em>, где <em>чч</em> — часы, <em>mm</em> — минуты, <em>SS</em> — секунды, а <em>FF</em> — кадры.</span><span class="sxs-lookup"><span data-stu-id="34704-363">The <em>time</em> is expressed as <em>hh</em>: <em>mm</em>: <em>ss</em>: <em>ff</em>, where <em>hh</em> is hours, <em>mm</em> is minutes, <em>ss</em> is seconds, and <em>ff</em> is frames.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-364">Выходное <em>целое число</em></span><span class="sxs-lookup"><span data-stu-id="34704-364">output <em>integer</em></span></span></td>
<td><span data-ttu-id="34704-365">Задает канал звука, используемый в качестве выходных данных.</span><span class="sxs-lookup"><span data-stu-id="34704-365">Sets the audio channel used as the output.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-366"><em>время ожидания</em> приостановки</span><span class="sxs-lookup"><span data-stu-id="34704-366">pause <em>timeout</em></span></span></td>
<td><span data-ttu-id="34704-367">Задает максимальную продолжительность команды <a href="pause.md">Pause</a> в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="34704-367">Sets the maximum duration, in milliseconds, of a <a href="pause.md">pause</a> command.</span></span> <span data-ttu-id="34704-368">Нулевое значение <em>времени ожидания</em> указывает, что время ожидания не произойдет.</span><span class="sxs-lookup"><span data-stu-id="34704-368">A <em>timeout</em> value of zero indicates that no time-out will occur.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-369"><em>Длительность длительности</em></span><span class="sxs-lookup"><span data-stu-id="34704-369">postroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="34704-370">Задает длину (в текущем формате времени), необходимую для переноса данных из ВИДЕОМАГНИТОФОНА при выполнении команды <a href="stop.md">остановки</a> или <strong>приостановки</strong> .</span><span class="sxs-lookup"><span data-stu-id="34704-370">Sets the length, in the current time format, needed to brake the VCR transport when a <a href="stop.md">stop</a> or <strong>pause</strong> command is issued.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-371">сопоставитель портов</span><span class="sxs-lookup"><span data-stu-id="34704-371">port mapper</span></span></td>
<td><span data-ttu-id="34704-372">Устанавливает сопоставитель MIDI в качестве порта, получающего сообщения MIDI.</span><span class="sxs-lookup"><span data-stu-id="34704-372">Sets the MIDI mapper as the port receiving the MIDI messages.</span></span> <span data-ttu-id="34704-373">Эта команда завершается ошибкой, если в другом приложении используется сопоставитель MIDI или порт.</span><span class="sxs-lookup"><span data-stu-id="34704-373">This command fails if the MIDI mapper or a port it needs is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-374">порт отсутствует</span><span class="sxs-lookup"><span data-stu-id="34704-374">port none</span></span></td>
<td><span data-ttu-id="34704-375">Отключает отправку сообщений MIDI.</span><span class="sxs-lookup"><span data-stu-id="34704-375">Disables the sending of MIDI messages.</span></span> <span data-ttu-id="34704-376">Эта команда также закрывает порт MIDI.</span><span class="sxs-lookup"><span data-stu-id="34704-376">This command also closes a MIDI port.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-377"><em>port_number</em> порта</span><span class="sxs-lookup"><span data-stu-id="34704-377">port <em>port_number</em></span></span></td>
<td><span data-ttu-id="34704-378">Задает порт MIDI, получающий сообщения MIDI.</span><span class="sxs-lookup"><span data-stu-id="34704-378">Sets the MIDI port receiving the MIDI messages.</span></span> <span data-ttu-id="34704-379">Эта команда завершается ошибкой, если открываемый порт используется другим приложением.</span><span class="sxs-lookup"><span data-stu-id="34704-379">This command fails if the port you are trying to open is being used by another application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-380">Включение</span><span class="sxs-lookup"><span data-stu-id="34704-380">power on</span></span> <br/> <span data-ttu-id="34704-381">выключение питания</span><span class="sxs-lookup"><span data-stu-id="34704-381">power off</span></span> <br/></td>
<td><span data-ttu-id="34704-382">Задает включение или выключение питания устройства.</span><span class="sxs-lookup"><span data-stu-id="34704-382">Sets the device power to on or off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-383"><em>Длительность</em> преддействия</span><span class="sxs-lookup"><span data-stu-id="34704-383">preroll duration <em>duration</em></span></span></td>
<td><span data-ttu-id="34704-384">Задает длину в текущем формате времени, необходимую для стабилизации выходных данных ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="34704-384">Sets the length, in the current time format, needed to stabilize the VCR output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-385">формат записи SP</span><span class="sxs-lookup"><span data-stu-id="34704-385">record format SP</span></span> <br/> <span data-ttu-id="34704-386">формат записи LP</span><span class="sxs-lookup"><span data-stu-id="34704-386">record format LP</span></span> <br/> <span data-ttu-id="34704-387">формат записи EP</span><span class="sxs-lookup"><span data-stu-id="34704-387">record format EP</span></span> <br/></td>
<td><span data-ttu-id="34704-388">Устанавливает режим записи для ВИДЕОМАГНИТОФОНА в значение SP для Standard Play, EP для расширенного воспроизведения или LP для длительного воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="34704-388">Sets the recording mode for the VCR to SP for standard play, EP for extended play, or LP for long play.</span></span> <span data-ttu-id="34704-389">Эти значения не предназначены для ВХС.</span><span class="sxs-lookup"><span data-stu-id="34704-389">These values are not intended to be VHS specific.</span></span> <span data-ttu-id="34704-390">Они сопоставляются с любыми тремя подходящими режимами с другими форматами ленты.</span><span class="sxs-lookup"><span data-stu-id="34704-390">They map to any three appropriate modes with other tape formats.</span></span> <span data-ttu-id="34704-391">Например, SP сопоставляется с самой быстрой и высококачественной записью.</span><span class="sxs-lookup"><span data-stu-id="34704-391">For example, SP maps to the fastest, highest quality recording.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-392">самплесперсек <em>целое число</em></span><span class="sxs-lookup"><span data-stu-id="34704-392">samplespersec <em>integer</em></span></span></td>
<td><span data-ttu-id="34704-393">Задает частоту выборки для воспроизведения и записи.</span><span class="sxs-lookup"><span data-stu-id="34704-393">Sets the sample rate for playing and recording.</span></span> <span data-ttu-id="34704-394">Файл сохраняется в этом формате.</span><span class="sxs-lookup"><span data-stu-id="34704-394">The file is saved in this format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-395">Поиск в точности</span><span class="sxs-lookup"><span data-stu-id="34704-395">seek exactly on</span></span><br/> <span data-ttu-id="34704-396">Поиск в точности</span><span class="sxs-lookup"><span data-stu-id="34704-396">seek exactly off</span></span> <br/></td>
<td><span data-ttu-id="34704-397">Выбирает один из двух режимов поиска.</span><span class="sxs-lookup"><span data-stu-id="34704-397">Selects one of two seek modes.</span></span> <span data-ttu-id="34704-398">Если &quot; Поиск выполняется в точности &quot; , поиск всегда будет перемещаться к заданному кадру.</span><span class="sxs-lookup"><span data-stu-id="34704-398">With &quot;seek exactly on&quot;, seek will always move to the frame specified.</span></span> <span data-ttu-id="34704-399">Если &quot; Поиск выполняется в точности &quot; , поиск будет перемещен к ближайшему ключевому кадру до указанного кадра.</span><span class="sxs-lookup"><span data-stu-id="34704-399">With &quot;seek exactly off&quot;, seek will move to the closest key frame prior to the frame specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-400">ведомый файл</span><span class="sxs-lookup"><span data-stu-id="34704-400">slave file</span></span></td>
<td><span data-ttu-id="34704-401">Задает секвенсор MIDI для использования файловых данных в качестве источника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="34704-401">Sets the MIDI sequencer to use file data as the synchronization source.</span></span> <span data-ttu-id="34704-402">Это параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="34704-402">This is the default setting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-403">ведомый MIDI</span><span class="sxs-lookup"><span data-stu-id="34704-403">slave midi</span></span></td>
<td><span data-ttu-id="34704-404">Задает секвенсор MIDI для использования входящих данных MIDI для источника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="34704-404">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="34704-405">Секвенсор распознает данные синхронизации в формате MIDI.</span><span class="sxs-lookup"><span data-stu-id="34704-405">The sequencer recognizes synchronization data with the MIDI format.</span></span> <span data-ttu-id="34704-406">МЦИСЕК Sequencer не поддерживает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="34704-406">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-407">подчиненный нет</span><span class="sxs-lookup"><span data-stu-id="34704-407">slave none</span></span></td>
<td><span data-ttu-id="34704-408">Задает для секвенсора MIDI игнорирование синхронизации</span><span class="sxs-lookup"><span data-stu-id="34704-408">Sets the MIDI sequencer to ignore synchronization</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-409">Ведомая SMPTE</span><span class="sxs-lookup"><span data-stu-id="34704-409">slave smpte</span></span></td>
<td><span data-ttu-id="34704-410">Задает секвенсор MIDI для использования входящих данных MIDI для источника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="34704-410">Sets the MIDI sequencer to use incoming MIDI data for the synchronization source.</span></span> <span data-ttu-id="34704-411">Секвенсор распознает данные синхронизации в формате SMPTE.</span><span class="sxs-lookup"><span data-stu-id="34704-411">The sequencer recognizes synchronization data with the SMPTE format.</span></span> <span data-ttu-id="34704-412">МЦИСЕК Sequencer не поддерживает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="34704-412">The MCISEQ sequencer does not support this flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-413">коэффициент скорости</span><span class="sxs-lookup"><span data-stu-id="34704-413">speed factor</span></span></td>
<td><span data-ttu-id="34704-414">Задает относительную скорость воспроизведения видео и звука из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="34704-414">Sets the relative speed of video and audio playback from the workspace.</span></span> <span data-ttu-id="34704-415">Коэффициент — это отношение между номинальной частотой кадров и требуемой частотой кадров, где Номинальная частота кадров обозначена как 1000.</span><span class="sxs-lookup"><span data-stu-id="34704-415">Factor is the ratio between the nominal frame rate and the desired frame rate, where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="34704-416">(Частота 500 составляет половину обычной скорости, 2000 — вдвое нормальная скорость и т. д.) Установка нулевой скорости воспроизводит видео как можно быстрее без удаления кадров и без звука.</span><span class="sxs-lookup"><span data-stu-id="34704-416">(A rate of 500 is half normal speed, 2000 is twice normal speed, and so on.) Setting the speed to zero plays the video as fast as possible without dropping frames and without audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-417"><em>Формат</em> файла по-прежнему</span><span class="sxs-lookup"><span data-stu-id="34704-417">still file format <em>format</em></span></span></td>
<td><span data-ttu-id="34704-418">Указывает формат файла, используемый для команд записи.</span><span class="sxs-lookup"><span data-stu-id="34704-418">Specifies the file format used for capture commands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-419">темп tempo_value</span><span class="sxs-lookup"><span data-stu-id="34704-419">tempo tempo_value</span></span></td>
<td><span data-ttu-id="34704-420">Задает темп последовательности в соответствии с текущим форматом времени.</span><span class="sxs-lookup"><span data-stu-id="34704-420">Sets the tempo of the sequence according to the current time format.</span></span> <span data-ttu-id="34704-421">Для файла, основанного на ППКН, tempo_value интерпретируется как ритм в минуту.</span><span class="sxs-lookup"><span data-stu-id="34704-421">For a PPQN-based file, the tempo_value is interpreted as beats per minute.</span></span> <span data-ttu-id="34704-422">Для файла на основе SMPTE tempo_value интерпретируется как число кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="34704-422">For a SMPTE-based file, the tempo_value is interpreted as frames per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-423">байты формата времени</span><span class="sxs-lookup"><span data-stu-id="34704-423">time format bytes</span></span></td>
<td><span data-ttu-id="34704-424">В формате файла PCM устанавливает формат времени в байтах.</span><span class="sxs-lookup"><span data-stu-id="34704-424">In a PCM file format, sets the time format to bytes.</span></span> <span data-ttu-id="34704-425">Все сведения о положении указываются в байтах после этой команды.</span><span class="sxs-lookup"><span data-stu-id="34704-425">All position information is specified as bytes following this command.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-426">кадры формата времени</span><span class="sxs-lookup"><span data-stu-id="34704-426">time format frames</span></span></td>
<td><span data-ttu-id="34704-427">Задает формат времени для кадров.</span><span class="sxs-lookup"><span data-stu-id="34704-427">Sets the time format to frames.</span></span> <span data-ttu-id="34704-428">Все команды, использующие значения позиций, предполагают наличие кадров.</span><span class="sxs-lookup"><span data-stu-id="34704-428">All commands that use position values will assume frames.</span></span> <span data-ttu-id="34704-429">При открытии устройства в качестве режима по умолчанию используется кадр.</span><span class="sxs-lookup"><span data-stu-id="34704-429">When the device is opened, frames is the default mode.</span></span> <span data-ttu-id="34704-430">Поддерживается видеодискс с использованием формата Кав.</span><span class="sxs-lookup"><span data-stu-id="34704-430">Supported by videodiscs using CAV format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-431">формат времени ХМс</span><span class="sxs-lookup"><span data-stu-id="34704-431">time format hms</span></span></td>
<td><span data-ttu-id="34704-432">Задает формат времени в часах, минутах и секундах.</span><span class="sxs-lookup"><span data-stu-id="34704-432">Sets the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="34704-433">Все команды, использующие значения позиций, будут считаться ХМС.</span><span class="sxs-lookup"><span data-stu-id="34704-433">All commands that use position values will assume HMS.</span></span> <span data-ttu-id="34704-434">ХМС является форматом по умолчанию для CLV видеодискс.</span><span class="sxs-lookup"><span data-stu-id="34704-434">HMS is the default format for CLV videodiscs.</span></span> <span data-ttu-id="34704-435">Укажите значение ХМС в формате чч: мм: СС, где чч — часы, мм — минуты, а SS — секунды.</span><span class="sxs-lookup"><span data-stu-id="34704-435">Specify an HMS value as hh:mm:ss, where hh is hours, mm is minutes, and ss is seconds.</span></span> <span data-ttu-id="34704-436">Можно опустить поле, если оно и все следующие поля равны нулю.</span><span class="sxs-lookup"><span data-stu-id="34704-436">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="34704-437">Например, 3, 3:0 и 3:0:0 — это все допустимые способы выражения 3 часа.</span><span class="sxs-lookup"><span data-stu-id="34704-437">For example, 3, 3:0, and 3:0:0 are all valid ways to express 3 hours.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-438">формат времени (МС)</span><span class="sxs-lookup"><span data-stu-id="34704-438">time format milliseconds</span></span></td>
<td><span data-ttu-id="34704-439">Устанавливает формат времени в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="34704-439">Sets the time format to milliseconds.</span></span> <span data-ttu-id="34704-440">Все команды, использующие значения позиций, будут считаться миллисекундами.</span><span class="sxs-lookup"><span data-stu-id="34704-440">All commands that use position values will assume milliseconds.</span></span> <span data-ttu-id="34704-441">Время в миллисекундах можно сократить как &quot; МС &quot; .</span><span class="sxs-lookup"><span data-stu-id="34704-441">You can abbreviate milliseconds as &quot;ms&quot;.</span></span> <span data-ttu-id="34704-442">Для устройств Sequencer файл последовательности устанавливает формат по умолчанию ППКН или SMPTE.</span><span class="sxs-lookup"><span data-stu-id="34704-442">For sequencer devices, the sequence file sets the default format to PPQN or SMPTE.</span></span> <span data-ttu-id="34704-443">Устройства с наложением видео не поддерживают этот флаг.</span><span class="sxs-lookup"><span data-stu-id="34704-443">Video-overlay devices do not support this flag.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-444">формат времени, MSF</span><span class="sxs-lookup"><span data-stu-id="34704-444">time format msf</span></span></td>
<td><span data-ttu-id="34704-445">Устанавливает формат времени в минутах, секундах и кадрах.</span><span class="sxs-lookup"><span data-stu-id="34704-445">Sets the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="34704-446">Все команды, использующие значения позиций, предполагают использование MSF (формат по умолчанию для аудио компакт-диска).</span><span class="sxs-lookup"><span data-stu-id="34704-446">All commands that use position values will assume MSF (the default format for CD audio).</span></span> <span data-ttu-id="34704-447">Укажите значение MSF в формате mm: SS: FF, где mm — минуты, SS — секунды, а FF — кадры.</span><span class="sxs-lookup"><span data-stu-id="34704-447">Specify an MSF value as mm:ss:ff, where mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="34704-448">Можно опустить поле, если оно и все следующие поля равны нулю.</span><span class="sxs-lookup"><span data-stu-id="34704-448">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="34704-449">Например, 3, 3:0 и 3:0:0 — допустимые способы выразить 3 минуты.</span><span class="sxs-lookup"><span data-stu-id="34704-449">For example, 3, 3:0, and 3:0:0 are valid ways to express 3 minutes.</span></span><br/> <span data-ttu-id="34704-450">Поля MSF имеют следующие максимальные значения:</span><span class="sxs-lookup"><span data-stu-id="34704-450">The MSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="34704-451">Минуты 99</span><span class="sxs-lookup"><span data-stu-id="34704-451">Minutes 99</span></span></li>
<li><span data-ttu-id="34704-452">Секунды 59</span><span class="sxs-lookup"><span data-stu-id="34704-452">Seconds 59</span></span></li>
<li><span data-ttu-id="34704-453">Кадры 74</span><span class="sxs-lookup"><span data-stu-id="34704-453">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-454">Примеры форматов времени</span><span class="sxs-lookup"><span data-stu-id="34704-454">time format samples</span></span></td>
<td><span data-ttu-id="34704-455">Задает формат времени для выборок.</span><span class="sxs-lookup"><span data-stu-id="34704-455">Sets the time format to samples.</span></span> <span data-ttu-id="34704-456">Все сведения о положении указываются в качестве примеров после этой команды.</span><span class="sxs-lookup"><span data-stu-id="34704-456">All position information is specified as samples following this command.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-457">формат времени SMPTE 24</span><span class="sxs-lookup"><span data-stu-id="34704-457">time format smpte 24</span></span><br/> <span data-ttu-id="34704-458">формат времени SMPTE 25</span><span class="sxs-lookup"><span data-stu-id="34704-458">time format smpte 25</span></span><br/> <span data-ttu-id="34704-459">формат времени SMPTE 30</span><span class="sxs-lookup"><span data-stu-id="34704-459">time format smpte 30</span></span><br/></td>
<td><span data-ttu-id="34704-460">Задает формат времени для SMPTE частоты кадров.</span><span class="sxs-lookup"><span data-stu-id="34704-460">Sets the time format to an SMPTE frame rate.</span></span> <span data-ttu-id="34704-461">Для видеомагнитофона задает формат времени ЧЧ: мм: СС: FF, где допустимые значения: от 00:00:00:00 до 23:59:59: XX, а XX — один меньше, чем число кадров в секунду, заданное в числе 24, 25 или 30, как указано в флаге.</span><span class="sxs-lookup"><span data-stu-id="34704-461">For VCRs, sets the time format to hh:mm:ss:ff, where the legal values are 00:00:00:00 through 23:59:59:xx, and xx is one less than the frames per second as specified by the number 24, 25, or 30 as specified in the flag.</span></span> <span data-ttu-id="34704-462">На входе, двоеточия (:) для разделения компонентов требуются.</span><span class="sxs-lookup"><span data-stu-id="34704-462">On input, colons (:) are required to separate the components.</span></span> <span data-ttu-id="34704-463">Наименее значащие единицы можно опустить, если они равны 00; Например, 02:00 совпадает с 02:00:00:00.</span><span class="sxs-lookup"><span data-stu-id="34704-463">The least significant units can be omitted if they are 00; for example, 02:00 is the same as 02:00:00:00.</span></span> <span data-ttu-id="34704-464">Все команды, использующие значения позиций, будут иметь формат SMPTE.</span><span class="sxs-lookup"><span data-stu-id="34704-464">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="34704-465">Файл последовательности устанавливает формат по умолчанию ППКН или SMPTE.</span><span class="sxs-lookup"><span data-stu-id="34704-465">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-466">формат времени SMPTE 30 Drop</span><span class="sxs-lookup"><span data-stu-id="34704-466">time format smpte 30 drop</span></span></td>
<td><span data-ttu-id="34704-467">Устанавливает для формата времени значение SMPTE 30 скорость кадров.</span><span class="sxs-lookup"><span data-stu-id="34704-467">Sets the time format to SMPTE 30 drop frame rate.</span></span> <span data-ttu-id="34704-468">Для видеомагнитофонов, то же, что и SMPTE 30, за исключением того, что определенные позиции времени удаляются из формата, чтобы записывались позиции временного периода для каждого кадра (в частоте кадров NTSC 29,97 кадров/с) соответствует реальное время (30 кадров/с).</span><span class="sxs-lookup"><span data-stu-id="34704-468">For VCRs, same as SMPTE 30, except that certain timecode positions are dropped from the format to have the recorded timecode positions for each frame (at the NTSC frame rate of 29.97 fps) correspond to real time (at 30 fps).</span></span> <span data-ttu-id="34704-469">Удаляемые позиции времени выполнения: две минуты (в минуту) для первых девяти каждых 10 минут записанного содержимого.</span><span class="sxs-lookup"><span data-stu-id="34704-469">Timecode positions that are dropped are as follows: two every minute, on the minute, for the first nine of every ten minutes of recorded content.</span></span> <span data-ttu-id="34704-470">Например, в 01:04:59:29 следующий код времени будет равен 01:05:00:02, а не 01:05:00:00.</span><span class="sxs-lookup"><span data-stu-id="34704-470">For example, at 01:04:59:29, the next timecode position would be 01:05:00:02, not 01:05:00:00.</span></span> <span data-ttu-id="34704-471">Все команды, использующие значения позиций, будут иметь формат SMPTE.</span><span class="sxs-lookup"><span data-stu-id="34704-471">All commands that use position values will assume SMPTE format.</span></span><br/> <span data-ttu-id="34704-472">Файл последовательности устанавливает формат по умолчанию ППКН или SMPTE.</span><span class="sxs-lookup"><span data-stu-id="34704-472">The sequence file sets the default format to PPQN or SMPTE.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-473">Указатель песни формата времени</span><span class="sxs-lookup"><span data-stu-id="34704-473">time format song pointer</span></span></td>
<td><span data-ttu-id="34704-474">Задает формат времени для указателя композиции (шестнадцатые примечания).</span><span class="sxs-lookup"><span data-stu-id="34704-474">Sets the time format to song pointer (sixteenth notes).</span></span> <span data-ttu-id="34704-475">Во всех командах, использующих значения позиции, будут использоваться единицы указателей песни.</span><span class="sxs-lookup"><span data-stu-id="34704-475">All commands that use position values will assume song pointer units.</span></span> <span data-ttu-id="34704-476">Этот флаг допустим только для последовательности типа деления ППКН.</span><span class="sxs-lookup"><span data-stu-id="34704-476">This flag is valid only for a sequence of division type PPQN.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-477">формат времени тмсф</span><span class="sxs-lookup"><span data-stu-id="34704-477">time format tmsf</span></span></td>
<td><span data-ttu-id="34704-478">Задает формат времени для записей, минут, секунд и кадров.</span><span class="sxs-lookup"><span data-stu-id="34704-478">Sets the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="34704-479">Все команды, использующие значения позиций, будут считаться ТМСФ.</span><span class="sxs-lookup"><span data-stu-id="34704-479">All commands that use position values will assume TMSF.</span></span> <span data-ttu-id="34704-480">Укажите значение ТМСФ в формате TT: mm: SS: FF, где TT отслеживается, mm — минуты, SS — секунды, а FF — кадры.</span><span class="sxs-lookup"><span data-stu-id="34704-480">Specify a TMSF value as tt:mm:ss:ff, where tt is tracks, mm is minutes, ss is seconds, and ff is frames.</span></span> <span data-ttu-id="34704-481">Можно опустить поле, если оно и все следующие поля равны нулю.</span><span class="sxs-lookup"><span data-stu-id="34704-481">You can omit a field if it and all following fields are zero.</span></span> <span data-ttu-id="34704-482">Например, 3, 3:0, 3:0:0 и 3:0:0:0 являются допустимыми способами для выражения направления 3.</span><span class="sxs-lookup"><span data-stu-id="34704-482">For example, 3, 3:0, 3:0:0, and 3:0:0:0 are all valid ways to express track 3.</span></span> <br/> <span data-ttu-id="34704-483">Поля ТМСФ имеют следующие максимальные значения:</span><span class="sxs-lookup"><span data-stu-id="34704-483">The TMSF fields have the following maximum values:</span></span><br/>
<ul>
<li><span data-ttu-id="34704-484">Дорожки 99</span><span class="sxs-lookup"><span data-stu-id="34704-484">Tracks 99</span></span></li>
<li><span data-ttu-id="34704-485">Минуты 90</span><span class="sxs-lookup"><span data-stu-id="34704-485">Minutes 90</span></span></li>
<li><span data-ttu-id="34704-486">Секунды 59</span><span class="sxs-lookup"><span data-stu-id="34704-486">Seconds 59</span></span></li>
<li><span data-ttu-id="34704-487">Кадры 74</span><span class="sxs-lookup"><span data-stu-id="34704-487">Frames 74</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-488">формат времени</span><span class="sxs-lookup"><span data-stu-id="34704-488">time format track</span></span></td>
<td><span data-ttu-id="34704-489">Задает формат расположения для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="34704-489">Sets the position format to tracks.</span></span> <span data-ttu-id="34704-490">Все команды, использующие значения позиций, будут считаться дорожками.</span><span class="sxs-lookup"><span data-stu-id="34704-490">All commands that use position values will assume tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-491">Счетчик режима времени</span><span class="sxs-lookup"><span data-stu-id="34704-491">time mode counter</span></span></td>
<td><span data-ttu-id="34704-492">Задает режим сведений о положении для использования счетчиков ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="34704-492">Sets the position-information mode to use the VCR counters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-493">Обнаружение режима времени</span><span class="sxs-lookup"><span data-stu-id="34704-493">time mode detect</span></span></td>
<td><span data-ttu-id="34704-494">Задает режим сведений о положении на основе обнаружения на ленте сведений о времени.</span><span class="sxs-lookup"><span data-stu-id="34704-494">Sets the position information mode based on detection of timecode information on the tape.</span></span> <span data-ttu-id="34704-495">Если обнаружены сведения о периоде времени, то для типа Time устанавливается значение код периода &quot; &quot; ; в противном случае для типа времени устанавливается значение &quot; Счетчик &quot; .</span><span class="sxs-lookup"><span data-stu-id="34704-495">If timecode information is detected, the time type is set to &quot;timecode&quot;; otherwise, the time type is set to &quot;counter&quot;.</span></span> <span data-ttu-id="34704-496">&quot;Обнаружение &quot; является специальным режимом.</span><span class="sxs-lookup"><span data-stu-id="34704-496">&quot;Detect&quot; is a special mode.</span></span> <span data-ttu-id="34704-497">При открытии драйвера, вставке новой ленты или &quot; выполнении команды режима времени &quot; драйвер проверяет, доступен ли текущий режим времени на ленте, и устанавливает &quot; для типа времени значение Time &quot; &quot; &quot; или &quot; Counter &quot; .</span><span class="sxs-lookup"><span data-stu-id="34704-497">Whenever the driver is opened, a new tape is inserted, or the &quot;time mode&quot; command is issued, the driver checks the current time mode available on the tape and sets &quot;time type&quot; to either &quot;timecode&quot; or &quot;counter&quot;.</span></span> <span data-ttu-id="34704-498">После &quot; установки типа Time &quot; драйвер не изменяет его, пока не произойдет одно из указанных выше условий.</span><span class="sxs-lookup"><span data-stu-id="34704-498">Once &quot;time type&quot; is set, the driver doesn't change it until one of the above conditions occurs again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-499">временной код режима времени</span><span class="sxs-lookup"><span data-stu-id="34704-499">time mode timecode</span></span></td>
<td><span data-ttu-id="34704-500">Задает режим сведений о положении для использования &quot; &quot; на ленте сведений о времени.</span><span class="sxs-lookup"><span data-stu-id="34704-500">Sets the position information mode to use &quot;timecode&quot; information on the tape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-501">Отслеживание и</span><span class="sxs-lookup"><span data-stu-id="34704-501">tracking plus</span></span> <br/> <span data-ttu-id="34704-502">Отслеживание минус</span><span class="sxs-lookup"><span data-stu-id="34704-502">tracking minus</span></span> <br/> <span data-ttu-id="34704-503">Отслеживание сброса</span><span class="sxs-lookup"><span data-stu-id="34704-503">tracking reset</span></span> <br/></td>
<td><span data-ttu-id="34704-504">Регулирует скорость передачи видеокассеты с точно увеличивающимся шагом.</span><span class="sxs-lookup"><span data-stu-id="34704-504">Adjusts the speed of the videotape transport in fine increments.</span></span> <span data-ttu-id="34704-505">Используйте &quot; &quot; Флаги отслеживания при получении шума изображения из видеомагнитофона.</span><span class="sxs-lookup"><span data-stu-id="34704-505">Use the &quot;tracking&quot; flags when a noisy picture is obtained from a VCR.</span></span> <span data-ttu-id="34704-506">&quot;Отслеживание и &quot; увеличение скорости транспорта.</span><span class="sxs-lookup"><span data-stu-id="34704-506">&quot;Tracking plus&quot; increases the transport speed.</span></span> <span data-ttu-id="34704-507">&quot;Отслеживание минус &quot; снижает скорость транспортировки.</span><span class="sxs-lookup"><span data-stu-id="34704-507">&quot;Tracking minus&quot; decreases the transport speed.</span></span> <span data-ttu-id="34704-508">&quot;Отслеживание сброса &quot; возвращает корректировку отслеживания до нуля.</span><span class="sxs-lookup"><span data-stu-id="34704-508">&quot;Tracking reset&quot; returns the tracking adjustment to zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34704-509">видео отключено</span><span class="sxs-lookup"><span data-stu-id="34704-509">video off</span></span></td>
<td><span data-ttu-id="34704-510">Отключает вывод видео.</span><span class="sxs-lookup"><span data-stu-id="34704-510">Disables video output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34704-511">видео вкл.</span><span class="sxs-lookup"><span data-stu-id="34704-511">video on</span></span></td>
<td><span data-ttu-id="34704-512">Включает вывод видео.</span><span class="sxs-lookup"><span data-stu-id="34704-512">Enables video output.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="34704-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="34704-513"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="34704-514">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="34704-514">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="34704-515">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="34704-515">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="34704-516">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="34704-516">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34704-517">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34704-517">Return Value</span></span>

<span data-ttu-id="34704-518">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="34704-518">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="34704-519">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34704-519">Remarks</span></span>

<span data-ttu-id="34704-520">При создании файла для хранения данных определяются некоторые свойства аудио-данных с волнами.</span><span class="sxs-lookup"><span data-stu-id="34704-520">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="34704-521">Эти свойства описывают, как данные структурированы в файле и не могут быть изменены после начала записи.</span><span class="sxs-lookup"><span data-stu-id="34704-521">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="34704-522">Эти свойства определяются в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="34704-522">The following list identifies these properties:</span></span>

-   <span data-ttu-id="34704-523">выравнивание</span><span class="sxs-lookup"><span data-stu-id="34704-523">alignment</span></span>
-   <span data-ttu-id="34704-524">битсперсампле</span><span class="sxs-lookup"><span data-stu-id="34704-524">bitspersample</span></span>
-   <span data-ttu-id="34704-525">битесперсек</span><span class="sxs-lookup"><span data-stu-id="34704-525">bytespersec</span></span>
-   <span data-ttu-id="34704-526">каналов</span><span class="sxs-lookup"><span data-stu-id="34704-526">channels</span></span>
-   <span data-ttu-id="34704-527">Формат тега</span><span class="sxs-lookup"><span data-stu-id="34704-527">format tag</span></span>
-   <span data-ttu-id="34704-528">самплесперсек</span><span class="sxs-lookup"><span data-stu-id="34704-528">samplespersec</span></span>

## <a name="examples"></a><span data-ttu-id="34704-529">Примеры</span><span class="sxs-lookup"><span data-stu-id="34704-529">Examples</span></span>

<span data-ttu-id="34704-530">Следующая команда задает для формата времени значение миллисекунд и задает для формата звуковой волны значение 8 бит, моно, 11 кГц.</span><span class="sxs-lookup"><span data-stu-id="34704-530">The following command sets the time format to milliseconds and sets the waveform-audio format to 8 bit, mono, 11 kHz.</span></span>

``` syntax
set mysound time format ms bitspersample 8 channels 1 samplespersec 11025
```

## <a name="requirements"></a><span data-ttu-id="34704-531">Требования</span><span class="sxs-lookup"><span data-stu-id="34704-531">Requirements</span></span>



| <span data-ttu-id="34704-532">Требование</span><span class="sxs-lookup"><span data-stu-id="34704-532">Requirement</span></span> | <span data-ttu-id="34704-533">Значение</span><span class="sxs-lookup"><span data-stu-id="34704-533">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="34704-534">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34704-534">Minimum supported client</span></span><br/> | <span data-ttu-id="34704-535">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34704-535">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="34704-536">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34704-536">Minimum supported server</span></span><br/> | <span data-ttu-id="34704-537">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34704-537">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="34704-538">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34704-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34704-539">MCI</span><span class="sxs-lookup"><span data-stu-id="34704-539">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="34704-540">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="34704-540">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="34704-541">выделяем</span><span class="sxs-lookup"><span data-stu-id="34704-541">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="34704-542">pause</span><span class="sxs-lookup"><span data-stu-id="34704-542">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="34704-543">сохранить</span><span class="sxs-lookup"><span data-stu-id="34704-543">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="34704-544">stop</span><span class="sxs-lookup"><span data-stu-id="34704-544">stop</span></span>](stop.md)
</dt> </dl>

 

