---
description: Граф помещает данные в буфер или прекратил буферизацию данных.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1395a10458abd7a29fdb65e7ab55fba62328d6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675577"
---
# <a name="ec_buffering_data"></a><span data-ttu-id="d2755-103">\_данные буферизации \_ EC</span><span class="sxs-lookup"><span data-stu-id="d2755-103">EC\_BUFFERING\_DATA</span></span>

<span data-ttu-id="d2755-104">Граф помещает данные в буфер или прекратил буферизацию данных.</span><span class="sxs-lookup"><span data-stu-id="d2755-104">The graph is buffering data, or has stopped buffering data.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2755-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2755-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2755-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d2755-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d2755-107">(**Bool**) **Значение true** , если граф начинается с buffer, или **значение false** , если граф прекратил буферизацию.</span><span class="sxs-lookup"><span data-stu-id="d2755-107">(**BOOL**) **TRUE** if the graph is starting to buffer, or **FALSE** if the graph has stopped buffering.</span></span>

</dd> <dt>

<span data-ttu-id="d2755-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d2755-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d2755-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="d2755-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="d2755-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d2755-110">Default Action</span></span>

<span data-ttu-id="d2755-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="d2755-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2755-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="d2755-112">Remarks</span></span>

<span data-ttu-id="d2755-113">Фильтр может отправить это событие, если ему нужно поместить данные из внешнего источника в буфер.</span><span class="sxs-lookup"><span data-stu-id="d2755-113">A filter can send this event if it needs to buffer data from an external source.</span></span> <span data-ttu-id="d2755-114">(Например, это может быть загрузка данных из сети.) Приложение может использовать это событие для настройки пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d2755-114">(For example, it might be loading data from a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2755-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d2755-115">Requirements</span></span>



| <span data-ttu-id="d2755-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d2755-116">Requirement</span></span> | <span data-ttu-id="d2755-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d2755-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2755-118">Header</span><span class="sxs-lookup"><span data-stu-id="d2755-118">Header</span></span><br/> | <dl> <span data-ttu-id="d2755-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2755-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2755-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2755-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2755-121">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="d2755-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d2755-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="d2755-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




