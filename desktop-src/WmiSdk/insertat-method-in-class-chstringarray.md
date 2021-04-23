---
description: Метод Инсертат вставляет элемент (или несколько копий элемента) или все элементы другого массива по указанному индексу.
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: 'Методы Чстрингаррай:: Инсертат (Чстрарр. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4047b740778c8d0adf1f2b5981b2f3aac5ba9529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703259"
---
# <a name="chstringarrayinsertat-methods"></a><span data-ttu-id="e766c-103">Методы Чстрингаррай:: Инсертат</span><span class="sxs-lookup"><span data-stu-id="e766c-103">CHStringArray::InsertAt methods</span></span>

<span data-ttu-id="e766c-104">\[Класс [**чстрингаррай**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="e766c-104">\[The [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="e766c-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="e766c-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="e766c-106">Метод **инсертат** вставляет элемент (или несколько копий элемента) или все элементы другого массива по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="e766c-106">The **InsertAt** method inserts an element (or multiple copies of an element) or all the elements of another array at a specified index.</span></span>

### <a name="overload-list"></a><span data-ttu-id="e766c-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="e766c-107">Overload list</span></span>



| <span data-ttu-id="e766c-108">Метод</span><span class="sxs-lookup"><span data-stu-id="e766c-108">Method</span></span>                                                                               | <span data-ttu-id="e766c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e766c-109">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e766c-110">[**Инсертат (int, ЛПКВСТР, int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e766c-110">[**InsertAt(int,LPCWSTR,int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span></span>       | <span data-ttu-id="e766c-111">Вставляет один или несколько элементов по указанному индексу в массиве.</span><span class="sxs-lookup"><span data-stu-id="e766c-111">Inserts one or more elements at a specified index in an array.</span></span><br/>                                               |
| <span data-ttu-id="e766c-112">[**Инсертат (int, Чстрингаррай \* )**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span><span class="sxs-lookup"><span data-stu-id="e766c-112">[**InsertAt(int,CHStringArray\*)**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span></span> | <span data-ttu-id="e766c-113">Вставляет все элементы другого [**чстрингаррай**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) с указанным индексом в массиве.</span><span class="sxs-lookup"><span data-stu-id="e766c-113">Inserts all the elements of another [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) at a specified index in an array.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e766c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e766c-114">Requirements</span></span>



| <span data-ttu-id="e766c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e766c-115">Requirement</span></span> | <span data-ttu-id="e766c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e766c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e766c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e766c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e766c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e766c-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e766c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e766c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e766c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e766c-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="e766c-121">Header</span><span class="sxs-lookup"><span data-stu-id="e766c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e766c-122"><dt>Чстрарр. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e766c-122"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e766c-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e766c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="e766c-124"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e766c-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="e766c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e766c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e766c-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e766c-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e766c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e766c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e766c-128">**чстрингаррай**</span><span class="sxs-lookup"><span data-stu-id="e766c-128">**CHStringArray**</span></span>](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

<span data-ttu-id="e766c-129">�</span><span class="sxs-lookup"><span data-stu-id="e766c-129">�</span></span>

<span data-ttu-id="e766c-130">�</span><span class="sxs-lookup"><span data-stu-id="e766c-130">�</span></span>
