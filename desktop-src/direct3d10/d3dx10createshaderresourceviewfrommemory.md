---
description: Создание представления "шейдер — представление ресурсов" из файла в памяти.
ms.assetid: 8316987f-75b4-4cee-a1f2-10bee77a28e6
title: Функция D3DX10CreateShaderResourceViewFromMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ca3cf26d54d37ab3e3a2141ba7c3e4ea9fdd533f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820988"
---
# <a name="d3dx10createshaderresourceviewfrommemory-function"></a><span data-ttu-id="f8ba4-103">Функция D3DX10CreateShaderResourceViewFromMemory</span><span class="sxs-lookup"><span data-stu-id="f8ba4-103">D3DX10CreateShaderResourceViewFromMemory function</span></span>

<span data-ttu-id="f8ba4-104">Создание представления "шейдер — представление ресурсов" из файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="f8ba4-104">Create a shader-resource view from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ba4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8ba4-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromMemory(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="f8ba4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8ba4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ba4-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8ba4-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ba4-108">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="f8ba4-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="f8ba4-109">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурс.</span><span class="sxs-lookup"><span data-stu-id="f8ba4-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f8ba4-110">*псркдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8ba4-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ba4-111">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8ba4-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8ba4-112">Указатель на файл в памяти, который содержит представление "шейдер-ресурс".</span><span class="sxs-lookup"><span data-stu-id="f8ba4-112">Pointer to the file in memory that contains the shader-resource view.</span></span>

</dd> <dt>

<span data-ttu-id="f8ba4-113">*Сркдатасизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8ba4-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ba4-114">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8ba4-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8ba4-115">Размер файла в памяти.</span><span class="sxs-lookup"><span data-stu-id="f8ba4-115">Size of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="f8ba4-116">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8ba4-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ba4-117">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8ba4-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="f8ba4-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="f8ba4-118">Optional.</span></span> <span data-ttu-id="f8ba4-119">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="f8ba4-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="f8ba4-120">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8ba4-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ba4-121">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8ba4-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="f8ba4-122">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="f8ba4-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="f8ba4-123">Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.</span><span class="sxs-lookup"><span data-stu-id="f8ba4-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="f8ba4-124">*ппшадерресаурцевиев* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f8ba4-124">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ba4-125">Тип: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="f8ba4-125">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="f8ba4-126">Адрес указателя на только что созданное представление ресурсов шейдера.</span><span class="sxs-lookup"><span data-stu-id="f8ba4-126">Address of a pointer to the newly created shader resource view.</span></span> <span data-ttu-id="f8ba4-127">См. раздел [**интерфейс ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="f8ba4-127">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="f8ba4-128">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f8ba4-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ba4-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="f8ba4-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="f8ba4-130">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="f8ba4-130">A pointer to the return value.</span></span> <span data-ttu-id="f8ba4-131">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f8ba4-131">May be **NULL**.</span></span> <span data-ttu-id="f8ba4-132">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="f8ba4-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ba4-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8ba4-133">Return value</span></span>

<span data-ttu-id="f8ba4-134">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8ba4-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8ba4-135">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f8ba4-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ba4-136">Требования</span><span class="sxs-lookup"><span data-stu-id="f8ba4-136">Requirements</span></span>



| <span data-ttu-id="f8ba4-137">Требование</span><span class="sxs-lookup"><span data-stu-id="f8ba4-137">Requirement</span></span> | <span data-ttu-id="f8ba4-138">Значение</span><span class="sxs-lookup"><span data-stu-id="f8ba4-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ba4-139">Header</span><span class="sxs-lookup"><span data-stu-id="f8ba4-139">Header</span></span><br/>  | <dl> <span data-ttu-id="f8ba4-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ba4-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f8ba4-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8ba4-141">Library</span></span><br/> | <dl> <span data-ttu-id="f8ba4-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8ba4-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f8ba4-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8ba4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ba4-144">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="f8ba4-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="f8ba4-145">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="f8ba4-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
