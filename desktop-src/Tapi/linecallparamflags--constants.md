---
description: '\_Константы линекаллпарамфлагс описывают различные флаги состояния вызова.'
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: Константы LINECALLPARAMFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674896"
---
# <a name="linecallparamflags_-constants"></a><span data-ttu-id="35ab2-103">\_Константы линекаллпарамфлагс</span><span class="sxs-lookup"><span data-stu-id="35ab2-103">LINECALLPARAMFLAGS\_ Constants</span></span>

<span data-ttu-id="35ab2-104">Константы **линекаллпарамфлагс \_** описывают различные флаги состояния вызова.</span><span class="sxs-lookup"><span data-stu-id="35ab2-104">The **LINECALLPARAMFLAGS\_** constants describe various status flags about a call.</span></span>

<dl> <dt>

<span data-ttu-id="35ab2-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ ИД блока**</span><span class="sxs-lookup"><span data-stu-id="35ab2-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS\_BLOCKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35ab2-106">Удостоверение инициатора следует скрыть (блокировать вызывающий код).</span><span class="sxs-lookup"><span data-stu-id="35ab2-106">The originator identity should be concealed (block caller ID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35ab2-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ дестоффхук**</span><span class="sxs-lookup"><span data-stu-id="35ab2-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35ab2-108">Телефонный номер вызываемой стороны должен быть автоматически сделан оффхук.</span><span class="sxs-lookup"><span data-stu-id="35ab2-108">The called party's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35ab2-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ бездействие**</span><span class="sxs-lookup"><span data-stu-id="35ab2-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35ab2-110">Вызов должен быть создан на внешнем представлении вызова, но не присоединяться к выполняемому вызову.</span><span class="sxs-lookup"><span data-stu-id="35ab2-110">The call should be originated on an idle call appearance and not join a call in progress.</span></span> <span data-ttu-id="35ab2-111">Если при использовании функции [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) \_ значение неактивности линекаллпарамфлагс не задано и в строке уже существует вызов, функция переключается на существующий вызов, если это необходимо для создания нового вызова.</span><span class="sxs-lookup"><span data-stu-id="35ab2-111">When using the [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) function, if the LINECALLPARAMFLAGS\_IDLE value is not set and there is an existing call on the line, the function breaks into the existing call if necessary to make the new call.</span></span> <span data-ttu-id="35ab2-112">Если нет существующего вызова, функция создает новый вызов, как указано.</span><span class="sxs-lookup"><span data-stu-id="35ab2-112">If there is no existing call, the function makes the new call as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35ab2-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ нохолдконференце**</span><span class="sxs-lookup"><span data-stu-id="35ab2-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35ab2-114">Этот бит используется только совместно с [**линесетупконференце**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) и [**линепрепареаддтоконференце**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span><span class="sxs-lookup"><span data-stu-id="35ab2-114">This bit is used only in conjunction with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) and [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span></span> <span data-ttu-id="35ab2-115">Адрес для Конференции с текущим вызовом указывается в элементе **targetAddress** в [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span><span class="sxs-lookup"><span data-stu-id="35ab2-115">The address to be conferenced with the current call is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="35ab2-116">Вызов консультации не является физическим выдачей сигнала от коммутатора, но будет проходить по различным состояниям набора вызовов (например, по набору номера, по продолжению работы).</span><span class="sxs-lookup"><span data-stu-id="35ab2-116">The consultation call does not physically draw dial tone from the switch, but will progress through various call establishment states (for example, dialing, proceeding).</span></span> <span data-ttu-id="35ab2-117">Когда вызов консультации достигнет состояния Connected, Конференция устанавливается автоматически. Исходный вызов, который оставался в состоянии Connected (подключен), переходит в состояние conferenceed. вызов консультации переходит в состояние conferenceed (конференция). Хконфкалл переходит в состояние Connected.</span><span class="sxs-lookup"><span data-stu-id="35ab2-117">When the consultation call reaches the connected state, the conference is automatically established; the original call, which had remained in the connected state, enters the conferenced state; the consultation call enters the conferenced state; the hConfCall enters the connected state.</span></span> <span data-ttu-id="35ab2-118">Если вызов консультации завершается неудачей (переходит в состояние DISCONNECTED, а затем в режиме простоя), Хконфкалл также переходит в состояние простоя, а исходный вызов (который мог быть уже существующей конференции в случае **линепрепареаддтоконференце**) остается в подключенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="35ab2-118">If the consultation call fails (enters the disconnected state followed by idle), the hConfCall also enters the idle state, and the original call (which may have been an existing conference, in the case of **linePrepareAddToConference**) remains in the connected state.</span></span> <span data-ttu-id="35ab2-119">Исходная сторона (или стороны) никогда не воспринимает вызов.</span><span class="sxs-lookup"><span data-stu-id="35ab2-119">The original party (or parties) never perceive the call has having gone onhold.</span></span> <span data-ttu-id="35ab2-120">Эта функция часто используется для добавления супервизора в вызов ACD-агента, когда это необходимо для отслеживания взаимодействия с вызывающим объектом ирате.</span><span class="sxs-lookup"><span data-stu-id="35ab2-120">This feature is often used to add a supervisor to an ACD agent call when necessary to monitor interactions with an irate caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35ab2-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ онестептрансфер**</span><span class="sxs-lookup"><span data-stu-id="35ab2-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35ab2-122">Этот бит используется только совместно с [**линесетуптрансфер**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span><span class="sxs-lookup"><span data-stu-id="35ab2-122">This bit is used only in conjunction with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="35ab2-123">Он сочетает в себе операцию **линесетуптрансфер** , за которой следует [**линедиал**](/windows/desktop/api/Tapi/nf-tapi-linedial) на вызов консультации в один шаг.</span><span class="sxs-lookup"><span data-stu-id="35ab2-123">It combines the operation of **lineSetupTransfer** followed by [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) on the consultation call into a single step.</span></span> <span data-ttu-id="35ab2-124">Адрес, который необходимо набрать, указывается в элементе **targetAddress** в [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span><span class="sxs-lookup"><span data-stu-id="35ab2-124">The address to be dialed is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="35ab2-125">Исходный вызов помещается в состояние *онхолдпендингтрансфер* , как если бы **линесетуптрансфер** вызывался обычным образом, а вызов консультации устанавливается обычным образом.</span><span class="sxs-lookup"><span data-stu-id="35ab2-125">The original call is placed in *onholdpendingtransfer* state, just as if **lineSetupTransfer** were called normally, and the consultation call is established normally.</span></span> <span data-ttu-id="35ab2-126">Приложение по-прежнему должно вызывать [**линекомплететрансфер**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) , чтобы влиять на перемещение.</span><span class="sxs-lookup"><span data-stu-id="35ab2-126">The application must still call [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) to effect the transfer.</span></span> <span data-ttu-id="35ab2-127">Эта функция часто используется при вызове передачи с сервера по ссылке на управление вызовами стороннего производителя, так как такие ссылки часто не поддерживают стандартный двухэтапный процесс.</span><span class="sxs-lookup"><span data-stu-id="35ab2-127">This feature is often used when invoking a transfer from a server over a third-party call control link, because such links frequently do not support the normal two-step process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35ab2-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ оригоффхук**</span><span class="sxs-lookup"><span data-stu-id="35ab2-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35ab2-129">Телефон инициатора должен автоматически принимать оффхук.</span><span class="sxs-lookup"><span data-stu-id="35ab2-129">The originator's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35ab2-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ предиктиведиал**</span><span class="sxs-lookup"><span data-stu-id="35ab2-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS\_PREDICTIVEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35ab2-131">Этот бит используется только при помещении вызова на адрес с возможностью прогнозного набора (ЛИНЕАДДРКАПФЛАГС \_ предиктиведиалер включен в член **Дваддркапфлагс** в [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span><span class="sxs-lookup"><span data-stu-id="35ab2-131">This bit is used only when placing a call on an address with predictive dialing capability (LINEADDRCAPFLAGS\_PREDICTIVEDIALER is on in the **dwAddrCapFlags** member in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span></span> <span data-ttu-id="35ab2-132">Чтобы включить расширенный ход вызова и (или) возможности мониторинга устройства мультимедиа, бит должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="35ab2-132">The bit must be on to enable the enhanced call progress and/or media device monitoring capabilities of the device.</span></span> <span data-ttu-id="35ab2-133">Если этот бит не включен, вызов будет помещен без улучшенного хода выполнения вызова или наблюдения за типами мультимедиа, а автоматическое перемещение не будет инициировано на основе состояния вызова.</span><span class="sxs-lookup"><span data-stu-id="35ab2-133">If this bit is not on, the call will be placed without enhanced call progress or media type monitoring, and no automatic transfer will be initiated based on call state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="35ab2-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ безопасность**</span><span class="sxs-lookup"><span data-stu-id="35ab2-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="35ab2-135">Вызов должен быть настроен как безопасный.</span><span class="sxs-lookup"><span data-stu-id="35ab2-135">The call should be set up as secure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35ab2-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35ab2-136">Remarks</span></span>

