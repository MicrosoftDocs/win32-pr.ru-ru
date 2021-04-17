---
description: Уведомляет о ходе выполнения приложения при открытии сетевого файла.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679810"
---
# <a name="ec_loadstatus"></a><span data-ttu-id="48883-103">EC \_ лоадстатус</span><span class="sxs-lookup"><span data-stu-id="48883-103">EC\_LOADSTATUS</span></span>

<span data-ttu-id="48883-104">Уведомляет о ходе выполнения приложения при открытии сетевого файла.</span><span class="sxs-lookup"><span data-stu-id="48883-104">Notifies the application of progress when opening a network file.</span></span>

## <a name="parameters"></a><span data-ttu-id="48883-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="48883-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48883-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="48883-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="48883-107">Код состояния.</span><span class="sxs-lookup"><span data-stu-id="48883-107">Status code.</span></span> <span data-ttu-id="48883-108">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="48883-108">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="48883-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="48883-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="48883-110">Ноль.</span><span class="sxs-lookup"><span data-stu-id="48883-110">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="48883-111">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="48883-111">Default Action</span></span>

<span data-ttu-id="48883-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="48883-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="48883-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="48883-113">Remarks</span></span>

<span data-ttu-id="48883-114">Это событие отправляется фильтром [чтения WM ASF](wm-asf-reader-filter.md) и устаревшим фильтром [источников Windows Media](windows-media-source-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="48883-114">The [WM ASF Reader](wm-asf-reader-filter.md) filter and the legacy [Windows Media Source](windows-media-source-filter.md) filter send this event.</span></span> <span data-ttu-id="48883-115">Первый параметр события имеет одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="48883-115">The first event parameter has one of the following values.</span></span>



| <span data-ttu-id="48883-116">Значение</span><span class="sxs-lookup"><span data-stu-id="48883-116">Value</span></span>                        | <span data-ttu-id="48883-117">Описание</span><span class="sxs-lookup"><span data-stu-id="48883-117">Description</span></span>                                    |
|------------------------------|------------------------------------------------|
| <span data-ttu-id="48883-118">\_лоадстатус \_ закрыто</span><span class="sxs-lookup"><span data-stu-id="48883-118">AM\_LOADSTATUS\_CLOSED</span></span>       | <span data-ttu-id="48883-119">Фильтр источника закрыл файл.</span><span class="sxs-lookup"><span data-stu-id="48883-119">The source filter has closed the file.</span></span>         |
| <span data-ttu-id="48883-120">\_Подключение лоадстатус \_</span><span class="sxs-lookup"><span data-stu-id="48883-120">AM\_LOADSTATUS\_CONNECTING</span></span>   | <span data-ttu-id="48883-121">Фильтр источника подключается к серверу.</span><span class="sxs-lookup"><span data-stu-id="48883-121">The source filter is connecting to the server.</span></span> |
| <span data-ttu-id="48883-122">\_лоадстатус \_ лоадингдескр</span><span class="sxs-lookup"><span data-stu-id="48883-122">AM\_LOADSTATUS\_LOADINGDESCR</span></span> | <span data-ttu-id="48883-123">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48883-123">Not used.</span></span>                                      |
| <span data-ttu-id="48883-124">\_лоадстатус \_ лоадингмкаст</span><span class="sxs-lookup"><span data-stu-id="48883-124">AM\_LOADSTATUS\_LOADINGMCAST</span></span> | <span data-ttu-id="48883-125">Не используется</span><span class="sxs-lookup"><span data-stu-id="48883-125">Not used</span></span>                                       |
| <span data-ttu-id="48883-126">\_лоадстатус \_ расположение</span><span class="sxs-lookup"><span data-stu-id="48883-126">AM\_LOADSTATUS\_LOCATING</span></span>     | <span data-ttu-id="48883-127">Фильтр источника наследует поиск запрошенных данных.</span><span class="sxs-lookup"><span data-stu-id="48883-127">The source filter is locating requested data.</span></span>  |
| <span data-ttu-id="48883-128">\_открытая лоадстатус \_</span><span class="sxs-lookup"><span data-stu-id="48883-128">AM\_LOADSTATUS\_OPEN</span></span>         | <span data-ttu-id="48883-129">Фильтр источника открыл файл.</span><span class="sxs-lookup"><span data-stu-id="48883-129">The source filter has opened the file.</span></span>         |
| <span data-ttu-id="48883-130">\_лоадстатус \_ Открытие</span><span class="sxs-lookup"><span data-stu-id="48883-130">AM\_LOADSTATUS\_OPENING</span></span>      | <span data-ttu-id="48883-131">Фильтр источника открывает файл.</span><span class="sxs-lookup"><span data-stu-id="48883-131">The source filter is opening the file.</span></span>         |



 

## <a name="requirements"></a><span data-ttu-id="48883-132">Требования</span><span class="sxs-lookup"><span data-stu-id="48883-132">Requirements</span></span>



| <span data-ttu-id="48883-133">Требование</span><span class="sxs-lookup"><span data-stu-id="48883-133">Requirement</span></span> | <span data-ttu-id="48883-134">Значение</span><span class="sxs-lookup"><span data-stu-id="48883-134">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="48883-135">Header</span><span class="sxs-lookup"><span data-stu-id="48883-135">Header</span></span><br/> | <dl> <span data-ttu-id="48883-136"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="48883-136"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48883-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48883-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48883-138">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="48883-138">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="48883-139">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="48883-139">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




