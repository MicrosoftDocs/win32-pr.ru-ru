---
title: Перечисление Додовнлоадпропертекс
description: Указывает идентификатор расширенных свойств для операции "выполнить скачивание".
keywords:
- Перечисление Додовнлоадпропертекс, Додовнлоадпропертекс
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 5df0f53778d9059ef8767f5b8052940847e36c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892069"
---
# <a name="dodownloadpropertyex-enumeration"></a><span data-ttu-id="1e09b-104">Перечисление Додовнлоадпропертекс</span><span class="sxs-lookup"><span data-stu-id="1e09b-104">DODownloadPropertyEx enumeration</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e09b-105">Перечисление **додовнлоадпропертекс** является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="1e09b-105">The **DODownloadPropertyEx** enumeration is deprecated.</span></span> <span data-ttu-id="1e09b-106">Вместо этого используйте перечисление [додовнлоадпроперти](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) с [идодовнлоад::](../do/nf-do-idodownload-getproperty.md) и [идодовнлоад:: SetProperty](../do/nf-do-idodownload-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1e09b-106">Instead, use the [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) enumeration with [IDODownload::GetProperty](../do/nf-do-idodownload-getproperty.md) and [IDODownload::SetProperty](../do/nf-do-idodownload-setproperty.md).</span></span>

<span data-ttu-id="1e09b-107">Перечисление **додовнлоадпропертекс** указывает идентификатор расширенных свойств для операции скачивания Do.</span><span class="sxs-lookup"><span data-stu-id="1e09b-107">The **DODownloadPropertyEx** enumeration specifies the ID of extended properties for the DO download operation.</span></span> <span data-ttu-id="1e09b-108">Это перечисление используется интерфейсом **идодовнлоадинтернал** , а значение **типа Variant** используется для получения и задания значения свойства.</span><span class="sxs-lookup"><span data-stu-id="1e09b-108">This enumeration is used by the **IDODownloadInternal** interface, and a **VARIANT** value is used to get and set the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e09b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e09b-109">Syntax</span></span>

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a><span data-ttu-id="1e09b-110">Константы</span><span class="sxs-lookup"><span data-stu-id="1e09b-110">Constants</span></span>

| <span data-ttu-id="1e09b-111">Требование</span><span class="sxs-lookup"><span data-stu-id="1e09b-111">Requirement</span></span> | <span data-ttu-id="1e09b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1e09b-112">Value</span></span> |
|-|-|
| <span data-ttu-id="1e09b-113">DODownloadPropertyEx_UpdateId</span><span class="sxs-lookup"><span data-stu-id="1e09b-113">DODownloadPropertyEx_UpdateId</span></span> | <span data-ttu-id="1e09b-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="1e09b-114">Reserved.</span></span> <span data-ttu-id="1e09b-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1e09b-115">Do not use.</span></span> |
| <span data-ttu-id="1e09b-116">DODownloadPropertyEx_CorrelationVector</span><span class="sxs-lookup"><span data-stu-id="1e09b-116">DODownloadPropertyEx_CorrelationVector</span></span> | <span data-ttu-id="1e09b-117">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="1e09b-117">Optional.</span></span> <span data-ttu-id="1e09b-118">Задает конкретный вектор корреляции для телеметрии.</span><span class="sxs-lookup"><span data-stu-id="1e09b-118">Sets a specific correlation vector for telemetry purposes.</span></span> <span data-ttu-id="1e09b-119">Тип VARIANT — VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="1e09b-119">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="1e09b-120">DODownloadPropertyEx_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="1e09b-120">DODownloadPropertyEx_DecryptionInfo</span></span> | <span data-ttu-id="1e09b-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="1e09b-121">Reserved.</span></span> <span data-ttu-id="1e09b-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1e09b-122">Do not use.</span></span> |
| <span data-ttu-id="1e09b-123">DODownloadPropertyEx_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="1e09b-123">DODownloadPropertyEx_IntegrityCheckInfo</span></span> | <span data-ttu-id="1e09b-124">Необязательный только для записи.</span><span class="sxs-lookup"><span data-stu-id="1e09b-124">Optional write-only.</span></span> <span data-ttu-id="1e09b-125">Задает расположение файлового хэша (ФФ), которое используется, чтобы выполнять проверку целостности во время выполнения для загруженного содержимого.</span><span class="sxs-lookup"><span data-stu-id="1e09b-125">Sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="1e09b-126">Тип VARIANT — VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="1e09b-126">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="1e09b-127">DODownloadPropertyEx_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="1e09b-127">DODownloadPropertyEx_IntegrityCheckMandatory</span></span> | <span data-ttu-id="1e09b-128">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="1e09b-128">Optional.</span></span> <span data-ttu-id="1e09b-129">Задает логический флаг, указывающий, является ли использование хэш-файла фрагмента (ФФ) обязательным.</span><span class="sxs-lookup"><span data-stu-id="1e09b-129">Sets a boolean flag indicating whether usage of the piece hash file (PHF) is mandatory.</span></span> <span data-ttu-id="1e09b-130">Если VARIANT_TRUE, загрузка будет прервана после сбоя проверки целостности.</span><span class="sxs-lookup"><span data-stu-id="1e09b-130">If VARIANT_TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="1e09b-131">Тип VARIANT — VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="1e09b-131">VARIANT type is VT_BOOL.</span></span> |
| <span data-ttu-id="1e09b-132">DODownloadPropertyEx_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="1e09b-132">DODownloadPropertyEx_TotalSizeBytes</span></span> | <span data-ttu-id="1e09b-133">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="1e09b-133">Reserved.</span></span> <span data-ttu-id="1e09b-134">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1e09b-134">Do not use.</span></span> |
| <span data-ttu-id="1e09b-135">DODownloadPropertyEx_TempLocalFileUsage</span><span class="sxs-lookup"><span data-stu-id="1e09b-135">DODownloadPropertyEx_TempLocalFileUsage</span></span> | <span data-ttu-id="1e09b-136">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="1e09b-136">Reserved.</span></span> <span data-ttu-id="1e09b-137">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1e09b-137">Do not use.</span></span> |

## <a name="requirements"></a><span data-ttu-id="1e09b-138">Требования</span><span class="sxs-lookup"><span data-stu-id="1e09b-138">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1e09b-139">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="1e09b-139">**Minimum supported client**</span></span> | <span data-ttu-id="1e09b-140">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="1e09b-140">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="1e09b-141">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="1e09b-141">**Minimum supported server**</span></span> | <span data-ttu-id="1e09b-142">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="1e09b-142">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="1e09b-143">**Header**</span><span class="sxs-lookup"><span data-stu-id="1e09b-143">**Header**</span></span> | <span data-ttu-id="1e09b-144">Додовнлоадинтернал. h</span><span class="sxs-lookup"><span data-stu-id="1e09b-144">DODownloadInternal.h</span></span> |
