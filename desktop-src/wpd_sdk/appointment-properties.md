---
description: Портативные устройства Windows поддерживают следующие свойства встречи.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Свойства встречи (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 542029f9eb698c8093c43cbb8ee309b3d1f9da6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699004"
---
# <a name="appointment-properties"></a><span data-ttu-id="9dab1-103">Свойства встречи</span><span class="sxs-lookup"><span data-stu-id="9dab1-103">Appointment Properties</span></span>

<span data-ttu-id="9dab1-104">Портативные устройства Windows поддерживают следующие свойства встречи.</span><span class="sxs-lookup"><span data-stu-id="9dab1-104">Windows Portable Devices supports the following appointment properties.</span></span>



| <span data-ttu-id="9dab1-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="9dab1-105">Property</span></span>                                   | <span data-ttu-id="9dab1-106">VarType</span><span class="sxs-lookup"><span data-stu-id="9dab1-106">VarType</span></span>        | <span data-ttu-id="9dab1-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9dab1-107">Description</span></span>                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9dab1-108">**\_встреча, \_ принятая \_ участником WPD**</span><span class="sxs-lookup"><span data-stu-id="9dab1-108">**WPD\_APPOINTMENT\_ACCEPTED\_ATTENDEES**</span></span>  | <span data-ttu-id="9dab1-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9dab1-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9dab1-110">Разделенный точками с запятой список участников, которые приняли встречу.</span><span class="sxs-lookup"><span data-stu-id="9dab1-110">Semicolon-delimited list of attendees who have accepted the appointment.</span></span>             |
| <span data-ttu-id="9dab1-111">**\_встречи с \_ неотклоненной ВСТРЕЧей WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9dab1-111">**WPD\_APPOINTMENT\_DECLINED\_ATTENDEES**</span></span>  | <span data-ttu-id="9dab1-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9dab1-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9dab1-113">Разделенный точками с запятой список участников, которые отклонили встречу.</span><span class="sxs-lookup"><span data-stu-id="9dab1-113">Semicolon-delimited list of attendees who have declined the appointment.</span></span>             |
| <span data-ttu-id="9dab1-114">**\_Расположение встречи \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="9dab1-114">**WPD\_APPOINTMENT\_LOCATION**</span></span>             | <span data-ttu-id="9dab1-115">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="9dab1-115">VT\_LPWSTR</span></span>     | <span data-ttu-id="9dab1-116">Удобное для чтения место встречи, например "здание 5, комната 7".</span><span class="sxs-lookup"><span data-stu-id="9dab1-116">A reader-friendly location of the appointment, for example, "Building 5, Room 7".</span></span>    |
| <span data-ttu-id="9dab1-117">**\_ \_ Дополнительные участники встречи \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="9dab1-117">**WPD\_APPOINTMENT\_OPTIONAL\_ATTENDEES**</span></span>  | <span data-ttu-id="9dab1-118">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9dab1-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9dab1-119">Разделенный точками с запятой список необязательных участников встречи.</span><span class="sxs-lookup"><span data-stu-id="9dab1-119">Semicolon-delimited list of optional attendees for the appointment.</span></span>                  |
| <span data-ttu-id="9dab1-120">**\_Участники, \_ необходимые для встречи с WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9dab1-120">**WPD\_APPOINTMENT\_REQUIRED\_ATTENDEES**</span></span>  | <span data-ttu-id="9dab1-121">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9dab1-121">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9dab1-122">Разделенный точками с запятой список обязательных участников встречи.</span><span class="sxs-lookup"><span data-stu-id="9dab1-122">Semicolon-delimited list of required attendees for the appointment.</span></span>                  |
| <span data-ttu-id="9dab1-123">**\_ресурсы для встреч WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9dab1-123">**WPD\_APPOINTMENT\_RESOURCES**</span></span>            | <span data-ttu-id="9dab1-124">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9dab1-124">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9dab1-125">Разделенный точками с запятой список ресурсов, необходимых для встречи.</span><span class="sxs-lookup"><span data-stu-id="9dab1-125">Semicolon-delimited list of resources required for the appointment.</span></span>                  |
| <span data-ttu-id="9dab1-126">**\_встречи с неоднократными \_ \_ участниками**</span><span class="sxs-lookup"><span data-stu-id="9dab1-126">**WPD\_APPOINTMENT\_TENTATIVE\_ATTENDEES**</span></span> | <span data-ttu-id="9dab1-127">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9dab1-127">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9dab1-128">Разделенный точками с запятой список участников, которые предварительно приняли встречу.</span><span class="sxs-lookup"><span data-stu-id="9dab1-128">Semicolon-delimited list of attendees who have tentatively accepted the appointment.</span></span> |
| <span data-ttu-id="9dab1-129">**\_тип встречи \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="9dab1-129">**WPD\_APPOINTMENT\_TYPE**</span></span>                 | <span data-ttu-id="9dab1-130">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9dab1-130">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9dab1-131">Тип встречи, например "Личное", "Бизнес" и т. д.</span><span class="sxs-lookup"><span data-stu-id="9dab1-131">The type of appointment, for example,"Personal", "Business", and so on.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="9dab1-132">Требования</span><span class="sxs-lookup"><span data-stu-id="9dab1-132">Requirements</span></span>



| <span data-ttu-id="9dab1-133">Требование</span><span class="sxs-lookup"><span data-stu-id="9dab1-133">Requirement</span></span> | <span data-ttu-id="9dab1-134">Значение</span><span class="sxs-lookup"><span data-stu-id="9dab1-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dab1-135">Header</span><span class="sxs-lookup"><span data-stu-id="9dab1-135">Header</span></span><br/> | <dl> <span data-ttu-id="9dab1-136"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dab1-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dab1-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9dab1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dab1-138">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="9dab1-138">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




