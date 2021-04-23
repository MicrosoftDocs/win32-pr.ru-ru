---
description: 'Метод CInstance:: GetWBEMINT64 задает свойство 64-разрядного целого числа.'
audience: developer
ms.assetid: a1789091-ddb6-44f7-bc02-82e7c0209bf9
ms.tgt_platform: multiple
title: 'Методы CInstance:: SetWBEMINT64 (instance. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f83e39170125a07f28a25d594ad7203f44750a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998986"
---
# <a name="cinstancesetwbemint64-methods"></a><span data-ttu-id="5ced2-103">Методы CInstance:: SetWBEMINT64</span><span class="sxs-lookup"><span data-stu-id="5ced2-103">CInstance::SetWBEMINT64 methods</span></span>

<span data-ttu-id="5ced2-104">\[Класс [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="5ced2-104">\[The [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="5ced2-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="5ced2-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="5ced2-106">Метод [**CInstance:: GetWBEMINT64**](cinstance-getwbemint64.md) задает свойство 64-разрядного целого числа.</span><span class="sxs-lookup"><span data-stu-id="5ced2-106">The [**CInstance::GetWBEMINT64**](cinstance-getwbemint64.md) method sets a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="5ced2-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="5ced2-107">Overload list</span></span>



| <span data-ttu-id="5ced2-108">Метод</span><span class="sxs-lookup"><span data-stu-id="5ced2-108">Method</span></span>                                                                                               | <span data-ttu-id="5ced2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5ced2-109">Description</span></span>                                |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------|
| <span data-ttu-id="5ced2-110">[**SetWBEMINT64 (ЛПКВСТР, const ЛОНГЛОНГ&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span><span class="sxs-lookup"><span data-stu-id="5ced2-110">[**SetWBEMINT64(LPCWSTR, const LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span></span>    | <span data-ttu-id="5ced2-111">Задает 64-разрядное целочисленное свойство.</span><span class="sxs-lookup"><span data-stu-id="5ced2-111">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="5ced2-112">[**SetWBEMINT64 (ЛПКВСТР, const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="5ced2-112">[**SetWBEMINT64(LPCWSTR, const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span> | <span data-ttu-id="5ced2-113">Задает 64-разрядное целочисленное свойство.</span><span class="sxs-lookup"><span data-stu-id="5ced2-113">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="5ced2-114">[**SetWBEMINT64 (ЛПКВСТР, const УЛОНГЛОНГ&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="5ced2-114">[**SetWBEMINT64(LPCWSTR, const ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span>  | <span data-ttu-id="5ced2-115">Задает 64-разрядное целочисленное свойство.</span><span class="sxs-lookup"><span data-stu-id="5ced2-115">Sets a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5ced2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5ced2-116">Requirements</span></span>



| <span data-ttu-id="5ced2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5ced2-117">Requirement</span></span> | <span data-ttu-id="5ced2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5ced2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ced2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ced2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5ced2-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ced2-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="5ced2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ced2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5ced2-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ced2-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="5ced2-123">Header</span><span class="sxs-lookup"><span data-stu-id="5ced2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ced2-124"><dt>Instance. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ced2-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5ced2-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5ced2-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ced2-126"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ced2-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="5ced2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5ced2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ced2-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ced2-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ced2-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ced2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ced2-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="5ced2-130">**CInstance**</span></span>](/windows/win32/api/instance/nl-instance-cinstance)
</dt> </dl>

<span data-ttu-id="5ced2-131">�</span><span class="sxs-lookup"><span data-stu-id="5ced2-131">�</span></span>

<span data-ttu-id="5ced2-132">�</span><span class="sxs-lookup"><span data-stu-id="5ced2-132">�</span></span>
