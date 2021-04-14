---
description: Отправляется фильтром модуля чтения WM ASF при чтении файлов ASF, защищенных с помощью управления цифровыми правами (DRM).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651665"
---
# <a name="ec_wmt_event-dshowh"></a><span data-ttu-id="9b0b5-103">EC_WMT_EVENT (DShow. h)</span><span class="sxs-lookup"><span data-stu-id="9b0b5-103">EC_WMT_EVENT (Dshow.h)</span></span>

<span data-ttu-id="9b0b5-104">Отправляется фильтром [модуля чтения WM ASF](wm-asf-reader-filter.md) при чтении файлов ASF, защищенных с помощью управления цифровыми правами (DRM).</span><span class="sxs-lookup"><span data-stu-id="9b0b5-104">Sent by the [WM ASF Reader](wm-asf-reader-filter.md) filter when it reads ASF files protected by digital rights management (DRM).</span></span>

## <a name="parameters"></a><span data-ttu-id="9b0b5-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b0b5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b0b5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9b0b5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9b0b5-107">Одно из следующих значений **\_ состояния ВМТ** :</span><span class="sxs-lookup"><span data-stu-id="9b0b5-107">One of the following **WMT\_STATUS** values:</span></span>



| <span data-ttu-id="9b0b5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9b0b5-108">Value</span></span>                         | <span data-ttu-id="9b0b5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9b0b5-109">Description</span></span>                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b0b5-110">ВМТ \_ получить \_ лицензию</span><span class="sxs-lookup"><span data-stu-id="9b0b5-110">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="9b0b5-111">Посылается, когда компонент DRM завершил процесс приобретения лицензии успешно или неудачно.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-111">Sent when the DRM component has completed the license acquisition process, either successfully or unsuccessfully.</span></span> |
| <span data-ttu-id="9b0b5-112">ВМТ \_ индивидуализируйте</span><span class="sxs-lookup"><span data-stu-id="9b0b5-112">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="9b0b5-113">Процесс обновления безопасности завершен успешно или неудачно.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-113">The security upgrade process has completed, either successfully or unsuccessfully.</span></span>                                |
| <span data-ttu-id="9b0b5-114">ВМТ \_ нуждается в \_ индивидуализации</span><span class="sxs-lookup"><span data-stu-id="9b0b5-114">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="9b0b5-115">Для выполнения запрошенного действия в файле необходимо, чтобы приложение получало обновление системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-115">The file requires that an application receive a security upgrade before performing the requested action.</span></span>          |
| <span data-ttu-id="9b0b5-116">ВМТ \_ без \_ прав</span><span class="sxs-lookup"><span data-stu-id="9b0b5-116">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="9b0b5-117">Приложение не имеет прав на выполнение запрошенного действия с файлом, защищенным DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-117">The application has no rights to perform he requested action on a file protected by DRM version 1.</span></span>                |
| <span data-ttu-id="9b0b5-118">ВМТ \_ без \_ прав \_</span><span class="sxs-lookup"><span data-stu-id="9b0b5-118">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="9b0b5-119">Приложение не имеет прав на выполнение запрошенного действия с файлом, защищенным DRM версии 7.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-119">The application has no rights to perform he requested action on a file protected by DRM version 7.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="9b0b5-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9b0b5-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9b0b5-121">Указатель на структуру [**\_ \_ \_ данных события ВМТ**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) , которая содержит сведения о событии, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-121">Pointer to an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) structure that contains information about the event, or **NULL**.</span></span> <span data-ttu-id="9b0b5-122">Элемент **pData** этой структуры указывает на дополнительные данные, тип которых зависит от значения **lParam1**, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-122">The **pData** member of this structure points to additional data, whose type depends on the value of **lParam1**, as shown in the following table.</span></span>



| <span data-ttu-id="9b0b5-123">lParam1</span><span class="sxs-lookup"><span data-stu-id="9b0b5-123">lParam1</span></span>                       | <span data-ttu-id="9b0b5-124">\_ВМТ \_ события \_ Data. pdata</span><span class="sxs-lookup"><span data-stu-id="9b0b5-124">AM\_WMT\_EVENT\_DATA.pData</span></span>                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b0b5-125">ВМТ \_ получить \_ лицензию</span><span class="sxs-lookup"><span data-stu-id="9b0b5-125">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="9b0b5-126">Указатель на структуру [**\_ \_ \_ данных лицензии WM Get**](/windows/desktop/wmformat/wm-get-license-data) .</span><span class="sxs-lookup"><span data-stu-id="9b0b5-126">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span> <span data-ttu-id="9b0b5-127">Эта структура описана в пакете SDK для формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-127">This structure is documented in the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="9b0b5-128">ВМТ \_ индивидуализируйте</span><span class="sxs-lookup"><span data-stu-id="9b0b5-128">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="9b0b5-129">Указатель на структуру [**\_ \_ состояния WM индивидуализируйте**](/windows/desktop/wmformat/wm-individualize-status) .</span><span class="sxs-lookup"><span data-stu-id="9b0b5-129">Pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](/windows/desktop/wmformat/wm-individualize-status) structure.</span></span>                                                        |
| <span data-ttu-id="9b0b5-130">ВМТ \_ нуждается в \_ индивидуализации</span><span class="sxs-lookup"><span data-stu-id="9b0b5-130">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="9b0b5-131">**Значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-131">**NULL**.</span></span>                                                                                                                                        |
| <span data-ttu-id="9b0b5-132">ВМТ \_ без \_ прав</span><span class="sxs-lookup"><span data-stu-id="9b0b5-132">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="9b0b5-133">Указатель на строку расширенных символов, содержащую URL-адрес запроса.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-133">Pointer to a wide-character string containing a challenge URL.</span></span>                                                                                   |
| <span data-ttu-id="9b0b5-134">ВМТ \_ без \_ прав \_</span><span class="sxs-lookup"><span data-stu-id="9b0b5-134">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="9b0b5-135">Указатель на структуру [**\_ \_ \_ данных лицензии WM Get**](/windows/desktop/wmformat/wm-get-license-data) .</span><span class="sxs-lookup"><span data-stu-id="9b0b5-135">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span>                                                               |



 

<span data-ttu-id="9b0b5-136">Значение *lParam2* может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-136">The value of *lParam2* might be **NULL**.</span></span> <span data-ttu-id="9b0b5-137">Проверьте значение перед разыменованием указателя.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-137">Check the value before dereferencing the pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b0b5-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b0b5-138">Remarks</span></span>

<span data-ttu-id="9b0b5-139">Дополнительные сведения о включении воспроизведения файлов, защищенных с помощью DRM, см. в документации пакета Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="9b0b5-139">See the Windows Media Format SDK documentation for more information on enabling playback of DRM-protected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b0b5-140">Требования</span><span class="sxs-lookup"><span data-stu-id="9b0b5-140">Requirements</span></span>



| <span data-ttu-id="9b0b5-141">Требование</span><span class="sxs-lookup"><span data-stu-id="9b0b5-141">Requirement</span></span> | <span data-ttu-id="9b0b5-142">Значение</span><span class="sxs-lookup"><span data-stu-id="9b0b5-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b0b5-143">Header</span><span class="sxs-lookup"><span data-stu-id="9b0b5-143">Header</span></span><br/> | <dl> <span data-ttu-id="9b0b5-144"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b0b5-144"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b0b5-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b0b5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b0b5-146">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="9b0b5-146">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="9b0b5-147">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="9b0b5-147">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

