---
description: Сохранение текстуры в файл.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: Функция D3DX10SaveTextureToFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694356"
---
# <a name="d3dx10savetexturetofile-function"></a><span data-ttu-id="671a9-103">Функция D3DX10SaveTextureToFile</span><span class="sxs-lookup"><span data-stu-id="671a9-103">D3DX10SaveTextureToFile function</span></span>

<span data-ttu-id="671a9-104">Сохранение текстуры в файл.</span><span class="sxs-lookup"><span data-stu-id="671a9-104">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="671a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="671a9-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="671a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="671a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="671a9-107">*псрктекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="671a9-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671a9-108">Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="671a9-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="671a9-109">Указатель на текстуру, которую необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="671a9-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="671a9-110">См. раздел [**интерфейс ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="671a9-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="671a9-111">*Дестформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="671a9-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671a9-112">Тип: **[ **D3DX10 \_ image \_ File \_ Format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="671a9-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="671a9-113">Формат текстуры будет сохранен как (см. раздел [**\_ \_ \_ Формат файла изображения D3DX10**](d3dx10-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="671a9-113">The format the texture will be saved as (see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)).</span></span> <span data-ttu-id="671a9-114">D3DX10 \_ одиночная \_ DDS — это предпочтительный формат, так как это единственный вариант, поддерживающий все форматы [**в \_ формате DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="671a9-114">D3DX10\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="671a9-115">*пдестфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="671a9-115">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671a9-116">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="671a9-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="671a9-117">Имя целевого выходного файла, в котором будет сохранена текстура.</span><span class="sxs-lookup"><span data-stu-id="671a9-117">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="671a9-118">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="671a9-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="671a9-119">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="671a9-119">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="671a9-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="671a9-120">Return value</span></span>

<span data-ttu-id="671a9-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="671a9-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="671a9-122">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md). Используйте возвращаемое значение, чтобы узнать, поддерживается ли *дестформат* .</span><span class="sxs-lookup"><span data-stu-id="671a9-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="671a9-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="671a9-123">Remarks</span></span>

<span data-ttu-id="671a9-124">**D3DX10SaveTextureToFile** записывает дополнительную [**\_ \_ DXT10 структуру заголовков DDS**](../direct3ddds/dds-header-dxt10.md) для текстуры ввода, только если это необходимо (например, поскольку текстура ввода имеет стандартный RGB-формат (sRGB)).</span><span class="sxs-lookup"><span data-stu-id="671a9-124">**D3DX10SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](../direct3ddds/dds-header-dxt10.md) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="671a9-125">Если **D3DX10SaveTextureToFile** записывает **\_ \_ DXT10 структуру заголовков DDS** , он устанавливает для текстуры **двфауркк** член в структуре [**\_ PIXELFORMAT DDS**](../direct3ddds/dds-pixelformat.md) **, чтобы указать** содержимым DX10 в заголовке **DDS \_ \_ пресценсе** расширенный заголовок.</span><span class="sxs-lookup"><span data-stu-id="671a9-125">If **D3DX10SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](../direct3ddds/dds-pixelformat.md) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="671a9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="671a9-126">Requirements</span></span>



| <span data-ttu-id="671a9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="671a9-127">Requirement</span></span> | <span data-ttu-id="671a9-128">Значение</span><span class="sxs-lookup"><span data-stu-id="671a9-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="671a9-129">Header</span><span class="sxs-lookup"><span data-stu-id="671a9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="671a9-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="671a9-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="671a9-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="671a9-131">Library</span></span><br/> | <dl> <span data-ttu-id="671a9-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="671a9-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="671a9-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="671a9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671a9-134">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="671a9-134">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="671a9-135">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="671a9-135">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
