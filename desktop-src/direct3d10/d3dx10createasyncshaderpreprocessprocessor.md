---
description: Асинхронно Создайте обработчик данных для шейдера.
ms.assetid: f5521e55-5f20-422d-979e-98b70efd3b13
title: Функция D3DX10CreateAsyncShaderPreprocessProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderPreprocessProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 14afdb899d99b7c0278d3042fbc9a108f446c692
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703929"
---
# <a name="d3dx10createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="3ce27-103">Функция D3DX10CreateAsyncShaderPreprocessProcessor</span><span class="sxs-lookup"><span data-stu-id="3ce27-103">D3DX10CreateAsyncShaderPreprocessProcessor function</span></span>

<span data-ttu-id="3ce27-104">Асинхронно Создайте обработчик данных для шейдера.</span><span class="sxs-lookup"><span data-stu-id="3ce27-104">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce27-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ce27-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="3ce27-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ce27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce27-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce27-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce27-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ce27-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ce27-109">Строка, содержащая имя файла шейдера.</span><span class="sxs-lookup"><span data-stu-id="3ce27-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="3ce27-110">*пдефинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce27-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce27-111">Тип: **неконстантный \* [**\_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**</span><span class="sxs-lookup"><span data-stu-id="3ce27-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="3ce27-112">Массив макросов шейдера, заканчивающийся НУЛЕМ (см. [**раздел \_ \_ макрос шейдера D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); установите значение **null** , чтобы не указывать макросы.</span><span class="sxs-lookup"><span data-stu-id="3ce27-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="3ce27-113">*пинклуде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ce27-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce27-114">Тип: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3ce27-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="3ce27-115">Указатель на интерфейс include (см. [**интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Установите значение **null** , чтобы указать, что файл не включен.</span><span class="sxs-lookup"><span data-stu-id="3ce27-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="3ce27-116">*ппшадертекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3ce27-116">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce27-117">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3ce27-117">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3ce27-118">Адрес указателя на буфер, который содержит текст ASCII шейдера (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="3ce27-118">Address of a pointer to a buffer that contains the ASCII text of the shader (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="3ce27-119">*пперрорбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3ce27-119">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce27-120">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="3ce27-120">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="3ce27-121">Адрес указателя на буфер, содержащий ошибки компиляции (см. [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="3ce27-121">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="3ce27-122">*ппдатапроцессор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3ce27-122">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce27-123">Тип: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3ce27-123">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="3ce27-124">Адрес указателя на буфер, содержащий созданный обработчик данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="3ce27-124">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce27-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ce27-125">Return value</span></span>

<span data-ttu-id="3ce27-126">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3ce27-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3ce27-127">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3ce27-127">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce27-128">Требования</span><span class="sxs-lookup"><span data-stu-id="3ce27-128">Requirements</span></span>



| <span data-ttu-id="3ce27-129">Требование</span><span class="sxs-lookup"><span data-stu-id="3ce27-129">Requirement</span></span> | <span data-ttu-id="3ce27-130">Значение</span><span class="sxs-lookup"><span data-stu-id="3ce27-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce27-131">Header</span><span class="sxs-lookup"><span data-stu-id="3ce27-131">Header</span></span><br/> | <dl> <span data-ttu-id="3ce27-132"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ce27-132"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ce27-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ce27-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce27-134">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="3ce27-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
