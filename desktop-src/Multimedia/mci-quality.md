---
title: Команда MCI_QUALITY (Ммсистем. h)
description: '\_Команда качества MCI определяет пользовательский уровень качества для сжатия данных в аудио, видео или по-прежнему. Устройство Digital-Video распознает эту команду.'
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- MCI_QUALITY команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996703c1a5b7d3adec1a001af58ebc8d916301a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414729"
---
# <a name="mci_quality-command"></a><span data-ttu-id="c86fc-105">\_Команда качества MCI</span><span class="sxs-lookup"><span data-stu-id="c86fc-105">MCI\_QUALITY command</span></span>

<span data-ttu-id="c86fc-106">\_Команда качества MCI определяет пользовательский уровень качества для сжатия данных в аудио, видео или по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="c86fc-106">The MCI\_QUALITY command defines a custom quality level for audio, video, or still image data compression.</span></span> <span data-ttu-id="c86fc-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="c86fc-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="c86fc-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="c86fc-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
);
```



## <a name="parameters"></a><span data-ttu-id="c86fc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c86fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c86fc-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="c86fc-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c86fc-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="c86fc-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c86fc-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c86fc-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c86fc-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="c86fc-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="c86fc-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c86fc-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c86fc-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*лпкуалити*</span><span class="sxs-lookup"><span data-stu-id="c86fc-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span></span>
</dt> <dd>

<span data-ttu-id="c86fc-116">Указатель на структуру [**\_ \_ \_ пармс качества MCI ДГВ**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="c86fc-116">Pointer to an [**MCI\_DGV\_QUALITY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c86fc-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c86fc-117">Return Value</span></span>

<span data-ttu-id="c86fc-118">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c86fc-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c86fc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c86fc-119">Remarks</span></span>

<span data-ttu-id="c86fc-120">Имя, определенное для этого уровня качества, можно использовать при настройке звука, видео или по-прежнему качества с помощью команд [MCI \_ Сетаудио](mci-setaudio.md) и [MCI \_ сетвидео](mci-setvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="c86fc-120">The name defined for this quality level can be used when setting the audio, video, or still quality with the [MCI\_SETAUDIO](mci-setaudio.md) and [MCI\_SETVIDEO](mci-setvideo.md) commands.</span></span>

<span data-ttu-id="c86fc-121">Следующие дополнительные флаги применяются к устройствам цифрового видео:</span><span class="sxs-lookup"><span data-stu-id="c86fc-121">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="c86fc-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>\_алгоритм качества \_ MCI</span><span class="sxs-lookup"><span data-stu-id="c86fc-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI\_QUALITY\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="c86fc-123">Элемент **лпстралгорисм** структуры, идентифицируемой *лпкуалити* , содержит адрес буфера, содержащего имя алгоритма.</span><span class="sxs-lookup"><span data-stu-id="c86fc-123">The **lpstrAlgorithm** member of the structure identified by *lpQuality* contains an address of a buffer containing the name of the algorithm.</span></span> <span data-ttu-id="c86fc-124">Этот алгоритм должен поддерживаться драйвером устройства и должен быть совместим с используемым аудио-или видеодескриптором.</span><span class="sxs-lookup"><span data-stu-id="c86fc-124">This algorithm must be supported by the device driver, and must be compatible with the audio, still, or video descriptor that is used.</span></span> <span data-ttu-id="c86fc-125">Если этот флаг опущен, используется текущий алгоритм.</span><span class="sxs-lookup"><span data-stu-id="c86fc-125">If this flag is omitted, the current algorithm is used.</span></span>

</dd> <dt>

<span data-ttu-id="c86fc-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>\_ \_ диалоговое окно качества MCI</span><span class="sxs-lookup"><span data-stu-id="c86fc-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>MCI\_QUALITY\_DIALOG</span></span>
</dt> <dd>

<span data-ttu-id="c86fc-127">Драйвер устройства должен отображать диалоговое окно для указания уровня качества.</span><span class="sxs-lookup"><span data-stu-id="c86fc-127">The device driver should display a dialog box for specifying the quality level.</span></span> <span data-ttu-id="c86fc-128">Диалоговое окно содержит внутренние поля, используемые драйвером устройства для создания структуры, описывающей конкретный уровень качества.</span><span class="sxs-lookup"><span data-stu-id="c86fc-128">The dialog box has algorithm-specific fields used internally by the device driver to create a structure describing a specific quality level.</span></span>

</dd> <dt>

<span data-ttu-id="c86fc-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>\_маркер качества \_ MCI</span><span class="sxs-lookup"><span data-stu-id="c86fc-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI\_QUALITY\_HANDLE</span></span>
</dt> <dd>

<span data-ttu-id="c86fc-130">Элемент **двхандле** структуры, идентифицируемой *лпкуалити* , содержит маркер для структуры.</span><span class="sxs-lookup"><span data-stu-id="c86fc-130">The **dwHandle** member of the structure identified by *lpQuality* contains a handle to a structure.</span></span> <span data-ttu-id="c86fc-131">Структура содержит зависящие от алгоритма данные, описывающие конкретный уровень качества.</span><span class="sxs-lookup"><span data-stu-id="c86fc-131">The structure contains algorithmic-specific data describing the specific quality level.</span></span> <span data-ttu-id="c86fc-132">Формат структур для алгоритмов зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="c86fc-132">The format of the structures for the algorithms is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="c86fc-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>\_элемент качества \_ MCI</span><span class="sxs-lookup"><span data-stu-id="c86fc-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>MCI\_QUALITY\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="c86fc-134">Константа, указывающая тип алгоритма, включенный в элемент **двитем** структуры, идентифицируемой *лпкуалити*.</span><span class="sxs-lookup"><span data-stu-id="c86fc-134">A constant indicating the type of algorithm is included in the **dwItem** member of the structure identified by *lpQuality*.</span></span>

</dd> <dt>

<span data-ttu-id="c86fc-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>\_имя качества \_ MCI</span><span class="sxs-lookup"><span data-stu-id="c86fc-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>MCI\_QUALITY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="c86fc-136">Элемент **лпстрнаме** структуры, идентифицируемой *лпкуалити* , содержит адрес буфера, содержащего дескриптор качества.</span><span class="sxs-lookup"><span data-stu-id="c86fc-136">The **lpstrName** member of the structure identified by *lpQuality* contains an address of a buffer containing the quality descriptor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c86fc-137">Требования</span><span class="sxs-lookup"><span data-stu-id="c86fc-137">Requirements</span></span>



| <span data-ttu-id="c86fc-138">Требование</span><span class="sxs-lookup"><span data-stu-id="c86fc-138">Requirement</span></span> | <span data-ttu-id="c86fc-139">Значение</span><span class="sxs-lookup"><span data-stu-id="c86fc-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c86fc-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c86fc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c86fc-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c86fc-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c86fc-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c86fc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c86fc-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c86fc-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c86fc-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c86fc-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c86fc-145"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c86fc-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c86fc-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c86fc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c86fc-147">MCI</span><span class="sxs-lookup"><span data-stu-id="c86fc-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c86fc-148">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="c86fc-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

