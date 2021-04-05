---
description: Создайте ресурс текстуры из файла, находящегося в системной памяти.
ms.assetid: 63eac44b-0540-457f-96c0-d151fbd44df0
title: Функция D3DX10CreateTextureFromMemory (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 885f734cd9caeaccbab27b2fcdb258c032c5d7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000338"
---
# <a name="d3dx10createtexturefrommemory-function"></a><span data-ttu-id="b3581-103">Функция D3DX10CreateTextureFromMemory</span><span class="sxs-lookup"><span data-stu-id="b3581-103">D3DX10CreateTextureFromMemory function</span></span>

<span data-ttu-id="b3581-104">Создайте ресурс текстуры из файла, находящегося в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="b3581-104">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3581-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3581-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromMemory(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="b3581-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3581-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3581-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3581-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3581-108">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="b3581-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="b3581-109">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурс.</span><span class="sxs-lookup"><span data-stu-id="b3581-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="b3581-110">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3581-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3581-111">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3581-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3581-112">Указатель на ресурс в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="b3581-112">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="b3581-113">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3581-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3581-114">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3581-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3581-115">Размер ресурса в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="b3581-115">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="b3581-116">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3581-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3581-117">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3581-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="b3581-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="b3581-118">Optional.</span></span> <span data-ttu-id="b3581-119">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="b3581-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="b3581-120">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3581-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3581-121">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3581-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="b3581-122">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="b3581-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="b3581-123">Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.</span><span class="sxs-lookup"><span data-stu-id="b3581-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="b3581-124">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b3581-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3581-125">Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="b3581-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="b3581-126">Адрес указателя на созданный ресурс.</span><span class="sxs-lookup"><span data-stu-id="b3581-126">Address of a pointer to the created resource.</span></span> <span data-ttu-id="b3581-127">См. раздел [**интерфейс ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="b3581-127">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="b3581-128">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b3581-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3581-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="b3581-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="b3581-130">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="b3581-130">A pointer to the return value.</span></span> <span data-ttu-id="b3581-131">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b3581-131">May be **NULL**.</span></span> <span data-ttu-id="b3581-132">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="b3581-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3581-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3581-133">Return value</span></span>

<span data-ttu-id="b3581-134">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3581-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3581-135">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b3581-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3581-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3581-136">Remarks</span></span>

<span data-ttu-id="b3581-137">Список поддерживаемых форматов изображений см. в разделе [**\_ \_ \_ Формат файла изображения D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="b3581-137">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3581-138">Требования</span><span class="sxs-lookup"><span data-stu-id="b3581-138">Requirements</span></span>



| <span data-ttu-id="b3581-139">Требование</span><span class="sxs-lookup"><span data-stu-id="b3581-139">Requirement</span></span> | <span data-ttu-id="b3581-140">Значение</span><span class="sxs-lookup"><span data-stu-id="b3581-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3581-141">Header</span><span class="sxs-lookup"><span data-stu-id="b3581-141">Header</span></span><br/>  | <dl> <span data-ttu-id="b3581-142"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3581-142"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3581-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b3581-143">Library</span></span><br/> | <dl> <span data-ttu-id="b3581-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3581-144"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3581-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3581-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3581-146">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="b3581-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="b3581-147">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="b3581-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
