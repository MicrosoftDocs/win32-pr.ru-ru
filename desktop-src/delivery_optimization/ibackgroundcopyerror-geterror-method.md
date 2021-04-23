---
title: Метод Ибаккграундкоперрор-Error (Deliveryoptimization. h)
description: Извлекает код ошибки и определяет контекст, в котором произошла ошибка.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- Метод метода с ошибками
- Метод Ибаккграундкоперрор, интерфейс
- Интерфейс Ибаккграундкоперрор, метод method
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988564"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a><span data-ttu-id="d05e4-106">Метод Ибаккграундкоперрор:: Error</span><span class="sxs-lookup"><span data-stu-id="d05e4-106">IBackgroundCopyError::GetError method</span></span>

<span data-ttu-id="d05e4-107">Извлекает код ошибки и определяет контекст, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="d05e4-107">Retrieves the error code and identify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="d05e4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d05e4-108">Syntax</span></span>


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="d05e4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d05e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d05e4-110">*пконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d05e4-110">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d05e4-111">Контекст, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="d05e4-111">Context in which the error occurred.</span></span> <span data-ttu-id="d05e4-112">Список значений контекста см. в разделе Перечисление [**BG_ERROR_CONTEXT**](bg-error-context.md) .</span><span class="sxs-lookup"><span data-stu-id="d05e4-112">For a list of context values, see the [**BG_ERROR_CONTEXT**](bg-error-context.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="d05e4-113">*перроркоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d05e4-113">*pErrorCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d05e4-114">Код ошибки произошедшей ошибки.</span><span class="sxs-lookup"><span data-stu-id="d05e4-114">Error code of the error that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d05e4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d05e4-115">Return value</span></span>

<span data-ttu-id="d05e4-116">Этот метод возвращает **S_OK** при успешном или одном из стандартных значений HRESULT com при ошибке.</span><span class="sxs-lookup"><span data-stu-id="d05e4-116">This method returns **S_OK** on success or one of the standard COM HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d05e4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d05e4-117">Requirements</span></span>



| <span data-ttu-id="d05e4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d05e4-118">Requirement</span></span> | <span data-ttu-id="d05e4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d05e4-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d05e4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d05e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d05e4-121">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="d05e4-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d05e4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d05e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d05e4-123">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="d05e4-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d05e4-124">Header</span><span class="sxs-lookup"><span data-stu-id="d05e4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d05e4-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d05e4-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d05e4-126">IDL</span><span class="sxs-lookup"><span data-stu-id="d05e4-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d05e4-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d05e4-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d05e4-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d05e4-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d05e4-129"><dt>Досвк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d05e4-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d05e4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d05e4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d05e4-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d05e4-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d05e4-132">IID</span><span class="sxs-lookup"><span data-stu-id="d05e4-132">IID</span></span><br/>                      | <span data-ttu-id="d05e4-133">IID_IBackgroundCopyError определен как 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="d05e4-133">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d05e4-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d05e4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d05e4-135">**ибаккграундкоперрор**</span><span class="sxs-lookup"><span data-stu-id="d05e4-135">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="d05e4-136">**Ибаккграундкоперрор:: onfile**</span><span class="sxs-lookup"><span data-stu-id="d05e4-136">**IBackgroundCopyError::GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





