---
description: Конструктор классов Вбемтиме упрощает преобразование между различными форматами времени выполнения Windows и ANSI C.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'Конструкторы Вбемтиме:: Вбемтиме (Вбемтиме. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 778b9af2e732b3d294b0348ff2d2b91b60518d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713023"
---
# <a name="wbemtimewbemtime-constructors"></a><span data-ttu-id="228c7-103">Конструкторы Вбемтиме:: Вбемтиме</span><span class="sxs-lookup"><span data-stu-id="228c7-103">WBEMTime::WBEMTime constructors</span></span>

<span data-ttu-id="228c7-104">\[Класс [**вбемтиме**](wbemtime.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="228c7-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="228c7-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="228c7-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="228c7-106">Конструктор классов **вбемтиме** упрощает преобразование между различными форматами времени выполнения Windows и ANSI C.</span><span class="sxs-lookup"><span data-stu-id="228c7-106">The **WBEMTime** class constructor facilitates conversions between various Windows and ANSI C run-time time formats.</span></span>

### <a name="overload-list"></a><span data-ttu-id="228c7-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="228c7-107">Overload list</span></span>



| <span data-ttu-id="228c7-108">Конструктор</span><span class="sxs-lookup"><span data-stu-id="228c7-108">Constructor</span></span>                                                                 | <span data-ttu-id="228c7-109">Описание</span><span class="sxs-lookup"><span data-stu-id="228c7-109">Description</span></span>                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span data-ttu-id="228c7-110">[**Вбемтиме ()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="228c7-110">[**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                                   | <span data-ttu-id="228c7-111">Создает неинициализированный объект Time.</span><span class="sxs-lookup"><span data-stu-id="228c7-111">Creates an uninitialized time object.</span></span><br/>                          |
| <span data-ttu-id="228c7-112">[**Вбемтиме (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="228c7-112">[**WBEMTime(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                           | <span data-ttu-id="228c7-113">Инициализирует новый объект Time для значения в параметре.</span><span class="sxs-lookup"><span data-stu-id="228c7-113">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="228c7-114">[**Вбемтиме (время константы \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="228c7-114">[**WBEMTime(const time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span></span>        | <span data-ttu-id="228c7-115">Инициализирует новый объект Time для значения в параметре.</span><span class="sxs-lookup"><span data-stu-id="228c7-115">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="228c7-116">[**Вбемтиме (const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span><span class="sxs-lookup"><span data-stu-id="228c7-116">[**WBEMTime(const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span></span>    | <span data-ttu-id="228c7-117">Инициализирует новый объект Time для значения в параметре.</span><span class="sxs-lookup"><span data-stu-id="228c7-117">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="228c7-118">[**Вбемтиме (const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="228c7-118">[**WBEMTime(const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span></span>     | <span data-ttu-id="228c7-119">Инициализирует новый объект Time для значения в параметре.</span><span class="sxs-lookup"><span data-stu-id="228c7-119">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="228c7-120">[**Вбемтиме (const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="228c7-120">[**WBEMTime(const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span></span> | <span data-ttu-id="228c7-121">Инициализирует новый объект Time для значения в параметре.</span><span class="sxs-lookup"><span data-stu-id="228c7-121">Initializes the new time object to the value in the parameter.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="228c7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="228c7-122">Requirements</span></span>



| <span data-ttu-id="228c7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="228c7-123">Requirement</span></span> | <span data-ttu-id="228c7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="228c7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="228c7-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="228c7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="228c7-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="228c7-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="228c7-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="228c7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="228c7-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="228c7-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="228c7-129">Header</span><span class="sxs-lookup"><span data-stu-id="228c7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="228c7-130"><dt>Вбемтиме. h</dt></span><span class="sxs-lookup"><span data-stu-id="228c7-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="228c7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="228c7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="228c7-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="228c7-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="228c7-133">�</span><span class="sxs-lookup"><span data-stu-id="228c7-133">�</span></span>

<span data-ttu-id="228c7-134">�</span><span class="sxs-lookup"><span data-stu-id="228c7-134">�</span></span>
