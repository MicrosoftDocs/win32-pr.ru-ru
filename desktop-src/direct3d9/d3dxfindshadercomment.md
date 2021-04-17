---
description: Выполняет поиск определенного комментария в шейдере. Комментарий определяется с помощью кода с четырьмя символами (FOURCC) в первом DWORD комментария.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: Функция D3DXFindShaderComment (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703791"
---
# <a name="d3dxfindshadercomment-function"></a><span data-ttu-id="251eb-104">Функция D3DXFindShaderComment</span><span class="sxs-lookup"><span data-stu-id="251eb-104">D3DXFindShaderComment function</span></span>

<span data-ttu-id="251eb-105">Выполняет поиск определенного комментария в шейдере.</span><span class="sxs-lookup"><span data-stu-id="251eb-105">Searches through a shader for a particular comment.</span></span> <span data-ttu-id="251eb-106">Комментарий определяется с помощью кода с четырьмя символами (FOURCC) в первом DWORD комментария.</span><span class="sxs-lookup"><span data-stu-id="251eb-106">The comment is identified by a four-character code (FOURCC) in the first DWORD of the comment.</span></span>

## <a name="syntax"></a><span data-ttu-id="251eb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="251eb-107">Syntax</span></span>


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a><span data-ttu-id="251eb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="251eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="251eb-109">*пфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="251eb-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="251eb-110">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="251eb-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="251eb-111">Указатель на поток функции шейдера DWORD.</span><span class="sxs-lookup"><span data-stu-id="251eb-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="251eb-112">*FourCC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="251eb-112">*FourCC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="251eb-113">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="251eb-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="251eb-114">Код FOURCC, определяющий блок комментариев.</span><span class="sxs-lookup"><span data-stu-id="251eb-114">FOURCC code that identifies the comment block.</span></span> <span data-ttu-id="251eb-115">См. раздел [форматы FourCC](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="251eb-115">See [FourCC Formats](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="251eb-116">*ппдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="251eb-116">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="251eb-117">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="251eb-117">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="251eb-118">Возвращает указатель на данные комментария (не включая маркер комментария и код FOURCC).</span><span class="sxs-lookup"><span data-stu-id="251eb-118">Returns a pointer to the comment data (not including the comment token and FOURCC code).</span></span> <span data-ttu-id="251eb-119">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="251eb-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="251eb-120">*псизеинбитес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="251eb-120">*pSizeInBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="251eb-121">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="251eb-121">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="251eb-122">Возвращает размер данных комментария в байтах.</span><span class="sxs-lookup"><span data-stu-id="251eb-122">Returns the size of the comment data in bytes.</span></span> <span data-ttu-id="251eb-123">Это значение может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="251eb-123">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="251eb-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="251eb-124">Return value</span></span>

<span data-ttu-id="251eb-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="251eb-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="251eb-126">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="251eb-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="251eb-127">Если комментарий не найден и другие ошибки не произошли, \_ возвращается значение false.</span><span class="sxs-lookup"><span data-stu-id="251eb-127">If the comment is not found, and no other error has occurred, S\_FALSE is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="251eb-128">Требования</span><span class="sxs-lookup"><span data-stu-id="251eb-128">Requirements</span></span>



| <span data-ttu-id="251eb-129">Требование</span><span class="sxs-lookup"><span data-stu-id="251eb-129">Requirement</span></span> | <span data-ttu-id="251eb-130">Значение</span><span class="sxs-lookup"><span data-stu-id="251eb-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="251eb-131">Header</span><span class="sxs-lookup"><span data-stu-id="251eb-131">Header</span></span><br/>  | <dl> <span data-ttu-id="251eb-132"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="251eb-132"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="251eb-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="251eb-133">Library</span></span><br/> | <dl> <span data-ttu-id="251eb-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="251eb-134"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="251eb-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="251eb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="251eb-136">Функции шейдера</span><span class="sxs-lookup"><span data-stu-id="251eb-136">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
