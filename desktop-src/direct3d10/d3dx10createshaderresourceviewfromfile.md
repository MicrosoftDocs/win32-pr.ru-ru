---
description: Создание представления "шейдер — представление ресурсов" из файла.
ms.assetid: 97aa848b-e24c-4ebd-8819-b9741ea12b60
title: Функция D3DX10CreateShaderResourceViewFromFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eb787bed64d16f7593fba1f97c96ceeaa217b4e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424429"
---
# <a name="d3dx10createshaderresourceviewfromfile-function"></a><span data-ttu-id="6939d-103">Функция D3DX10CreateShaderResourceViewFromFile</span><span class="sxs-lookup"><span data-stu-id="6939d-103">D3DX10CreateShaderResourceViewFromFile function</span></span>

<span data-ttu-id="6939d-104">Создание представления "шейдер — представление ресурсов" из файла.</span><span class="sxs-lookup"><span data-stu-id="6939d-104">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6939d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6939d-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromFile(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="6939d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6939d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6939d-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6939d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6939d-108">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="6939d-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="6939d-109">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурс.</span><span class="sxs-lookup"><span data-stu-id="6939d-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-110">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6939d-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6939d-111">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6939d-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6939d-112">Имя файла, содержащего представление шейдера-ресурса.</span><span class="sxs-lookup"><span data-stu-id="6939d-112">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="6939d-113">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="6939d-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6939d-114">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6939d-114">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-115">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6939d-115">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6939d-116">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6939d-116">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="6939d-117">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6939d-117">Optional.</span></span> <span data-ttu-id="6939d-118">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="6939d-118">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-119">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6939d-119">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6939d-120">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="6939d-120">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="6939d-121">Указатель на интерфейс генератора потоков (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="6939d-121">Pointer to a thread-pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="6939d-122">Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.</span><span class="sxs-lookup"><span data-stu-id="6939d-122">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="6939d-123">*ппшадерресаурцевиев* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6939d-123">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6939d-124">Тип: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="6939d-124">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="6939d-125">Адрес указателя на представление шейдера-ресурса (см. [**интерфейс ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="6939d-125">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="6939d-126">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6939d-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6939d-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="6939d-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="6939d-128">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="6939d-128">A pointer to the return value.</span></span> <span data-ttu-id="6939d-129">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6939d-129">May be **NULL**.</span></span> <span data-ttu-id="6939d-130">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="6939d-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6939d-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6939d-131">Return value</span></span>

<span data-ttu-id="6939d-132">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6939d-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6939d-133">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6939d-133">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6939d-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6939d-134">Remarks</span></span>

<span data-ttu-id="6939d-135">Список поддерживаемых форматов изображений см. в разделе [**\_ \_ \_ Формат файла изображения D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="6939d-135">For a list of supported image formats, see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6939d-136">Требования</span><span class="sxs-lookup"><span data-stu-id="6939d-136">Requirements</span></span>



| <span data-ttu-id="6939d-137">Требование</span><span class="sxs-lookup"><span data-stu-id="6939d-137">Requirement</span></span> | <span data-ttu-id="6939d-138">Значение</span><span class="sxs-lookup"><span data-stu-id="6939d-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6939d-139">Header</span><span class="sxs-lookup"><span data-stu-id="6939d-139">Header</span></span><br/>  | <dl> <span data-ttu-id="6939d-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6939d-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6939d-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6939d-141">Library</span></span><br/> | <dl> <span data-ttu-id="6939d-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6939d-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6939d-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6939d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6939d-144">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="6939d-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="6939d-145">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="6939d-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
