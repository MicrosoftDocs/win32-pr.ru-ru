---
title: Перечисление Деливерйоптимизатионфилепроперти (Deliveryoptimization. h)
description: Перечисление Деливерйоптимизатионфилепроперти указывает идентификатор необязательного свойства для файла DO.
keywords:
- Перечисление Деливерйоптимизатионфилепроперти
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710485"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a><span data-ttu-id="809bd-104">Перечисление Деливерйоптимизатионфилепроперти</span><span class="sxs-lookup"><span data-stu-id="809bd-104">DeliveryOptimizationFileProperty enumeration</span></span>

<span data-ttu-id="809bd-105">Перечисление Деливерйоптимизатионфилепроперти указывает идентификатор необязательного свойства для файла DO.</span><span class="sxs-lookup"><span data-stu-id="809bd-105">The DeliveryOptimizationFileProperty enumeration specifies the ID of an optional property for the DO file.</span></span> <span data-ttu-id="809bd-106">Это перечисление используется в интерфейсе IDeliveryOptimizationFile2, где передается значение свойства типа VARIANT.</span><span class="sxs-lookup"><span data-stu-id="809bd-106">This enumeration is used in the IDeliveryOptimizationFile2 interface where the property value of type VARIANT is passed</span></span>

## <a name="syntax"></a><span data-ttu-id="809bd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="809bd-107">Syntax</span></span>

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a><span data-ttu-id="809bd-108">Константы</span><span class="sxs-lookup"><span data-stu-id="809bd-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="809bd-109">DOFilePropertyId_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="809bd-109">DOFilePropertyId_DecryptionInfo</span></span>
</dt> <dd>

<span data-ttu-id="809bd-110">Идентификатор свойства DOFilePropertyId_DecryptionInfo задает сведения о расшифровке в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="809bd-110">The DOFilePropertyId_DecryptionInfo property ID sets decryption information in the form of a JSON string.</span></span> <span data-ttu-id="809bd-111">DOFilePropertyId_DecryptionInfo является свойством только для записи типа VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="809bd-111">DOFilePropertyId_DecryptionInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="809bd-112">DOFilePropertyId_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="809bd-112">DOFilePropertyId_IntegrityCheckInfo</span></span>
</dt> <dd>

<span data-ttu-id="809bd-113">Идентификатор свойства DOFilePropertyId_IntegrityCheckInfo задает расположение файлового хэша (ФФ), которое используется, чтобы выполнять проверку целостности во время выполнения для загруженного содержимого.</span><span class="sxs-lookup"><span data-stu-id="809bd-113">The DOFilePropertyId_IntegrityCheckInfo property ID sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="809bd-114">DOFilePropertyId_IntegrityCheckInfo является свойством только для записи типа VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="809bd-114">DOFilePropertyId_IntegrityCheckInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="809bd-115">DOFilePropertyId_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="809bd-115">DOFilePropertyId_IntegrityCheckMandatory</span></span>
</dt> <dd>

<span data-ttu-id="809bd-116">Идентификатор свойства DOFilePropertyId_IntegrityCheckMandatory задает логический флаг, указывающий, является ли использование ФФ обязательным.</span><span class="sxs-lookup"><span data-stu-id="809bd-116">The DOFilePropertyId_IntegrityCheckMandatory property ID sets a boolean flag indicating whether usage of the PHF is mandatory.</span></span> <span data-ttu-id="809bd-117">Если значение — TRUE, загрузка будет прервана после сбоя проверки целостности.</span><span class="sxs-lookup"><span data-stu-id="809bd-117">If TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="809bd-118">DOFilePropertyId_IntegrityCheckMandatory является свойством для чтения и записи типа VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="809bd-118">DOFilePropertyId_IntegrityCheckMandatory is a Read/Write property of type VT_BOOL.</span></span>

</dd> <dt>

<span data-ttu-id="809bd-119">DOFilePropertyId_DownloadSinkFilePath</span><span class="sxs-lookup"><span data-stu-id="809bd-119">DOFilePropertyId_DownloadSinkFilePath</span></span>
</dt> <dd>

<span data-ttu-id="809bd-120">Идентификатор свойства DOFilePropertyId_DownloadSinkFilePath задает полное расположение файловой системы, где следует хранить загруженные фрагменты.</span><span class="sxs-lookup"><span data-stu-id="809bd-120">The DOFilePropertyId_DownloadSinkFilePath property ID sets a fully qualified file system location where DO should store the downloaded pieces.</span></span> <span data-ttu-id="809bd-121">DOFilePropertyId_DownloadSinkFilePath имеет тип VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="809bd-121">DOFilePropertyId_DownloadSinkFilePath is of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="809bd-122">DOFilePropertyId_DownloadSinkMemoryStream</span><span class="sxs-lookup"><span data-stu-id="809bd-122">DOFilePropertyId_DownloadSinkMemoryStream</span></span>
</dt> <dd>

<span data-ttu-id="809bd-123">Идентификатор свойства DOFilePropertyId_DownloadSinkMemoryStream является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="809bd-123">The DOFilePropertyId_DownloadSinkMemoryStream property ID is deprecated.</span></span> <span data-ttu-id="809bd-124">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="809bd-124">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="809bd-125">DOFilePropertyId_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="809bd-125">DOFilePropertyId_TotalSizeBytes</span></span>
</dt> <dd>

<span data-ttu-id="809bd-126">Идентификатор свойства DOFilePropertyId_TotalSizeBytes указывает общий размер загрузки.</span><span class="sxs-lookup"><span data-stu-id="809bd-126">The DOFilePropertyId_TotalSizeBytes property ID specifies the total download size.</span></span> <span data-ttu-id="809bd-127">DOFilePropertyId_TotalSizeBytes имеет тип VT_UI8.</span><span class="sxs-lookup"><span data-stu-id="809bd-127">DOFilePropertyId_TotalSizeBytes is of type VT_UI8.</span></span>
</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="809bd-128">Требования</span><span class="sxs-lookup"><span data-stu-id="809bd-128">Requirements</span></span>

| <span data-ttu-id="809bd-129">Требование</span><span class="sxs-lookup"><span data-stu-id="809bd-129">Requirement</span></span> | <span data-ttu-id="809bd-130">Значение</span><span class="sxs-lookup"><span data-stu-id="809bd-130">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="809bd-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="809bd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="809bd-132">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="809bd-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="809bd-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="809bd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="809bd-134">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="809bd-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="809bd-135">Header</span><span class="sxs-lookup"><span data-stu-id="809bd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="809bd-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="809bd-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
