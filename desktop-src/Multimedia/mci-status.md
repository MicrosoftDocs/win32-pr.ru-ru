---
title: Команда MCI_STATUS (Ммсистем. h)
description: Команда " \_ состояние MCI" получает сведения о устройстве MCI. Все устройства распознают эту команду. Сведения возвращаются в элементе Двретурн структуры, определяемой параметром Лпстатус.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- MCI_STATUS команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "104350692"
---
# <a name="mci_status-command"></a><span data-ttu-id="45ec8-106">\_Команда состояния MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-106">MCI\_STATUS command</span></span>

> [!NOTE]
> <span data-ttu-id="45ec8-107">Обмен данными без смещения — Корпорация Майкрософт поддерживает различные и включенные среды.</span><span class="sxs-lookup"><span data-stu-id="45ec8-107">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="45ec8-108">В этом документе есть ссылки на слово "Slave".</span><span class="sxs-lookup"><span data-stu-id="45ec8-108">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="45ec8-109">В соответствии с руководством корпорации Майкрософт в [стиле Bias-Freeного обмена данными](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) это слово является исключаемым.</span><span class="sxs-lookup"><span data-stu-id="45ec8-109">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="45ec8-110">Это слово используется в том виде, в котором оно используется в командах.</span><span class="sxs-lookup"><span data-stu-id="45ec8-110">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="45ec8-111">Для обеспечения согласованности этот документ содержит это слово.</span><span class="sxs-lookup"><span data-stu-id="45ec8-111">For consistency, this document contains this word.</span></span> <span data-ttu-id="45ec8-112">При изменении этого слова в командах будет исправлен этот документ в выравнивании.</span><span class="sxs-lookup"><span data-stu-id="45ec8-112">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="45ec8-113">Команда " \_ состояние MCI" получает сведения о устройстве MCI.</span><span class="sxs-lookup"><span data-stu-id="45ec8-113">The MCI\_STATUS command retrieves information about an MCI device.</span></span> <span data-ttu-id="45ec8-114">Все устройства распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="45ec8-114">All devices recognize this command.</span></span> <span data-ttu-id="45ec8-115">Сведения возвращаются в элементе **двретурн** структуры, определяемой параметром *лпстатус* .</span><span class="sxs-lookup"><span data-stu-id="45ec8-115">Information is returned in the **dwReturn** member of the structure identified by the *lpStatus* parameter.</span></span>

