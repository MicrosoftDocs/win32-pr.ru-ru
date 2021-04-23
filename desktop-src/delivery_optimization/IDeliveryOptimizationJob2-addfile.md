---
title: IDeliveryOptimizationJob2 AddFile, метод
description: Метод AddFile добавляет один файл к существующему заданию DO.
keywords:
- AddFile - метод
- Метод AddFile, интерфейс IDeliveryOptimizationJob2
- Интерфейс IDeliveryOptimizationJob2, метод AddFile
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8225db8cccb1e1d3bb364ba1dc29f30526fe36b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135479"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a><span data-ttu-id="69736-106">Метод IDeliveryOptimizationJob2:: Аддфилевисранжес</span><span class="sxs-lookup"><span data-stu-id="69736-106">IDeliveryOptimizationJob2::AddFileWithRanges method</span></span>

<span data-ttu-id="69736-107">Метод AddFile добавляет один файл к существующему заданию DO.</span><span class="sxs-lookup"><span data-stu-id="69736-107">The AddFile method adds a single file to an existing DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="69736-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69736-108">Syntax</span></span>

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a><span data-ttu-id="69736-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="69736-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69736-110">*ИД* \[ для окне\]</span><span class="sxs-lookup"><span data-stu-id="69736-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69736-111">Строка идентификатора файла, однозначно определяющая загружаемый файл.</span><span class="sxs-lookup"><span data-stu-id="69736-111">The file ID string, which uniquely identifies the file to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="69736-112">*ремотеурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69736-112">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69736-113">URL-адрес файла, который выполняет попытку подключения для скачивания файла.</span><span class="sxs-lookup"><span data-stu-id="69736-113">The file URL that DO will attempt to connect to download the file.</span></span>

</dd> <dt>

<span data-ttu-id="69736-114">*ранжекаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69736-114">*rangeCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69736-115">Количество элементов, содержащихся в *диапазонах*.</span><span class="sxs-lookup"><span data-stu-id="69736-115">The number of items contained in *ranges*.</span></span> <span data-ttu-id="69736-116">Нулевое значение означает, что для файла не используются диапазоны.</span><span class="sxs-lookup"><span data-stu-id="69736-116">A zero value means that no ranges are used for the file.</span></span>

</dd> <dt>

<span data-ttu-id="69736-117">*диапазоны* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69736-117">*ranges* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69736-118">Необязательный список диапазонов.</span><span class="sxs-lookup"><span data-stu-id="69736-118">The optional range list.</span></span> <span data-ttu-id="69736-119">Каждый диапазон в списке является структурой [**BG_FILE_RANGE**](bg-file-range.md) .</span><span class="sxs-lookup"><span data-stu-id="69736-119">Each range in the list is a [**BG_FILE_RANGE**](bg-file-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="69736-120">*riid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69736-120">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69736-121">Тип объекта, содержащегося в объекте.</span><span class="sxs-lookup"><span data-stu-id="69736-121">The type of object contained in object.</span></span> <span data-ttu-id="69736-122">Он должен иметь тип IID_IDeliveryOptimizationFile.</span><span class="sxs-lookup"><span data-stu-id="69736-122">This must by of type IID_IDeliveryOptimizationFile.</span></span>

</dd> <dt>

<span data-ttu-id="69736-123">*объект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="69736-123">*object* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69736-124">Объект Иделиверйоптимизатионфиле, представляющий загружаемый файл.</span><span class="sxs-lookup"><span data-stu-id="69736-124">The IDeliveryOptimizationFile object, which represents the download file.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69736-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69736-125">Return value</span></span>

<span data-ttu-id="69736-126">Этот метод возвращает S_OK при успешном или одном из стандартных значений HRESULT при ошибке.</span><span class="sxs-lookup"><span data-stu-id="69736-126">This method returns S_OK on success or one of the standard HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="69736-127">Требования</span><span class="sxs-lookup"><span data-stu-id="69736-127">Requirements</span></span>

| <span data-ttu-id="69736-128">Требование</span><span class="sxs-lookup"><span data-stu-id="69736-128">Requirement</span></span> | <span data-ttu-id="69736-129">Значение</span><span class="sxs-lookup"><span data-stu-id="69736-129">Value</span></span> |
|---------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="69736-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69736-130">Minimum supported client</span></span>  | <span data-ttu-id="69736-131">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="69736-131">Windows 10, version 1803 \[desktop apps only\]</span></span>                                  |
| <span data-ttu-id="69736-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69736-132">Minimum supported server</span></span>  | <span data-ttu-id="69736-133">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="69736-133">Windows Server, version 1709 \[desktop apps only\]</span></span>                              |
| <span data-ttu-id="69736-134">Header</span><span class="sxs-lookup"><span data-stu-id="69736-134">Header</span></span>                    | <span data-ttu-id="69736-135">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="69736-135">Deliveryoptimization.h</span></span>                                                          |
| <span data-ttu-id="69736-136">IDL</span><span class="sxs-lookup"><span data-stu-id="69736-136">IDL</span></span>                       | <span data-ttu-id="69736-137">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="69736-137">DeliveryOptimization.idl</span></span>                                                        |
| <span data-ttu-id="69736-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="69736-138">Library</span></span>                   | <span data-ttu-id="69736-139">Досвк. lib</span><span class="sxs-lookup"><span data-stu-id="69736-139">Dosvc.lib</span></span>                                                                       |
| <span data-ttu-id="69736-140">DLL</span><span class="sxs-lookup"><span data-stu-id="69736-140">DLL</span></span>                       | <span data-ttu-id="69736-141">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="69736-141">Dosvc.dll</span></span>                                                                       |
| <span data-ttu-id="69736-142">IID</span><span class="sxs-lookup"><span data-stu-id="69736-142">IID</span></span>                       | <span data-ttu-id="69736-143">IID_IDeliveryOptimizationJob определяется как EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="69736-143">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span> |

## <a name="see-also"></a><span data-ttu-id="69736-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69736-144">See also</span></span>

[<span data-ttu-id="69736-145">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="69736-145">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
