---
description: Граф открывает файл или завершает открытие файла.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf275a2f9b64f9a30c8049b5207622270edc5098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679805"
---
# <a name="ec_opening_file"></a><span data-ttu-id="53950-103">\_файл для открытия \_ файлов EC</span><span class="sxs-lookup"><span data-stu-id="53950-103">EC\_OPENING\_FILE</span></span>

<span data-ttu-id="53950-104">Граф открывает файл или завершает открытие файла.</span><span class="sxs-lookup"><span data-stu-id="53950-104">The graph is opening a file, or has finished opening a file.</span></span>

## <a name="parameters"></a><span data-ttu-id="53950-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="53950-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53950-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="53950-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="53950-107">**Значение true** , если граф начинает открывать файл, или **значение false** , если граф больше не открывает файл.</span><span class="sxs-lookup"><span data-stu-id="53950-107">**TRUE** if the graph is starting to open a file, or **FALSE** if the graph is no longer opening the file.</span></span>

</dd> <dt>

<span data-ttu-id="53950-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="53950-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="53950-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="53950-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="53950-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="53950-110">Default Action</span></span>

<span data-ttu-id="53950-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="53950-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="53950-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="53950-112">Remarks</span></span>

<span data-ttu-id="53950-113">Фильтр может отправить это событие, если оно тратит значительное время на открытие файла.</span><span class="sxs-lookup"><span data-stu-id="53950-113">A filter can send this event if it spends significant time opening a file.</span></span> <span data-ttu-id="53950-114">(Например, файл может находиться в сети.) Приложение может использовать это событие для настройки пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="53950-114">(For example, the file might be located on a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="53950-115">Требования</span><span class="sxs-lookup"><span data-stu-id="53950-115">Requirements</span></span>



| <span data-ttu-id="53950-116">Требование</span><span class="sxs-lookup"><span data-stu-id="53950-116">Requirement</span></span> | <span data-ttu-id="53950-117">Значение</span><span class="sxs-lookup"><span data-stu-id="53950-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53950-118">Header</span><span class="sxs-lookup"><span data-stu-id="53950-118">Header</span></span><br/> | <dl> <span data-ttu-id="53950-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="53950-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53950-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53950-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53950-121">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="53950-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="53950-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="53950-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




