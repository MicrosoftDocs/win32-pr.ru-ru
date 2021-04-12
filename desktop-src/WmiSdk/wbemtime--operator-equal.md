---
description: Операторы присваивания класса Вбемтиме перегружаются для упрощения преобразований между различными форматами времени выполнения Windows и ANSI C. Ниже перечислены различные перегруженные сигнатуры.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'Операторы Вбемтиме:: operator = (Вбемтиме. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349612"
---
# <a name="wbemtimeoperator-operators"></a><span data-ttu-id="95d7f-104">Операторы Вбемтиме:: operator =</span><span class="sxs-lookup"><span data-stu-id="95d7f-104">WBEMTime::operator= operators</span></span>

<span data-ttu-id="95d7f-105">\[Класс [**вбемтиме**](wbemtime.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="95d7f-105">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="95d7f-106">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="95d7f-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="95d7f-107">Операторы присваивания класса [**вбемтиме**](wbemtime.md) перегружаются для упрощения преобразований между различными форматами времени выполнения Windows и ANSI C.</span><span class="sxs-lookup"><span data-stu-id="95d7f-107">The [**WBEMTime**](wbemtime.md) class assignment operators are overloaded to facilitate conversions between various Windows and ANSI C run-time time formats.</span></span> <span data-ttu-id="95d7f-108">Ниже перечислены различные перегруженные сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="95d7f-108">The various overloaded signatures are listed below.</span></span>

### <a name="overload-list"></a><span data-ttu-id="95d7f-109">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="95d7f-109">Overload list</span></span>



| <span data-ttu-id="95d7f-110">Оператор</span><span class="sxs-lookup"><span data-stu-id="95d7f-110">Operator</span></span>                                                                     | <span data-ttu-id="95d7f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="95d7f-111">Description</span></span>                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span data-ttu-id="95d7f-112">[**operator = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span><span class="sxs-lookup"><span data-stu-id="95d7f-112">[**operator=(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span></span>               | <span data-ttu-id="95d7f-113">Преобразует **BSTR** в формат **вбемтиме** .</span><span class="sxs-lookup"><span data-stu-id="95d7f-113">Converts a **BSTR** to **WBEMTime** format.</span></span><br/>         |
| <span data-ttu-id="95d7f-114">[**operator = (время \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="95d7f-114">[**operator=(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span></span>        | <span data-ttu-id="95d7f-115">Преобразует **\_ t** в формат **вбемтиме** .</span><span class="sxs-lookup"><span data-stu-id="95d7f-115">Converts **time\_t** to **WBEMTime** format.</span></span><br/>        |
| <span data-ttu-id="95d7f-116">[**operator = (FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="95d7f-116">[**operator=(FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>     | <span data-ttu-id="95d7f-117">Преобразует значение **fileTime** в формат **вбемтиме** .</span><span class="sxs-lookup"><span data-stu-id="95d7f-117">Converts **FILETIME** to **WBEMTime** format.</span></span><br/>       |
| <span data-ttu-id="95d7f-118">[**operator = (структура TM&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span><span class="sxs-lookup"><span data-stu-id="95d7f-118">[**operator=(struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span></span>   | <span data-ttu-id="95d7f-119">Преобразует структуру **TM** в формат **вбемтиме** .</span><span class="sxs-lookup"><span data-stu-id="95d7f-119">Converts a **tm** structure to **WBEMTime** format.</span></span><br/> |
| <span data-ttu-id="95d7f-120">[**operator = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="95d7f-120">[**operator=(SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span></span> | <span data-ttu-id="95d7f-121">Преобразует **SYSTEMTIME** в формат **вбемтиме** .</span><span class="sxs-lookup"><span data-stu-id="95d7f-121">Converts **SYSTEMTIME** to **WBEMTime** format.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="95d7f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="95d7f-122">Requirements</span></span>



| <span data-ttu-id="95d7f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="95d7f-123">Requirement</span></span> | <span data-ttu-id="95d7f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="95d7f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d7f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95d7f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="95d7f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95d7f-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="95d7f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95d7f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="95d7f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95d7f-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="95d7f-129">Header</span><span class="sxs-lookup"><span data-stu-id="95d7f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="95d7f-130"><dt>Вбемтиме. h</dt></span><span class="sxs-lookup"><span data-stu-id="95d7f-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="95d7f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="95d7f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95d7f-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95d7f-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="95d7f-133">�</span><span class="sxs-lookup"><span data-stu-id="95d7f-133">�</span></span>

<span data-ttu-id="95d7f-134">�</span><span class="sxs-lookup"><span data-stu-id="95d7f-134">�</span></span>
