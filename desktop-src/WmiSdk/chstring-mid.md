---
description: Метод MID Извлекает подстроку length Нкаунт символов из строки Чстринг, начиная с позиции Nпервая (от нуля). Метод возвращает копию извлеченной подстроки.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: 'Методы Чстринг:: MID (Чстринг. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5d05259128f80bcb21d00144d19002ca58ce39c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712195"
---
# <a name="chstringmid-methods"></a><span data-ttu-id="c85df-104">Методы Чстринг:: mid</span><span class="sxs-lookup"><span data-stu-id="c85df-104">CHString::Mid methods</span></span>

<span data-ttu-id="c85df-105">\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="c85df-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="c85df-106">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="c85df-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="c85df-107">Метод **MID** Извлекает подстроку length *нкаунт* символов из строки [**Чстринг**](chstring.md) , начиная с позиции *nпервая* (от нуля).</span><span class="sxs-lookup"><span data-stu-id="c85df-107">The **Mid** method extracts a substring of length *nCount* characters from a [**CHString**](chstring.md) string, starting at position *nFirst* (zero-based).</span></span> <span data-ttu-id="c85df-108">Метод возвращает копию извлеченной подстроки.</span><span class="sxs-lookup"><span data-stu-id="c85df-108">The method returns a copy of the extracted substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c85df-109">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="c85df-109">Overload list</span></span>



| <span data-ttu-id="c85df-110">Метод</span><span class="sxs-lookup"><span data-stu-id="c85df-110">Method</span></span>                                        | <span data-ttu-id="c85df-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c85df-111">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| <span data-ttu-id="c85df-112">[**MID (int, int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span><span class="sxs-lookup"><span data-stu-id="c85df-112">[**Mid(int,int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span></span> | <span data-ttu-id="c85df-113">Извлекает подстроку заданной длины и начальную точку.</span><span class="sxs-lookup"><span data-stu-id="c85df-113">Extracts a substring of specified length and beginning point.</span></span><br/> |
| <span data-ttu-id="c85df-114">[**MID (int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="c85df-114">[**Mid(int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>         | <span data-ttu-id="c85df-115">Извлекает подстроку, начиная с int.</span><span class="sxs-lookup"><span data-stu-id="c85df-115">Extracts a substring beginning at int.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="c85df-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c85df-116">Requirements</span></span>



| <span data-ttu-id="c85df-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c85df-117">Requirement</span></span> | <span data-ttu-id="c85df-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c85df-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c85df-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c85df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c85df-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c85df-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="c85df-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c85df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c85df-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c85df-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="c85df-123">Header</span><span class="sxs-lookup"><span data-stu-id="c85df-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c85df-124"><dt>Чстринг. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c85df-124"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c85df-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c85df-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c85df-126"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c85df-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="c85df-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c85df-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c85df-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c85df-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="c85df-129">�</span><span class="sxs-lookup"><span data-stu-id="c85df-129">�</span></span>

<span data-ttu-id="c85df-130">�</span><span class="sxs-lookup"><span data-stu-id="c85df-130">�</span></span>
