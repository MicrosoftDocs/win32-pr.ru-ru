---
title: Метод ID3DX11EffectMatrixVariable Сетматрикстранспосеаррай (D3dx11effect. h)
description: Переставить и задайте массив матриц с плавающей запятой.
ms.assetid: 08223022-5e77-4a84-9b68-b9b0c9a02270
keywords:
- Метод Сетматрикстранспосеаррай Direct3D 11
- Метод Сетматрикстранспосеаррай Direct3D 11, интерфейс ID3DX11EffectMatrixVariable
- Интерфейс ID3DX11EffectMatrixVariable Direct3D 11, метод Сетматрикстранспосеаррай
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f70676b76658b5732c1a2ee15858f83694272b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000474"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtransposearray-method"></a><span data-ttu-id="a9600-106">Метод ID3DX11EffectMatrixVariable:: Сетматрикстранспосеаррай</span><span class="sxs-lookup"><span data-stu-id="a9600-106">ID3DX11EffectMatrixVariable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="a9600-107">Переставить и задайте массив матриц с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="a9600-107">Transpose and set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9600-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9600-108">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="a9600-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9600-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9600-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="a9600-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="a9600-111">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="a9600-111">Type: **float\***</span></span>

<span data-ttu-id="a9600-112">Указатель на массив матриц.</span><span class="sxs-lookup"><span data-stu-id="a9600-112">A pointer to an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="a9600-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="a9600-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="a9600-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a9600-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a9600-115">Смещение (в количестве матриц) между началом массива и первой заданной матрицей.</span><span class="sxs-lookup"><span data-stu-id="a9600-115">The offset (in number of matrices) between the start of the array and the first matrix to set.</span></span>

</dd> <dt>

<span data-ttu-id="a9600-116">*Количество*</span><span class="sxs-lookup"><span data-stu-id="a9600-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="a9600-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a9600-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a9600-118">Число матриц в заданном массиве.</span><span class="sxs-lookup"><span data-stu-id="a9600-118">The number of matrices in the array to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9600-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9600-119">Return value</span></span>

<span data-ttu-id="a9600-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a9600-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a9600-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a9600-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a9600-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="a9600-122">Remarks</span></span>

<span data-ttu-id="a9600-123">При перестановке матрицы порядок данных переупорядочивается из порядка строк в столбец в порядке строк (или наоборот).</span><span class="sxs-lookup"><span data-stu-id="a9600-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="a9600-124">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="a9600-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a9600-125">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="a9600-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a9600-126">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a9600-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a9600-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a9600-127">Requirements</span></span>



| <span data-ttu-id="a9600-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a9600-128">Requirement</span></span> | <span data-ttu-id="a9600-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a9600-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9600-130">Header</span><span class="sxs-lookup"><span data-stu-id="a9600-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a9600-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9600-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a9600-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a9600-132">Library</span></span><br/> | <dl> <span data-ttu-id="a9600-133"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="a9600-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9600-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9600-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9600-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="a9600-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

