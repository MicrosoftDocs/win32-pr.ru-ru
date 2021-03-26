---
title: Метод ID3DX11EffectMatrixVariable Жетматрикстранспосеаррай (D3dx11effect. h)
description: Переставить и получить массив матриц с плавающей запятой.
ms.assetid: cfcdbda0-b321-4e94-8d09-bb9d7ddfb4a5
keywords:
- Метод Жетматрикстранспосеаррай Direct3D 11
- Метод Жетматрикстранспосеаррай Direct3D 11, интерфейс ID3DX11EffectMatrixVariable
- Интерфейс ID3DX11EffectMatrixVariable Direct3D 11, метод Жетматрикстранспосеаррай
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d0a43e69ccf88c15d8296c024535dec42b3f31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986936"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtransposearray-method"></a><span data-ttu-id="1ec54-106">Метод ID3DX11EffectMatrixVariable:: Жетматрикстранспосеаррай</span><span class="sxs-lookup"><span data-stu-id="1ec54-106">ID3DX11EffectMatrixVariable::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="1ec54-107">Переставить и получить массив матриц с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="1ec54-107">Transpose and get an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec54-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ec54-108">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="1ec54-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ec54-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec54-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="1ec54-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec54-111">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="1ec54-111">Type: **float\***</span></span>

<span data-ttu-id="1ec54-112">Указатель на первый элемент массива матриц транпосед.</span><span class="sxs-lookup"><span data-stu-id="1ec54-112">A pointer to the first element of an array of tranposed matrices.</span></span>

</dd> <dt>

<span data-ttu-id="1ec54-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="1ec54-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec54-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1ec54-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1ec54-115">Смещение (в количестве матриц) между началом массива и первой матрицей, которую необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="1ec54-115">The offset (in number of matrices) between the start of the array and the first matrix to get.</span></span>

</dd> <dt>

<span data-ttu-id="1ec54-116">*Количество*</span><span class="sxs-lookup"><span data-stu-id="1ec54-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec54-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1ec54-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1ec54-118">Число матриц в массиве, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="1ec54-118">The number of matrices in the array to get.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec54-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ec54-119">Return value</span></span>

<span data-ttu-id="1ec54-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ec54-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ec54-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1ec54-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec54-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="1ec54-122">Remarks</span></span>

<span data-ttu-id="1ec54-123">При перестановке матрицы порядок данных переупорядочивается из порядка строк в столбец в порядке строк (или наоборот).</span><span class="sxs-lookup"><span data-stu-id="1ec54-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="1ec54-124">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="1ec54-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1ec54-125">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="1ec54-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1ec54-126">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1ec54-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1ec54-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1ec54-127">Requirements</span></span>



| <span data-ttu-id="1ec54-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1ec54-128">Requirement</span></span> | <span data-ttu-id="1ec54-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec54-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec54-130">Header</span><span class="sxs-lookup"><span data-stu-id="1ec54-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1ec54-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec54-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1ec54-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ec54-132">Library</span></span><br/> | <dl> <span data-ttu-id="1ec54-133"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec54-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec54-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ec54-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec54-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="1ec54-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

