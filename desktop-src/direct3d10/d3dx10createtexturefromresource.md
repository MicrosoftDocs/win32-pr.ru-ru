---
description: Создание текстуры из другого ресурса.
ms.assetid: 9758968a-652f-42bb-8c81-ad7816c57b17
title: Функция D3DX10CreateTextureFromResource (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 22be3b54c7aa9090fd95624a51bc248b01003dcc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694274"
---
# <a name="d3dx10createtexturefromresource-function"></a><span data-ttu-id="03ed9-103">Функция D3DX10CreateTextureFromResource</span><span class="sxs-lookup"><span data-stu-id="03ed9-103">D3DX10CreateTextureFromResource function</span></span>

<span data-ttu-id="03ed9-104">Создание текстуры из другого ресурса.</span><span class="sxs-lookup"><span data-stu-id="03ed9-104">Create a texture from another resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ed9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03ed9-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromResource(
  _In_  ID3D10Device           *pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="03ed9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03ed9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ed9-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03ed9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ed9-108">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="03ed9-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="03ed9-109">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурс.</span><span class="sxs-lookup"><span data-stu-id="03ed9-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="03ed9-110">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03ed9-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ed9-111">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03ed9-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="03ed9-112">Маркер исходного ресурса.</span><span class="sxs-lookup"><span data-stu-id="03ed9-112">A handle to the source resource.</span></span> <span data-ttu-id="03ed9-113">ХМОДУЛЕ можно получить с помощью [функции ошибка GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="03ed9-113">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="03ed9-114">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03ed9-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ed9-115">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03ed9-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="03ed9-116">Строка, содержащая имя исходного ресурса.</span><span class="sxs-lookup"><span data-stu-id="03ed9-116">A string that contains the name of the source resource.</span></span> <span data-ttu-id="03ed9-117">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="03ed9-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="03ed9-118">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="03ed9-118">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="03ed9-119">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03ed9-119">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ed9-120">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="03ed9-120">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="03ed9-121">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="03ed9-121">Optional.</span></span> <span data-ttu-id="03ed9-122">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="03ed9-122">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="03ed9-123">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03ed9-123">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ed9-124">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="03ed9-124">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="03ed9-125">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="03ed9-125">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="03ed9-126">Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.</span><span class="sxs-lookup"><span data-stu-id="03ed9-126">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="03ed9-127">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="03ed9-127">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03ed9-128">Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="03ed9-128">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="03ed9-129">Адрес указателя на ресурс текстуры (см. [**интерфейс ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span><span class="sxs-lookup"><span data-stu-id="03ed9-129">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="03ed9-130">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="03ed9-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03ed9-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="03ed9-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="03ed9-132">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="03ed9-132">A pointer to the return value.</span></span> <span data-ttu-id="03ed9-133">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="03ed9-133">May be **NULL**.</span></span> <span data-ttu-id="03ed9-134">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="03ed9-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ed9-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03ed9-135">Return value</span></span>

<span data-ttu-id="03ed9-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="03ed9-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="03ed9-137">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="03ed9-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="03ed9-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03ed9-138">Remarks</span></span>

<span data-ttu-id="03ed9-139">Список поддерживаемых форматов изображений см. в разделе [**\_ \_ \_ Формат файла изображения D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="03ed9-139">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03ed9-140">Требования</span><span class="sxs-lookup"><span data-stu-id="03ed9-140">Requirements</span></span>



| <span data-ttu-id="03ed9-141">Требование</span><span class="sxs-lookup"><span data-stu-id="03ed9-141">Requirement</span></span> | <span data-ttu-id="03ed9-142">Значение</span><span class="sxs-lookup"><span data-stu-id="03ed9-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03ed9-143">Header</span><span class="sxs-lookup"><span data-stu-id="03ed9-143">Header</span></span><br/>  | <dl> <span data-ttu-id="03ed9-144"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="03ed9-144"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="03ed9-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03ed9-145">Library</span></span><br/> | <dl> <span data-ttu-id="03ed9-146"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03ed9-146"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03ed9-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03ed9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ed9-148">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="03ed9-148">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="03ed9-149">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="03ed9-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
