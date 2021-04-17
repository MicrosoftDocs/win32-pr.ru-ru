---
description: Начинает обработку для создания декодированного изображения.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'Метод IDirect3DDXVADevice9:: Бегинфраме (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711794"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a><span data-ttu-id="655df-103">Метод IDirect3DDXVADevice9:: Бегинфраме</span><span class="sxs-lookup"><span data-stu-id="655df-103">IDirect3DDXVADevice9::BeginFrame method</span></span>

<span data-ttu-id="655df-104">Начинает обработку для создания декодированного изображения.</span><span class="sxs-lookup"><span data-stu-id="655df-104">Begins the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="655df-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="655df-105">Syntax</span></span>


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a><span data-ttu-id="655df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="655df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="655df-107">*пдстсурфаце*</span><span class="sxs-lookup"><span data-stu-id="655df-107">*pDstSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="655df-108">Указатель на интерфейс **IDirect3DSurface9** несжатой целевой поверхности.</span><span class="sxs-lookup"><span data-stu-id="655df-108">A pointer to the **IDirect3DSurface9** interface of the uncompressed destination surface.</span></span>

</dd> <dt>

<span data-ttu-id="655df-109">*сизеинпутдата*</span><span class="sxs-lookup"><span data-stu-id="655df-109">*SizeInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="655df-110">Размер буфера, заданного параметром *пинпутдата*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="655df-110">The size of the buffer specified by *pInputData*, in bytes.</span></span> <span data-ttu-id="655df-111">Значение должно быть равно 2.</span><span class="sxs-lookup"><span data-stu-id="655df-111">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="655df-112">*пинпутдата*</span><span class="sxs-lookup"><span data-stu-id="655df-112">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="655df-113">Указатель на буфер, содержащий данные для ускорителя видео.</span><span class="sxs-lookup"><span data-stu-id="655df-113">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="655df-114">Этот буфер должен содержать индекс кадра (от нуля), указанный в качестве значения **слова** .</span><span class="sxs-lookup"><span data-stu-id="655df-114">This buffer must contain the zero-based frame index, specified as a **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="655df-115">*псизеаутпутдата*</span><span class="sxs-lookup"><span data-stu-id="655df-115">*pSizeOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="655df-116">Размер буфера, заданного параметром *паутпутдата*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="655df-116">The size of the buffer specified by *pOutputData*, in bytes.</span></span> <span data-ttu-id="655df-117">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="655df-117">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="655df-118">*паутпутдата*</span><span class="sxs-lookup"><span data-stu-id="655df-118">*pOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="655df-119">Указатель на буфер, в который может записываться видео-ускоритель.</span><span class="sxs-lookup"><span data-stu-id="655df-119">Pointer to a buffer that the video accelerator can write to.</span></span> <span data-ttu-id="655df-120">Присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="655df-120">Set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="655df-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="655df-121">Return value</span></span>

<span data-ttu-id="655df-122">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="655df-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="655df-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="655df-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="655df-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="655df-124">Remarks</span></span>

<span data-ttu-id="655df-125">Для каждого вызова **бегинфраме** декодер должен выполнить соответствующий вызов [**IDirect3DDXVADevice9:: ендфраме**](idirect3ddxvadevice9-endframe.md).</span><span class="sxs-lookup"><span data-stu-id="655df-125">For each call to **BeginFrame**, the decoder must make a corresponding call to [**IDirect3DDXVADevice9::EndFrame**](idirect3ddxvadevice9-endframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="655df-126">Требования</span><span class="sxs-lookup"><span data-stu-id="655df-126">Requirements</span></span>



| <span data-ttu-id="655df-127">Требование</span><span class="sxs-lookup"><span data-stu-id="655df-127">Requirement</span></span> | <span data-ttu-id="655df-128">Значение</span><span class="sxs-lookup"><span data-stu-id="655df-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="655df-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="655df-129">Minimum supported client</span></span><br/> | <span data-ttu-id="655df-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="655df-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="655df-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="655df-131">Minimum supported server</span></span><br/> | <span data-ttu-id="655df-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="655df-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="655df-133">Header</span><span class="sxs-lookup"><span data-stu-id="655df-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="655df-134"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="655df-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="655df-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="655df-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="655df-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="655df-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




