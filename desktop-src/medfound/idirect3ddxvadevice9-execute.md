---
description: Выполняет операцию декодирования DirectX Video Acceleration (ДКСВА).
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'Метод IDirect3DDXVADevice9:: Execute (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711793"
---
# <a name="idirect3ddxvadevice9execute-method"></a><span data-ttu-id="24f34-103">Метод IDirect3DDXVADevice9:: Execute</span><span class="sxs-lookup"><span data-stu-id="24f34-103">IDirect3DDXVADevice9::Execute method</span></span>

<span data-ttu-id="24f34-104">Выполняет операцию декодирования DirectX Video Acceleration (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="24f34-104">Performs a DirectX Video Acceleration (DXVA) decoding operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f34-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24f34-105">Syntax</span></span>


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="24f34-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="24f34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f34-107">*функтионнум*</span><span class="sxs-lookup"><span data-stu-id="24f34-107">*FunctionNum*</span></span> 
</dt> <dd>

<span data-ttu-id="24f34-108">**DWORD** , содержащий один или несколько номеров функций дксва.</span><span class="sxs-lookup"><span data-stu-id="24f34-108">A **DWORD** that contains one or more DXVA function numbers.</span></span> <span data-ttu-id="24f34-109">Дополнительные сведения см. в [спецификации дксва 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="24f34-109">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> <dt>

<span data-ttu-id="24f34-110">*пинпутдата*</span><span class="sxs-lookup"><span data-stu-id="24f34-110">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="24f34-111">Указатель на буфер, содержащий входные данные для операции декодирования.</span><span class="sxs-lookup"><span data-stu-id="24f34-111">A pointer to a buffer that contains input data for the decoding operation.</span></span> <span data-ttu-id="24f34-112">Значение этих данных зависит от типа поверхности и номера функции.</span><span class="sxs-lookup"><span data-stu-id="24f34-112">The meaning of this data depends on the surface type and function number.</span></span>

</dd> <dt>

<span data-ttu-id="24f34-113">*инпутсизе*</span><span class="sxs-lookup"><span data-stu-id="24f34-113">*InputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="24f34-114">Размер входных данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="24f34-114">The size of the input data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="24f34-115">*OutputData*</span><span class="sxs-lookup"><span data-stu-id="24f34-115">*OutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="24f34-116">Указатель на буфер, в который видео-ускоритель записывает выходные данные.</span><span class="sxs-lookup"><span data-stu-id="24f34-116">Pointer to a buffer where the video accelerator writes output data.</span></span>

</dd> <dt>

<span data-ttu-id="24f34-117">*аутпутсизе*</span><span class="sxs-lookup"><span data-stu-id="24f34-117">*OutputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="24f34-118">Размер буфера *аутпутдата* в байтах.</span><span class="sxs-lookup"><span data-stu-id="24f34-118">The size of the *OutputData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="24f34-119">*нумбуфферс*</span><span class="sxs-lookup"><span data-stu-id="24f34-119">*NumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="24f34-120">Число элементов в массиве *пбуфферинфо* .</span><span class="sxs-lookup"><span data-stu-id="24f34-120">The number of elements in the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="24f34-121">*пбуфферинфо*</span><span class="sxs-lookup"><span data-stu-id="24f34-121">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="24f34-122">Указатель на массив структур [**дксвабуфферинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) .</span><span class="sxs-lookup"><span data-stu-id="24f34-122">A pointer to an array of [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f34-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24f34-123">Return value</span></span>

<span data-ttu-id="24f34-124">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="24f34-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="24f34-125">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24f34-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f34-126">Требования</span><span class="sxs-lookup"><span data-stu-id="24f34-126">Requirements</span></span>



| <span data-ttu-id="24f34-127">Требование</span><span class="sxs-lookup"><span data-stu-id="24f34-127">Requirement</span></span> | <span data-ttu-id="24f34-128">Значение</span><span class="sxs-lookup"><span data-stu-id="24f34-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="24f34-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24f34-129">Minimum supported client</span></span><br/> | <span data-ttu-id="24f34-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24f34-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24f34-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24f34-131">Minimum supported server</span></span><br/> | <span data-ttu-id="24f34-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="24f34-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="24f34-133">Header</span><span class="sxs-lookup"><span data-stu-id="24f34-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="24f34-134"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="24f34-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24f34-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24f34-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f34-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="24f34-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
