---
description: Каждый тип защищаемого объекта имеет набор прав доступа, соответствующих операциям, относящимся к этому типу объекта.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Стандартные права доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897770"
---
# <a name="standard-access-rights"></a><span data-ttu-id="c675e-103">Стандартные права доступа</span><span class="sxs-lookup"><span data-stu-id="c675e-103">Standard Access Rights</span></span>

<span data-ttu-id="c675e-104">Каждый тип защищаемого объекта имеет набор прав доступа, соответствующих операциям, относящимся к этому типу объекта.</span><span class="sxs-lookup"><span data-stu-id="c675e-104">Each type of securable object has a set of access rights that correspond to operations specific to that type of object.</span></span> <span data-ttu-id="c675e-105">Помимо этих прав доступа для конкретного объекта существует набор стандартных прав доступа, соответствующих операциям, общим для большинства типов защищаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="c675e-105">In addition to these object-specific access rights, there is a set of standard access rights that correspond to operations common to most types of securable objects.</span></span>

<span data-ttu-id="c675e-106">[Формат маски доступа](access-mask-format.md) включает набор битов для стандартных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c675e-106">The [access mask format](access-mask-format.md) includes a set of bits for the standard access rights.</span></span> <span data-ttu-id="c675e-107">Следующие константы Windows для стандартных прав доступа определяются в Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="c675e-107">The following Windows constants for standard access rights are defined in Winnt.h.</span></span>



| <span data-ttu-id="c675e-108">Константа</span><span class="sxs-lookup"><span data-stu-id="c675e-108">Constant</span></span>      | <span data-ttu-id="c675e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="c675e-109">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c675e-110">DELETE</span><span class="sxs-lookup"><span data-stu-id="c675e-110">DELETE</span></span>        | <span data-ttu-id="c675e-111">Право на удаление объекта.</span><span class="sxs-lookup"><span data-stu-id="c675e-111">The right to delete the object.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c675e-112">\_Контроль чтения</span><span class="sxs-lookup"><span data-stu-id="c675e-112">READ\_CONTROL</span></span> | <span data-ttu-id="c675e-113">Право на чтение сведений в [*дескрипторе безопасности*](/windows/desktop/SecGloss/s-gly)объекта, не включая сведения из [*системного списка управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="c675e-113">The right to read the information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), not including the information in the [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> |
| <span data-ttu-id="c675e-114">SYNCHRONIZE</span><span class="sxs-lookup"><span data-stu-id="c675e-114">SYNCHRONIZE</span></span>   | <span data-ttu-id="c675e-115">Право на использование данного объекта для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c675e-115">The right to use the object for synchronization.</span></span> <span data-ttu-id="c675e-116">Это позволяет потоку ожидать, пока объект находится в сигнальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="c675e-116">This enables a thread to wait until the object is in the signaled state.</span></span> <span data-ttu-id="c675e-117">Некоторые типы объектов не поддерживают это право доступа.</span><span class="sxs-lookup"><span data-stu-id="c675e-117">Some object types do not support this access right.</span></span>                                                                                                                                                                |
| <span data-ttu-id="c675e-118">ЗАПИСЬ \_ DAC</span><span class="sxs-lookup"><span data-stu-id="c675e-118">WRITE\_DAC</span></span>    | <span data-ttu-id="c675e-119">Право на изменение [*списка управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) в дескрипторе безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="c675e-119">The right to modify the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) in the object's security descriptor.</span></span>                                                                                                                    |
| <span data-ttu-id="c675e-120">\_владелец записи</span><span class="sxs-lookup"><span data-stu-id="c675e-120">WRITE\_OWNER</span></span>  | <span data-ttu-id="c675e-121">Право на изменение владельца в дескрипторе безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="c675e-121">The right to change the owner in the object's security descriptor.</span></span>                                                                                                                                                                                                                                                                           |



 

<span data-ttu-id="c675e-122">В Winnt. h также определяются следующие сочетания стандартных констант прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c675e-122">Winnt.h also defines the following combinations of the standard access rights constants.</span></span>



| <span data-ttu-id="c675e-123">Константа</span><span class="sxs-lookup"><span data-stu-id="c675e-123">Constant</span></span>                   | <span data-ttu-id="c675e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c675e-124">Meaning</span></span>                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c675e-125">\_все права \_ Standard</span><span class="sxs-lookup"><span data-stu-id="c675e-125">STANDARD\_RIGHTS\_ALL</span></span>      | <span data-ttu-id="c675e-126">Объединяет удаление, \_ Управление чтением, запись \_ DAC, запись \_ владельца и синхронизацию доступа.</span><span class="sxs-lookup"><span data-stu-id="c675e-126">Combines DELETE, READ\_CONTROL, WRITE\_DAC, WRITE\_OWNER, and SYNCHRONIZE access.</span></span> |
| <span data-ttu-id="c675e-127">\_выполнение стандартных прав \_</span><span class="sxs-lookup"><span data-stu-id="c675e-127">STANDARD\_RIGHTS\_EXECUTE</span></span>  | <span data-ttu-id="c675e-128">В настоящее время определено как эквивалентный \_ элемент управления Read.</span><span class="sxs-lookup"><span data-stu-id="c675e-128">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="c675e-129">\_Чтение стандартных прав \_</span><span class="sxs-lookup"><span data-stu-id="c675e-129">STANDARD\_RIGHTS\_READ</span></span>     | <span data-ttu-id="c675e-130">В настоящее время определено как эквивалентный \_ элемент управления Read.</span><span class="sxs-lookup"><span data-stu-id="c675e-130">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="c675e-131">\_требуются стандартные права \_</span><span class="sxs-lookup"><span data-stu-id="c675e-131">STANDARD\_RIGHTS\_REQUIRED</span></span> | <span data-ttu-id="c675e-132">Сочетает в себе удаление, \_ Управление чтением, запись \_ DAC и запись \_ доступа владельца.</span><span class="sxs-lookup"><span data-stu-id="c675e-132">Combines DELETE, READ\_CONTROL, WRITE\_DAC, and WRITE\_OWNER access.</span></span>              |
| <span data-ttu-id="c675e-133">\_запись стандартных прав \_</span><span class="sxs-lookup"><span data-stu-id="c675e-133">STANDARD\_RIGHTS\_WRITE</span></span>    | <span data-ttu-id="c675e-134">В настоящее время определено как эквивалентный \_ элемент управления Read.</span><span class="sxs-lookup"><span data-stu-id="c675e-134">Currently defined to equal READ\_CONTROL.</span></span>                                         |



 

 

 
