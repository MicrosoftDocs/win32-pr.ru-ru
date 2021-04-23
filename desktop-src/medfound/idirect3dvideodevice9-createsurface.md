---
description: Создает сжатую поверхность для декодирования DirectX Video Acceleration (ДКСВА).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'Метод IDirect3DVideoDevice9:: Креатесурфаце (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156174"
---
# <a name="idirect3dvideodevice9createsurface-method"></a><span data-ttu-id="2dcf9-103">Метод IDirect3DVideoDevice9:: Креатесурфаце</span><span class="sxs-lookup"><span data-stu-id="2dcf9-103">IDirect3DVideoDevice9::CreateSurface method</span></span>

<span data-ttu-id="2dcf9-104">Создает сжатую поверхность для декодирования DirectX Video Acceleration (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="2dcf9-104">Creates a compressed surface for DirectX Video Acceleration (DXVA) decoding.</span></span>

<span data-ttu-id="2dcf9-105">Чтобы получить требования к поверхности, вызовите метод [**IDirect3DVideoDevice9:: жетдксвакомпресседбуфферинфо**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) и изучите возвращенные структуры [**дксвакомпбуфферинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) .</span><span class="sxs-lookup"><span data-stu-id="2dcf9-105">To get the surface requirements, call [**IDirect3DVideoDevice9::GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) and examine the returned [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dcf9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2dcf9-106">Syntax</span></span>


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a><span data-ttu-id="2dcf9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2dcf9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dcf9-108">*Width*</span><span class="sxs-lookup"><span data-stu-id="2dcf9-108">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="2dcf9-109">Ширина поверхности в пикселях.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-109">The width of the surface, in pixels.</span></span> <span data-ttu-id="2dcf9-110">Установите этот параметр равным **дксвакомпбуфферинфо. видстокреате**.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-110">Set this parameter equal to **DXVACompBufferInfo.WidthToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="2dcf9-111">*Height*</span><span class="sxs-lookup"><span data-stu-id="2dcf9-111">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="2dcf9-112">Высота поверхности в пикселях.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-112">The height of the surface, in pixels.</span></span> <span data-ttu-id="2dcf9-113">Установите этот параметр равным **дксвакомпбуфферинфо. хеигхттокреате**.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-113">Set this parameter equal to **DXVACompBufferInfo.HeightToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="2dcf9-114">*Буферы обмена*</span><span class="sxs-lookup"><span data-stu-id="2dcf9-114">*BackBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="2dcf9-115">Число задних буферов.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-115">The number of back buffers.</span></span> <span data-ttu-id="2dcf9-116">Этот параметр может быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-116">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2dcf9-117">*Формат*</span><span class="sxs-lookup"><span data-stu-id="2dcf9-117">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="2dcf9-118">Формат пикселей, указанный как значение **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="2dcf9-118">The pixel format, specified as a **D3DFORMAT** value.</span></span> <span data-ttu-id="2dcf9-119">Установите этот параметр равным **дксвакомпбуфферинфо. Format**.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-119">Set this parameter equal to **DXVACompBufferInfo.Format**.</span></span>

</dd> <dt>

<span data-ttu-id="2dcf9-120">*Пул.*</span><span class="sxs-lookup"><span data-stu-id="2dcf9-120">*Pool*</span></span> 
</dt> <dd>

<span data-ttu-id="2dcf9-121">Пул памяти, в котором создается поверхность, указанная в качестве значения **D3DPOOL** .</span><span class="sxs-lookup"><span data-stu-id="2dcf9-121">The memory pool in which to create the surface, specified as a **D3DPOOL** value.</span></span> <span data-ttu-id="2dcf9-122">Установите этот параметр равным **дксвакомпбуфферинфо. pool**.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-122">Set this parameter equal to **DXVACompBufferInfo.Pool**.</span></span>

</dd> <dt>

<span data-ttu-id="2dcf9-123">*Использование*</span><span class="sxs-lookup"><span data-stu-id="2dcf9-123">*Usage*</span></span> 
</dt> <dd>

<span data-ttu-id="2dcf9-124">Побитовая операция **или** для одной или нескольких констант **D3DUSAGE** .</span><span class="sxs-lookup"><span data-stu-id="2dcf9-124">A bitwise **OR** of one or more **D3DUSAGE** constants.</span></span> <span data-ttu-id="2dcf9-125">Установите этот параметр равным **дксвакомпбуфферинфо. Usage**.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-125">Set this parameter equal to **DXVACompBufferInfo.Usage**.</span></span>

</dd> <dt>

<span data-ttu-id="2dcf9-126">*ппсурфаце*</span><span class="sxs-lookup"><span data-stu-id="2dcf9-126">*ppSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="2dcf9-127">Получает указатель на интерфейс **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="2dcf9-127">Receives a pointer to the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="2dcf9-128">Вызывающий объект должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-128">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="2dcf9-129">*пшаредхандле*</span><span class="sxs-lookup"><span data-stu-id="2dcf9-129">*pSharedHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="2dcf9-130">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-130">Reserved.</span></span> <span data-ttu-id="2dcf9-131">Задайте **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-131">Set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dcf9-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dcf9-132">Return value</span></span>

<span data-ttu-id="2dcf9-133">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2dcf9-133">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2dcf9-134">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2dcf9-134">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dcf9-135">Требования</span><span class="sxs-lookup"><span data-stu-id="2dcf9-135">Requirements</span></span>



| <span data-ttu-id="2dcf9-136">Требование</span><span class="sxs-lookup"><span data-stu-id="2dcf9-136">Requirement</span></span> | <span data-ttu-id="2dcf9-137">Значение</span><span class="sxs-lookup"><span data-stu-id="2dcf9-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2dcf9-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2dcf9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2dcf9-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2dcf9-139">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2dcf9-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2dcf9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2dcf9-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2dcf9-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2dcf9-142">Header</span><span class="sxs-lookup"><span data-stu-id="2dcf9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dcf9-143"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dcf9-143"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dcf9-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2dcf9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dcf9-145">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="2dcf9-145">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