<span data-ttu-id="35ab2-137">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="35ab2-137">No extensibility.</span></span> <span data-ttu-id="35ab2-138">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="35ab2-138">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ab2-139">Требования</span><span class="sxs-lookup"><span data-stu-id="35ab2-139">Requirements</span></span>



| <span data-ttu-id="35ab2-140">Требование</span><span class="sxs-lookup"><span data-stu-id="35ab2-140">Requirement</span></span> | <span data-ttu-id="35ab2-141">Значение</span><span class="sxs-lookup"><span data-stu-id="35ab2-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="35ab2-142">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="35ab2-142">TAPI version</span></span><br/> | <span data-ttu-id="35ab2-143">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="35ab2-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="35ab2-144">Header</span><span class="sxs-lookup"><span data-stu-id="35ab2-144">Header</span></span><br/>       | <dl> <span data-ttu-id="35ab2-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="35ab2-145"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ab2-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35ab2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ab2-147">**линеаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="35ab2-147">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="35ab2-148">**линекаллпарамс**</span><span class="sxs-lookup"><span data-stu-id="35ab2-148">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="35ab2-149">**линекомплететрансфер**</span><span class="sxs-lookup"><span data-stu-id="35ab2-149">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="35ab2-150">**линедиал**</span><span class="sxs-lookup"><span data-stu-id="35ab2-150">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="35ab2-151">**линемакекалл**</span><span class="sxs-lookup"><span data-stu-id="35ab2-151">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="35ab2-152">**линепрепареаддтоконференце**</span><span class="sxs-lookup"><span data-stu-id="35ab2-152">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="35ab2-153">**линесетупконференце**</span><span class="sxs-lookup"><span data-stu-id="35ab2-153">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="35ab2-154">**линесетуптрансфер**</span><span class="sxs-lookup"><span data-stu-id="35ab2-154">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




