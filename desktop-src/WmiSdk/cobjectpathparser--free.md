---
description: Перегруженный метод, который освобождает память, содержащую путь.
audience: developer
ms.assetid: 9164d7b2-15b8-4b73-ab8c-68ed45692ea0
ms.tgt_platform: multiple
title: 'Методы Кобжектпаспарсер:: Free (Обжпас. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 86494e569f68d8eff8b691c648ec5e221b28b39d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265611"
---
# <a name="cobjectpathparserfree-methods"></a><span data-ttu-id="d3056-103">Методы Кобжектпаспарсер:: Free</span><span class="sxs-lookup"><span data-stu-id="d3056-103">CObjectPathParser::Free methods</span></span>

<span data-ttu-id="d3056-104">\[Класс [**кобжектпаспарсер**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="d3056-104">\[The [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="d3056-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="d3056-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="d3056-106">Перегруженный метод, который освобождает память, содержащую путь.</span><span class="sxs-lookup"><span data-stu-id="d3056-106">An overloaded method that releases the memory that contains the path.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d3056-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="d3056-107">Overload list</span></span>



| <span data-ttu-id="d3056-108">Метод</span><span class="sxs-lookup"><span data-stu-id="d3056-108">Method</span></span>                                                                     | <span data-ttu-id="d3056-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d3056-109">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| <span data-ttu-id="d3056-110">[**Free (LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span><span class="sxs-lookup"><span data-stu-id="d3056-110">[**Free(LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span></span>                     | <span data-ttu-id="d3056-111">Освобождает память, содержащую неразобранный путь.</span><span class="sxs-lookup"><span data-stu-id="d3056-111">Releases the memory that contains the unparsed path.</span></span><br/>                      |
| <span data-ttu-id="d3056-112">[**Бесплатный (Парседобжектпас)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span><span class="sxs-lookup"><span data-stu-id="d3056-112">[**Free(ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span></span> | <span data-ttu-id="d3056-113">Освобождает память, содержащую структуру с проанализированным путем.</span><span class="sxs-lookup"><span data-stu-id="d3056-113">Releases the memory that contains the structure that has the parsed path.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d3056-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d3056-114">Requirements</span></span>



| <span data-ttu-id="d3056-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d3056-115">Requirement</span></span> | <span data-ttu-id="d3056-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d3056-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3056-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3056-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3056-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3056-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d3056-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3056-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3056-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3056-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d3056-121">Header</span><span class="sxs-lookup"><span data-stu-id="d3056-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3056-122"><dt>Обжпас. h (включение Обжпас. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3056-122"><dt>ObjPath.h (include ObjPath.h)</dt></span></span> </dl>                                                      |
| <span data-ttu-id="d3056-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d3056-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3056-124"><dt>Фрамедин. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3056-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="d3056-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d3056-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3056-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3056-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3056-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3056-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3056-128">**кобжектпаспарсер**</span><span class="sxs-lookup"><span data-stu-id="d3056-128">**CObjectPathParser**</span></span>](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)
</dt> </dl>

<span data-ttu-id="d3056-129">�</span><span class="sxs-lookup"><span data-stu-id="d3056-129">�</span></span>

<span data-ttu-id="d3056-130">�</span><span class="sxs-lookup"><span data-stu-id="d3056-130">�</span></span>
