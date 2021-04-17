---
description: Метод Find выполняет поиск в строке первого совпадения подстроки.
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: 'Методы Чстринг:: Find (Чстринг. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5996ca5c06e2101fad834ce2e37df31ee435fbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713113"
---
# <a name="chstringfind-methods"></a><span data-ttu-id="630fb-103">Методы Чстринг:: Find</span><span class="sxs-lookup"><span data-stu-id="630fb-103">CHString::Find methods</span></span>

<span data-ttu-id="630fb-104">\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="630fb-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="630fb-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="630fb-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="630fb-106">Метод **Find** выполняет поиск в строке первого совпадения подстроки.</span><span class="sxs-lookup"><span data-stu-id="630fb-106">The **Find** method searches a string for the first match of a substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="630fb-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="630fb-107">Overload list</span></span>



| <span data-ttu-id="630fb-108">Метод</span><span class="sxs-lookup"><span data-stu-id="630fb-108">Method</span></span>                                          | <span data-ttu-id="630fb-109">Описание</span><span class="sxs-lookup"><span data-stu-id="630fb-109">Description</span></span>                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| <span data-ttu-id="630fb-110">[**Find (WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="630fb-110">[**Find(WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span>     | <span data-ttu-id="630fb-111">Выполняет поиск **встр** в этой строке.</span><span class="sxs-lookup"><span data-stu-id="630fb-111">Searches for the **WSTR** in this string.</span></span><br/>    |
| <span data-ttu-id="630fb-112">[**Найти (ЛПКВСТР)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="630fb-112">[**Find(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span> | <span data-ttu-id="630fb-113">Выполняет поиск **лпквстр** в этой строке.</span><span class="sxs-lookup"><span data-stu-id="630fb-113">Searches for the **LPCWSTR** in this string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="630fb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="630fb-114">Requirements</span></span>



| <span data-ttu-id="630fb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="630fb-115">Requirement</span></span> | <span data-ttu-id="630fb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="630fb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="630fb-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="630fb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="630fb-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="630fb-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="630fb-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="630fb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="630fb-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="630fb-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="630fb-121">Header</span><span class="sxs-lookup"><span data-stu-id="630fb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="630fb-122"><dt>Чстринг. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="630fb-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="630fb-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="630fb-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="630fb-124"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="630fb-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="630fb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="630fb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="630fb-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="630fb-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="630fb-127">�</span><span class="sxs-lookup"><span data-stu-id="630fb-127">�</span></span>

<span data-ttu-id="630fb-128">�</span><span class="sxs-lookup"><span data-stu-id="630fb-128">�</span></span>
