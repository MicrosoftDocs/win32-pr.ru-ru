---
title: Метод ID3DX11EffectMatrixVariable Жетматриксаррай (D3dx11effect. h)
description: Получение массива матриц.
ms.assetid: a7598687-a11c-41ad-9fb6-2c16d12f5edc
keywords:
- Метод Жетматриксаррай Direct3D 11
- Метод Жетматриксаррай Direct3D 11, интерфейс ID3DX11EffectMatrixVariable
- Интерфейс ID3DX11EffectMatrixVariable Direct3D 11, метод Жетматриксаррай
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a339bf6918868473966b6d79bcbe6b6aa3eaa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000426"
---
# <a name="id3dx11effectmatrixvariablegetmatrixarray-method"></a><span data-ttu-id="c9a58-106">Метод ID3DX11EffectMatrixVariable:: Жетматриксаррай</span><span class="sxs-lookup"><span data-stu-id="c9a58-106">ID3DX11EffectMatrixVariable::GetMatrixArray method</span></span>

<span data-ttu-id="c9a58-107">Получение массива матриц.</span><span class="sxs-lookup"><span data-stu-id="c9a58-107">Get an array of matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a58-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9a58-108">Syntax</span></span>


```C++
HRESULT GetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="c9a58-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9a58-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a58-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="c9a58-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="c9a58-111">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="c9a58-111">Type: **float\***</span></span>

<span data-ttu-id="c9a58-112">Указатель на первый элемент первой матрицы в массиве матриц.</span><span class="sxs-lookup"><span data-stu-id="c9a58-112">A pointer to the first element of the first matrix in an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="c9a58-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="c9a58-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="c9a58-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c9a58-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c9a58-115">Смещение (в количестве матриц) между началом массива и первой возвращенной матрицей.</span><span class="sxs-lookup"><span data-stu-id="c9a58-115">The offset (in number of matrices) between the start of the array and the first matrix returned.</span></span>

</dd> <dt>

<span data-ttu-id="c9a58-116">*Количество*</span><span class="sxs-lookup"><span data-stu-id="c9a58-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="c9a58-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c9a58-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c9a58-118">Число матриц в возвращаемом массиве.</span><span class="sxs-lookup"><span data-stu-id="c9a58-118">The number of matrices in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a58-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9a58-119">Return value</span></span>

<span data-ttu-id="c9a58-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c9a58-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c9a58-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c9a58-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9a58-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9a58-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c9a58-123">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="c9a58-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c9a58-124">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="c9a58-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c9a58-125">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c9a58-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9a58-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c9a58-126">Requirements</span></span>



| <span data-ttu-id="c9a58-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c9a58-127">Requirement</span></span> | <span data-ttu-id="c9a58-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c9a58-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a58-129">Header</span><span class="sxs-lookup"><span data-stu-id="c9a58-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c9a58-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9a58-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c9a58-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9a58-131">Library</span></span><br/> | <dl> <span data-ttu-id="c9a58-132"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="c9a58-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a58-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9a58-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a58-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="c9a58-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

