---
title: Метод Ибаккграундкопифиле метода Progress (Deliveryoptimization. h)
description: Получает сведения о ходе перемещения файла.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- Метод Progress
- Метод Progress, интерфейс Ибаккграундкопифиле
- Интерфейс Ибаккграундкопифиле, метод Progress
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490266"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a><span data-ttu-id="a016d-106">Метод Ибаккграундкопифиле:: Progress</span><span class="sxs-lookup"><span data-stu-id="a016d-106">IBackgroundCopyFile::GetProgress method</span></span>

<span data-ttu-id="a016d-107">Получает сведения о ходе перемещения файла.</span><span class="sxs-lookup"><span data-stu-id="a016d-107">Retrieves information on the progress of the file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a016d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a016d-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="a016d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a016d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a016d-110">*ппрогресс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a016d-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a016d-111">Структура, члены которой указывают ход выполнения операции перемещения файла.</span><span class="sxs-lookup"><span data-stu-id="a016d-111">Structure whose members indicate the progress of the file transfer.</span></span> <span data-ttu-id="a016d-112">Дополнительные сведения о типе доступных сведений о ходе выполнения см. в разделе Структура [**BG_FILE_PROGRESS**](bg-file-progress.md) .</span><span class="sxs-lookup"><span data-stu-id="a016d-112">For details on the type of progress information available, see the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a016d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a016d-113">Return value</span></span>

<span data-ttu-id="a016d-114">Этот метод возвращает **S_OK** при успешном или одном из стандартных значений **HRESULT** com при ошибке.</span><span class="sxs-lookup"><span data-stu-id="a016d-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a016d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a016d-115">Requirements</span></span>



| <span data-ttu-id="a016d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a016d-116">Requirement</span></span> | <span data-ttu-id="a016d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a016d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a016d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a016d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a016d-119">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a016d-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a016d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a016d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a016d-121">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="a016d-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a016d-122">Header</span><span class="sxs-lookup"><span data-stu-id="a016d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a016d-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a016d-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a016d-124">IDL</span><span class="sxs-lookup"><span data-stu-id="a016d-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a016d-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a016d-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a016d-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a016d-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a016d-127"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a016d-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a016d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a016d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a016d-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a016d-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a016d-130">IID</span><span class="sxs-lookup"><span data-stu-id="a016d-130">IID</span></span><br/>                      | <span data-ttu-id="a016d-131">IID_IBackgroundCopyFile определен как 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="a016d-131">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="a016d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a016d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a016d-133">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="a016d-133">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="a016d-134">**ибаккграундкопифиле**</span><span class="sxs-lookup"><span data-stu-id="a016d-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="a016d-135">**Использованием метода ibackgroundcopyjob:: Progress**</span><span class="sxs-lookup"><span data-stu-id="a016d-135">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