<span data-ttu-id="45ec8-116">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="45ec8-116">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
);
```



## <a name="parameters"></a><span data-ttu-id="45ec8-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="45ec8-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45ec8-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="45ec8-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-119">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="45ec8-119">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="45ec8-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-121">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="45ec8-121">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="45ec8-122">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="45ec8-122">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*лпстатус*</span><span class="sxs-lookup"><span data-stu-id="45ec8-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-124">Указатель на структуру [**\_ \_ пармс состояния MCI**](mci-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-124">Pointer to an [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure.</span></span> <span data-ttu-id="45ec8-125">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="45ec8-125">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45ec8-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45ec8-126">Return Value</span></span>

<span data-ttu-id="45ec8-127">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="45ec8-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="45ec8-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45ec8-128">Remarks</span></span>

<span data-ttu-id="45ec8-129">Следующие дополнительные стандартные и специальные флаги применяются ко всем устройствам, поддерживающим \_ состояние MCI:</span><span class="sxs-lookup"><span data-stu-id="45ec8-129">The following additional standard and command-specific flags apply to all devices supporting MCI\_STATUS:</span></span>

<dl> <dt>

<span data-ttu-id="45ec8-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>\_элемент состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>MCI\_STATUS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-131">Указывает, что элемент **двитем** структуры, идентифицируемой *лпстатус* , содержит константу, указывающую, какой элемент состояния получить.</span><span class="sxs-lookup"><span data-stu-id="45ec8-131">Specifies that the **dwItem** member of the structure identified by *lpStatus* contains a constant specifying which status item to obtain.</span></span> <span data-ttu-id="45ec8-132">Следующие константы определяют, какой элемент Status должен возвращаться в элементе **двретурн** структуры:</span><span class="sxs-lookup"><span data-stu-id="45ec8-132">The following constants define which status item to return in the **dwReturn** member of the structure:</span></span>

<span data-ttu-id="45ec8-133">\_ \_ Текущая запись состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-133">MCI\_STATUS\_CURRENT\_TRACK</span></span>

<span data-ttu-id="45ec8-134">Для элемента **двретурн** задается номер текущей записи.</span><span class="sxs-lookup"><span data-stu-id="45ec8-134">The **dwReturn** member is set to the current track number.</span></span> <span data-ttu-id="45ec8-135">MCI использует номера непрерывной записи.</span><span class="sxs-lookup"><span data-stu-id="45ec8-135">MCI uses continuous track numbers.</span></span>

<span data-ttu-id="45ec8-136">\_Длина состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-136">MCI\_STATUS\_LENGTH</span></span>

<span data-ttu-id="45ec8-137">Для элемента **двретурн** задается Общая длина носителя.</span><span class="sxs-lookup"><span data-stu-id="45ec8-137">The **dwReturn** member is set to the total media length.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_режим состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-139">Элемент **двретурн** установлен в текущий режим устройства.</span><span class="sxs-lookup"><span data-stu-id="45ec8-139">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="45ec8-140">В число режимов входят следующие.</span><span class="sxs-lookup"><span data-stu-id="45ec8-140">The modes include the following:</span></span>

-   <span data-ttu-id="45ec8-141">\_режим MCI \_ не \_ готов</span><span class="sxs-lookup"><span data-stu-id="45ec8-141">MCI\_MODE\_NOT\_READY</span></span>
-   <span data-ttu-id="45ec8-142">\_приостановка режима MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-142">MCI\_MODE\_PAUSE</span></span>
-   <span data-ttu-id="45ec8-143">\_Воспроизведение в режиме MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-143">MCI\_MODE\_PLAY</span></span>
-   <span data-ttu-id="45ec8-144">\_Завершение режима \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-144">MCI\_MODE\_STOP</span></span>
-   <span data-ttu-id="45ec8-145">\_Открытие режима \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-145">MCI\_MODE\_OPEN</span></span>
-   <span data-ttu-id="45ec8-146">\_запись режима \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-146">MCI\_MODE\_RECORD</span></span>
-   <span data-ttu-id="45ec8-147">\_Поиск в режиме MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-147">MCI\_MODE\_SEEK</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>\_ \_ число \_ \_ ДОРОЖек в состоянии MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>MCI\_STATUS\_NUMBER\_OF\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-149">Для элемента **двретурн** задается общее число воссоздаваемых дорожек.</span><span class="sxs-lookup"><span data-stu-id="45ec8-149">The **dwReturn** member is set to the total number of playable tracks.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>\_Расположение состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>MCI\_STATUS\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-151">Элемент **двретурн** устанавливается в текущую точку.</span><span class="sxs-lookup"><span data-stu-id="45ec8-151">The **dwReturn** member is set to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>\_состояние MCI \_ Готово</span><span class="sxs-lookup"><span data-stu-id="45ec8-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>MCI\_STATUS\_READY</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-153">Элемент **двретурн** имеет значение **true** , если устройство готово. в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-153">The **dwReturn** member is set to **TRUE** if the device is ready; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>\_ \_ Формат времени состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>MCI\_STATUS\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-155">Для элемента **двретурн** задается текущий формат времени устройства.</span><span class="sxs-lookup"><span data-stu-id="45ec8-155">The **dwReturn** member is set to the current time format of the device.</span></span> <span data-ttu-id="45ec8-156">Форматы времени включают:</span><span class="sxs-lookup"><span data-stu-id="45ec8-156">The time formats include:</span></span>

-   <span data-ttu-id="45ec8-157">\_ \_ байты формата MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-157">MCI\_FORMAT\_BYTES</span></span>
-   <span data-ttu-id="45ec8-158">\_кадры формата \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-158">MCI\_FORMAT\_FRAMES</span></span>
-   <span data-ttu-id="45ec8-159">\_Формат MCI \_ ХМс</span><span class="sxs-lookup"><span data-stu-id="45ec8-159">MCI\_FORMAT\_HMS</span></span>
-   <span data-ttu-id="45ec8-160">\_ \_ миллисекунды формата MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-160">MCI\_FORMAT\_MILLISECONDS</span></span>
-   <span data-ttu-id="45ec8-161">формат MCI, \_ \_ MSF</span><span class="sxs-lookup"><span data-stu-id="45ec8-161">MCI\_FORMAT\_MSF</span></span>
-   <span data-ttu-id="45ec8-162">\_примеры формата \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-162">MCI\_FORMAT\_SAMPLES</span></span>
-   <span data-ttu-id="45ec8-163">\_Формат MCI \_ тмсф</span><span class="sxs-lookup"><span data-stu-id="45ec8-163">MCI\_FORMAT\_TMSF</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>\_Начало состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI\_STATUS\_START</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-165">Получает начальную точку носителя.</span><span class="sxs-lookup"><span data-stu-id="45ec8-165">Obtains the starting position of the media.</span></span> <span data-ttu-id="45ec8-166">Чтобы получить начальную позицию, объедините этот флаг с \_ элементом состояния MCI \_ и установите элемент **двитем** структуры, идентифицируемой *ЛПСТАТУС* , в \_ позицию состояния MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="45ec8-166">To get the starting position, combine this flag with MCI\_STATUS\_ITEM and set the **dwItem** member of the structure identified by *lpStatus* to MCI\_STATUS\_POSITION.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>\_направление MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-168">Указывает, что параметр Track состояния включен в элемент **двтракк** структуры, идентифицируемой *лпстатус*.</span><span class="sxs-lookup"><span data-stu-id="45ec8-168">Indicates a status track parameter is included in the **dwTrack** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="45ec8-169">Этот флаг следует использовать с константами состояния MCI или с презначением \_ \_ \_ длины состояния MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="45ec8-169">You must use this flag with the MCI\_STATUS\_POSITION or MCI\_STATUS\_LENGTH constants.</span></span> <span data-ttu-id="45ec8-170">При использовании с \_ позицией состояния MCI \_ Программа MCI \_ получает начальную точку указанной записи. При использовании с \_ длиной состояния MCI \_ Программа MCI \_ получает длину указанной записи. MCI использует номера непрерывной записи.</span><span class="sxs-lookup"><span data-stu-id="45ec8-170">When used with MCI\_STATUS\_POSITION, MCI\_TRACK obtains the starting position of the specified track. When used with MCI\_STATUS\_LENGTH, MCI\_TRACK obtains the length of the specified track. MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="45ec8-171">С типом устройства **кдаудио** используются следующие дополнительные флаги.</span><span class="sxs-lookup"><span data-stu-id="45ec8-171">The following additional flags are used with the **cdaudio** device type.</span></span> <span data-ttu-id="45ec8-172">Эти константы используются в элементе **двитем** структуры, на которую указывает параметр *лпстатус* , когда \_ \_ для параметра *dwFlags* указан элемент состояния MCI.</span><span class="sxs-lookup"><span data-stu-id="45ec8-172">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="45ec8-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>\_тип состояния CDA MCI — \_ \_ \_ Track</span><span class="sxs-lookup"><span data-stu-id="45ec8-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI\_CDA\_STATUS\_TYPE\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-174">Для элемента **двретурн** задается одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="45ec8-174">The **dwReturn** member is set to one of the following values:</span></span>

-   <span data-ttu-id="45ec8-175">MCI \_ CDA \_ дорожный \_ звук</span><span class="sxs-lookup"><span data-stu-id="45ec8-175">MCI\_CDA\_TRACK\_AUDIO</span></span>
-   <span data-ttu-id="45ec8-176">видеозапись MCI \_ CDA \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-176">MCI\_CDA\_TRACK\_OTHER</span></span>

<span data-ttu-id="45ec8-177">Чтобы использовать этот флаг, \_ необходимо установить флаг трассировки MCI, а элемент **двтракк** структуры, идентифицируемой *лпстатус* , должен содержать допустимый номер записи.</span><span class="sxs-lookup"><span data-stu-id="45ec8-177">To use this flag, the MCI\_TRACK flag must be set, and the **dwTrack** member of the structure identified by *lpStatus* must contain a valid track number.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_ \_ имеется носитель состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-179">Член **двретурн** имеет значение **true** , если носитель вставлен в устройство; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-179">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="45ec8-180">С типом устройства **дигиталвидео** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="45ec8-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="45ec8-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>\_ \_ места состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI\_DGV\_STATUS\_DISKSPACE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-182">Элемент **лпстрдриве** структуры, идентифицируемой *лпстатус* , указывает дисковый накопитель или, в некоторых реализациях, путь.</span><span class="sxs-lookup"><span data-stu-id="45ec8-182">The **lpstrDrive** member of the structure identified by *lpStatus* specifies a disk drive or, in some implementations, a path.</span></span> <span data-ttu-id="45ec8-183">Команда " \_ состояние MCI" возвращает приблизительный объем дискового пространства, который может быть получен командой [MCI \_ Reserve](mci-reserve.md) в элементе **двретурн** структуры, определенной параметром *лпстатус*.</span><span class="sxs-lookup"><span data-stu-id="45ec8-183">The MCI\_STATUS command returns the approximate amount of disk space that could be obtained by the [MCI\_RESERVE](mci-reserve.md) command in the **dwReturn** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="45ec8-184">Место на диске измеряется в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="45ec8-184">The disk space is measured in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>\_ \_ \_ входные данные состояния MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>MCI\_DGV\_STATUS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-186">Константа, заданная членом **двитем** структуры, идентифицируемой *лпстатус* , применяется к входным данным.</span><span class="sxs-lookup"><span data-stu-id="45ec8-186">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the input.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>\_состояние MCI \_ ДГВ \_ Left</span><span class="sxs-lookup"><span data-stu-id="45ec8-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>MCI\_DGV\_STATUS\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-188">Константа, определяемая элементом **двитем** структуры, определенной параметром *лпстатус* , применяется к левому каналу звука.</span><span class="sxs-lookup"><span data-stu-id="45ec8-188">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>\_состояние ДГВ \_ MCI \_ Номинальное</span><span class="sxs-lookup"><span data-stu-id="45ec8-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI\_DGV\_STATUS\_NOMINAL</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-190">Константа, определяемая элементом **двитем** структуры, определенной параметром *лпстатус* , запрашивает номинальное значение, а не текущее значение.</span><span class="sxs-lookup"><span data-stu-id="45ec8-190">The constant specified by the **dwItem** member of the structure identified by *lpStatus* requests the nominal value rather than the current value.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>\_ \_ выходные данные состояния MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>MCI\_DGV\_STATUS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-192">Константа, заданная членом **двитем** структуры, определенной параметром *лпстатус* , применяется к выходным данным.</span><span class="sxs-lookup"><span data-stu-id="45ec8-192">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the output.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>\_ \_ запись состояния ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI\_DGV\_STATUS\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-194">Частота кадров, возвращаемая для \_ \_ \_ флага частоты кадров состояния MCI ДГВ, — это \_ скорость, используемая для сжатия.</span><span class="sxs-lookup"><span data-stu-id="45ec8-194">The frame rate returned for the MCI\_DGV\_STATUS\_FRAME\_RATE flag is the rate used for compression.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>\_ \_ ссылка на состояние ДГВ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>MCI\_DGV\_STATUS\_REFERENCE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-196">Элемент **двретурн** структуры, идентифицируемой *лпстатус* , возвращает ближайший образ по ключевым кадрам, который предшествует кадру, указанному в элементе **двреференце** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-196">The **dwReturn** member of the structure identified by *lpStatus* returns the nearest key-frame image that precedes the frame specified in the **dwReference** member.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>\_состояние MCI \_ ДГВ \_ справа</span><span class="sxs-lookup"><span data-stu-id="45ec8-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI\_DGV\_STATUS\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-198">Константа, определяемая элементом **двитем** структуры, определенной параметром *лпстатус* , применяется к правильному звуковому каналу.</span><span class="sxs-lookup"><span data-stu-id="45ec8-198">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the right audio channel.</span></span>

</dd> </dl>

<span data-ttu-id="45ec8-199">Следующие константы используются с типом устройства **дигиталвидео** в элементе **двитем** структуры, на который указывает параметр *Лпстатус* , если \_ \_ для параметра *dwFlags* указан элемент состояния MCI.</span><span class="sxs-lookup"><span data-stu-id="45ec8-199">The following constants are used with the **digitalvideo** device type in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="45ec8-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>\_ \_ \_ звуковые переводы состояния MCI AVI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>MCI\_AVI\_STATUS\_AUDIO\_BREAKS</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-201">Элемент **двретурн** возвращает количество появлений звуковой части последней последовательности AVI.</span><span class="sxs-lookup"><span data-stu-id="45ec8-201">The **dwReturn** member returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="45ec8-202">Система подсчитывает разрыв звука при попытке записи звуковых данных в драйвер устройства и обнаруживает, что драйвер уже воспроизводил все доступные данные.</span><span class="sxs-lookup"><span data-stu-id="45ec8-202">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="45ec8-203">Этот флаг распознается только драйвером МЦИАВИ Digital-Video.</span><span class="sxs-lookup"><span data-stu-id="45ec8-203">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>\_ \_ \_ пропущенные кадры состояния MCI AVI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>MCI\_AVI\_STATUS\_FRAMES\_SKIPPED</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-205">Элемент **двретурн** возвращает число кадров, которые не были выведены при воспроизведении последней последовательности AVI.</span><span class="sxs-lookup"><span data-stu-id="45ec8-205">The **dwReturn** member returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="45ec8-206">Этот флаг распознается только драйвером МЦИАВИ Digital-Video.</span><span class="sxs-lookup"><span data-stu-id="45ec8-206">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>\_ \_ \_ \_ скорость последнего воспроизведения \_ для MCI AVI Status</span><span class="sxs-lookup"><span data-stu-id="45ec8-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI\_AVI\_STATUS\_LAST\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-208">Элемент **двретурн** возвращает значение, представляющее, насколько близко текущее время воспроизведения последней последовательности AVI соответствует целевому времени воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="45ec8-208">The **dwReturn** member returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="45ec8-209">Значение 1000 указывает на то, что целевое время и фактическое время одинаковы.</span><span class="sxs-lookup"><span data-stu-id="45ec8-209">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="45ec8-210">Значение 2000, например, указывает на то, что последовательность AVI заняла бы вдвое больше времени, чтобы играть, как нужно.</span><span class="sxs-lookup"><span data-stu-id="45ec8-210">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="45ec8-211">Этот флаг распознается только драйвером МЦИАВИ Digital-Video.</span><span class="sxs-lookup"><span data-stu-id="45ec8-211">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>\_ \_ звук состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI\_DGV\_STATUS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-213">Элемент **двретурн** возвращает MCI \_ или MCI в \_ зависимости от последнего \_ параметра MCI Set \_ Audio для команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-213">The **dwReturn** member returns MCI\_ON or MCI\_OFF depending on the most recent MCI\_SET\_AUDIO option for the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="45ec8-214">Он возвращает MCI \_ , если включен один или оба динамика, и \_ в противном случае — MCI.</span><span class="sxs-lookup"><span data-stu-id="45ec8-214">It returns MCI\_ON if either or both speakers are enabled, and MCI\_OFF otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>\_ \_ \_ \_ входные данные состояния MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI\_DGV\_STATUS\_AUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-216">Элемент **двретурн** Возвращает приблизительный моментальный звуковой сигнал аналогового звукового сигнала.</span><span class="sxs-lookup"><span data-stu-id="45ec8-216">The **dwReturn** member returns the approximate instantaneous audio level of the analog audio signal.</span></span> <span data-ttu-id="45ec8-217">Значение больше 1000 означает, что искажение обрезается.</span><span class="sxs-lookup"><span data-stu-id="45ec8-217">A value greater than 1000 implies there is clipping distortion.</span></span> <span data-ttu-id="45ec8-218">Некоторые устройства могут определить это значение только при записи звука.</span><span class="sxs-lookup"><span data-stu-id="45ec8-218">Some devices can determine this value only while recording audio.</span></span> <span data-ttu-id="45ec8-219">Это значение состояния не имеет связанного **\_ набора MCI** или [команды \_ MCI сетаудио](mci-setaudio.md) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-219">This status value has no associated **MCI\_SET** or [MCI\_SETAUDIO](mci-setaudio.md) command.</span></span> <span data-ttu-id="45ec8-220">Это значение связано с, но нормализовано от, в команде Wave-Audio на \_ уровне состояния звукового сигнала MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="45ec8-220">This value is related to, but normalized differently from, the waveform-audio command MCI\_WAVE\_STATUS\_LEVEL.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>\_ \_ \_ запись звука состояния ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI\_DGV\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-222">Элемент **двретурн** возвращает MCI \_ в или MCI, \_ отражая состояние, заданное \_ \_ флагом ДГВ Сетаудио записи MCI, \_ для команды **MCI \_ сетаудио** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-222">The **dwReturn** member returns MCI\_ON or MCI\_OFF reflecting the state set by the MCI\_DGV\_SETAUDIO\_RECORD flag of the **MCI\_SETAUDIO** command.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>\_ \_ \_ источник звука состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI\_DGV\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-224">Элемент **двретурн** возвращает текущий источник аудио дигитайзера:</span><span class="sxs-lookup"><span data-stu-id="45ec8-224">The **dwReturn** member returns the current audio digitizer source:</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>\_ \_ Среднее СЕТАУДИО ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI\_DGV\_SETAUDIO\_AVERAGE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-226">Указывает среднее значение левого и правого звукового канала.</span><span class="sxs-lookup"><span data-stu-id="45ec8-226">Specifies the average of the left and right audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>\_ДГВ MCI \_ сетаудио, \_ слева</span><span class="sxs-lookup"><span data-stu-id="45ec8-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-228">Указывает левый канал звука.</span><span class="sxs-lookup"><span data-stu-id="45ec8-228">Specifies the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ ДГВ \_ сетаудио \_ right</span><span class="sxs-lookup"><span data-stu-id="45ec8-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-230">Указывает правильный канал звука.</span><span class="sxs-lookup"><span data-stu-id="45ec8-230">Specifies the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ ДГВ \_ сетаудио \_ стерео</span><span class="sxs-lookup"><span data-stu-id="45ec8-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI\_DGV\_SETAUDIO\_STEREO</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-232">Указывает стерео.</span><span class="sxs-lookup"><span data-stu-id="45ec8-232">Specifies stereo.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>\_ \_ \_ поток звука состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI\_DGV\_STATUS\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-234">Элемент **двретурн** возвращает текущий номер звукового потока.</span><span class="sxs-lookup"><span data-stu-id="45ec8-234">The **dwReturn** member returns the current audio-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>\_ \_ АВГБИТЕСПЕРСЕК состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI\_DGV\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-236">Элемент **двретурн** Возвращает среднее число байтов, используемых для записи в секунду.</span><span class="sxs-lookup"><span data-stu-id="45ec8-236">The **dwReturn** member returns the average number of bytes per second used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>\_состояние MCI \_ ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI\_DGV\_STATUS\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-238">Элемент **двретурн** возвращает текущий уровень громкости звука.</span><span class="sxs-lookup"><span data-stu-id="45ec8-238">The **dwReturn** member returns the current audio bass level.</span></span> <span data-ttu-id="45ec8-239">\_ \_ \_ Чтобы получить номинальный уровень, используйте параметр MCI ДГВ Status номинальный с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-239">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>\_ \_ БИТСПЕРПЕЛ состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI\_DGV\_STATUS\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-241">Элемент **двретурн** возвращает число бит на пиксель, используемых для сохранения записанных или записанных данных.</span><span class="sxs-lookup"><span data-stu-id="45ec8-241">The **dwReturn** member returns the number of bits per pixel used for saving captured or recorded data.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>\_ \_ БИТСПЕРСАМПЛЕ состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI\_DGV\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-243">Элемент **двретурн** возвращает количество битов на выборку, используемую устройством для записи.</span><span class="sxs-lookup"><span data-stu-id="45ec8-243">The **dwReturn** member returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="45ec8-244">Это относится только к устройствам, поддерживающим формат PCM.</span><span class="sxs-lookup"><span data-stu-id="45ec8-244">This applies only to devices supporting the PCM format.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>\_ \_ БЛОККАЛИГН состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI\_DGV\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-246">Элемент **двретурн** возвращает выравнивание блоков данных относительно начала входной волны.</span><span class="sxs-lookup"><span data-stu-id="45ec8-246">The **dwReturn** member returns the alignment of data blocks relative to the start of the input waveform.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>\_ \_ яркость состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>MCI\_DGV\_STATUS\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-248">Элемент **двретурн** возвращает текущий уровень яркости видео.</span><span class="sxs-lookup"><span data-stu-id="45ec8-248">The **dwReturn** member returns the current video brightness level.</span></span> <span data-ttu-id="45ec8-249">\_ \_ \_ Чтобы получить номинальный уровень, используйте параметр MCI ДГВ Status номинальный с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-249">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>\_ \_ Цвет состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI\_DGV\_STATUS\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-251">Элемент **двретурн** возвращает текущий уровень цвета.</span><span class="sxs-lookup"><span data-stu-id="45ec8-251">The **dwReturn** member returns the current color level.</span></span> <span data-ttu-id="45ec8-252">\_ \_ \_ Чтобы получить номинальный уровень, используйте параметр MCI ДГВ Status номинальный с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-252">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>\_ \_ контраст состояния ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI\_DGV\_STATUS\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-254">Элемент **двретурн** возвращает текущий уровень контрастности.</span><span class="sxs-lookup"><span data-stu-id="45ec8-254">The **dwReturn** member returns the current contrast level.</span></span> <span data-ttu-id="45ec8-255">\_ \_ \_ Чтобы получить номинальный уровень, используйте параметр MCI ДГВ Status номинальный с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-255">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>\_ \_ FILEFORMAT состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI\_DGV\_STATUS\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-257">Элемент **двретурн** возвращает текущий формат файла для записи или сохранения.</span><span class="sxs-lookup"><span data-stu-id="45ec8-257">The **dwReturn** member returns the current file format for recording or saving.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>\_ \_ \_ режим файла состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI\_DGV\_STATUS\_FILE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-259">Элемент **двретурн** возвращает состояние операции с файлом:</span><span class="sxs-lookup"><span data-stu-id="45ec8-259">The **dwReturn** member returns the state of the file operation:</span></span>

<span data-ttu-id="45ec8-260">\_Редактирование в \_ \_ режиме файла MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-260">MCI\_DGV\_FILE\_MODE\_EDITING</span></span>

<span data-ttu-id="45ec8-261">Возвращается во время операций вырезания, копирования, удаления, вставки и отмены.</span><span class="sxs-lookup"><span data-stu-id="45ec8-261">Returned during cut, copy, delete, paste, and undo operations.</span></span>

<span data-ttu-id="45ec8-262">\_бездействие \_ в \_ режиме \_ файла MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-262">MCI\_DGV\_FILE\_MODE\_IDLE</span></span>

<span data-ttu-id="45ec8-263">Возвращается, когда файл готов к следующей операции.</span><span class="sxs-lookup"><span data-stu-id="45ec8-263">Returned when the file is ready for the next operation.</span></span>

<span data-ttu-id="45ec8-264">\_ \_ Загрузка файлового \_ режима MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-264">MCI\_DGV\_FILE\_MODE\_LOADING</span></span>

<span data-ttu-id="45ec8-265">Возвращается во время загрузки файла.</span><span class="sxs-lookup"><span data-stu-id="45ec8-265">Returned while the file is being loaded.</span></span>

<span data-ttu-id="45ec8-266">\_ \_ Сохранение файлового \_ режима MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-266">MCI\_DGV\_FILE\_MODE\_SAVING</span></span>

<span data-ttu-id="45ec8-267">Возвращается во время сохранения файла.</span><span class="sxs-lookup"><span data-stu-id="45ec8-267">Returned while the file is being saved.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>\_ \_ \_ завершение файла состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI\_DGV\_STATUS\_FILE\_COMPLETION</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-269">Элемент **двретурн** возвращает оценочный процент выполнения операции загрузки, сохранения, записи, вырезания, копирования, удаления, вставки или отмены.</span><span class="sxs-lookup"><span data-stu-id="45ec8-269">The **dwReturn** member returns the estimated percentage a load, save, capture, cut, copy, delete, paste, or undo operation has progressed.</span></span> <span data-ttu-id="45ec8-270">(Приложения могут использовать это для предоставления визуального индикатора хода выполнения.) Этот флаг не поддерживается всеми устройствами Digital-Video.</span><span class="sxs-lookup"><span data-stu-id="45ec8-270">(Applications can use this to provide a visual indicator of progress.) This flag is not supported by all digital-video devices.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>\_состояние MCI ДГВ " \_ \_ вперед"</span><span class="sxs-lookup"><span data-stu-id="45ec8-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI\_DGV\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-272">Член **двретурн** возвращает **значение true** , если направление устройства — вперед или устройство не воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="45ec8-272">The **dwReturn** member returns **TRUE** if the device direction is forward or the device is not playing.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>\_ \_ \_ Частота кадров состояния ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI\_DGV\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-274">Элемент **двретурн** должен использоваться со ДГВ MCI с \_ \_ \_ номинальным состоянием, \_ \_ запись состояния MCI ДГВ \_ или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="45ec8-274">The **dwReturn** member must be used with MCI\_DGV\_STATUS\_NOMINAL, MCI\_DGV\_STATUS\_RECORD, or both.</span></span> <span data-ttu-id="45ec8-275">При использовании \_ \_ записи состояния MCI ДГВ \_ возвращается текущая частота кадров, используемая для записи.</span><span class="sxs-lookup"><span data-stu-id="45ec8-275">When used with MCI\_DGV\_STATUS\_RECORD, the current frame rate used for recording is returned.</span></span> <span data-ttu-id="45ec8-276">При использовании с \_ \_ записью состояния MCI ДГВ \_ и \_ \_ номинальным состоянием MCI ДГВ \_ , возвращается Номинальная частота кадров, связанная с входным видеосигналом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-276">When used with both MCI\_DGV\_STATUS\_RECORD and MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the input video signal is returned.</span></span> <span data-ttu-id="45ec8-277">При использовании с \_ дгвой MCI с \_ \_ номинальным состоянием возвращается Номинальная частота кадров, связанная с файлом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-277">When used with MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the file is returned.</span></span> <span data-ttu-id="45ec8-278">Во всех случаях единицы находятся в кадрах в секунду, умноженные на 1000.</span><span class="sxs-lookup"><span data-stu-id="45ec8-278">In all cases the units are in frames per second multiplied by 1000.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>\_ \_ гамма состояния ДГВ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI\_DGV\_STATUS\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-280">Элемент **двретурн** возвращает текущее значение гаммы.</span><span class="sxs-lookup"><span data-stu-id="45ec8-280">The **dwReturn** member returns the current gamma value.</span></span> <span data-ttu-id="45ec8-281">\_ \_ \_ Чтобы получить номинальный уровень, используйте параметр MCI ДГВ Status номинальный с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-281">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>\_ \_ ХПАЛ состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI\_DGV\_STATUS\_HPAL</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-283">Элемент **двретурн** возвращает десятичное значение ASCII для текущего маркера палитры.</span><span class="sxs-lookup"><span data-stu-id="45ec8-283">The **dwReturn** member returns the ASCII decimal value for the current palette handle.</span></span> <span data-ttu-id="45ec8-284">Этот маркер содержится в слове с низким порядком возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="45ec8-284">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>\_ \_ HWND состояния ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI\_DGV\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-286">Элемент **двретурн** возвращает десятичное значение ASCII для текущего явного или стандартного маркера окна, связанного с этим экземпляром драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="45ec8-286">The **dwReturn** member returns the ASCII decimal value for the current explicit or default window handle associated with this device driver instance.</span></span> <span data-ttu-id="45ec8-287">Этот маркер содержится в слове с низким порядком возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="45ec8-287">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>\_ \_ \_ Цвет ключа состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI\_DGV\_STATUS\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-289">Элемент **двретурн** возвращает текущее значение ключевого цвета.</span><span class="sxs-lookup"><span data-stu-id="45ec8-289">The **dwReturn** member returns the current key-color value.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>\_ \_ \_ индекс ключа состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI\_DGV\_STATUS\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-291">Элемент **двретурн** возвращает текущее значение индекса ключа.</span><span class="sxs-lookup"><span data-stu-id="45ec8-291">The **dwReturn** member returns the current key-index value.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>\_ \_ Монитор состояния ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MCI\_DGV\_STATUS\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-293">Элемент **двретурн** возвращает константу, указывающую источник текущей презентации.</span><span class="sxs-lookup"><span data-stu-id="45ec8-293">The **dwReturn** member returns a constant indicating the source of the current presentation.</span></span> <span data-ttu-id="45ec8-294">Определены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="45ec8-294">The following constants are defined:</span></span>

<span data-ttu-id="45ec8-295">\_ \_ файл монитора MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-295">MCI\_DGV\_MONITOR\_FILE</span></span>

<span data-ttu-id="45ec8-296">Файл является источником.</span><span class="sxs-lookup"><span data-stu-id="45ec8-296">A file is the source.</span></span>

<span data-ttu-id="45ec8-297">\_ \_ \_ входные данные монитора MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-297">MCI\_DGV\_MONITOR\_INPUT</span></span>

<span data-ttu-id="45ec8-298">Входными данными является источник.</span><span class="sxs-lookup"><span data-stu-id="45ec8-298">The input is the source.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>\_ \_ \_ метод монитора состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI\_DGV\_STATUS\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-300">Элемент **двретурн** возвращает константу, указывающую метод, используемый для мониторинга ввода.</span><span class="sxs-lookup"><span data-stu-id="45ec8-300">The **dwReturn** member returns a constant indicating the method used for input monitoring.</span></span> <span data-ttu-id="45ec8-301">Определены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="45ec8-301">The following constants are defined:</span></span>

<span data-ttu-id="45ec8-302">\_прямой ДГВ \_ метод \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-302">MCI\_DGV\_METHOD\_DIRECT</span></span>

<span data-ttu-id="45ec8-303">Прямой мониторинг ввода.</span><span class="sxs-lookup"><span data-stu-id="45ec8-303">Direct input monitoring.</span></span>

<span data-ttu-id="45ec8-304">\_ \_ запись метода ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-304">MCI\_DGV\_METHOD\_POST</span></span>

<span data-ttu-id="45ec8-305">Мониторинг после ввода.</span><span class="sxs-lookup"><span data-stu-id="45ec8-305">Post-input monitoring.</span></span>

<span data-ttu-id="45ec8-306">\_метод ДГВ \_ MCI \_ предварительно</span><span class="sxs-lookup"><span data-stu-id="45ec8-306">MCI\_DGV\_METHOD\_PRE</span></span>

<span data-ttu-id="45ec8-307">Мониторинг перед входом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-307">Pre-input monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>\_ \_ \_ режим приостановки в состоянии ДГВ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI\_DGV\_STATUS\_PAUSE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-309">Элемент **двретурн** ВОЗВРАЩАЕТ режим MCI \_ \_ , если устройство было приостановлено во время воспроизведения, и возвращает \_ запись режима MCI, \_ Если устройство было приостановлено во время записи.</span><span class="sxs-lookup"><span data-stu-id="45ec8-309">The **dwReturn** member returns MCI\_MODE\_PLAY if the device was paused while playing and returns MCI\_MODE\_RECORD if the device was paused while recording.</span></span> <span data-ttu-id="45ec8-310">Команда возвращает МЦИЕРР \_ НЕприменимую \_ функцию как ошибку, если устройство не приостановлено.</span><span class="sxs-lookup"><span data-stu-id="45ec8-310">The command returns MCIERR\_NONAPPLICABLE\_FUNCTION as an error return if the device is not paused.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>\_ \_ САМПЛЕСПЕРСЕКОНД состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI\_DGV\_STATUS\_SAMPLESPERSECOND</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-312">Элемент **двретурн** возвращает число записанных выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="45ec8-312">The **dwReturn** member returns the number of samples per second recorded.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>\_Поиск состояния MCI ДГВ в \_ \_ \_ точности</span><span class="sxs-lookup"><span data-stu-id="45ec8-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI\_DGV\_STATUS\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-314">Элемент **двретурн** возвращает **значение true** или **false** , указывающее, задан ли точный формат поиска.</span><span class="sxs-lookup"><span data-stu-id="45ec8-314">The **dwReturn** member returns **TRUE** or **FALSE** indicating whether or not the seek exactly format is set.</span></span> <span data-ttu-id="45ec8-315">(Приложения могут задать этот формат с помощью команды [MCI \_ Set](mci-set.md) с \_ флагом MCI ДГВ \_ Set \_ Seek \_ .)</span><span class="sxs-lookup"><span data-stu-id="45ec8-315">(Applications can set this format by using the [MCI\_SET](mci-set.md) command with the MCI\_DGV\_SET\_SEEK\_EXACTLY flag.)</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>\_ \_ резкость состояния ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI\_DGV\_STATUS\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-317">Элемент **двретурн** возвращает текущий уровень резкости.</span><span class="sxs-lookup"><span data-stu-id="45ec8-317">The **dwReturn** member returns the current sharpness level.</span></span> <span data-ttu-id="45ec8-318">\_ \_ \_ Чтобы получить номинальный уровень, используйте параметр MCI ДГВ Status номинальный с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-318">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>\_ \_ размер состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI\_DGV\_STATUS\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-320">Элемент **двретурн** Возвращает приблизительную продолжительность воспроизведения сжатых данных, которые будут храниться в зарезервированной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="45ec8-320">The **dwReturn** member returns the approximate playback duration of compressed data that the reserved workspace will hold.</span></span> <span data-ttu-id="45ec8-321">Единицы длительности находятся в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="45ec8-321">The duration units are in the current time format.</span></span> <span data-ttu-id="45ec8-322">При отсутствии зарезервированного места на диске он возвращает нуль.</span><span class="sxs-lookup"><span data-stu-id="45ec8-322">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="45ec8-323">Возвращаемый размер приблизительный, так как точное место на диске для сжатых данных не может быть прогнозным до тех пор, пока данные не будут сжаты.</span><span class="sxs-lookup"><span data-stu-id="45ec8-323">The size returned is approximate since the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>\_ \_ SMPTE состояния MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="45ec8-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI\_DGV\_STATUS\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-325">Элемент **двретурн** возвращает код времени SMPTE, связанный с текущей позицией в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="45ec8-325">The **dwReturn** member returns the SMPTE time code associated with the current position in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>\_ \_ скорость состояния ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI\_DGV\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-327">Элемент **двретурн** возвращает текущую скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="45ec8-327">The **dwReturn** member returns the current playback speed.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>\_состояние ДГВ \_ MCI \_ по-прежнему \_ FILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="45ec8-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI\_DGV\_STATUS\_STILL\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-329">Элемент **двретурн** возвращает текущий формат файла для команды [ \_ захвата MCI](mci-capture.md) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-329">The **dwReturn** member returns the current file format for the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>\_оттенок \_ состояния ДГВ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI\_DGV\_STATUS\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-331">Элемент **двретурн** возвращает текущий уровень оттенка видео.</span><span class="sxs-lookup"><span data-stu-id="45ec8-331">The **dwReturn** member returns the current video tint level.</span></span> <span data-ttu-id="45ec8-332">\_ \_ \_ Чтобы получить номинальный уровень, используйте параметр MCI ДГВ Status номинальный с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-332">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>\_ \_ состояние высоких ДГВ \_ для MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI\_DGV\_STATUS\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-334">Элемент **двретурн** возвращает текущий уровень громкости звука.</span><span class="sxs-lookup"><span data-stu-id="45ec8-334">The **dwReturn** member returns the current audio treble level.</span></span> <span data-ttu-id="45ec8-335">\_ \_ \_ Чтобы получить номинальный уровень, используйте параметр MCI ДГВ Status номинальный с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-335">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>\_ \_ несохраненное состояние MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>MCI\_DGV\_STATUS\_UNSAVED</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-337">Член **двретурн** возвращает **значение true** , если в рабочей области записаны данные, которые могут быть потеряны в результате [ \_ закрытия MCI](mci-close.md), [ \_ загрузки MCI](mci-load.md), [ \_ записи MCI](mci-record.md), [ \_ зарезервированного](mci-reserve.md)MCI, [MCI \_ Вырезать](mci-cut.md), [MCI \_ Delete](mci-delete.md)или команды [MCI \_ Paste](mci-paste.md) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-337">The **dwReturn** member returns **TRUE** if there is recorded data in the workspace that might be lost as a result of a [MCI\_CLOSE](mci-close.md), [MCI\_LOAD](mci-load.md), [MCI\_RECORD](mci-record.md), [MCI\_RESERVE](mci-reserve.md), [MCI\_CUT](mci-cut.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="45ec8-338">В противном случае член возвращает **значение false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-338">The member returns **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>\_ \_ видео о состоянии ДГВ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>MCI\_DGV\_STATUS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-340">Элемент **двретурн** возвращает MCI \_ , если видео включено, или MCI отключен \_ .</span><span class="sxs-lookup"><span data-stu-id="45ec8-340">The **dwReturn** member returns MCI\_ON if video is enabled or MCI\_OFF if it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>\_ \_ запись видео о состоянии ДГВ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>MCI\_DGV\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-342">Элемент **двретурн** возвращает MCI \_ в или с \_ отключением MCI, отражая состояние, заданное \_ \_ флагом ДГВ сетвидео записи MCI в \_ команде [MCI \_ сетвидео](mci-setvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-342">The **dwReturn** member returns MCI\_ON or MCI\_OFF, reflecting the state set by the MCI\_DGV\_SETVIDEO\_RECORD flag of the [MCI\_SETVIDEO](mci-setvideo.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>\_ \_ источник видео о состоянии ДГВ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI\_DGV\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-344">Элемент **двретурн** возвращает константу, указывающую тип источника видео, заданный \_ \_ флагом MCI ДГВ Сетвидео \_ Source в команде **MCI \_ сетвидео** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-344">The **dwReturn** member returns a constant indicating the type of video source set by the MCI\_DGV\_SETVIDEO\_SOURCE flag of the **MCI\_SETVIDEO** command.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>\_ \_ \_ \_ номер src видео о состоянии ДГВ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI\_DGV\_STATUS\_VIDEO\_SRC\_NUM</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-346">Элемент **двретурн** возвращает число в своем типе исходного входного видео.</span><span class="sxs-lookup"><span data-stu-id="45ec8-346">The **dwReturn** member returns the number within its type of the video-input source currently active.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>\_ \_ поток видео о состоянии ДГВ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI\_DGV\_STATUS\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-348">Элемент **двретурн** возвращает текущий номер видео-потока.</span><span class="sxs-lookup"><span data-stu-id="45ec8-348">The **dwReturn** member returns the current video-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>\_ \_ Громкость состояния MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI\_DGV\_STATUS\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-350">Элемент **двретурн** Возвращает среднее значение тома для левого и правого докладчика.</span><span class="sxs-lookup"><span data-stu-id="45ec8-350">The **dwReturn** member returns the average of the volume to the left and right speakers.</span></span> <span data-ttu-id="45ec8-351">\_ \_ \_ Чтобы получить номинальный уровень, используйте параметр MCI ДГВ Status номинальный с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="45ec8-351">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>\_ \_ \_ видимое окно состояния ДГВ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>MCI\_DGV\_STATUS\_WINDOW\_VISIBLE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-353">Элемент **двретурн** возвращает **значение true** , если окно не скрыто.</span><span class="sxs-lookup"><span data-stu-id="45ec8-353">The **dwReturn** member returns **TRUE** if the window is not hidden.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>\_окно состояния ДГВ MCI в \_ \_ \_ уменьшенном состоянии</span><span class="sxs-lookup"><span data-stu-id="45ec8-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>MCI\_DGV\_STATUS\_WINDOW\_MINIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-355">Элемент **двретурн** возвращает **значение true** , если окно является сведенным.</span><span class="sxs-lookup"><span data-stu-id="45ec8-355">The **dwReturn** member returns **TRUE** if the window is minimized.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>\_ \_ \_ развернутое окно \_ состояния ДГВ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>MCI\_DGV\_STATUS\_WINDOW\_MAXIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-357">Элемент **двретурн** возвращает **значение true** , если окно развернуто.</span><span class="sxs-lookup"><span data-stu-id="45ec8-357">The **dwReturn** member returns **TRUE** if the window is maximized.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_ \_ имеется носитель состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-359">Элемент **двретурн** возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="45ec8-359">The **dwReturn** member returns **TRUE**.</span></span>

</dd> </dl>

<span data-ttu-id="45ec8-360">Для устройств с цифровыми видео параметр *лпстатус* указывает на структуру [**ДГВ MCI с \_ \_ состоянием \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-360">For digital-video devices, the *lpStatus* parameter points to an [**MCI\_DGV\_STATUS\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) structure.</span></span>

<span data-ttu-id="45ec8-361">Для типа устройства **Sequencer** используются следующие дополнительные флаги.</span><span class="sxs-lookup"><span data-stu-id="45ec8-361">The following additional flags are used with the **sequencer** device type.</span></span> <span data-ttu-id="45ec8-362">Эти константы используются в элементе **двитем** структуры, на которую указывает параметр *лпстатус* , когда \_ \_ для параметра *dwFlags* указан элемент состояния MCI.</span><span class="sxs-lookup"><span data-stu-id="45ec8-362">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="45ec8-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI \_ Seq \_ Status \_ дивтипе</span><span class="sxs-lookup"><span data-stu-id="45ec8-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI\_SEQ\_STATUS\_DIVTYPE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-364">Для элемента **двретурн** задается одно из следующих значений, указывающее текущий тип деления для последовательности:</span><span class="sxs-lookup"><span data-stu-id="45ec8-364">The **dwReturn** member is set to one of the following values indicating the current division type of a sequence:</span></span>

-   <span data-ttu-id="45ec8-365">MCI \_ Seq \_ div \_ ппкн</span><span class="sxs-lookup"><span data-stu-id="45ec8-365">MCI\_SEQ\_DIV\_PPQN</span></span>
-   <span data-ttu-id="45ec8-366">MCI \_ Seq \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="45ec8-366">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>
-   <span data-ttu-id="45ec8-367">MCI \_ Seq \_ div \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="45ec8-367">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>
-   <span data-ttu-id="45ec8-368">MCI \_ Seq \_ div \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="45ec8-368">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>
-   <span data-ttu-id="45ec8-369">MCI \_ Seq \_ div \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="45ec8-369">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>\_ \_ образец состояния MCI \_ Seq</span><span class="sxs-lookup"><span data-stu-id="45ec8-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI\_SEQ\_STATUS\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-371">Для элемента **двретурн** задан тип синхронизации, используемый для главной операции.</span><span class="sxs-lookup"><span data-stu-id="45ec8-371">The **dwReturn** member is set to the synchronization type used for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>\_ \_ смещение состояния MCI \_ Seq</span><span class="sxs-lookup"><span data-stu-id="45ec8-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>MCI\_SEQ\_STATUS\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-373">Для элемента **двретурн** задано текущее смещение SMPTE последовательности.</span><span class="sxs-lookup"><span data-stu-id="45ec8-373">The **dwReturn** member is set to the current SMPTE offset of a sequence.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>\_ \_ порт состояния MCI \_ Seq</span><span class="sxs-lookup"><span data-stu-id="45ec8-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI\_SEQ\_STATUS\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-375">Для элемента **двретурн** задается идентификатор устройства MIDI для текущего порта, используемого в последовательности.</span><span class="sxs-lookup"><span data-stu-id="45ec8-375">The **dwReturn** member is set to the MIDI device identifier for the current port used by the sequence.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>\_ \_ ведомая состояние MCI Seq \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI\_SEQ\_STATUS\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-377">Для элемента **двретурн** задан тип синхронизации, используемый для подчиненной операции.</span><span class="sxs-lookup"><span data-stu-id="45ec8-377">The **dwReturn** member is set to the synchronization type used for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI \_ Seq \_ Status \_ темп</span><span class="sxs-lookup"><span data-stu-id="45ec8-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI\_SEQ\_STATUS\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-379">Элемент **двретурн** устанавливается равным текущему темпу последовательности MIDI в число файлов ппкн или кадров в секунду для SMPTE файлов.</span><span class="sxs-lookup"><span data-stu-id="45ec8-379">The **dwReturn** member is set to the current tempo of a MIDI sequence in beats per minute for PPQN files, or frames per second for SMPTE files.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_ \_ имеется носитель состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-381">Член **двретурн** имеет значение **true** , если носитель вставлен в устройство; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-381">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="45ec8-382">Для типа устройства **видеомагнитофона** используются следующие дополнительные флаги.</span><span class="sxs-lookup"><span data-stu-id="45ec8-382">The following additional flags are used with the **vcr** device type.</span></span> <span data-ttu-id="45ec8-383">Эти константы используются в элементе **двитем** структуры, на которую указывает параметр *лпстатус* , когда \_ \_ для параметра *dwFlags* указан элемент состояния MCI.</span><span class="sxs-lookup"><span data-stu-id="45ec8-383">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="45ec8-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_ \_ имеется носитель состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-385">Член **двретурн** имеет значение **true** , если носитель вставлен в устройство; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-385">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>\_ \_ запись состояния видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI\_VCR\_STATUS\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-387">Элемент **двретурн** имеет значение **true** , если включен режим сборки. в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-387">The **dwReturn** member is set to **TRUE** if assemble mode is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>\_ \_ \_ звуковой \_ Монитор состояния видеомагнитофона MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-389">Для элемента **двретурн** задается константа, указывающая на выбранный в данный момент тип звукового монитора.</span><span class="sxs-lookup"><span data-stu-id="45ec8-389">The **dwReturn** member is set to a constant, indicating the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>\_ \_ \_ номер звукового \_ монитора состояния видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-391">Для элемента **двретурн** задается номер выбранного в данный момент типа звукового монитора.</span><span class="sxs-lookup"><span data-stu-id="45ec8-391">The **dwReturn** member is set to the number of the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>\_ \_ \_ звуковая запись состояния видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI\_VCR\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-393">Элемент **двретурн** имеет значение **true** , если звук будет записан при указании команды следующей записи. в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-393">The **dwReturn** member is set to **TRUE** if audio will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="45ec8-394">Если \_ в параметре *dwFlags* этой команды указать Track MCI, **двтракк** содержит запись, к которой относится этот запрос.</span><span class="sxs-lookup"><span data-stu-id="45ec8-394">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>\_ \_ \_ источник аудио состояния ВИДЕОмагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-396">Для элемента **двретурн** задается константа, указывающая текущий тип звукового источника.</span><span class="sxs-lookup"><span data-stu-id="45ec8-396">The **dwReturn** member is set to a constant, indicating the current audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>\_ \_ \_ номер источника ЗВУКового \_ видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-398">Для элемента **двретурн** задается номер выбранного в данный момент типа звукового источника.</span><span class="sxs-lookup"><span data-stu-id="45ec8-398">The **dwReturn** member is set to the number of the currently selected audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>\_ \_ часы состояния видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI\_VCR\_STATUS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-400">Для элемента **двретурн** задается текущее значение часов, в общем приращении часов.</span><span class="sxs-lookup"><span data-stu-id="45ec8-400">The **dwReturn** member is set to the current clock value, in total clock increments.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>\_ \_ \_ код часового состояния видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI\_VCR\_STATUS\_CLOCK\_ID</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-402">Для элемента **двретурн** задается число, которое однозначно описывает используемые часы.</span><span class="sxs-lookup"><span data-stu-id="45ec8-402">The **dwReturn** member is set to a number which uniquely describes the clock in use.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>\_ \_ \_ Формат счетчика состояния видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI\_VCR\_STATUS\_COUNTER\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-404">Для элемента **двретурн** задается константа, описывающая текущий формат счетчика.</span><span class="sxs-lookup"><span data-stu-id="45ec8-404">The **dwReturn** member is set to a constant describing the current counter format.</span></span> <span data-ttu-id="45ec8-405">Дополнительные сведения см. в разделе \_ Установка \_ \_ флага формата времени MCI для команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-405">For more information, see the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>\_ \_ \_ разрешение счетчика состояния видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>MCI\_VCR\_STATUS\_COUNTER\_RESOLUTION</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-407">Элемент **двретурн** имеет константу, описывающую разрешение счетчика, и может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="45ec8-407">The **dwReturn** member is set to a constant describing the resolution of the counter, and is one of the following values:</span></span>

-   <span data-ttu-id="45ec8-408">Видеомагнитофон MCI \_ \_ Счетчик \_ \_ кадров "Res": Счетчик имеет разрешение кадров.</span><span class="sxs-lookup"><span data-stu-id="45ec8-408">MCI\_VCR\_COUNTER\_RES\_FRAMES: Counter has resolution of frames.</span></span>
-   <span data-ttu-id="45ec8-409">\_Счетчик видеомагнитофонов MCI \_ \_ \_ , секунд: Счетчик имеет разрешение в секундах.</span><span class="sxs-lookup"><span data-stu-id="45ec8-409">MCI\_VCR\_COUNTER\_RES\_SECONDS: Counter has resolution of seconds.</span></span>
-   <span data-ttu-id="45ec8-410">\_ \_ \_ Значение счетчика состояния видеомагнитофона MCI \_ : для элемента **двретурн** задается текущий счетчик в текущем формате времени счетчика.</span><span class="sxs-lookup"><span data-stu-id="45ec8-410">MCI\_VCR\_STATUS\_COUNTER\_VALUE: The **dwReturn** member is set to the current counter reading, in the current counter-time format.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>\_ \_ \_ Частота кадров состояния ВИДЕОмагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI\_VCR\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-412">Для элемента **двретурн** задана текущая частота кадров в машинном формате.</span><span class="sxs-lookup"><span data-stu-id="45ec8-412">The **dwReturn** member is set to the current native frame rate of the device.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>\_ \_ индекс состояния видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>MCI\_VCR\_STATUS\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-414">Для элемента **двретурн** задается константа, описывающая текущее содержимое экрана на экране, и является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="45ec8-414">The **dwReturn** member is set to a constant, describing the current contents of the on-screen display, and is one of the following:</span></span>

-   <span data-ttu-id="45ec8-415">\_ \_ Счетчик индекса видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-415">MCI\_VCR\_INDEX\_COUNTER</span></span>
-   <span data-ttu-id="45ec8-416">\_ \_ Дата индекса видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-416">MCI\_VCR\_INDEX\_DATE</span></span>
-   <span data-ttu-id="45ec8-417">\_ \_ время индекса видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-417">MCI\_VCR\_INDEX\_TIME</span></span>
-   <span data-ttu-id="45ec8-418">\_временной код \_ индекса \_ видеомагнитофона MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-418">MCI\_VCR\_INDEX\_TIMECODE</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>\_ \_ индекс состояния видеомагнитофона \_ MCI \_ в</span><span class="sxs-lookup"><span data-stu-id="45ec8-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>MCI\_VCR\_STATUS\_INDEX\_ON</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-420">Элемент **двретурн** имеет значение **true** , если экран на экране включен; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-420">The **dwReturn** member is set to **TRUE** if the on-screen display is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>\_ \_ \_ тип носителя состояния видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MCI\_VCR\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-422">Элементу **двретурн** присваивается один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="45ec8-422">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="45ec8-423">\_ \_ 8MM Media видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-423">MCI\_VCR\_MEDIA\_8MM</span></span>
-   <span data-ttu-id="45ec8-424">\_ \_ HI8 Media видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-424">MCI\_VCR\_MEDIA\_HI8</span></span>
-   <span data-ttu-id="45ec8-425">\_ \_ ВХС Media видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-425">MCI\_VCR\_MEDIA\_VHS</span></span>
-   <span data-ttu-id="45ec8-426">\_ \_ свхс Media видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-426">MCI\_VCR\_MEDIA\_SVHS</span></span>
-   <span data-ttu-id="45ec8-427">\_ \_ \_ бета-версия ВИДЕОмагнитофона MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-427">MCI\_VCR\_MEDIA\_BETA</span></span>
-   <span data-ttu-id="45ec8-428">\_ \_ едбета Media видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-428">MCI\_VCR\_MEDIA\_EDBETA</span></span>
-   <span data-ttu-id="45ec8-429">\_ \_ другое устройство видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-429">MCI\_VCR\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>\_ \_ номер состояния видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>MCI\_VCR\_STATUS\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-431">При  использовании этого флага с \_ \_ \_ \_ флагом канала тюнера MCI в качестве элемента двнумбер задается номер логического тюнера.</span><span class="sxs-lookup"><span data-stu-id="45ec8-431">The **dwNumber** member is set to the logical-tuner number when you use this flag with the MCI\_VCR\_STATUS\_TUNER\_CHANNEL flag.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>\_состояние видеомагнитофона MCI. \_ \_ число \_ \_ звуковых \_ дорожек</span><span class="sxs-lookup"><span data-stu-id="45ec8-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_AUDIO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-433">Для элемента **двретурн** задается число звуковых дорожек, которые могут быть выбраны независимо.</span><span class="sxs-lookup"><span data-stu-id="45ec8-433">The **dwReturn** member is set to the number of audio tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>\_состояние видеомагнитофона \_ Устройства MCI. \_ число \_ \_ \_ видеодорожек</span><span class="sxs-lookup"><span data-stu-id="45ec8-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_VIDEO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-435">Для элемента **двретурн** задается число видеодорожек, которые могут быть выбраны независимо.</span><span class="sxs-lookup"><span data-stu-id="45ec8-435">The **dwReturn** member is set to the number of video tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>\_ \_ \_ время ожидания приостановки воспроизведения видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI\_VCR\_STATUS\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-437">Для элемента **двретурн** задается максимальная длительность (в миллисекундах) команды Pause.</span><span class="sxs-lookup"><span data-stu-id="45ec8-437">The **dwReturn** member is set to the maximum duration, in milliseconds, of a pause command.</span></span> <span data-ttu-id="45ec8-438">Возвращаемое значение, равное нулю, указывает, что тайм-аут не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45ec8-438">The return value of zero indicates that no time-out will occur.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>\_ \_ \_ Формат воспроизведения состояния видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI\_VCR\_STATUS\_PLAY\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-440">Элементу **двретурн** присваивается один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="45ec8-440">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="45ec8-441">\_Формат видеомагнитофона MCI ( \_ \_ EP)</span><span class="sxs-lookup"><span data-stu-id="45ec8-441">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="45ec8-442">\_Формат видеомагнитофона MCI \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="45ec8-442">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="45ec8-443">\_другой формат видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-443">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="45ec8-444">\_Формат видеомагнитофона MCI \_ \_ SP</span><span class="sxs-lookup"><span data-stu-id="45ec8-444">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>\_ \_ длительность состояния видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>MCI\_VCR\_STATUS\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-446">Для элемента **двретурн** задается длина видеокассеты, которая будет воспроизводиться после точки, в которой оно было остановлено, в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="45ec8-446">The **dwReturn** member is set to the length of the videotape that will play after the spot at which it was stopped, in the current time format.</span></span> <span data-ttu-id="45ec8-447">Это необходимо для переноса ленточной ленты ВИДЕОМАГНИТОФОНА из команды остановки или приостановки.</span><span class="sxs-lookup"><span data-stu-id="45ec8-447">This is needed to brake the VCR tape transport from a stop or pause command.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>\_ \_ Включение состояния видеомагнитофона \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI\_VCR\_STATUS\_POWER\_ON</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-449">Элемент **двретурн** имеет значение **true** , если включено питание; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-449">The **dwReturn** member is set to **TRUE** if the power is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>\_ \_ \_ Длительность предрулона для состояния видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>MCI\_VCR\_STATUS\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-451">Для элемента **двретурн** задается длина видеокассеты, которая будет воспроизводиться до точки, с которой он был запущен, в текущем формате времени.</span><span class="sxs-lookup"><span data-stu-id="45ec8-451">The **dwReturn** member is set to the length of the videotape that will play before the spot at which it was started, in the current time format.</span></span> <span data-ttu-id="45ec8-452">Это необходимо для стабилизации выходных данных ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="45ec8-452">This is needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>\_ \_ \_ Формат записи состояния видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>MCI\_VCR\_STATUS\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-454">Элементу **двретурн** присваивается один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="45ec8-454">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="45ec8-455">\_Формат видеомагнитофона MCI ( \_ \_ EP)</span><span class="sxs-lookup"><span data-stu-id="45ec8-455">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="45ec8-456">\_Формат видеомагнитофона MCI \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="45ec8-456">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="45ec8-457">\_другой формат видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-457">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="45ec8-458">\_Формат видеомагнитофона MCI \_ \_ SP</span><span class="sxs-lookup"><span data-stu-id="45ec8-458">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>\_ \_ скорость состояния видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>MCI\_VCR\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-460">Для элемента **двретурн** устанавливается текущая скорость.</span><span class="sxs-lookup"><span data-stu-id="45ec8-460">The **dwReturn** member is set to the current speed.</span></span> <span data-ttu-id="45ec8-461">Дополнительные сведения см. в разделе \_ \_ Установка \_ флага Speed видеомагнитофона MCI для команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-461">For more information, see the MCI\_VCR\_SET\_SPEED flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>\_ \_ режим времени для состояния видеомагнитофона \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI\_VCR\_STATUS\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-463">Элементу **двретурн** присваивается один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="45ec8-463">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="45ec8-464">\_ \_ Счетчик времени видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-464">MCI\_VCR\_TIME\_COUNTER</span></span>
-   <span data-ttu-id="45ec8-465">\_ \_ Обнаружение времени видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-465">MCI\_VCR\_TIME\_DETECT</span></span>
-   <span data-ttu-id="45ec8-466">временной код \_ видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-466">MCI\_VCR\_TIME\_TIMECODE</span></span>

<span data-ttu-id="45ec8-467">Дополнительные сведения см. в описании \_ \_ флага "Установка режима времени видеомагнитофона MCI" \_ \_ в команде [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-467">For more information, see the MCI\_VCR\_SET\_TIME\_MODE flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>\_ \_ тип времени для состояния видеомагнитофона \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI\_VCR\_STATUS\_TIME\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-469">Для элемента **двретурн** задается константа, описывающая текущий используемый тип времени (используется [воспроизведением](play.md), [записью](record.md), [поиском](seek.md)и т. д.) и является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="45ec8-469">The **dwReturn** member is set to a constant describing the current time type in use (used by [play](play.md), [record](record.md), [seek](seek.md), and so on), and is one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_ \_ Счетчик времени видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-471">Счетчик используется.</span><span class="sxs-lookup"><span data-stu-id="45ec8-471">Counter is in use.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>временной код \_ видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-473">Код времени используется.</span><span class="sxs-lookup"><span data-stu-id="45ec8-473">Timecode is in use.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>код \_ состояния видеомагнитофона MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>MCI\_VCR\_STATUS\_TIMECODE\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-475">Элемент **двретурн** имеет значение **true** , если код времени имеется в текущей позиции в содержимом; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-475">The **dwReturn** member is set to **TRUE** if timecode is present at the current position in the content; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>\_запись времени \_ \_ регистрации состояния \_ видеомагнитофона MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI\_VCR\_STATUS\_TIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-477">Элемент **двретурн** имеет значение **true** , если код времени будет записан при указании команды следующей записи. в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-477">The **dwReturn** member is set to **TRUE** if the timecode will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>\_ \_ тип временной код состояния видеомагнитофона \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>MCI\_VCR\_STATUS\_TIMECODE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-479">Для элемента **двретурн** задается константа, описывающая тип времени действия, который напрямую поддерживается устройством, и является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="45ec8-479">The **dwReturn** member is set to a constant, describing the type of timecode that is directly supported by the device, and is one of the following:</span></span>

-   <span data-ttu-id="45ec8-480">Код времени \_ ВИДЕОМАГНИТОФОНА MCI \_ \_ тип \_ Нет: это устройство не использует код времени.</span><span class="sxs-lookup"><span data-stu-id="45ec8-480">MCI\_VCR\_TIMECODE\_TYPE\_NONE: This device does not use a timecode.</span></span>
-   <span data-ttu-id="45ec8-481">Код времени \_ ВИДЕОМАГНИТОФОНА MCI \_ \_ тип \_ : это устройство использует неуказанный код времени.</span><span class="sxs-lookup"><span data-stu-id="45ec8-481">MCI\_VCR\_TIMECODE\_TYPE\_OTHER: This device uses an unspecified timecode.</span></span>
-   <span data-ttu-id="45ec8-482">Код времени \_ ВИДЕОМАГНИТОФОНА MCI \_ \_ тип \_ SMPTE: это устройство использует код времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="45ec8-482">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE: This device uses SMPTE timecode.</span></span>
-   <span data-ttu-id="45ec8-483">Код времени \_ ВИДЕОМАГНИТОФОНА MCI \_ \_ тип \_ SMPTE \_ Drop: это устройство использует код времени удаления SMPTE.</span><span class="sxs-lookup"><span data-stu-id="45ec8-483">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE\_DROP: This device uses SMPTE drop timecode.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>\_ \_ \_ канал тюнера "состояние видеомагнитофона MCI" \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI\_VCR\_STATUS\_TUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-485">Для элемента **двретурн** задается номер текущего канала.</span><span class="sxs-lookup"><span data-stu-id="45ec8-485">The **dwReturn** member is set to the current channel number.</span></span> <span data-ttu-id="45ec8-486">Если указать \_ \_ номер состояния видеомагнитофона MCI \_ в параметре *DwFlags* этой команды, **двнумбер** содержит номер логического тюнера, к которому применяется эта команда.</span><span class="sxs-lookup"><span data-stu-id="45ec8-486">If you specify MCI\_VCR\_STATUS\_NUMBER in the *dwFlags* parameter of this command, **dwNumber** contains the logical-tuner number this command applies to.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>\_ \_ монитор видео о состоянии видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-488">Для элемента **двретурн** задается константа, указывающая на текущий выбранный тип монитора видео.</span><span class="sxs-lookup"><span data-stu-id="45ec8-488">The **dwReturn** member is set to a constant, indicating the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>\_ \_ \_ номер монитора для видео о состоянии \_ видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-490">Для элемента **двретурн** задается номер выбранного в данный момент типа монитора видео.</span><span class="sxs-lookup"><span data-stu-id="45ec8-490">The **dwReturn** member is set to the number of the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>\_ \_ запись видео о состоянии видеомагнитофона \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>MCI\_VCR\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-492">Элемент **двретурн** имеет значение **true** , если видео будет записано при указании команды следующей записи. в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-492">The **dwReturn** member is set to **TRUE** if video will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="45ec8-493">Если \_ в параметре *dwFlags* этой команды указать Track MCI, **двтракк** содержит запись, к которой относится этот запрос.</span><span class="sxs-lookup"><span data-stu-id="45ec8-493">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>\_ \_ источник видео о состоянии видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-495">Для элемента **двретурн** задается константа, указывающая на текущий выбранный тип видео-источника.</span><span class="sxs-lookup"><span data-stu-id="45ec8-495">The **dwReturn** member is set to a constant indicating the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>\_ \_ \_ \_ Исходный номер видео о состоянии видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-497">Для элемента **двретурн** задается номер выбранного в данный момент типа источника видео.</span><span class="sxs-lookup"><span data-stu-id="45ec8-497">The **dwReturn** member is set to the number of the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>\_ \_ запись состояния видеомагнитофона \_ MCI \_ защищена</span><span class="sxs-lookup"><span data-stu-id="45ec8-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI\_VCR\_STATUS\_WRITE\_PROTECTED</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-499">Элемент **двретурн** имеет значение **true** , если носитель защищен от записи; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-499">The **dwReturn** member is set to **TRUE** if the media is write-protected; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="45ec8-500">Для устройств ВИДЕОМАГНИТОФОНА параметр *лпстатус* указывает на структуру [**\_ \_ \_ пармс состояния видеомагнитофона MCI**](mci-vcr-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-500">For VCR devices, the *lpStatus* parameter points to an [**MCI\_VCR\_STATUS\_PARMS**](mci-vcr-status-parms.md) structure.</span></span>

<span data-ttu-id="45ec8-501">Использование \_ \_ флага длины состояния MCI для определения длины носителя всегда возвращает 2 часа для устройств видеомагнитофона, если только длина не была явно изменена с помощью команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="45ec8-501">Using the MCI\_STATUS\_LENGTH flag to determine the length of the media always returns 2 hours for VCR devices, unless the length has been explicitly changed using the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="45ec8-502">Для типа устройства **наложения** используются следующие дополнительные флаги.</span><span class="sxs-lookup"><span data-stu-id="45ec8-502">The following additional flags are used with the **overlay** device type.</span></span> <span data-ttu-id="45ec8-503">Эти константы используются в элементе **двитем** структуры, на которую указывает параметр *лпстатус* , когда \_ \_ для параметра *dwFlags* указан элемент состояния MCI.</span><span class="sxs-lookup"><span data-stu-id="45ec8-503">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="45ec8-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>\_ \_ HWND состояния овли \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI\_OVLY\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-505">Для элемента **двретурн** задается маркер окна, связанного с устройством наложения видео.</span><span class="sxs-lookup"><span data-stu-id="45ec8-505">The **dwReturn** member is set to the handle of the window associated with the video-overlay device.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>\_ \_ растяжение состояния овли MCI \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI\_OVLY\_STATUS\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-507">Элемент **двретурн** имеет значение **true** , если растяжение включено. в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-507">The **dwReturn** member is set to **TRUE** if stretching is enabled; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_ \_ имеется носитель состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-509">Член **двретурн** имеет значение **true** , если носитель вставлен в устройство; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-509">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="45ec8-510">С типом устройства **видеодиск** используются следующие дополнительные флаги.</span><span class="sxs-lookup"><span data-stu-id="45ec8-510">The following additional flags are used with the **videodisc** device type.</span></span> <span data-ttu-id="45ec8-511">Эти константы используются в элементе **двитем** структуры, на которую указывает параметр *лпстатус* , когда \_ \_ для параметра *dwFlags* указан элемент состояния MCI.</span><span class="sxs-lookup"><span data-stu-id="45ec8-511">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="45ec8-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_ \_ имеется носитель состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-513">Член **двретурн** имеет значение **true** , если носитель вставлен в устройство; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-513">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_режим состояния \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-515">Элемент **двретурн** установлен в текущий режим устройства.</span><span class="sxs-lookup"><span data-stu-id="45ec8-515">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="45ec8-516">Устройства видеодиск могут возвращать \_ \_ \_ константу приостановки в режиме VD MCI, а также константы, которые может возвращать любое устройство, как описано в параметре *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="45ec8-516">Videodisc devices can return the MCI\_VD\_MODE\_PARK constant, in addition to the constants any device can return, as documented with the *dwFlags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>\_ \_ Размер диска с состоянием MCI VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI\_VD\_STATUS\_DISC\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-518">Для элемента **двретурн** задается размер загруженного диска в дюймах (8 или 12).</span><span class="sxs-lookup"><span data-stu-id="45ec8-518">The **dwReturn** member is set to the size of the loaded disc in inches (8 or 12).</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>\_состояние MCI VD " \_ \_ вперед"</span><span class="sxs-lookup"><span data-stu-id="45ec8-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI\_VD\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-520">Для элемента **двретурн** задано **значение true** при воспроизведении вперед; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="45ec8-520">The **dwReturn** member is set to **TRUE** if playing forward; it is set to **FALSE** otherwise.</span></span>

<span data-ttu-id="45ec8-521">Устройство MCI видеодиск не поддерживает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="45ec8-521">The MCI videodisc device does not support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>\_ \_ \_ тип носителя состояния MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="45ec8-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI\_VD\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-523">Для элемента **двретурн** задается тип носителя вставленного носителя.</span><span class="sxs-lookup"><span data-stu-id="45ec8-523">The **dwReturn** member is set to the media type of the inserted media.</span></span> <span data-ttu-id="45ec8-524">Можно вернуть следующие типы носителей:</span><span class="sxs-lookup"><span data-stu-id="45ec8-524">The following media types can be returned:</span></span>

<span data-ttu-id="45ec8-525">\_ \_ Кав мультимедиа MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="45ec8-525">MCI\_VD\_MEDIA\_CAV</span></span>

<span data-ttu-id="45ec8-526">\_ \_ CLV мультимедиа MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="45ec8-526">MCI\_VD\_MEDIA\_CLV</span></span>

<span data-ttu-id="45ec8-527">\_мультимедиа MCI \_ VD \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-527">MCI\_VD\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>\_ \_ сторона состояния VD \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI\_VD\_STATUS\_SIDE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-529">Элемент **двретурн** имеет значение 1 или 2, чтобы указать, какая сторона диска загружена.</span><span class="sxs-lookup"><span data-stu-id="45ec8-529">The **dwReturn** member is set to 1 or 2 to indicate which side of the disc is loaded.</span></span> <span data-ttu-id="45ec8-530">Этот флаг поддерживают не все устройства видеодиск.</span><span class="sxs-lookup"><span data-stu-id="45ec8-530">Not all videodisc devices support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>\_ \_ скорость состояния VD \_ MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI\_VD\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-532">Для элемента **двретурн** задается скорость воспроизведения в кадрах за секунду.</span><span class="sxs-lookup"><span data-stu-id="45ec8-532">The **dwReturn** member is set to the play speed in frames per second.</span></span> <span data-ttu-id="45ec8-533">МЦИПИОНР. ПеремЦиерр драйвер устройства DRV возвращает \_ НЕподдерживаемую \_ функцию.</span><span class="sxs-lookup"><span data-stu-id="45ec8-533">The MCIPIONR.DRV device driver returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> </dl>

<span data-ttu-id="45ec8-534">С типом устройства **вавеаудио** используются следующие дополнительные флаги.</span><span class="sxs-lookup"><span data-stu-id="45ec8-534">The following additional flags are used with the **waveaudio** device type.</span></span> <span data-ttu-id="45ec8-535">Эти константы используются в элементе **двитем** структуры, на которую указывает параметр *лпстатус* , когда \_ \_ для параметра *dwFlags* указан элемент состояния MCI.</span><span class="sxs-lookup"><span data-stu-id="45ec8-535">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="45ec8-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI \_ Wave \_ форматтаг</span><span class="sxs-lookup"><span data-stu-id="45ec8-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI\_WAVE\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-537">Для элемента **двретурн** задан текущий тег формата, используемый для воспроизведения, записи и сохранения.</span><span class="sxs-lookup"><span data-stu-id="45ec8-537">The **dwReturn** member is set to the current format tag used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_звуковые \_ входные данные MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-539">Для элемента **двретурн** задается устройство ввода Wave, используемое для записи.</span><span class="sxs-lookup"><span data-stu-id="45ec8-539">The **dwReturn** member is set to the wave input device used for recording.</span></span> <span data-ttu-id="45ec8-540">Если устройство не используется и не было явно задано, возвращается ошибка МЦИЕРР \_ Wave \_ инпутунспеЦифиед.</span><span class="sxs-lookup"><span data-stu-id="45ec8-540">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_INPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_звуковые \_ выходные данные MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-542">Для элемента **двретурн** задано устройство вывода Wave, используемое для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="45ec8-542">The **dwReturn** member is set to the wave output device used for playing.</span></span> <span data-ttu-id="45ec8-543">Если устройство не используется и не было явно задано, возвращается ошибка МЦИЕРР \_ Wave \_ аутпутунспеЦифиед.</span><span class="sxs-lookup"><span data-stu-id="45ec8-543">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_OUTPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>\_состояние волновой волны MCI \_ \_ авгбитесперсек</span><span class="sxs-lookup"><span data-stu-id="45ec8-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI\_WAVE\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-545">Для элемента **двретурн** заданы текущие байты в секунду, используемые для воспроизведения, записи и сохранения.</span><span class="sxs-lookup"><span data-stu-id="45ec8-545">The **dwReturn** member is set to the current bytes per second used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>\_состояние волновой волны MCI \_ \_ битсперсампле</span><span class="sxs-lookup"><span data-stu-id="45ec8-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI\_WAVE\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-547">Для элемента **двретурн** задается текущий бит на выборку, используемый для воспроизведения, записи и сохранения данных в формате PCM.</span><span class="sxs-lookup"><span data-stu-id="45ec8-547">The **dwReturn** member is set to the current bits per sample used for playing, recording, and saving PCM formatted data.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>\_состояние волновой волны MCI \_ \_ блоккалигн</span><span class="sxs-lookup"><span data-stu-id="45ec8-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI\_WAVE\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-549">Для элемента **двретурн** задано выравнивание текущего блока, используемое для воспроизведения, записи и сохранения.</span><span class="sxs-lookup"><span data-stu-id="45ec8-549">The **dwReturn** member is set to the current block alignment used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>\_каналы состояния волновой волны MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI\_WAVE\_STATUS\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-551">Для элемента **двретурн** задано текущее число каналов, используемое для воспроизведения, записи и сохранения.</span><span class="sxs-lookup"><span data-stu-id="45ec8-551">The **dwReturn** member is set to the current channel count used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>\_уровень состояния звуковой волны MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="45ec8-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI\_WAVE\_STATUS\_LEVEL</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-553">Для элемента **двретурн** задана текущая запись или уровень воспроизведения данных в формате PCM.</span><span class="sxs-lookup"><span data-stu-id="45ec8-553">The **dwReturn** member is set to the current record or playback level of PCM formatted data.</span></span> <span data-ttu-id="45ec8-554">Значение возвращается как 8-или 16-разрядное значение в зависимости от используемого размера выборки.</span><span class="sxs-lookup"><span data-stu-id="45ec8-554">The value is returned as an 8- or 16-bit value, depending on the sample size used.</span></span> <span data-ttu-id="45ec8-555">Правый или нижний уровень канала возвращается в слове нижнего порядка.</span><span class="sxs-lookup"><span data-stu-id="45ec8-555">The right or mono channel level is returned in the low-order word.</span></span> <span data-ttu-id="45ec8-556">Левый уровень канала возвращается в слове высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="45ec8-556">The left channel level is returned in the high-order word.</span></span>

</dd> <dt>

<span data-ttu-id="45ec8-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>\_состояние волновой волны MCI \_ \_ самплесперсек</span><span class="sxs-lookup"><span data-stu-id="45ec8-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI\_WAVE\_STATUS\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="45ec8-558">Для элемента **двретурн** заданы текущие выборки в секунду, используемые для воспроизведения, записи и сохранения.</span><span class="sxs-lookup"><span data-stu-id="45ec8-558">The **dwReturn** member is set to the current samples per second used for playing, recording, and saving.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45ec8-559">Требования</span><span class="sxs-lookup"><span data-stu-id="45ec8-559">Requirements</span></span>



| <span data-ttu-id="45ec8-560">Требование</span><span class="sxs-lookup"><span data-stu-id="45ec8-560">Requirement</span></span> | <span data-ttu-id="45ec8-561">Значение</span><span class="sxs-lookup"><span data-stu-id="45ec8-561">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ec8-562">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45ec8-562">Minimum supported client</span></span><br/> | <span data-ttu-id="45ec8-563">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="45ec8-563">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="45ec8-564">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45ec8-564">Minimum supported server</span></span><br/> | <span data-ttu-id="45ec8-565">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="45ec8-565">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="45ec8-566">Заголовок</span><span class="sxs-lookup"><span data-stu-id="45ec8-566">Header</span></span><br/>                   | <dl> <span data-ttu-id="45ec8-567"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45ec8-567"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45ec8-568">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45ec8-568">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ec8-569">MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-569">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="45ec8-570">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-570">MCI Commands</span></span>](mci-commands.md)
</dt> <dt>

[<span data-ttu-id="45ec8-571">\_Вырезать MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-571">MCI\_CUT</span></span>](mci-cut.md)
</dt> <dt>

[<span data-ttu-id="45ec8-572">\_Удаление MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-572">MCI\_DELETE</span></span>](mci-delete.md)
</dt> <dt>

[<span data-ttu-id="45ec8-573">\_Вставка MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-573">MCI\_PASTE</span></span>](mci-paste.md)
</dt> <dt>

[<span data-ttu-id="45ec8-574">\_резервирование MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-574">MCI\_RESERVE</span></span>](mci-reserve.md)
</dt> <dt>

[<span data-ttu-id="45ec8-575">\_набор MCI</span><span class="sxs-lookup"><span data-stu-id="45ec8-575">MCI\_SET</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="45ec8-576">воспроизводит</span><span class="sxs-lookup"><span data-stu-id="45ec8-576">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="45ec8-577">record</span><span class="sxs-lookup"><span data-stu-id="45ec8-577">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="45ec8-578">поиска</span><span class="sxs-lookup"><span data-stu-id="45ec8-578">seek</span></span>](seek.md)
</dt> </dl>

 

