---
description: Реализованный пользователем метод для открытия и чтения содержимого \# включаемого файла шейдера.
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'Метод ID3DXInclude:: Open (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694300"
---
# <a name="id3dxincludeopen-method"></a><span data-ttu-id="ee35f-103">Метод ID3DXInclude:: Open</span><span class="sxs-lookup"><span data-stu-id="ee35f-103">ID3DXInclude::Open method</span></span>

<span data-ttu-id="ee35f-104">Реализованный пользователем метод для открытия и чтения содержимого \# включаемого файла шейдера.</span><span class="sxs-lookup"><span data-stu-id="ee35f-104">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee35f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee35f-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a><span data-ttu-id="ee35f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee35f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee35f-107">*Инклудетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee35f-107">*IncludeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee35f-108">Тип: **[ **D3DXINCLUDE \_ тип**](./d3dxinclude-type.md)**</span><span class="sxs-lookup"><span data-stu-id="ee35f-108">Type: **[**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md)**</span></span>

<span data-ttu-id="ee35f-109">Расположение \# включаемого файла.</span><span class="sxs-lookup"><span data-stu-id="ee35f-109">The location of the \#include file.</span></span> <span data-ttu-id="ee35f-110">См. раздел [**\_ тип D3DXINCLUDE**](./d3dxinclude-type.md).</span><span class="sxs-lookup"><span data-stu-id="ee35f-110">See [**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee35f-111">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee35f-111">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee35f-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee35f-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee35f-113">Имя \# включаемого файла.</span><span class="sxs-lookup"><span data-stu-id="ee35f-113">Name of the \#include file.</span></span>

</dd> <dt>

<span data-ttu-id="ee35f-114">*ппарентдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee35f-114">*pParentData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee35f-115">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee35f-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee35f-116">Указатель на контейнер, содержащий \# включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="ee35f-116">Pointer to the container that includes the \#include file.</span></span> <span data-ttu-id="ee35f-117">Компилятор может передать значение NULL в *ппарентдата*.</span><span class="sxs-lookup"><span data-stu-id="ee35f-117">The compiler might pass NULL in *pParentData*.</span></span> <span data-ttu-id="ee35f-118">Дополнительные сведения см. в подразделе "Поиск включаемых файлов" статьи [Компиляция влияния (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span><span class="sxs-lookup"><span data-stu-id="ee35f-118">For more information, see the "Searching for Include Files" section in [Compile an Effect (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee35f-119">*ппдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ee35f-119">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee35f-120">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee35f-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ee35f-121">Указатель на возвращаемый буфер, содержащий директивы include.</span><span class="sxs-lookup"><span data-stu-id="ee35f-121">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="ee35f-122">Этот указатель остается действительным до вызова [**ID3DXInclude:: Close**](id3dxinclude--close.md) .</span><span class="sxs-lookup"><span data-stu-id="ee35f-122">This pointer remains valid until [**ID3DXInclude::Close**](id3dxinclude--close.md) is called.</span></span>

</dd> <dt>

<span data-ttu-id="ee35f-123">*пбитес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ee35f-123">*pBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee35f-124">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee35f-124">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ee35f-125">Число байтов, возвращенных в Ппдата.</span><span class="sxs-lookup"><span data-stu-id="ee35f-125">Number of bytes returned in ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee35f-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee35f-126">Return value</span></span>

<span data-ttu-id="ee35f-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee35f-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee35f-128">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ee35f-128">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="ee35f-129">Если при чтении включаемого файла происходит сбой обратного вызова \# , то API-интерфейс, который вызвал вызов функции обратного вызова, завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ee35f-129">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="ee35f-130">Возможны следующие варианты.</span><span class="sxs-lookup"><span data-stu-id="ee35f-130">This is one of the following:</span></span>

-   <span data-ttu-id="ee35f-131">Шейдер HLSL не сможет выполнить одну из \* \* \* функций D3DXCompileShader.</span><span class="sxs-lookup"><span data-stu-id="ee35f-131">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="ee35f-132">Шейдер сборки завершится ошибкой одной из \* \* \* функций D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="ee35f-132">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="ee35f-133">Этот результат приведет к сбою одной из \* \* \* функций D3DXCreateEffect или D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="ee35f-133">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee35f-134">Требования</span><span class="sxs-lookup"><span data-stu-id="ee35f-134">Requirements</span></span>



| <span data-ttu-id="ee35f-135">Требование</span><span class="sxs-lookup"><span data-stu-id="ee35f-135">Requirement</span></span> | <span data-ttu-id="ee35f-136">Значение</span><span class="sxs-lookup"><span data-stu-id="ee35f-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee35f-137">Header</span><span class="sxs-lookup"><span data-stu-id="ee35f-137">Header</span></span><br/>  | <dl> <span data-ttu-id="ee35f-138"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee35f-138"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ee35f-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ee35f-139">Library</span></span><br/> | <dl> <span data-ttu-id="ee35f-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee35f-140"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ee35f-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee35f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee35f-142">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="ee35f-142">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="ee35f-143">**ID3DXInclude:: Close**</span><span class="sxs-lookup"><span data-stu-id="ee35f-143">**ID3DXInclude::Close**</span></span>](id3dxinclude--close.md)
</dt> </dl>

 

 
