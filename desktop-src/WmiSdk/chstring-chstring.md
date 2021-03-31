---
description: Каждый из следующих конструкторов Инициализирует новый объект Чстринг с указанными данными.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: 'Конструкторы Чстринг:: Чстринг (Чстринг. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 711d2f28680a9f273ff808876e30e92f66336b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264799"
---
# <a name="chstringchstring-constructors"></a><span data-ttu-id="fbad3-103">Конструкторы Чстринг:: Чстринг</span><span class="sxs-lookup"><span data-stu-id="fbad3-103">CHString::CHString constructors</span></span>

<span data-ttu-id="fbad3-104">\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="fbad3-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="fbad3-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="fbad3-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="fbad3-106">Каждый из следующих конструкторов Инициализирует новый объект [**чстринг**](chstring.md) с указанными данными.</span><span class="sxs-lookup"><span data-stu-id="fbad3-106">Each of the following constructors initializes a new [**CHString**](chstring.md) object with the specified data.</span></span>

### <a name="overload-list"></a><span data-ttu-id="fbad3-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="fbad3-107">Overload list</span></span>



| <span data-ttu-id="fbad3-108">Конструктор</span><span class="sxs-lookup"><span data-stu-id="fbad3-108">Constructor</span></span>                                                                        | <span data-ttu-id="fbad3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fbad3-109">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="fbad3-110">**Чстринг ()**</span><span class="sxs-lookup"><span data-stu-id="fbad3-110">**CHString()**</span></span>](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | <span data-ttu-id="fbad3-111">Создает пустой объект Чстринг.</span><span class="sxs-lookup"><span data-stu-id="fbad3-111">Creates an empty CHString object.</span></span><br/>                 |
| <span data-ttu-id="fbad3-112">[**Чстринг (LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span><span class="sxs-lookup"><span data-stu-id="fbad3-112">[**CHString(LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span></span>                              | <span data-ttu-id="fbad3-113">Инициализирует со значением LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="fbad3-113">Initializes with the LPCSTR value.</span></span><br/>                |
| <span data-ttu-id="fbad3-114">[**Чстринг (ЛПКВСТР)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="fbad3-114">[**CHString(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span></span>                            | <span data-ttu-id="fbad3-115">Инициализирует со значением ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="fbad3-115">Initializes with the LPCWSTR value.</span></span><br/>               |
| <span data-ttu-id="fbad3-116">[**Чстринг (WCHAR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span><span class="sxs-lookup"><span data-stu-id="fbad3-116">[**CHString(WCHAR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span></span>                        | <span data-ttu-id="fbad3-117">Инициализирует целочисленные копии значения WCHAR.</span><span class="sxs-lookup"><span data-stu-id="fbad3-117">Initializes with int copies of the WCHAR value.</span></span><br/>   |
| <span data-ttu-id="fbad3-118">[**Чстринг (ЛПКВСТР, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span><span class="sxs-lookup"><span data-stu-id="fbad3-118">[**CHString(LPCWSTR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span></span>                    | <span data-ttu-id="fbad3-119">Инициализирует целочисленные копии значения ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="fbad3-119">Initializes with int copies of the LPCWSTR value.</span></span><br/> |
| <span data-ttu-id="fbad3-120">[**Чстринг (const Чстринг&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="fbad3-120">[**CHString(const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span></span>            | <span data-ttu-id="fbad3-121">Реплицирует параметр Чстринг.</span><span class="sxs-lookup"><span data-stu-id="fbad3-121">Replicates the CHString parameter.</span></span><br/>                |
| <span data-ttu-id="fbad3-122">[**Чстринг (const без знака \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span><span class="sxs-lookup"><span data-stu-id="fbad3-122">[**CHString(const unsigned char\*)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span></span> | <span data-ttu-id="fbad3-123">Инициализирует со значением, на которое указывает char \* .</span><span class="sxs-lookup"><span data-stu-id="fbad3-123">Initializes with the value pointed to by char\*.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="fbad3-124">Требования</span><span class="sxs-lookup"><span data-stu-id="fbad3-124">Requirements</span></span>



| <span data-ttu-id="fbad3-125">Требование</span><span class="sxs-lookup"><span data-stu-id="fbad3-125">Requirement</span></span> | <span data-ttu-id="fbad3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="fbad3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbad3-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbad3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fbad3-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbad3-128">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="fbad3-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbad3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fbad3-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbad3-130">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="fbad3-131">Header</span><span class="sxs-lookup"><span data-stu-id="fbad3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbad3-132"><dt>Чстринг. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fbad3-132"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fbad3-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fbad3-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="fbad3-134"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbad3-134"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="fbad3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fbad3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbad3-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbad3-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="fbad3-137">�</span><span class="sxs-lookup"><span data-stu-id="fbad3-137">�</span></span>

<span data-ttu-id="fbad3-138">�</span><span class="sxs-lookup"><span data-stu-id="fbad3-138">�</span></span>
