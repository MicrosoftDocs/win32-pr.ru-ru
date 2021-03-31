---
description: Метод Жетлокалоффсетфордате возвращает смещение в минутах (+ или &\# 8211;) между GMT и местным временем для времени, заданного в аргументе.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'Методы Вбемтиме:: Жетлокалоффсетфордате (Вбемтиме. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911479"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a><span data-ttu-id="a8061-103">Методы Вбемтиме:: Жетлокалоффсетфордате</span><span class="sxs-lookup"><span data-stu-id="a8061-103">WBEMTime::GetLocalOffsetForDate methods</span></span>

<span data-ttu-id="a8061-104">\[Класс [**вбемтиме**](wbemtime.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="a8061-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="a8061-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="a8061-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="a8061-106">Метод **жетлокалоффсетфордате** возвращает смещение в минутах (+ или) между GMT и местным временем для времени, заданного в аргументе.</span><span class="sxs-lookup"><span data-stu-id="a8061-106">The **GetLocalOffsetForDate** method returns the offset in minutes (+ or �) between GMT and local time for the time supplied in the argument.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a8061-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="a8061-107">Overload list</span></span>



| <span data-ttu-id="a8061-108">Метод</span><span class="sxs-lookup"><span data-stu-id="a8061-108">Method</span></span>                                                                                           | <span data-ttu-id="a8061-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a8061-109">Description</span></span>                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span data-ttu-id="a8061-110">[**Жетлокалоффсетфордате (время \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="a8061-110">[**GetLocalOffsetForDate(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span></span>         | <span data-ttu-id="a8061-111">Аргумент — это ссылка на **время \_ t**.</span><span class="sxs-lookup"><span data-stu-id="a8061-111">Argument is a reference to a **time\_t**.</span></span><br/>  |
| <span data-ttu-id="a8061-112">[**Жетлокалоффсетфордате (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span><span class="sxs-lookup"><span data-stu-id="a8061-112">[**GetLocalOffsetForDate(FILETIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span></span>     | <span data-ttu-id="a8061-113">Аргумент — это указатель на **fileTime**.</span><span class="sxs-lookup"><span data-stu-id="a8061-113">Argument is a pointer to a **FILETIME**.</span></span><br/>   |
| [<span data-ttu-id="a8061-114">**Жетлокалоффсетфордате (структура TM \* )**</span><span class="sxs-lookup"><span data-stu-id="a8061-114">**GetLocalOffsetForDate(struct tm\*)**</span></span>](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | <span data-ttu-id="a8061-115">Аргумент — это указатель на структуру **TM** .</span><span class="sxs-lookup"><span data-stu-id="a8061-115">Argument is a pointer to **tm** structure.</span></span><br/> |
| <span data-ttu-id="a8061-116">[**Жетлокалоффсетфордате (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span><span class="sxs-lookup"><span data-stu-id="a8061-116">[**GetLocalOffsetForDate(SYSTEMTIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span></span> | <span data-ttu-id="a8061-117">Аргумент является указателем на **SYSTEMTIME**.</span><span class="sxs-lookup"><span data-stu-id="a8061-117">Argument is a pointer to a **SYSTEMTIME**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a8061-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a8061-118">Requirements</span></span>



| <span data-ttu-id="a8061-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a8061-119">Requirement</span></span> | <span data-ttu-id="a8061-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a8061-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8061-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8061-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a8061-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8061-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="a8061-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8061-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a8061-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8061-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="a8061-125">Header</span><span class="sxs-lookup"><span data-stu-id="a8061-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8061-126"><dt>Вбемтиме. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8061-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="a8061-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a8061-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8061-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8061-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="a8061-129">�</span><span class="sxs-lookup"><span data-stu-id="a8061-129">�</span></span>

<span data-ttu-id="a8061-130">�</span><span class="sxs-lookup"><span data-stu-id="a8061-130">�</span></span>
