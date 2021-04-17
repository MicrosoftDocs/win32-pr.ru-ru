---
description: Портативные устройства Windows поддерживают следующие свойства задач.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Свойства задачи (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704251"
---
# <a name="task-properties"></a><span data-ttu-id="d4edd-103">Свойства задачи</span><span class="sxs-lookup"><span data-stu-id="d4edd-103">Task Properties</span></span>

<span data-ttu-id="d4edd-104">Портативные устройства Windows поддерживают следующие свойства задач.</span><span class="sxs-lookup"><span data-stu-id="d4edd-104">Windows Portable Devices supports the following task properties.</span></span>



| <span data-ttu-id="d4edd-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="d4edd-105">Property</span></span>                         | <span data-ttu-id="d4edd-106">VarType</span><span class="sxs-lookup"><span data-stu-id="d4edd-106">VarType</span></span>        | <span data-ttu-id="d4edd-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d4edd-107">Description</span></span>                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4edd-108">**\_владелец задачи \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="d4edd-108">**WPD\_TASK\_OWNER**</span></span>             | <span data-ttu-id="d4edd-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="d4edd-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d4edd-110">Владелец задачи.</span><span class="sxs-lookup"><span data-stu-id="d4edd-110">The owner of the task.</span></span>                                                                      |
| <span data-ttu-id="d4edd-111">**\_ \_ процент выполнения задачи \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="d4edd-111">**WPD\_TASK\_PERCENT\_COMPLETE**</span></span> | <span data-ttu-id="d4edd-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="d4edd-112">**VT\_UI4**</span></span>    | <span data-ttu-id="d4edd-113">Число от 0 до 100, указывающее, как завершается задача.</span><span class="sxs-lookup"><span data-stu-id="d4edd-113">A number between 0 and 100 that specifies how complete the task is.</span></span>                         |
| <span data-ttu-id="d4edd-114">**\_ \_ Дата напоминания о ЗАДАЧе WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d4edd-114">**WPD\_TASK\_REMINDER\_DATE**</span></span>    | <span data-ttu-id="d4edd-115">**\_Дата VT**</span><span class="sxs-lookup"><span data-stu-id="d4edd-115">**VT\_DATE**</span></span>   | <span data-ttu-id="d4edd-116">Значение, указывающее, когда следует отправить напоминание для выполнения задачи, если оно не завершено.</span><span class="sxs-lookup"><span data-stu-id="d4edd-116">A value that specifies when a reminder should be sent to perform the task, if not complete.</span></span> |
| <span data-ttu-id="d4edd-117">**\_состояние задачи \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="d4edd-117">**WPD\_TASK\_STATUS**</span></span>            | <span data-ttu-id="d4edd-118">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="d4edd-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="d4edd-119">Строковое описание состояния задачи, например "выполняется".</span><span class="sxs-lookup"><span data-stu-id="d4edd-119">A string description of the status of the task, for example, "In Progress".</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="d4edd-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d4edd-120">Requirements</span></span>



| <span data-ttu-id="d4edd-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d4edd-121">Requirement</span></span> | <span data-ttu-id="d4edd-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d4edd-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4edd-123">Header</span><span class="sxs-lookup"><span data-stu-id="d4edd-123">Header</span></span><br/> | <dl> <span data-ttu-id="d4edd-124"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4edd-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4edd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4edd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4edd-126">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="d4edd-126">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




