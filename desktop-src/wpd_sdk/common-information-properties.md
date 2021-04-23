---
description: Портативные устройства Windows поддерживают следующие общие свойства информации.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Общие сведения о свойствах (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b773d8404997da20b4196c802ba12286679af683
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718043"
---
# <a name="common-information-properties"></a><span data-ttu-id="a13d4-103">Общие сведения о свойствах</span><span class="sxs-lookup"><span data-stu-id="a13d4-103">Common Information Properties</span></span>

<span data-ttu-id="a13d4-104">Портативные устройства Windows поддерживают следующие общие свойства информации.</span><span class="sxs-lookup"><span data-stu-id="a13d4-104">Windows Portable Devices supports the following common information properties.</span></span>



| <span data-ttu-id="a13d4-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="a13d4-105">Property</span></span>                                      | <span data-ttu-id="a13d4-106">VarType</span><span class="sxs-lookup"><span data-stu-id="a13d4-106">VarType</span></span>        | <span data-ttu-id="a13d4-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a13d4-107">Description</span></span>                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a13d4-108">**\_Общие \_ сведения о \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="a13d4-108">**WPD\_COMMON\_INFORMATION\_NOTES**</span></span>           | <span data-ttu-id="a13d4-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a13d4-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="a13d4-110">Для встреч, задач и аналогичных объектов это свойство содержит заметки для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="a13d4-110">For appointments, tasks, and similar objects, this property contains any notes for the given object.</span></span>     |
| <span data-ttu-id="a13d4-111">**\_субъект общей \_ информации о \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="a13d4-111">**WPD\_COMMON\_INFORMATION\_SUBJECT**</span></span>         | <span data-ttu-id="a13d4-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a13d4-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="a13d4-113">Значение типа, указывающее поле темы данного объекта.</span><span class="sxs-lookup"><span data-stu-id="a13d4-113">A value that specifies the subject field of this object.</span></span>                                                 |
| <span data-ttu-id="a13d4-114">**\_ \_ \_ основной текст общей информации о WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a13d4-114">**WPD\_COMMON\_INFORMATION\_BODY\_TEXT**</span></span>      | <span data-ttu-id="a13d4-115">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a13d4-115">**VT\_LPWSTR**</span></span> | <span data-ttu-id="a13d4-116">Это свойство содержит текст тела объекта в формате обычного текста или HTML.</span><span class="sxs-lookup"><span data-stu-id="a13d4-116">This property contains the body text of an object, in plaintext or HTML format.</span></span>                          |
| <span data-ttu-id="a13d4-117">**\_стандартный \_ приоритет данных \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="a13d4-117">**WPD\_COMMON\_INFORMATION\_PRIORITY**</span></span>        | <span data-ttu-id="a13d4-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="a13d4-118">**VT\_UI4**</span></span>    | <span data-ttu-id="a13d4-119">Значение, указывающее приоритет данного объекта.</span><span class="sxs-lookup"><span data-stu-id="a13d4-119">A value that specifies the priority of this object.</span></span> <span data-ttu-id="a13d4-120">0 означает наивысший приоритет.</span><span class="sxs-lookup"><span data-stu-id="a13d4-120">0 indicates the highest priority.</span></span>                    |
| <span data-ttu-id="a13d4-121">**\_ \_ \_ \_ Дата и время начала общей информации для WPD**</span><span class="sxs-lookup"><span data-stu-id="a13d4-121">**WPD\_COMMON\_INFORMATION\_START\_DATETIME**</span></span> | <span data-ttu-id="a13d4-122">**\_Дата VT**</span><span class="sxs-lookup"><span data-stu-id="a13d4-122">**VT\_DATE**</span></span>   | <span data-ttu-id="a13d4-123">Значение типа, указывающее дату и время запланированного запуска встречи, задачи или аналогичного объекта.</span><span class="sxs-lookup"><span data-stu-id="a13d4-123">A value that specifies the date/time that an appointment, task, or similar object is scheduled to start.</span></span> |
| <span data-ttu-id="a13d4-124">**\_ \_ \_ \_ Дата и время окончания общей информации о WPD**</span><span class="sxs-lookup"><span data-stu-id="a13d4-124">**WPD\_COMMON\_INFORMATION\_END\_DATETIME**</span></span>   | <span data-ttu-id="a13d4-125">**\_Дата VT**</span><span class="sxs-lookup"><span data-stu-id="a13d4-125">**VT\_DATE**</span></span>   | <span data-ttu-id="a13d4-126">Значение типа, указывающее дату и время, когда запланировано завершение встречи, задачи или аналогичного объекта.</span><span class="sxs-lookup"><span data-stu-id="a13d4-126">A value that specifies the date/time that an appointment, task, or similar object is scheduled to end.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="a13d4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a13d4-127">Requirements</span></span>



| <span data-ttu-id="a13d4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a13d4-128">Requirement</span></span> | <span data-ttu-id="a13d4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a13d4-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a13d4-130">Header</span><span class="sxs-lookup"><span data-stu-id="a13d4-130">Header</span></span><br/> | <dl> <span data-ttu-id="a13d4-131"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="a13d4-131"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a13d4-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a13d4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a13d4-133">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="a13d4-133">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




