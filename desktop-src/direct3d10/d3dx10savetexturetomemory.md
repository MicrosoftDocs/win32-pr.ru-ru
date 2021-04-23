---
description: Сохранение текстуры в памяти.
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: Функция D3DX10SaveTextureToMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f20278f9fc590e72f93051d5fdd4cfbd918098df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694176"
---
# <a name="d3dx10savetexturetomemory-function"></a><span data-ttu-id="fc744-103">Функция D3DX10SaveTextureToMemory</span><span class="sxs-lookup"><span data-stu-id="fc744-103">D3DX10SaveTextureToMemory function</span></span>

<span data-ttu-id="fc744-104">Сохранение текстуры в памяти.</span><span class="sxs-lookup"><span data-stu-id="fc744-104">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc744-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc744-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="fc744-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc744-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc744-107">*псрктекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc744-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc744-108">Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="fc744-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="fc744-109">Указатель на текстуру, которую необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="fc744-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="fc744-110">См. раздел [**интерфейс ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="fc744-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="fc744-111">*Дестформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc744-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc744-112">Тип: **[ **D3DX10 \_ image \_ File \_ Format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="fc744-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="fc744-113">Формат текстуры будет сохранен как.</span><span class="sxs-lookup"><span data-stu-id="fc744-113">The format the texture will be saved as.</span></span> <span data-ttu-id="fc744-114">См. раздел [**\_ \_ \_ Формат файла изображения D3DX10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="fc744-114">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc744-115">*ппдестбуф* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fc744-115">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc744-116">Тип: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="fc744-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="fc744-117">Адрес указателя на память, содержащую сохраненную текстуру.</span><span class="sxs-lookup"><span data-stu-id="fc744-117">Address of a pointer to the memory containing the saved texture.</span></span> <span data-ttu-id="fc744-118">См. раздел [**интерфейс ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).</span><span class="sxs-lookup"><span data-stu-id="fc744-118">See [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="fc744-119">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc744-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc744-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc744-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc744-121">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fc744-121">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc744-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc744-122">Return value</span></span>

<span data-ttu-id="fc744-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc744-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc744-124">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fc744-124">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc744-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fc744-125">Requirements</span></span>



| <span data-ttu-id="fc744-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fc744-126">Requirement</span></span> | <span data-ttu-id="fc744-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fc744-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc744-128">Header</span><span class="sxs-lookup"><span data-stu-id="fc744-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fc744-129"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc744-129"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fc744-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fc744-130">Library</span></span><br/> | <dl> <span data-ttu-id="fc744-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc744-131"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fc744-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc744-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc744-133">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="fc744-133">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="fc744-134">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="fc744-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
