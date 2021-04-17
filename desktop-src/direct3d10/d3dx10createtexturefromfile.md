---
description: Создание ресурса текстуры из файла.
ms.assetid: 23edad1f-89bb-4b62-8c48-3be1cd0690d2
title: Функция D3DX10CreateTextureFromFile (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27db799bfd521133a2c137556fdd7408be974854
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694204"
---
# <a name="d3dx10createtexturefromfile-function"></a><span data-ttu-id="43d5c-103">Функция D3DX10CreateTextureFromFile</span><span class="sxs-lookup"><span data-stu-id="43d5c-103">D3DX10CreateTextureFromFile function</span></span>

<span data-ttu-id="43d5c-104">Создание ресурса текстуры из файла.</span><span class="sxs-lookup"><span data-stu-id="43d5c-104">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d5c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43d5c-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromFile(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="43d5c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43d5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43d5c-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43d5c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43d5c-108">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="43d5c-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="43d5c-109">Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), который будет использовать ресурс.</span><span class="sxs-lookup"><span data-stu-id="43d5c-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="43d5c-110">*псркфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43d5c-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43d5c-111">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43d5c-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43d5c-112">Имя файла, содержащего ресурс.</span><span class="sxs-lookup"><span data-stu-id="43d5c-112">The name of the file containing the resource.</span></span> <span data-ttu-id="43d5c-113">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="43d5c-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="43d5c-114">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="43d5c-114">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="43d5c-115">Список поддерживаемых форматов файлов изображений см. в разделе Перечисление [**\_ \_ \_ формата файлов изображений D3DX10**](d3dx10-image-file-format.md) .</span><span class="sxs-lookup"><span data-stu-id="43d5c-115">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md) enumeration for a list of the supported image file formats.</span></span>

</dd> <dt>

<span data-ttu-id="43d5c-116">*плоадинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43d5c-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43d5c-117">Тип: **[ **\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="43d5c-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="43d5c-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="43d5c-118">Optional.</span></span> <span data-ttu-id="43d5c-119">Определяет характеристики текстуры (см. раздел [**\_ \_ \_ сведения о загрузке образа D3DX10**](d3dx10-image-load-info.md)) при создании обработчика данных; установите значение **null** , чтобы считать характеристики текстуры при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="43d5c-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="43d5c-120">*ппумп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43d5c-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43d5c-121">Тип: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="43d5c-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="43d5c-122">Указатель на интерфейсный конвейер потока (см. [**интерфейс ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="43d5c-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="43d5c-123">Если указано **значение NULL** , функция будет вести себя синхронно и не вернется до завершения.</span><span class="sxs-lookup"><span data-stu-id="43d5c-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="43d5c-124">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="43d5c-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43d5c-125">Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="43d5c-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="43d5c-126">Адрес указателя на ресурс текстуры (см. [**интерфейс ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span><span class="sxs-lookup"><span data-stu-id="43d5c-126">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="43d5c-127">*фресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="43d5c-127">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43d5c-128">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="43d5c-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="43d5c-129">Указатель на возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="43d5c-129">A pointer to the return value.</span></span> <span data-ttu-id="43d5c-130">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="43d5c-130">May be **NULL**.</span></span> <span data-ttu-id="43d5c-131">Если *ппумп* не **равно NULL**, то *фресулт* должен быть допустимым расположением в памяти до завершения асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="43d5c-131">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43d5c-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43d5c-132">Return value</span></span>

<span data-ttu-id="43d5c-133">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43d5c-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43d5c-134">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="43d5c-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="43d5c-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43d5c-135">Remarks</span></span>

<span data-ttu-id="43d5c-136">Список поддерживаемых форматов изображений см. в разделе [**\_ \_ \_ Формат файла изображения D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="43d5c-136">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43d5c-137">Требования</span><span class="sxs-lookup"><span data-stu-id="43d5c-137">Requirements</span></span>



| <span data-ttu-id="43d5c-138">Требование</span><span class="sxs-lookup"><span data-stu-id="43d5c-138">Requirement</span></span> | <span data-ttu-id="43d5c-139">Значение</span><span class="sxs-lookup"><span data-stu-id="43d5c-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43d5c-140">Header</span><span class="sxs-lookup"><span data-stu-id="43d5c-140">Header</span></span><br/>  | <dl> <span data-ttu-id="43d5c-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="43d5c-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="43d5c-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43d5c-142">Library</span></span><br/> | <dl> <span data-ttu-id="43d5c-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43d5c-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43d5c-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43d5c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d5c-145">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="43d5c-145">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="43d5c-146">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="43d5c-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
