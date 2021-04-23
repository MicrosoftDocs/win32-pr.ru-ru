---
description: Создание представления "шейдер — представление ресурсов" из ресурса.
ms.assetid: 207cda5f-5b7e-420a-988f-135cd2a04eb0
title: Функция D3DX10CreateShaderResourceViewFromResource (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 12de92153b6f812b4f014f53e918e7a97000eda6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703847"
---
# <a name="d3dx10createshaderresourceviewfromresource-function"></a><span data-ttu-id="55b50-103">Функция D3DX10CreateShaderResourceViewFromResource</span><span class="sxs-lookup"><span data-stu-id="55b50-103">D3DX10CreateShaderResourceViewFromResource function</span></span>

<span data-ttu-id="55b50-104">Создание представления "шейдер — представление ресурсов" из ресурса.</span><span class="sxs-lookup"><span data-stu-id="55b50-104">Create a shader-resource view from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55b50-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromResource(
  _In_  ID3D10Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="55b50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55b50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b50-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55b50-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b50-108">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="55b50-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="55b50-109">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурс.</span><span class="sxs-lookup"><span data-stu-id="55b50-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="55b50-110">*хсркмодуле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55b50-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b50-111">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55b50-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55b50-112">Обработчик для модуля ресурсов, содержащего представление «шейдер-ресурс».</span><span class="sxs-lookup"><span data-stu-id="55b50-112">Handle to the resource module containing the shader-resource view.</span></span> <span data-ttu-id="55b50-113">ХМОДУЛЕ можно получить с помощью [функции ошибка GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="55b50-113">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="55b50-114">*псркресаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55b50-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b50-115">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55b50-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55b50-116">Имя представления ресурсов шейдера в Хсркмодуле.</span><span class="sxs-lookup"><span data-stu-id="55b50-116">Name of the shader resource view in hSrcModule.</span></span> <span data-ttu-id="55b50-117">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="55b50-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="55b50-118">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="55b50-118">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="55b50-119">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55b50-119">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b50-120">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="55b50-120">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="55b50-121">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="55b50-121">Optional.</span></span> <span data-ttu-id="55b50-122">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="55b50-122">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="55b50-123">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55b50-123">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b50-124">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="55b50-124">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="55b50-125">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="55b50-125">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="55b50-126">Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.</span><span class="sxs-lookup"><span data-stu-id="55b50-126">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="55b50-127">*ппшадерресаурцевиев* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="55b50-127">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55b50-128">Тип: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="55b50-128">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="55b50-129">Адрес указателя на представление шейдера-ресурса (см. [**интерфейс ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="55b50-129">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="55b50-130">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="55b50-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55b50-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="55b50-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="55b50-132">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="55b50-132">A pointer to the return value.</span></span> <span data-ttu-id="55b50-133">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="55b50-133">May be **NULL**.</span></span> <span data-ttu-id="55b50-134">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="55b50-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b50-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55b50-135">Return value</span></span>

<span data-ttu-id="55b50-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55b50-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55b50-137">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="55b50-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55b50-138">Требования</span><span class="sxs-lookup"><span data-stu-id="55b50-138">Requirements</span></span>



| <span data-ttu-id="55b50-139">Требование</span><span class="sxs-lookup"><span data-stu-id="55b50-139">Requirement</span></span> | <span data-ttu-id="55b50-140">Значение</span><span class="sxs-lookup"><span data-stu-id="55b50-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55b50-141">Header</span><span class="sxs-lookup"><span data-stu-id="55b50-141">Header</span></span><br/>  | <dl> <span data-ttu-id="55b50-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="55b50-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="55b50-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55b50-143">Library</span></span><br/> | <dl> <span data-ttu-id="55b50-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55b50-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="55b50-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55b50-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b50-146">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="55b50-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="55b50-147">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="55b50-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
