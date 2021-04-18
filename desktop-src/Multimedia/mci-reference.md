---
title: Справочник по MCI
description: Справочник по MCI
ms.assetid: e7cedfc2-ce01-481c-a431-c93c97d45baf
keywords:
- Справочник по MCI, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cc54f69e714960d189567e759cf4b254275807
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105674669"
---
# <a name="mci-reference"></a><span data-ttu-id="f5e1a-104">Справочник по MCI</span><span class="sxs-lookup"><span data-stu-id="f5e1a-104">MCI Reference</span></span>

<span data-ttu-id="f5e1a-105">В этом разделе перечислены функции MCI, структуры, сообщения, макросы, команды и строки команд, которые описаны в разделе [мультимедиа Reference](multimedia-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f5e1a-105">This section lists the MCI functions, structures, messages, macros, commands, and command strings, which are documented under [Multimedia Reference](multimedia-reference.md).</span></span> <span data-ttu-id="f5e1a-106">Эти элементы группируются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="f5e1a-106">These elements are grouped as follows.</span></span>

## <a name="notifications"></a><span data-ttu-id="f5e1a-107">Уведомления</span><span class="sxs-lookup"><span data-stu-id="f5e1a-107">Notifications</span></span>

-   [<span data-ttu-id="f5e1a-108">**\_МЦИНОТИФИ мм**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-108">**MM\_MCINOTIFY**</span></span>](mm-mcinotify.md)
-   [<span data-ttu-id="f5e1a-109">**\_МЦИСИГНАЛ мм**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-109">**MM\_MCISIGNAL**</span></span>](mm-mcisignal.md)

## <a name="getting-information"></a><span data-ttu-id="f5e1a-110">Получение сведений</span><span class="sxs-lookup"><span data-stu-id="f5e1a-110">Getting Information</span></span>

-   <span data-ttu-id="f5e1a-111">[**мЦижеткреатортаск**](/previous-versions//dd757155(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-111">[**mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85))</span></span>
-   <span data-ttu-id="f5e1a-112">[**мЦижетдевицеид**](/previous-versions//dd757156(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-112">[**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85))</span></span>
-   <span data-ttu-id="f5e1a-113">[**мЦижетдевицеидфромелементид**](/previous-versions//dd757157(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-113">[**mciGetDeviceIDFromElementID**](/previous-versions//dd757157(v=vs.85))</span></span>
-   <span data-ttu-id="f5e1a-114">[**мЦижетеррорстринг**](/previous-versions//dd757158(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-114">[**mciGetErrorString**](/previous-versions//dd757158(v=vs.85))</span></span>

## <a name="sending-commands"></a><span data-ttu-id="f5e1a-115">Отправка команд</span><span class="sxs-lookup"><span data-stu-id="f5e1a-115">Sending Commands</span></span>

-   <span data-ttu-id="f5e1a-116">[**мЦиексекуте**](/previous-versions//dd757154(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-116">[**mciExecute**](/previous-versions//dd757154(v=vs.85))</span></span>
-   <span data-ttu-id="f5e1a-117">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-117">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
-   <span data-ttu-id="f5e1a-118">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-118">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span></span>

## <a name="time-formats"></a><span data-ttu-id="f5e1a-119">Форматы времени</span><span class="sxs-lookup"><span data-stu-id="f5e1a-119">Time Formats</span></span>

-   [<span data-ttu-id="f5e1a-120">**ХМс MCI, \_ \_ час**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-120">**MCI\_HMS\_HOUR**</span></span>](mci-hms-hour.md)
-   [<span data-ttu-id="f5e1a-121">**MCI \_ ХМс \_ минута**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-121">**MCI\_HMS\_MINUTE**</span></span>](mci-hms-minute.md)
-   [<span data-ttu-id="f5e1a-122">**ХМс MCI, \_ \_ секунда**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-122">**MCI\_HMS\_SECOND**</span></span>](mci-hms-second.md)
-   [<span data-ttu-id="f5e1a-123">**\_Создание \_ ХМСов MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-123">**MCI\_MAKE\_HMS**</span></span>](mci-make-hms.md)
-   [<span data-ttu-id="f5e1a-124">**\_платформа MCI делает \_ MSF**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-124">**MCI\_MAKE\_MSF**</span></span>](mci-make-msf.md)
-   [<span data-ttu-id="f5e1a-125">**\_Создание \_ ТМСФов MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-125">**MCI\_MAKE\_TMSF**</span></span>](mci-make-tmsf.md)
-   <span data-ttu-id="f5e1a-126">[**\_фрейм MSF для MCI \_**](/previous-versions//dd743438(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-126">[**MCI\_MSF\_FRAME**](/previous-versions//dd743438(v=vs.85))</span></span>
-   [<span data-ttu-id="f5e1a-127">**Платформа MCI, \_ \_ минута**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-127">**MCI\_MSF\_MINUTE**</span></span>](mci-msf-minute.md)
-   [<span data-ttu-id="f5e1a-128">**Платформа MCI, \_ \_ Вторая**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-128">**MCI\_MSF\_SECOND**</span></span>](mci-msf-second.md)
-   [<span data-ttu-id="f5e1a-129">**\_фрейм ТМСФ \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-129">**MCI\_TMSF\_FRAME**</span></span>](mci-tmsf-frame.md)
-   [<span data-ttu-id="f5e1a-130">**MCI \_ тмсф \_ минута**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-130">**MCI\_TMSF\_MINUTE**</span></span>](mci-tmsf-minute.md)
-   [<span data-ttu-id="f5e1a-131">**тмсф MCI, \_ \_ секунда**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-131">**MCI\_TMSF\_SECOND**</span></span>](mci-tmsf-second.md)
-   [<span data-ttu-id="f5e1a-132">**\_средство MCI тмсф \_ Track**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-132">**MCI\_TMSF\_TRACK**</span></span>](mci-tmsf-track.md)

## <a name="yield-procedures"></a><span data-ttu-id="f5e1a-133">Процедуры yield</span><span class="sxs-lookup"><span data-stu-id="f5e1a-133">Yield Procedures</span></span>

-   <span data-ttu-id="f5e1a-134">[**мЦижетиелдпрок**](/previous-versions//dd757159(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-134">[**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85))</span></span>
-   <span data-ttu-id="f5e1a-135">[**мЦисетиелдпрок**](/previous-versions//dd757163(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-135">[**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85))</span></span>

## <a name="configuring-a-device"></a><span data-ttu-id="f5e1a-136">Настройка устройства</span><span class="sxs-lookup"><span data-stu-id="f5e1a-136">Configuring a Device</span></span>

-   [<span data-ttu-id="f5e1a-137">**разбиени**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-137">**break**</span></span>](break.md)
-   [<span data-ttu-id="f5e1a-138">**выбрать**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-138">**configure**</span></span>](configure.md)
-   [<span data-ttu-id="f5e1a-139">выполняет</span><span class="sxs-lookup"><span data-stu-id="f5e1a-139">escape</span></span>](escape.md)
-   [<span data-ttu-id="f5e1a-140">**номер**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-140">**index**</span></span>](./windows-multimedia-start-page.md)
-   [<span data-ttu-id="f5e1a-141">**\_разрыв MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-141">**MCI\_BREAK**</span></span>](mci-break.md)
-   [<span data-ttu-id="f5e1a-142">**\_пармс прерываний MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-142">**MCI\_BREAK\_PARMS**</span></span>](mci-break-parms.md)
-   [<span data-ttu-id="f5e1a-143">**\_Настройка MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-143">**MCI\_CONFIGURE**</span></span>](mci-configure.md)
-   [<span data-ttu-id="f5e1a-144">**MCI \_ ДГВ \_ Set \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-144">**MCI\_DGV\_SET\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms)
-   [<span data-ttu-id="f5e1a-145">**MCI \_ ДГВ \_ сетаудио \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-145">**MCI\_DGV\_SETAUDIO\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa)
-   [<span data-ttu-id="f5e1a-146">**MCI \_ ДГВ \_ сетвидео \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-146">**MCI\_DGV\_SETVIDEO\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa)
-   [<span data-ttu-id="f5e1a-147">**\_escape-последовательность MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-147">**MCI\_ESCAPE**</span></span>](mci-escape.md)
-   [<span data-ttu-id="f5e1a-148">**\_указатель MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-148">**MCI\_INDEX**</span></span>](mci-index.md)
-   [<span data-ttu-id="f5e1a-149">**MCI \_ Seq \_ Set \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-149">**MCI\_SEQ\_SET\_PARMS**</span></span>](mci-seq-set-parms.md)
-   [<span data-ttu-id="f5e1a-150">**\_набор MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-150">**MCI\_SET**</span></span>](mci-set.md)
-   [<span data-ttu-id="f5e1a-151">**\_пармс набора \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-151">**MCI\_SET\_PARMS**</span></span>](mci-set-parms.md)
-   [<span data-ttu-id="f5e1a-152">**\_СЕТАУДИО MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-152">**MCI\_SETAUDIO**</span></span>](mci-setaudio.md)
-   [<span data-ttu-id="f5e1a-153">**\_СЕТТИМЕКОДЕ MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-153">**MCI\_SETTIMECODE**</span></span>](mci-settimecode.md)
-   [<span data-ttu-id="f5e1a-154">**\_СЕТТУНЕР MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-154">**MCI\_SETTUNER**</span></span>](mci-settuner.md)
-   [<span data-ttu-id="f5e1a-155">**\_СЕТВИДЕО MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-155">**MCI\_SETVIDEO**</span></span>](mci-setvideo.md)
-   [<span data-ttu-id="f5e1a-156">**\_Счетчик MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-156">**MCI\_SPIN**</span></span>](mci-spin.md)
-   [<span data-ttu-id="f5e1a-157">**\_пармс ВИДЕОМАГНИТОФОНА MCI \_ Set \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-157">**MCI\_VCR\_SET\_PARMS**</span></span>](mci-vcr-set-parms.md)
-   [<span data-ttu-id="f5e1a-158">**MCI \_ видеомагнитофон \_ сетаудио \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-158">**MCI\_VCR\_SETAUDIO\_PARMS**</span></span>](mci-vcr-setaudio-parms.md)
-   [<span data-ttu-id="f5e1a-159">**MCI \_ видеомагнитофон \_ сеттунер \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-159">**MCI\_VCR\_SETTUNER\_PARMS**</span></span>](mci-vcr-settuner-parms.md)
-   [<span data-ttu-id="f5e1a-160">**MCI \_ видеомагнитофон \_ сетвидео \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-160">**MCI\_VCR\_SETVIDEO\_PARMS**</span></span>](mci-vcr-setvideo-parms.md)
-   [<span data-ttu-id="f5e1a-161">**\_Escape- \_ \_ пармс MCI VD**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-161">**MCI\_VD\_ESCAPE\_PARMS**</span></span>](mci-vd-escape-parms.md)
-   [<span data-ttu-id="f5e1a-162">**\_пармс, \_ набор ЗВУКОзаписи MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-162">**MCI\_WAVE\_SET\_PARMS**</span></span>](mci-wave-set-parms.md)
-   [<span data-ttu-id="f5e1a-163">**параметр**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-163">**set**</span></span>](set.md)
-   [<span data-ttu-id="f5e1a-164">**сетаудио**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-164">**setaudio**</span></span>](setaudio.md)
-   [<span data-ttu-id="f5e1a-165">**сеттимекоде**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-165">**settimecode**</span></span>](settimecode.md)
-   [<span data-ttu-id="f5e1a-166">**сеттунер**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-166">**settuner**</span></span>](settuner.md)
-   [<span data-ttu-id="f5e1a-167">**сетвидео**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-167">**setvideo**</span></span>](setvideo.md)
-   [<span data-ttu-id="f5e1a-168">**оборот**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-168">**spin**</span></span>](spin.md)

## <a name="controlling-playback"></a><span data-ttu-id="f5e1a-169">Управление воспроизведением</span><span class="sxs-lookup"><span data-stu-id="f5e1a-169">Controlling Playback</span></span>

-   [<span data-ttu-id="f5e1a-170">**фиксировать**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-170">**freeze**</span></span>](freeze.md)
-   [<span data-ttu-id="f5e1a-171">**загрузить**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-171">**load**</span></span>](load.md)
-   [<span data-ttu-id="f5e1a-172">**MCI \_ ДГВ \_ заморозить \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-172">**MCI\_DGV\_FREEZE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms)
-   <span data-ttu-id="f5e1a-173">[**MCI \_ ДГВ \_ Load \_ пармс**](/previous-versions//dd743391(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-173">[**MCI\_DGV\_LOAD\_PARMS**](/previous-versions//dd743391(v=vs.85))</span></span>
-   <span data-ttu-id="f5e1a-174">[**MCI \_ ДГВ \_ приостановить \_ пармс**](/previous-versions//dd743395(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-174">[**MCI\_DGV\_PAUSE\_PARMS**](/previous-versions//dd743395(v=vs.85))</span></span>
-   <span data-ttu-id="f5e1a-175">[**MCI \_ ДГВ \_ Play \_ пармс**](/previous-versions//dd743396(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-175">[**MCI\_DGV\_PLAY\_PARMS**](/previous-versions//dd743396(v=vs.85))</span></span>
-   <span data-ttu-id="f5e1a-176">[**\_ДГВ \_ возобновления работы MCI \_ пармс**](/previous-versions//dd743403(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-176">[**MCI\_DGV\_RESUME\_PARMS**](/previous-versions//dd743403(v=vs.85))</span></span>
-   <span data-ttu-id="f5e1a-177">[**MCI \_ ДГВ \_ останавливает \_ пармс**](/previous-versions//dd743411(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-177">[**MCI\_DGV\_STOP\_PARMS**](/previous-versions//dd743411(v=vs.85))</span></span>
-   [<span data-ttu-id="f5e1a-178">**\_замораживание MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-178">**MCI\_FREEZE**</span></span>](mci-freeze.md)
-   [<span data-ttu-id="f5e1a-179">**\_Загрузка MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-179">**MCI\_LOAD**</span></span>](mci-load.md)
-   [<span data-ttu-id="f5e1a-180">**\_пармс загрузки \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-180">**MCI\_LOAD\_PARMS**</span></span>](mci-load-parms.md)
-   [<span data-ttu-id="f5e1a-181">**MCI \_ овли \_ Load \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-181">**MCI\_OVLY\_LOAD\_PARMS**</span></span>](mci-ovly-load-parms.md)
-   [<span data-ttu-id="f5e1a-182">**Приостановка MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-182">**MCI\_PAUSE**</span></span>](mci-pause.md)
-   [<span data-ttu-id="f5e1a-183">**\_Воспроизведение MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-183">**MCI\_PLAY**</span></span>](mci-play.md)
-   [<span data-ttu-id="f5e1a-184">**MCI \_ Play \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-184">**MCI\_PLAY\_PARMS**</span></span>](mci-play-parms.md)
-   [<span data-ttu-id="f5e1a-185">**\_возобновление работы MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-185">**MCI\_RESUME**</span></span>](mci-resume.md)
-   [<span data-ttu-id="f5e1a-186">**\_прерывание MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-186">**MCI\_STOP**</span></span>](mci-stop.md)
-   [<span data-ttu-id="f5e1a-187">**Отмена \_ замораживания MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-187">**MCI\_UNFREEZE**</span></span>](mci-unfreeze.md)
-   [<span data-ttu-id="f5e1a-188">**\_Воспроизведение видеомагнитофона MCI \_ \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-188">**MCI\_VCR\_PLAY\_PARMS**</span></span>](mci-vcr-play-parms.md)
-   [<span data-ttu-id="f5e1a-189">**MCI \_ VD \_ Play \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-189">**MCI\_VD\_PLAY\_PARMS**</span></span>](mci-vd-play-parms.md)
-   [<span data-ttu-id="f5e1a-190">**работу**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-190">**pause**</span></span>](pause.md)
-   [<span data-ttu-id="f5e1a-191">**воспроизводит**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-191">**play**</span></span>](play.md)
-   [<span data-ttu-id="f5e1a-192">**выход**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-192">**resume**</span></span>](resume.md)
-   [<span data-ttu-id="f5e1a-193">**позиции**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-193">**stop**</span></span>](stop.md)
-   [<span data-ttu-id="f5e1a-194">**освободить**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-194">**unfreeze**</span></span>](unfreeze.md)

## <a name="controlling-the-position"></a><span data-ttu-id="f5e1a-195">Управление положением</span><span class="sxs-lookup"><span data-stu-id="f5e1a-195">Controlling the Position</span></span>

-   [<span data-ttu-id="f5e1a-196">**cue**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-196">**cue**</span></span>](cue.md)
-   [<span data-ttu-id="f5e1a-197">**как**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-197">**mark**</span></span>](mark.md)
-   [<span data-ttu-id="f5e1a-198">**\_Подсказка MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-198">**MCI\_CUE**</span></span>](mci-cue.md)
-   [<span data-ttu-id="f5e1a-199">**MCI \_ ДГВ \_ Cue \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-199">**MCI\_DGV\_CUE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms)
-   [<span data-ttu-id="f5e1a-200">**\_ \_ ПАРМС сигнала MCI \_ ДГВ**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-200">**MCI\_DGV\_SIGNAL\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms)
-   [<span data-ttu-id="f5e1a-201">**\_пармс ДГВ на \_ шаге \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-201">**MCI\_DGV\_STEP\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms)
-   [<span data-ttu-id="f5e1a-202">**\_маркер MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-202">**MCI\_MARK**</span></span>](mci-mark.md)
-   [<span data-ttu-id="f5e1a-203">**\_Поиск MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-203">**MCI\_SEEK**</span></span>](mci-seek.md)
-   [<span data-ttu-id="f5e1a-204">**\_пармс поиска \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-204">**MCI\_SEEK\_PARMS**</span></span>](mci-seek-parms.md)
-   [<span data-ttu-id="f5e1a-205">**\_сигнал MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-205">**MCI\_SIGNAL**</span></span>](mci-signal.md)
-   [<span data-ttu-id="f5e1a-206">**\_шаг MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-206">**MCI\_STEP**</span></span>](mci-step.md)
-   [<span data-ttu-id="f5e1a-207">**\_Подсказка видеомагнитофона MCI \_ \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-207">**MCI\_VCR\_CUE\_PARMS**</span></span>](mci-vcr-cue-parms.md)
-   [<span data-ttu-id="f5e1a-208">**видеомагнитофон MCI, \_ \_ Поиск \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-208">**MCI\_VCR\_SEEK\_PARMS**</span></span>](mci-vcr-seek-parms.md)
-   [<span data-ttu-id="f5e1a-209">**\_пармс, \_ шаг видеомагнитофона MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-209">**MCI\_VCR\_STEP\_PARMS**</span></span>](mci-vcr-step-parms.md)
-   [<span data-ttu-id="f5e1a-210">**\_пармс VD на \_ шаге \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-210">**MCI\_VD\_STEP\_PARMS**</span></span>](mci-vd-step-parms.md)
-   [<span data-ttu-id="f5e1a-211">**поиска**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-211">**seek**</span></span>](seek.md)
-   [<span data-ttu-id="f5e1a-212">**имел**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-212">**signal**</span></span>](signal.md)
-   [<span data-ttu-id="f5e1a-213">**первом**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-213">**step**</span></span>](step.md)

## <a name="editing"></a><span data-ttu-id="f5e1a-214">Редактирование</span><span class="sxs-lookup"><span data-stu-id="f5e1a-214">Editing</span></span>

-   [<span data-ttu-id="f5e1a-215">**копии**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-215">**copy**</span></span>](copy.md)
-   [<span data-ttu-id="f5e1a-216">**бавьте**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-216">**cut**</span></span>](cut.md)
-   [<span data-ttu-id="f5e1a-217">**удален**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-217">**delete**</span></span>](delete.md)
-   [<span data-ttu-id="f5e1a-218">**\_копирование MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-218">**MCI\_COPY**</span></span>](mci-copy.md)
-   [<span data-ttu-id="f5e1a-219">**\_Вырезать MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-219">**MCI\_CUT**</span></span>](mci-cut.md)
-   [<span data-ttu-id="f5e1a-220">**\_Удаление MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-220">**MCI\_DELETE**</span></span>](mci-delete.md)
-   [<span data-ttu-id="f5e1a-221">**MCI \_ ДГВ \_ Copy \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-221">**MCI\_DGV\_COPY\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms)
-   [<span data-ttu-id="f5e1a-222">**\_ДГВ \_ вырезания MCI \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-222">**MCI\_DGV\_CUT\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms)
-   [<span data-ttu-id="f5e1a-223">**\_ \_ Удаление пармс MCI \_ ДГВ**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-223">**MCI\_DGV\_DELETE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms)
-   [<span data-ttu-id="f5e1a-224">**MCI \_ ДГВ \_ Вставить \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-224">**MCI\_DGV\_PASTE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms)
-   [<span data-ttu-id="f5e1a-225">**\_Вставка MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-225">**MCI\_PASTE**</span></span>](mci-paste.md)
-   [<span data-ttu-id="f5e1a-226">**\_Отмена MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-226">**MCI\_UNDO**</span></span>](mci-undo.md)
-   [<span data-ttu-id="f5e1a-227">**\_пармс для \_ удаления \_ волны MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-227">**MCI\_WAVE\_DELETE\_PARMS**</span></span>](mci-wave-delete-parms.md)
-   [<span data-ttu-id="f5e1a-228">**авить**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-228">**paste**</span></span>](paste.md)
-   [<span data-ttu-id="f5e1a-229">**отмен**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-229">**undo**</span></span>](undo.md)

## <a name="miscellaneous"></a><span data-ttu-id="f5e1a-230">Разное</span><span class="sxs-lookup"><span data-stu-id="f5e1a-230">Miscellaneous</span></span>

-   [<span data-ttu-id="f5e1a-231">**\_универсальный \_ пармс MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-231">**MCI\_GENERIC\_PARMS**</span></span>](mci-generic-parms.md)

## <a name="opening-and-closing"></a><span data-ttu-id="f5e1a-232">Открытие и закрытие</span><span class="sxs-lookup"><span data-stu-id="f5e1a-232">Opening and Closing</span></span>

-   [<span data-ttu-id="f5e1a-233">**выхода**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-233">**close**</span></span>](close.md)
-   [<span data-ttu-id="f5e1a-234">**\_закрытие MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-234">**MCI\_CLOSE**</span></span>](mci-close.md)
-   [<span data-ttu-id="f5e1a-235">**MCI \_ ДГВ \_ открыть \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-235">**MCI\_DGV\_OPEN\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa)
-   [<span data-ttu-id="f5e1a-236">**MCI \_ открыт**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-236">**MCI\_OPEN**</span></span>](mci-open.md)
-   [<span data-ttu-id="f5e1a-237">**MCI \_ Open \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-237">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
-   [<span data-ttu-id="f5e1a-238">**MCI \_ овли \_ открыть \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-238">**MCI\_OVLY\_OPEN\_PARMS**</span></span>](mci-ovly-open-parms.md)
-   [<span data-ttu-id="f5e1a-239">**Воспроизведение MCI, \_ \_ Открытие \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-239">**MCI\_WAVE\_OPEN\_PARMS**</span></span>](mci-wave-open-parms.md)
-   [<span data-ttu-id="f5e1a-240">**открыт**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-240">**open**</span></span>](open.md)

## <a name="realizing-a-palette"></a><span data-ttu-id="f5e1a-241">Реализация палитры</span><span class="sxs-lookup"><span data-stu-id="f5e1a-241">Realizing a Palette</span></span>

-   [<span data-ttu-id="f5e1a-242">**\_выясняется MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-242">**MCI\_REALIZE**</span></span>](mci-realize.md)
-   [<span data-ttu-id="f5e1a-243">**повысить**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-243">**realize**</span></span>](realize.md)

## <a name="repainting-a-frame"></a><span data-ttu-id="f5e1a-244">Перерисовка рамки</span><span class="sxs-lookup"><span data-stu-id="f5e1a-244">Repainting a Frame</span></span>

-   [<span data-ttu-id="f5e1a-245">**\_ПАРМС MCI ДГВ \_ обновления \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-245">**MCI\_DGV\_UPDATE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms)
-   [<span data-ttu-id="f5e1a-246">**\_Обновление MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-246">**MCI\_UPDATE**</span></span>](mci-update.md)
-   [<span data-ttu-id="f5e1a-247">**обновляют**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-247">**update**</span></span>](update.md)

## <a name="retrieving-information"></a><span data-ttu-id="f5e1a-248">Извлечение сведений</span><span class="sxs-lookup"><span data-stu-id="f5e1a-248">Retrieving Information</span></span>

-   [<span data-ttu-id="f5e1a-249">**возможностями**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-249">**capability**</span></span>](capability.md)
-   [<span data-ttu-id="f5e1a-250">**контактные**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-250">**info**</span></span>](info.md)
-   [<span data-ttu-id="f5e1a-251">**числ**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-251">**list**</span></span>](list.md)
-   [<span data-ttu-id="f5e1a-252">**\_пармс ДГВ \_ сведения о \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-252">**MCI\_DGV\_INFO\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa)
-   [<span data-ttu-id="f5e1a-253">**MCI \_ ДГВ \_ List \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-253">**MCI\_DGV\_LIST\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa)
-   [<span data-ttu-id="f5e1a-254">**\_ \_ ПАРМС состояния MCI \_ ДГВ**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-254">**MCI\_DGV\_STATUS\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa)
-   [<span data-ttu-id="f5e1a-255">**\_ЖЕТДЕВКАПС MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-255">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md)
-   [<span data-ttu-id="f5e1a-256">**\_ПАРМС MCI жетдевкапс \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-256">**MCI\_GETDEVCAPS\_PARMS**</span></span>](mci-getdevcaps-parms.md)
-   [<span data-ttu-id="f5e1a-257">**\_сведения о MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-257">**MCI\_INFO**</span></span>](mci-info.md)
-   [<span data-ttu-id="f5e1a-258">**\_пармс сведения о MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-258">**MCI\_INFO\_PARMS**</span></span>](mci-info-parms.md)
-   [<span data-ttu-id="f5e1a-259">**\_список MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-259">**MCI\_LIST**</span></span>](mci-list.md)
-   [<span data-ttu-id="f5e1a-260">**\_состояние MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-260">**MCI\_STATUS**</span></span>](mci-status.md)
-   [<span data-ttu-id="f5e1a-261">**\_пармс состояния \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-261">**MCI\_STATUS\_PARMS**</span></span>](mci-status-parms.md)
-   [<span data-ttu-id="f5e1a-262">**\_СИСИНФО MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-262">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)
-   [<span data-ttu-id="f5e1a-263">**\_ПАРМС MCI сисинфо \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-263">**MCI\_SYSINFO\_PARMS**</span></span>](mci-sysinfo-parms.md)
-   [<span data-ttu-id="f5e1a-264">**\_список видеомагнитофонов MCI \_ \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-264">**MCI\_VCR\_LIST\_PARMS**</span></span>](mci-vcr-list-parms.md)
-   [<span data-ttu-id="f5e1a-265">**\_состояние ВИДЕОМАГНИТОФОНА \_ MCI \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-265">**MCI\_VCR\_STATUS\_PARMS**</span></span>](mci-vcr-status-parms.md)
-   [<span data-ttu-id="f5e1a-266">**состояние**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-266">**status**</span></span>](status.md)
-   [<span data-ttu-id="f5e1a-267">сисинфо</span><span class="sxs-lookup"><span data-stu-id="f5e1a-267">sysinfo</span></span>](sysinfo.md)

## <a name="saving"></a><span data-ttu-id="f5e1a-268">Сохранение</span><span class="sxs-lookup"><span data-stu-id="f5e1a-268">Saving</span></span>

-   [<span data-ttu-id="f5e1a-269">**\_запись ДГВ \_ MCI \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-269">**MCI\_DGV\_RECORD\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms)
-   [<span data-ttu-id="f5e1a-270">**MCI \_ ДГВ \_ Сохранить \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-270">**MCI\_DGV\_SAVE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa)
-   <span data-ttu-id="f5e1a-271">[**MCI \_ овли \_ Сохранить \_ пармс**](/previous-versions//dd743447(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-271">[**MCI\_OVLY\_SAVE\_PARMS**](/previous-versions//dd743447(v=vs.85))</span></span>
-   [<span data-ttu-id="f5e1a-272">**\_запись MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-272">**MCI\_RECORD**</span></span>](mci-record.md)
-   [<span data-ttu-id="f5e1a-273">**\_пармс запись \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-273">**MCI\_RECORD\_PARMS**</span></span>](mci-record-parms.md)
-   [<span data-ttu-id="f5e1a-274">**\_Сохранение MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-274">**MCI\_SAVE**</span></span>](mci-save.md)
-   [<span data-ttu-id="f5e1a-275">**\_пармс сохранить в MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-275">**MCI\_SAVE\_PARMS**</span></span>](mci-save-parms.md)
-   [<span data-ttu-id="f5e1a-276">**\_ \_ пармс записи видеомагнитофона \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-276">**MCI\_VCR\_RECORD\_PARMS**</span></span>](mci-vcr-record-parms.md)
-   [<span data-ttu-id="f5e1a-277">**запись**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-277">**record**</span></span>](record.md)
-   [<span data-ttu-id="f5e1a-278">**автоматически**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-278">**save**</span></span>](save.md)

## <a name="video-control"></a><span data-ttu-id="f5e1a-279">Элемент управления видео</span><span class="sxs-lookup"><span data-stu-id="f5e1a-279">Video Control</span></span>

-   [<span data-ttu-id="f5e1a-280">**выделяем**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-280">**capture**</span></span>](capture.md)
-   [<span data-ttu-id="f5e1a-281">**\_захват MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-281">**MCI\_CAPTURE**</span></span>](mci-capture.md)
-   [<span data-ttu-id="f5e1a-282">**\_монитор ДГВ \_ MCI \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-282">**MCI\_DGV\_MONITOR\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms)
-   [<span data-ttu-id="f5e1a-283">**MCI \_ ДГВ \_ Quality \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-283">**MCI\_DGV\_QUALITY\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa)
-   [<span data-ttu-id="f5e1a-284">**\_пармс ДГВ \_ MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-284">**MCI\_DGV\_RESERVE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa)
-   [<span data-ttu-id="f5e1a-285">**\_ПАРМС MCI ДГВ \_ RESTORE \_**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-285">**MCI\_DGV\_RESTORE\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa)
-   [<span data-ttu-id="f5e1a-286">**\_монитор MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-286">**MCI\_MONITOR**</span></span>](mci-monitor.md)
-   [<span data-ttu-id="f5e1a-287">**\_качество MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-287">**MCI\_QUALITY**</span></span>](mci-quality.md)
-   [<span data-ttu-id="f5e1a-288">**\_резервирование MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-288">**MCI\_RESERVE**</span></span>](mci-reserve.md)
-   [<span data-ttu-id="f5e1a-289">**\_Восстановление MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-289">**MCI\_RESTORE**</span></span>](mci-restore.md)
-   [<span data-ttu-id="f5e1a-290">**слежен**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-290">**monitor**</span></span>](monitor.md)
-   [<span data-ttu-id="f5e1a-291">**повышения**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-291">**quality**</span></span>](quality.md)
-   [<span data-ttu-id="f5e1a-292">**предназначен**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-292">**reserve**</span></span>](reserve.md)
-   [<span data-ttu-id="f5e1a-293">**восстановление**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-293">**restore**</span></span>](restore.md)

## <a name="window-or-display-rectangles"></a><span data-ttu-id="f5e1a-294">Окна или экранные прямоугольники</span><span class="sxs-lookup"><span data-stu-id="f5e1a-294">Window or Display Rectangles</span></span>

-   <span data-ttu-id="f5e1a-295">[**MCI \_ ДГВ \_ Размещение \_ пармс**](/previous-versions//dd743397(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5e1a-295">[**MCI\_DGV\_PUT\_PARMS**](/previous-versions//dd743397(v=vs.85))</span></span>
-   [<span data-ttu-id="f5e1a-296">**MCI \_ ДГВ \_ Rect \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-296">**MCI\_DGV\_RECT\_PARMS**</span></span>](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms)
-   [<span data-ttu-id="f5e1a-297">**\_окно MCI \_ ДГВ \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-297">**MCI\_DGV\_WINDOW\_PARMS**</span></span>](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa)
-   [<span data-ttu-id="f5e1a-298">**MCI \_ овли \_ Rect \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-298">**MCI\_OVLY\_RECT\_PARMS**</span></span>](mci-ovly-rect-parms.md)
-   [<span data-ttu-id="f5e1a-299">**\_окно MCI \_ овли \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-299">**MCI\_OVLY\_WINDOW\_PARMS**</span></span>](mci-ovly-window-parms.md)
-   [<span data-ttu-id="f5e1a-300">**\_Добавление MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-300">**MCI\_PUT**</span></span>](mci-put.md)
-   [<span data-ttu-id="f5e1a-301">**MCI, \_ где**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-301">**MCI\_WHERE**</span></span>](mci-where.md)
-   [<span data-ttu-id="f5e1a-302">**\_окно MCI**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-302">**MCI\_WINDOW**</span></span>](mci-window.md)
-   [<span data-ttu-id="f5e1a-303">**PUT**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-303">**put**</span></span>](put.md)
-   [<span data-ttu-id="f5e1a-304">**которому**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-304">**where**</span></span>](where.md)
-   [<span data-ttu-id="f5e1a-305">**окно**</span><span class="sxs-lookup"><span data-stu-id="f5e1a-305">**window**</span></span>](window.md)

## <a name="related-topics"></a><span data-ttu-id="f5e1a-306">См. также</span><span class="sxs-lookup"><span data-stu-id="f5e1a-306">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5e1a-307">MCI</span><span class="sxs-lookup"><span data-stu-id="f5e1a-307">MCI</span></span>](mci.md)
</dt> </dl>

 

 