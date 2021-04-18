---
description: Метод Format форматирует и сохраняет ряд символов и значений в Чстринг строке.
audience: developer
ms.assetid: 95d24b0e-3580-4a5d-8dad-50d44ef1ca39
ms.tgt_platform: multiple
title: 'Методы Чстринг:: Format (Чстринг. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7187d2c691c6efb2054d766ae432c55be893cd05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712114"
---
# <a name="chstringformat-methods"></a><span data-ttu-id="a9a5d-103">Методы Чстринг:: Format</span><span class="sxs-lookup"><span data-stu-id="a9a5d-103">CHString::Format methods</span></span>

<span data-ttu-id="a9a5d-104">\[Класс [**чстринг**](chstring.md) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="a9a5d-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="a9a5d-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="a9a5d-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="a9a5d-106">Метод **Format** форматирует и сохраняет ряд символов и значений в [**чстринг**](chstring.md) строке.</span><span class="sxs-lookup"><span data-stu-id="a9a5d-106">The **Format** method formats and stores a series of characters and values in a [**CHString**](chstring.md) string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a9a5d-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="a9a5d-107">Overload list</span></span>



| <span data-ttu-id="a9a5d-108">Метод</span><span class="sxs-lookup"><span data-stu-id="a9a5d-108">Method</span></span>                                              | <span data-ttu-id="a9a5d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a9a5d-109">Description</span></span>                                                                                      |
|:----------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a5d-110">[**Формат (UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a9a5d-110">[**Format(UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span></span>       | <span data-ttu-id="a9a5d-111">Форматирует этот Чстринг в соответствии с идентификатором ресурса, указанным в параметре **uint**.</span><span class="sxs-lookup"><span data-stu-id="a9a5d-111">Formats this CHString according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="a9a5d-112">[**Формат (ЛПКВСТР)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="a9a5d-112">[**Format(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span></span> | <span data-ttu-id="a9a5d-113">Форматирует этот Чстринг в соответствии с форматом, заданным параметром **лпквстр**.</span><span class="sxs-lookup"><span data-stu-id="a9a5d-113">Formats this CHString according to the format specified by the **LPCWSTR**.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="a9a5d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a9a5d-114">Requirements</span></span>



| <span data-ttu-id="a9a5d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a9a5d-115">Requirement</span></span> | <span data-ttu-id="a9a5d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a9a5d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a5d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9a5d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a5d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9a5d-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="a9a5d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9a5d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a5d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9a5d-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="a9a5d-121">Header</span><span class="sxs-lookup"><span data-stu-id="a9a5d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9a5d-122"><dt>Чстринг. h (включение Фвкоммон. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9a5d-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a9a5d-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a9a5d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9a5d-124"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9a5d-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="a9a5d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a9a5d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9a5d-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9a5d-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="a9a5d-127">�</span><span class="sxs-lookup"><span data-stu-id="a9a5d-127">�</span></span>

<span data-ttu-id="a9a5d-128">�</span><span class="sxs-lookup"><span data-stu-id="a9a5d-128">�</span></span>
