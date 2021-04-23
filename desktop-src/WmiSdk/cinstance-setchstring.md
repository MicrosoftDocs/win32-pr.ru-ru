---
description: 'Метод CInstance:: Сетчстринг задает строковое свойство.'
ms.assetid: a75b574d-9ee7-4930-a003-5d71c5f1d687
ms.tgt_platform: multiple
title: 'Методы CInstance:: Сетчстринг (instance. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 187c07b5cf0f867ee838f2f3725d6a82319d4634
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656649"
---
# <a name="cinstancesetchstring-methods"></a><span data-ttu-id="1b70d-103">Методы CInstance:: Сетчстринг</span><span class="sxs-lookup"><span data-stu-id="1b70d-103">CInstance::SetCHString methods</span></span>

<span data-ttu-id="1b70d-104">\[Класс [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="1b70d-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="1b70d-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="1b70d-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="1b70d-106">Метод **CInstance:: сетчстринг** задает строковое свойство.</span><span class="sxs-lookup"><span data-stu-id="1b70d-106">The **CInstance::SetCHString** method sets a string property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="1b70d-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="1b70d-107">Overload list</span></span>



| <span data-ttu-id="1b70d-108">Метод</span><span class="sxs-lookup"><span data-stu-id="1b70d-108">Method</span></span>                                                                                           | <span data-ttu-id="1b70d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1b70d-109">Description</span></span>                        |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span data-ttu-id="1b70d-110">[**Сетчстринг (ЛПКВСТР, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span><span class="sxs-lookup"><span data-stu-id="1b70d-110">[**SetCHString(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span></span>                   | <span data-ttu-id="1b70d-111">Задает строковое свойство.</span><span class="sxs-lookup"><span data-stu-id="1b70d-111">Sets a string property.</span></span><br/> |
| <span data-ttu-id="1b70d-112">[**Сетчстринг (ЛПКВСТР, const Чстринг&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span><span class="sxs-lookup"><span data-stu-id="1b70d-112">[**SetCHString(LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span></span> | <span data-ttu-id="1b70d-113">Задает строковое свойство.</span><span class="sxs-lookup"><span data-stu-id="1b70d-113">Sets a string property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1b70d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1b70d-114">Requirements</span></span>



| <span data-ttu-id="1b70d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1b70d-115">Requirement</span></span> | <span data-ttu-id="1b70d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1b70d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b70d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b70d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1b70d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b70d-118">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="1b70d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b70d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1b70d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b70d-120">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="1b70d-121">Header</span><span class="sxs-lookup"><span data-stu-id="1b70d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b70d-122"><dt>Instance. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b70d-122"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1b70d-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1b70d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b70d-124"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b70d-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="1b70d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1b70d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b70d-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b70d-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b70d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b70d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b70d-128">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="1b70d-128">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

