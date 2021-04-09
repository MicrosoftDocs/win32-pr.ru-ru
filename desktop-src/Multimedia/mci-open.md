---
title: Команда MCI_OPEN (Ммсистем. h)
description: Команда MCI \_ Open инициализирует устройство или файл. Все устройства распознают эту команду.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- MCI_OPEN команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891397"
---
# <a name="mci_open-command"></a><span data-ttu-id="238fd-105">\_Команда MCI Open</span><span class="sxs-lookup"><span data-stu-id="238fd-105">MCI\_OPEN command</span></span>

<span data-ttu-id="238fd-106">Команда MCI \_ Open инициализирует устройство или файл.</span><span class="sxs-lookup"><span data-stu-id="238fd-106">The MCI\_OPEN command initializes a device or file.</span></span> <span data-ttu-id="238fd-107">Все устройства распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="238fd-107">All devices recognize this command.</span></span>

<span data-ttu-id="238fd-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="238fd-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
);
```



## <a name="parameters"></a><span data-ttu-id="238fd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="238fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="238fd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="238fd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="238fd-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="238fd-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="238fd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="238fd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="238fd-113">\_Ожидание с уведомлением MCI или MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="238fd-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="238fd-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="238fd-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="238fd-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*лпопен*</span><span class="sxs-lookup"><span data-stu-id="238fd-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span></span>
</dt> <dd>

<span data-ttu-id="238fd-116">Указатель на структуру [**\_ \_ пармс для MCI Open**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="238fd-116">Pointer to an [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span> <span data-ttu-id="238fd-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="238fd-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="238fd-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="238fd-118">Return Value</span></span>

<span data-ttu-id="238fd-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="238fd-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="238fd-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="238fd-120">Remarks</span></span>

<span data-ttu-id="238fd-121">\_ \_ Флаг открытого типа MCI должен использоваться при указании устройства в функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="238fd-121">The MCI\_OPEN\_TYPE flag must be used whenever a device is specified in the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="238fd-122">Если вы открываете устройство, указав константу типа устройства, \_ \_ \_ в дополнение к типу открытия MCI необходимо указать флаг открытого идентификатора типа MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="238fd-122">If you open a device by specifying a device-type constant, you must specify the MCI\_OPEN\_TYPE\_ID flag in addition to MCI\_OPEN\_TYPE.</span></span> <span data-ttu-id="238fd-123">Список констант типа устройства см. в разделе [типы устройств MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="238fd-123">For a list of device-type constants, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="238fd-124">Если флаг с \_ открытым \_ общим доступом MCI не указан при первоначальном открытии устройства или файла, все последующие \_ команды MCI Open для устройства или файла завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="238fd-124">If the MCI\_OPEN\_SHAREABLE flag is not specified when a device or file is initially opened, all subsequent MCI\_OPEN commands to the device or file will fail.</span></span> <span data-ttu-id="238fd-125">Если устройство или файл уже открыты и этот флаг не указан, вызов завершится ошибкой, даже если первая команда открытия, заданная командой MCI, \_ открыла \_ общий доступ.</span><span class="sxs-lookup"><span data-stu-id="238fd-125">If the device or file is already open and this flag is not specified, the call will fail even if the first open command specified MCI\_OPEN\_SHAREABLE.</span></span> <span data-ttu-id="238fd-126">Файлы, открытые для МЦИСЕК. DRV и МЦИВАВЕ. Устройства DRV не додаются совместной работе.</span><span class="sxs-lookup"><span data-stu-id="238fd-126">Files opened for the MCISEQ.DRV and MCIWAVE.DRV devices are nonsharable.</span></span>

<span data-ttu-id="238fd-127">Регистр игнорируется в имени устройства, но не может начинаться или заканчиваться пробелами.</span><span class="sxs-lookup"><span data-stu-id="238fd-127">Case is ignored in the device name, but there cannot be leading or trailing blanks.</span></span>

<span data-ttu-id="238fd-128">Чтобы использовать автоматический выбор типа (с помощью записей в реестре), назначьте имя файла и расширение файла **лпстрелементнаме** члену структуры, идентифицируемой *лпопен*, установите для элемента **лпстрдевицетипе** **значение NULL** и установите \_ \_ флаг открытия элемента MCI.</span><span class="sxs-lookup"><span data-stu-id="238fd-128">To use automatic type selection (via the entries in the registry), assign the filename and file extension to the **lpstrElementName** member of the structure identified by *lpOpen*, set the **lpstrDeviceType** member to **NULL**, and set the MCI\_OPEN\_ELEMENT flag.</span></span>

<span data-ttu-id="238fd-129">Следующие дополнительные флаги применяются ко всем устройствам, поддерживающим MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="238fd-129">The following additional flags apply to all devices supporting MCI\_OPEN:</span></span>

<dl> <dt>

<span data-ttu-id="238fd-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>\_псевдоним для открытия MCI \_</span><span class="sxs-lookup"><span data-stu-id="238fd-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI\_OPEN\_ALIAS</span></span>
</dt> <dd>

<span data-ttu-id="238fd-131">Псевдоним включается в элемент **лпстралиас** структуры, идентифицируемой *лпопен*.</span><span class="sxs-lookup"><span data-stu-id="238fd-131">An alias is included in the **lpstrAlias** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="238fd-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>\_доступ к MCI с открытым \_ общим доступом</span><span class="sxs-lookup"><span data-stu-id="238fd-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI\_OPEN\_SHAREABLE</span></span>
</dt> <dd>

<span data-ttu-id="238fd-133">Устройство или файл должны быть открыты для совместного открытия.</span><span class="sxs-lookup"><span data-stu-id="238fd-133">The device or file should be opened as sharable.</span></span>

</dd> <dt>

<span data-ttu-id="238fd-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>\_тип открытия \_ MCI</span><span class="sxs-lookup"><span data-stu-id="238fd-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI\_OPEN\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="238fd-135">Имя типа устройства или константа включается в элемент **лпстрдевицетипе** структуры, определяемой *лпопен*.</span><span class="sxs-lookup"><span data-stu-id="238fd-135">A device type name or constant is included in the **lpstrDeviceType** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="238fd-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>\_идентификатор открытого \_ типа \_ MCI</span><span class="sxs-lookup"><span data-stu-id="238fd-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI\_OPEN\_TYPE\_ID</span></span>
</dt> <dd>

<span data-ttu-id="238fd-137">Неупорядоченное слово элемента **лпстрдевицетипе** структуры, идентифицируемой *лпопен* , содержит стандартный идентификатор типа устройства MCI, а в верхнем и обязательном варианте — порядковый номер устройства.</span><span class="sxs-lookup"><span data-stu-id="238fd-137">The low-order word of the **lpstrDeviceType** member of the structure identified by *lpOpen* contains a standard MCI device type identifier and the high-order word optionally contains the ordinal index for the device.</span></span> <span data-ttu-id="238fd-138">Используйте этот флаг с \_ \_ флагом открытого типа MCI.</span><span class="sxs-lookup"><span data-stu-id="238fd-138">Use this flag with the MCI\_OPEN\_TYPE flag.</span></span>

</dd> </dl>

<span data-ttu-id="238fd-139">Следующие дополнительные флаги применяются к составным устройствам.</span><span class="sxs-lookup"><span data-stu-id="238fd-139">The following additional flags apply to compound devices:</span></span>

<dl> <dt>

<span data-ttu-id="238fd-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>\_элемент Open \_ MCI</span><span class="sxs-lookup"><span data-stu-id="238fd-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI\_OPEN\_ELEMENT</span></span>
</dt> <dd>

<span data-ttu-id="238fd-141">Имя файла включается в элемент **лпстрелементнаме** структуры, определенной параметром *лпопен*.</span><span class="sxs-lookup"><span data-stu-id="238fd-141">A filename is included in the **lpstrElementName** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="238fd-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>\_идентификатор открытого \_ элемента \_ MCI</span><span class="sxs-lookup"><span data-stu-id="238fd-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI\_OPEN\_ELEMENT\_ID</span></span>
</dt> <dd>

<span data-ttu-id="238fd-143">Элемент **лпстрелементнаме** структуры, идентифицируемой *лпопен* , интерпретируется как значение **типа DWORD** и является внутренним для устройства.</span><span class="sxs-lookup"><span data-stu-id="238fd-143">The **lpstrElementName** member of the structure identified by *lpOpen* is interpreted as a **DWORD** value and has meaning internal to the device.</span></span> <span data-ttu-id="238fd-144">Используйте этот флаг с \_ \_ флагом элемента MCI Open element.</span><span class="sxs-lookup"><span data-stu-id="238fd-144">Use this flag with the MCI\_OPEN\_ELEMENT flag.</span></span>

</dd> </dl>

<span data-ttu-id="238fd-145">С типом устройства **дигиталвидео** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="238fd-145">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="238fd-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>\_ДГВ MCI \_ Open \_ static</span><span class="sxs-lookup"><span data-stu-id="238fd-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI\_DGV\_OPEN\_NOSTATIC</span></span>
</dt> <dd>

<span data-ttu-id="238fd-147">Устройство должно уменьшить число статических (системных) цветов в палитре.</span><span class="sxs-lookup"><span data-stu-id="238fd-147">The device should reduce the number of static (system) colors in the palette.</span></span> <span data-ttu-id="238fd-148">Это увеличивает количество цветов, доступных для отрисовки видеопотока.</span><span class="sxs-lookup"><span data-stu-id="238fd-148">This increases the number of colors available for rendering the video stream.</span></span> <span data-ttu-id="238fd-149">Этот флаг применяется только к устройствам, которые совместно используют палитру с Windows.</span><span class="sxs-lookup"><span data-stu-id="238fd-149">This flag applies only to devices that share a palette with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="238fd-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>\_ \_ открыть \_ родительский элемент MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="238fd-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI\_DGV\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="238fd-151">Маркер родительского окна указывается в элементе **хвндпарент** структуры, определенной параметром *лпопен*.</span><span class="sxs-lookup"><span data-stu-id="238fd-151">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="238fd-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ ДГВ \_ Open \_ WS</span><span class="sxs-lookup"><span data-stu-id="238fd-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI\_DGV\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="238fd-153">Стиль окна указывается в элементе **двстиле** структуры, определенной параметром *лпопен*.</span><span class="sxs-lookup"><span data-stu-id="238fd-153">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="238fd-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ ДГВ \_ открыть \_ 16-разрядный</span><span class="sxs-lookup"><span data-stu-id="238fd-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI\_DGV\_OPEN\_16BIT</span></span>
</dt> <dd>

<span data-ttu-id="238fd-155">Указывает предпочитаемый параметр для поддержки 16-разрядных устройств MCI.</span><span class="sxs-lookup"><span data-stu-id="238fd-155">Indicates a preference for 16-bit MCI device support.</span></span>

</dd> <dt>

<span data-ttu-id="238fd-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>\_ДГВ MCI \_ открыть \_ 32-разрядное</span><span class="sxs-lookup"><span data-stu-id="238fd-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI\_DGV\_OPEN\_32BIT</span></span>
</dt> <dd>

<span data-ttu-id="238fd-157">Указывает параметры поддержки 32-разрядного устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="238fd-157">Indicates a preference for 32-bit MCI device support.</span></span>

</dd> </dl>

<span data-ttu-id="238fd-158">Для устройств с цифровыми видео параметр *лпопен* указывает на структуру [**MCI \_ ДГВ \_ Open \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) Structure.</span><span class="sxs-lookup"><span data-stu-id="238fd-158">For digital-video devices, the *lpOpen* parameter points to an [**MCI\_DGV\_OPEN\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) structure.</span></span>

<span data-ttu-id="238fd-159">Для типа устройства **наложения** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="238fd-159">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="238fd-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>\_ \_ открыть \_ родительский элемент MCI овли</span><span class="sxs-lookup"><span data-stu-id="238fd-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI\_OVLY\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="238fd-161">Маркер родительского окна указывается в элементе **хвндпарент** структуры, определенной параметром *лпопен*.</span><span class="sxs-lookup"><span data-stu-id="238fd-161">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="238fd-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ овли \_ Open \_ WS</span><span class="sxs-lookup"><span data-stu-id="238fd-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI\_OVLY\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="238fd-163">Стиль окна указывается в элементе **двстиле** структуры, определенной параметром *лпопен*.</span><span class="sxs-lookup"><span data-stu-id="238fd-163">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span> <span data-ttu-id="238fd-164">Значение **двстиле** задает стиль окна, который будет создан драйвером и отображаемый, если приложение не предоставляет его.</span><span class="sxs-lookup"><span data-stu-id="238fd-164">The **dwStyle** value specifies the style of the window that the driver will create and display if the application does not provide one.</span></span> <span data-ttu-id="238fd-165">Параметр Style принимает целое число, определяющее стиль окна.</span><span class="sxs-lookup"><span data-stu-id="238fd-165">The style parameter takes an integer that defines the window style.</span></span> <span data-ttu-id="238fd-166">Эти константы совпадают со стандартными стилями окна (например \_ , вложенным меню WS, WS \_ ОВЕРЛАППЕДВИНДОВ или WS \_ ).</span><span class="sxs-lookup"><span data-stu-id="238fd-166">These constants are the same as the standard window styles (such as WS\_CHILD, WS\_OVERLAPPEDWINDOW, or WS\_POPUP).</span></span>

</dd> </dl>

<span data-ttu-id="238fd-167">Для устройств с наложением параметр *лпопен* указывает на структуру [**MCI \_ овли \_ Open \_ пармс**](mci-ovly-open-parms.md) Structure.</span><span class="sxs-lookup"><span data-stu-id="238fd-167">For video-overlay devices, the *lpOpen* parameter points to an [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md) structure.</span></span>

<span data-ttu-id="238fd-168">С типом устройства **вавеаудио** используется следующий дополнительный флаг:</span><span class="sxs-lookup"><span data-stu-id="238fd-168">The following additional flag is used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="238fd-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>\_ \_ Открытый буфер MCI \_ Wave</span><span class="sxs-lookup"><span data-stu-id="238fd-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI\_WAVE\_OPEN\_BUFFER</span></span>
</dt> <dd>

<span data-ttu-id="238fd-170">Длина буфера указана в элементе **двбуфферсекондс** структуры, определенной параметром *лпопен*.</span><span class="sxs-lookup"><span data-stu-id="238fd-170">A buffer length is specified in the **dwBufferSeconds** member of the structure identified by *lpOpen*.</span></span>

</dd> </dl>

<span data-ttu-id="238fd-171">Для устройств с аудио-волнами параметр *лпопен* указывает на структуру [**MCI \_ Wave \_ Open \_ пармс**](mci-wave-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="238fd-171">For waveform-audio devices, the *lpOpen* parameter points to an [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) structure.</span></span> <span data-ttu-id="238fd-172">Драйвер МЦИВАВЕ требует наличия асинхронного устройства аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="238fd-172">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="238fd-173">Требования</span><span class="sxs-lookup"><span data-stu-id="238fd-173">Requirements</span></span>



| <span data-ttu-id="238fd-174">Требование</span><span class="sxs-lookup"><span data-stu-id="238fd-174">Requirement</span></span> | <span data-ttu-id="238fd-175">Значение</span><span class="sxs-lookup"><span data-stu-id="238fd-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="238fd-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="238fd-176">Minimum supported client</span></span><br/> | <span data-ttu-id="238fd-177">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="238fd-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="238fd-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="238fd-178">Minimum supported server</span></span><br/> | <span data-ttu-id="238fd-179">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="238fd-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="238fd-180">Заголовок</span><span class="sxs-lookup"><span data-stu-id="238fd-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="238fd-181"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="238fd-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="238fd-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="238fd-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="238fd-183">MCI</span><span class="sxs-lookup"><span data-stu-id="238fd-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="238fd-184">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="238fd-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

