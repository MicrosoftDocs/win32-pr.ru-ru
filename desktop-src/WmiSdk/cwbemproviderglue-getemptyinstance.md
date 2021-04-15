---
description: Метод Жетемптинстанце извлекает один незаполненный экземпляр указанного класса.
audience: developer
ms.assetid: 2873b466-3782-4d63-a777-5b25e3fb7615
ms.tgt_platform: multiple
title: 'Методы Квбемпровидерглуе:: Жетемптинстанце (Вбемглуе. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 853afbf3789969fbfca66d5f9cb40f41eadf7630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702074"
---
# <a name="cwbemprovidergluegetemptyinstance-methods"></a><span data-ttu-id="a476a-103">Методы Квбемпровидерглуе:: Жетемптинстанце</span><span class="sxs-lookup"><span data-stu-id="a476a-103">CWbemProviderGlue::GetEmptyInstance methods</span></span>

<span data-ttu-id="a476a-104">\[Класс [**квбемпровидерглуе**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="a476a-104">\[The [**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="a476a-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="a476a-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="a476a-106">Метод **жетемптинстанце** извлекает один незаполненный экземпляр указанного класса.</span><span class="sxs-lookup"><span data-stu-id="a476a-106">The **GetEmptyInstance** method retrieves a single unpopulated instance of the specified class.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a476a-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="a476a-107">Overload list</span></span>



| <span data-ttu-id="a476a-108">Метод</span><span class="sxs-lookup"><span data-stu-id="a476a-108">Method</span></span>                                                                                                                                            | <span data-ttu-id="a476a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a476a-109">Description</span></span>                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="a476a-110">[**Жетемптинстанце (ЛПКВСТР, CInstance, ЛПКВСТР)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="a476a-110">[**GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span>                            | <span data-ttu-id="a476a-111">Извлекает один незаполненный экземпляр указанного класса.</span><span class="sxs-lookup"><span data-stu-id="a476a-111">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |
| <span data-ttu-id="a476a-112">[**Жетемптинстанце (Месодконтекст, ЛПКВСТР, CInstance, ЛПКВСТР)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="a476a-112">[**GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span> | <span data-ttu-id="a476a-113">Извлекает один незаполненный экземпляр указанного класса.</span><span class="sxs-lookup"><span data-stu-id="a476a-113">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a476a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a476a-114">Requirements</span></span>



| <span data-ttu-id="a476a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a476a-115">Requirement</span></span> | <span data-ttu-id="a476a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a476a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a476a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a476a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a476a-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a476a-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="a476a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a476a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a476a-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a476a-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="a476a-121">Header</span><span class="sxs-lookup"><span data-stu-id="a476a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a476a-122"><dt>Вбемглуе. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a476a-122"><dt>WbemGlue.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a476a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a476a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a476a-124"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a476a-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="a476a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a476a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a476a-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a476a-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="a476a-127">�</span><span class="sxs-lookup"><span data-stu-id="a476a-127">�</span></span>

<span data-ttu-id="a476a-128">�</span><span class="sxs-lookup"><span data-stu-id="a476a-128">�</span></span>
