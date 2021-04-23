---
title: Команда MCI_LIST (Ммсистем. h)
description: Команда MCI \_ List получает сведения о количестве и типах входных данных, доступных для устройства. Эта команда распознает устройства цифрового видео и ВИДЕОМАГНИТОФОНА.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- MCI_LIST команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535423"
---
# <a name="mci_list-command"></a><span data-ttu-id="ba1b3-105">\_Команда MCI List</span><span class="sxs-lookup"><span data-stu-id="ba1b3-105">MCI\_LIST command</span></span>

<span data-ttu-id="ba1b3-106">Команда MCI \_ List получает сведения о количестве и типах входных данных, доступных для устройства.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-106">The MCI\_LIST command obtains information about the number and types of inputs available to the device.</span></span> <span data-ttu-id="ba1b3-107">Эта команда распознает устройства цифрового видео и ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="ba1b3-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
);
```



## <a name="parameters"></a><span data-ttu-id="ba1b3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba1b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba1b3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="ba1b3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ba1b3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="ba1b3-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ba1b3-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*лплист*</span><span class="sxs-lookup"><span data-stu-id="ba1b3-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ba1b3-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="ba1b3-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="ba1b3-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba1b3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba1b3-118">Return Value</span></span>

<span data-ttu-id="ba1b3-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba1b3-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba1b3-120">Remarks</span></span>

<span data-ttu-id="ba1b3-121">Следующие дополнительные флаги применяются к типу устройства **дигиталвидео** :</span><span class="sxs-lookup"><span data-stu-id="ba1b3-121">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ba1b3-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>\_ \_ список \_ алгоритмов MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="ba1b3-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI\_DGV\_LIST\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-123">Элемент **лпстралгорисм** структуры, идентифицируемой *лплист* , содержит адрес буфера, содержащего имя алгоритма.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-123">The **lpstrAlgorithm** member of the structure identified by *lpList* contains an address of a buffer containing the name of an algorithm.</span></span> <span data-ttu-id="ba1b3-124">Имя используется для получения типов дескрипторов качества, связанных с алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-124">The name is used to retrieve the types of quality descriptors associated with an algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>\_ \_ число СПИСКОВ ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="ba1b3-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI\_DGV\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-126">Возвращает число параметров указанного типа.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-126">Returns the number of options of the specified type.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>\_ \_ элемент списка ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="ba1b3-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI\_DGV\_LIST\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-128">Константа, указывающая, что тип списка включен в элемент **двитем** структуры, идентифицируемой *лплист*.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-128">A constant indicating the list type is included in the **dwItem** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="ba1b3-129">Этот флаг является обязательным.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-129">This flag is required.</span></span> <span data-ttu-id="ba1b3-130">Чтобы указать тип списка, используйте одну из следующих констант:</span><span class="sxs-lookup"><span data-stu-id="ba1b3-130">Use one of the following constants to indicate the list type:</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ ДГВ \_ список \_ звуковых \_ алгоритмов</span><span class="sxs-lookup"><span data-stu-id="ba1b3-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI\_DGV\_LIST\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-132">Команда должна получить имена звуковых алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-132">The command should retrieve names of audio algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>\_ \_ качество звука в списке ДГВ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="ba1b3-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI\_DGV\_LIST\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-134">Команда должна получить уровни качества звука.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-134">The command should retrieve audio quality levels.</span></span> <span data-ttu-id="ba1b3-135">Возвращаемые уровни связаны с алгоритмом, на который ссылается элемент **лпстралгорисм** структуры, идентифицируемой *лплист*.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-135">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="ba1b3-136">Если этот элемент указан с помощью строки "Current", то возвращаются качества, связанные с текущим алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-136">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>\_ \_ поток аудио в списке ДГВ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="ba1b3-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI\_DGV\_LIST\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-138">Команда должна получить имена звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-138">The command should retrieve names of audio streams.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>\_список ДГВ \_ MCI \_ все равно \_ ВС</span><span class="sxs-lookup"><span data-stu-id="ba1b3-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI\_DGV\_LIST\_STILL\_AL</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-140">Команда должна получить имена алгоритмов по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-140">The command should retrieve names of still algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>\_ \_ \_ все еще качество списка ДГВ MCI \_</span><span class="sxs-lookup"><span data-stu-id="ba1b3-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI\_DGV\_LIST\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-142">Команда должна получить уровни качества.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-142">The command should retrieve quality levels.</span></span> <span data-ttu-id="ba1b3-143">Возвращаемые уровни связаны с алгоритмом, на который ссылается элемент **лпстралгорисм** структуры, идентифицируемой *лплист*.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-143">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="ba1b3-144">Если этот элемент указан с помощью строки "Current", то возвращаются качества, связанные с текущим алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-144">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>\_устройство MCI \_ ДГВ \_ List \_ ALG</span><span class="sxs-lookup"><span data-stu-id="ba1b3-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI\_DGV\_LIST\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-146">Команда должна получить имена алгоритмов видео.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-146">The command should retrieve names of video algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>\_ \_ качество видео в списке ДГВ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="ba1b3-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI\_DGV\_LIST\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-148">Команда должна получить уровни качества видео.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-148">The command should retrieve video quality levels.</span></span> <span data-ttu-id="ba1b3-149">Возвращаемые уровни связаны с алгоритмом, на который ссылается элемент **лпстралгорисм** структуры, идентифицируемой *лплист*.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-149">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="ba1b3-150">Если этот элемент указан с помощью строки "Current", то возвращаются качества, связанные с текущим алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-150">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>\_ \_ \_ источник видео ДГВ MCI \_ List</span><span class="sxs-lookup"><span data-stu-id="ba1b3-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI\_DGV\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-152">Команда должна возвращать сведения об источниках видео.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-152">The command should return information about the video sources.</span></span> <span data-ttu-id="ba1b3-153">При использовании с \_ \_ \_ количеством элементов MCI ДГВ команда возвращает число источников видео.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-153">When used with MCI\_DGV\_LIST\_COUNT, the command returns the number of video sources.</span></span> <span data-ttu-id="ba1b3-154">При использовании с \_ \_ номером списка MCI ДГВ \_ команда возвращает тип источника видео.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-154">When used with MCI\_DGV\_LIST\_NUMBER, the command returns the type of a video source.</span></span> <span data-ttu-id="ba1b3-155">MCI определяет следующие типы:</span><span class="sxs-lookup"><span data-stu-id="ba1b3-155">MCI defines the following types:</span></span>

-   <span data-ttu-id="ba1b3-156">\_универсальный ДГВ MCI \_ сетвидео \_ src \_</span><span class="sxs-lookup"><span data-stu-id="ba1b3-156">MCI\_DGV\_SETVIDEO\_SRC\_GENERIC</span></span>
-   <span data-ttu-id="ba1b3-157">MCI \_ ДГВ \_ сетвидео \_ src \_ NTSC</span><span class="sxs-lookup"><span data-stu-id="ba1b3-157">MCI\_DGV\_SETVIDEO\_SRC\_NTSC</span></span>
-   <span data-ttu-id="ba1b3-158">MCI \_ ДГВ \_ сетвидео \_ src \_ PAL</span><span class="sxs-lookup"><span data-stu-id="ba1b3-158">MCI\_DGV\_SETVIDEO\_SRC\_PAL</span></span>
-   <span data-ttu-id="ba1b3-159">MCI \_ ДГВ \_ сетвидео \_ src \_ RGB</span><span class="sxs-lookup"><span data-stu-id="ba1b3-159">MCI\_DGV\_SETVIDEO\_SRC\_RGB</span></span>
-   <span data-ttu-id="ba1b3-160">MCI \_ ДГВ \_ сетвидео \_ src \_ СЕКАМ</span><span class="sxs-lookup"><span data-stu-id="ba1b3-160">MCI\_DGV\_SETVIDEO\_SRC\_SECAM</span></span>
-   <span data-ttu-id="ba1b3-161">MCI \_ ДГВ \_ сетвидео \_ src \_ свидео</span><span class="sxs-lookup"><span data-stu-id="ba1b3-161">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO</span></span>

<span data-ttu-id="ba1b3-162">Может быть больше одного источника для каждого возвращаемого типа.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-162">There might be more than one source of each type returned.</span></span> <span data-ttu-id="ba1b3-163">Универсальный тип источника используется, когда для этого соединителя разрешено больше одного типа сигналов.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-163">The generic source type is used when more then one type of signal is allowed for that connector.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>\_ \_ поток видео со СПИСКОМ ДГВ \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="ba1b3-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI\_DGV\_LIST\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-165">Команда должна получить имена видеопотоков.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-165">The command should retrieve names of video streams.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>\_ \_ номер списка ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="ba1b3-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI\_DGV\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-167">Индекс указывается в элементе **двнумбер** структуры, определенной параметром *лплист*.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-167">An index is specified in the **dwNumber** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="ba1b3-168">Индекс должен быть целым числом от 1 до значения, возвращаемого для \_ \_ \_ флага ДГВ списка элементов MCI.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-168">The index must be an integer between 1 and the value returned for the MCI\_DGV\_LIST\_COUNT flag.</span></span>

</dd> </dl>

<span data-ttu-id="ba1b3-169">Для устройств с цифровыми видео *лплист* указывает на структуру [**ДГВ MCI \_ \_ List \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="ba1b3-169">For digital-video devices, *lpList* points to an [**MCI\_DGV\_LIST\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) structure.</span></span>

<span data-ttu-id="ba1b3-170">Следующие дополнительные флаги применяются к типу устройства **видеомагнитофона** :</span><span class="sxs-lookup"><span data-stu-id="ba1b3-170">The following additional flags apply to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ba1b3-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>\_ \_ источник звука для списка видеомагнитофона \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="ba1b3-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>MCI\_VCR\_LIST\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-172">Перечисление входов или типов звука.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-172">List audio inputs or types.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>\_ \_ число СПИСКОВ видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="ba1b3-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>MCI\_VCR\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-174">Задает для элемента **двретурн** структуры, определяемой параметром *лплист* , общее количество входных видео или аудио.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-174">Sets the **dwReturn** member of the structure identified by *lpList* to the total number of video or audio inputs.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>\_ \_ номер списка видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="ba1b3-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI\_VCR\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-176">Задает элемент **двретурн** структуры, идентифицируемой *лплист* , на тип входного видео или звука, указанного в элементе **двнумбер** .</span><span class="sxs-lookup"><span data-stu-id="ba1b3-176">Sets the **dwReturn** member of the structure identified by *lpList* to the type of the video or audio input specified by the **dwNumber** member.</span></span>

</dd> <dt>

<span data-ttu-id="ba1b3-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>\_ \_ источник видео со списком видеомагнитофонов MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba1b3-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>MCI\_VCR\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="ba1b3-178">Вывод списка входных и типов видео.</span><span class="sxs-lookup"><span data-stu-id="ba1b3-178">List video inputs or types.</span></span>

</dd> </dl>

<span data-ttu-id="ba1b3-179">Для устройств ВИДЕОМАГНИТОФОНА *лплист* указывает на структуру пармс в виде [**\_ \_ списка \_ видеомагнитофонов MCI**](mci-vcr-list-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ba1b3-179">For VCR devices, *lpList* points to an [**MCI\_VCR\_LIST\_PARMS**](mci-vcr-list-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba1b3-180">Требования</span><span class="sxs-lookup"><span data-stu-id="ba1b3-180">Requirements</span></span>



| <span data-ttu-id="ba1b3-181">Требование</span><span class="sxs-lookup"><span data-stu-id="ba1b3-181">Requirement</span></span> | <span data-ttu-id="ba1b3-182">Значение</span><span class="sxs-lookup"><span data-stu-id="ba1b3-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba1b3-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba1b3-183">Minimum supported client</span></span><br/> | <span data-ttu-id="ba1b3-184">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ba1b3-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ba1b3-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba1b3-185">Minimum supported server</span></span><br/> | <span data-ttu-id="ba1b3-186">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ba1b3-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ba1b3-187">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ba1b3-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba1b3-188"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba1b3-188"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba1b3-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba1b3-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba1b3-190">MCI</span><span class="sxs-lookup"><span data-stu-id="ba1b3-190">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ba1b3-191">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="ba1b3-191">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

