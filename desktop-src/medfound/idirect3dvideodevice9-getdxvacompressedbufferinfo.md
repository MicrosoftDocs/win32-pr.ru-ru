---
description: Возвращает сведения о сжатых буферах, необходимых для декодирования с аппаратным ускорением.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'Метод IDirect3DVideoDevice9:: Жетдксвакомпресседбуфферинфо (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 2bd2dcdd931ac8778e4f1c11f1479fe54e23d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711346"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a><span data-ttu-id="93bd4-103">Метод IDirect3DVideoDevice9:: Жетдксвакомпресседбуфферинфо</span><span class="sxs-lookup"><span data-stu-id="93bd4-103">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo method</span></span>

<span data-ttu-id="93bd4-104">Возвращает сведения о сжатых буферах, необходимых для декодирования с аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="93bd4-104">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="93bd4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93bd4-105">Syntax</span></span>


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="93bd4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="93bd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93bd4-107">*пгуид*</span><span class="sxs-lookup"><span data-stu-id="93bd4-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="93bd4-108">Указатель на идентификатор GUID, указывающий профиль ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="93bd4-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="93bd4-109">Чтобы получить список поддерживаемых профилей, вызовите [**IDirect3DVideoDevice9:: жетдксвагуидс**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="93bd4-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="93bd4-110">*пункомпдата*</span><span class="sxs-lookup"><span data-stu-id="93bd4-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="93bd4-111">Указатель на структуру [**дксваункомпдатаинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) , указывающую размер и формат пикселей для несжатых данных.</span><span class="sxs-lookup"><span data-stu-id="93bd4-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="93bd4-112">*пнумбуфферс*</span><span class="sxs-lookup"><span data-stu-id="93bd4-112">*pNumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="93bd4-113">В поле входные данные указывает количество элементов в массиве *пбуфферинфо* .</span><span class="sxs-lookup"><span data-stu-id="93bd4-113">On input, specifies the number of elements in the *pBufferInfo* array.</span></span> <span data-ttu-id="93bd4-114">Если *пбуфферинфо* имеет **значение NULL**, значение `*pNumBuffers` должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="93bd4-114">If *pBufferInfo* is **NULL**, the value of `*pNumBuffers` must be zero.</span></span>

<span data-ttu-id="93bd4-115">В выходных данных, если *пбуфферинфо* имеет **значение NULL**, *пнумбуфферс* получает размер массива для выделения.</span><span class="sxs-lookup"><span data-stu-id="93bd4-115">On output, if *pBufferInfo* is **NULL**, *pNumBuffers* receives the size of array to allocate.</span></span> <span data-ttu-id="93bd4-116">В противном случае *пнумбуфферс* получает фактическое число элементов, копируемых в массив *пбуфферинфо* .</span><span class="sxs-lookup"><span data-stu-id="93bd4-116">Otherwise, *pNumBuffers* receives the actual number of elements that are copied to the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="93bd4-117">*пбуфферинфо*</span><span class="sxs-lookup"><span data-stu-id="93bd4-117">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="93bd4-118">Адрес массива структур [**дксвакомпбуфферинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="93bd4-118">Address of an array of [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures or **NULL**.</span></span> <span data-ttu-id="93bd4-119">Если значение не равно **null**, метод копирует список структур **дксвакомпбуфферинфо** в этот массив.</span><span class="sxs-lookup"><span data-stu-id="93bd4-119">If the value is non-**NULL**, the method copies a list of **DXVACompBufferInfo** structures to this array.</span></span> <span data-ttu-id="93bd4-120">Каждая структура соответствует одному типу сжатого буфера данных, который используется ускорителем видео.</span><span class="sxs-lookup"><span data-stu-id="93bd4-120">Each structure corresponds to one type of compressed data buffer that is used by the video accelerator.</span></span>

<span data-ttu-id="93bd4-121">Перед вызовом этого метода установите все элементы массива в ноль.</span><span class="sxs-lookup"><span data-stu-id="93bd4-121">Set all of the array elements to zero before calling this method.</span></span>

<span data-ttu-id="93bd4-122">Каждый индекс массива соответствует одному из типов ДКСВА Surface, определенных в дксва. h.</span><span class="sxs-lookup"><span data-stu-id="93bd4-122">Each array index corresponds to one of the DXVA surface types defined in dxva.h.</span></span> <span data-ttu-id="93bd4-123">Видеоускоритель возвращает список, в котором **дксва число числовых \_ \_ типов в \_ \_ буфере Comp** .</span><span class="sxs-lookup"><span data-stu-id="93bd4-123">The video accelerator returns a list of up to **DXVA\_NUM\_TYPES\_COMP\_BUFFERS** array entries.</span></span> <span data-ttu-id="93bd4-124">Дополнительные сведения см. в [спецификации дксва 1,0](/windows-hardware/drivers/display/directx-video-acceleration), раздел 3,4, "список описания буферов".</span><span class="sxs-lookup"><span data-stu-id="93bd4-124">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration), section 3.4, "Buffer Description List."</span></span> <span data-ttu-id="93bd4-125">Если определенный тип буфера не используется профилем ДКСВА, запись в этом индексе будет содержать нули для всех значений.</span><span class="sxs-lookup"><span data-stu-id="93bd4-125">If a particular buffer type is not used by the DXVA profile, the entry at that index contains zeros for all values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93bd4-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93bd4-126">Return value</span></span>

<span data-ttu-id="93bd4-127">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="93bd4-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="93bd4-128">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93bd4-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="93bd4-129">Требования</span><span class="sxs-lookup"><span data-stu-id="93bd4-129">Requirements</span></span>



| <span data-ttu-id="93bd4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="93bd4-130">Requirement</span></span> | <span data-ttu-id="93bd4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="93bd4-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="93bd4-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93bd4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="93bd4-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93bd4-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="93bd4-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93bd4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="93bd4-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93bd4-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="93bd4-136">Header</span><span class="sxs-lookup"><span data-stu-id="93bd4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="93bd4-137"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="93bd4-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93bd4-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93bd4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93bd4-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="93bd4-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
