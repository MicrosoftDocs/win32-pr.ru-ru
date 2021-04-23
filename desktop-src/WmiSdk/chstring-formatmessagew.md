---
description: Перегруженный метод Форматмессажев форматирует строку сообщения.
audience: developer
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.tgt_platform: multiple
title: 'Методы Чстринг:: Форматмессажев (Чстринг. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a4f6be83c2cec8f3ae02cdbafac8a6c10ab72578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712115"
---
# <a name="chstringformatmessagew-methods"></a><span data-ttu-id="4809c-103">Методы Чстринг:: Форматмессажев</span><span class="sxs-lookup"><span data-stu-id="4809c-103">CHString::FormatMessageW methods</span></span>

<span data-ttu-id="4809c-104">\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="4809c-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="4809c-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="4809c-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="4809c-106">Перегруженный метод **форматмессажев** форматирует строку сообщения.</span><span class="sxs-lookup"><span data-stu-id="4809c-106">The overloaded **FormatMessageW** method formats a message string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4809c-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="4809c-107">Overload list</span></span>



| <span data-ttu-id="4809c-108">Метод</span><span class="sxs-lookup"><span data-stu-id="4809c-108">Method</span></span>                                                              | <span data-ttu-id="4809c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4809c-109">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4809c-110">[**Форматмессажев (UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4809c-110">[**FormatMessageW(UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span></span>       | <span data-ttu-id="4809c-111">Форматирует это сообщение в соответствии с идентификатором ресурса, указанным в параметре **uint**.</span><span class="sxs-lookup"><span data-stu-id="4809c-111">Formats this message according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="4809c-112">[**Форматмессажев (ЛПКВСТР)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="4809c-112">[**FormatMessageW(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span></span> | <span data-ttu-id="4809c-113">Форматирует эту строку сообщения в соответствии с форматом, заданным параметром **лпквстр**.</span><span class="sxs-lookup"><span data-stu-id="4809c-113">Formats this message string according to the format specified by the **LPCWSTR**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="4809c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4809c-114">Requirements</span></span>



| <span data-ttu-id="4809c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4809c-115">Requirement</span></span> | <span data-ttu-id="4809c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4809c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4809c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4809c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4809c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4809c-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4809c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4809c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4809c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4809c-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="4809c-121">Header</span><span class="sxs-lookup"><span data-stu-id="4809c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4809c-122"><dt>Чстринг. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4809c-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4809c-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4809c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="4809c-124"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4809c-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="4809c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4809c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4809c-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4809c-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="4809c-127">�</span><span class="sxs-lookup"><span data-stu-id="4809c-127">�</span></span>

<span data-ttu-id="4809c-128">�</span><span class="sxs-lookup"><span data-stu-id="4809c-128">�</span></span>
