---
description: 'Метод CInstance:: GetWBEMINT64 получает свойство 64-разрядное целое число.'
ms.assetid: b51d0c51-3b72-4358-8fc3-d1dbc298b4d9
ms.tgt_platform: multiple
title: 'Методы CInstance:: GetWBEMINT64 (instance. h)'
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
ms.openlocfilehash: 3d7b7a9f4091125bd722aea197c1670defb0c21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346775"
---
# <a name="cinstancegetwbemint64-methods"></a><span data-ttu-id="39f99-103">Методы CInstance:: GetWBEMINT64</span><span class="sxs-lookup"><span data-stu-id="39f99-103">CInstance::GetWBEMINT64 methods</span></span>

<span data-ttu-id="39f99-104">\[Класс [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="39f99-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="39f99-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="39f99-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="39f99-106">Метод **CInstance:: GetWBEMINT64** получает свойство 64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="39f99-106">The **CInstance::GetWBEMINT64** method retrieves a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="39f99-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="39f99-107">Overload list</span></span>



| <span data-ttu-id="39f99-108">Метод</span><span class="sxs-lookup"><span data-stu-id="39f99-108">Method</span></span>                                                                                   | <span data-ttu-id="39f99-109">Описание</span><span class="sxs-lookup"><span data-stu-id="39f99-109">Description</span></span>                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------|
| <span data-ttu-id="39f99-110">[**GetWBEMINT64 (ЛПКВСТР, ЛОНГЛОНГ&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span><span class="sxs-lookup"><span data-stu-id="39f99-110">[**GetWBEMINT64(LPCWSTR, LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span></span>   | <span data-ttu-id="39f99-111">Извлекает 64-разрядное целочисленное свойство.</span><span class="sxs-lookup"><span data-stu-id="39f99-111">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="39f99-112">[**GetWBEMINT64 (ЛПКВСТР, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="39f99-112">[**GetWBEMINT64(LPCWSTR, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="39f99-113">Извлекает 64-разрядное целочисленное свойство.</span><span class="sxs-lookup"><span data-stu-id="39f99-113">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="39f99-114">[**GetWBEMINT64 (ЛПКВСТР, УЛОНГЛОНГ&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="39f99-114">[**GetWBEMINT64(LPCWSTR, ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="39f99-115">Извлекает 64-разрядное целочисленное свойство.</span><span class="sxs-lookup"><span data-stu-id="39f99-115">Retrieves a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="39f99-116">Требования</span><span class="sxs-lookup"><span data-stu-id="39f99-116">Requirements</span></span>



| <span data-ttu-id="39f99-117">Требование</span><span class="sxs-lookup"><span data-stu-id="39f99-117">Requirement</span></span> | <span data-ttu-id="39f99-118">Значение</span><span class="sxs-lookup"><span data-stu-id="39f99-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39f99-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39f99-119">Minimum supported client</span></span><br/> | <span data-ttu-id="39f99-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39f99-120">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="39f99-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39f99-121">Minimum supported server</span></span><br/> | <span data-ttu-id="39f99-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39f99-122">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="39f99-123">Header</span><span class="sxs-lookup"><span data-stu-id="39f99-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="39f99-124"><dt>Instance. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39f99-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="39f99-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="39f99-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="39f99-126"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39f99-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="39f99-127">DLL</span><span class="sxs-lookup"><span data-stu-id="39f99-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39f99-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39f99-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f99-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39f99-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f99-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="39f99-130">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

