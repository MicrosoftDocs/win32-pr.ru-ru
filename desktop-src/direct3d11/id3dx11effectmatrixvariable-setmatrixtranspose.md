---
title: Метод ID3DX11EffectMatrixVariable Сетматрикстранспосе (D3dx11effect. h)
description: Переставить и установить матрицу с плавающей точкой.
ms.assetid: 228546c9-0141-4e17-bc8f-bff7201825d7
keywords:
- Метод Сетматрикстранспосе Direct3D 11
- Метод Сетматрикстранспосе Direct3D 11, интерфейс ID3DX11EffectMatrixVariable
- Интерфейс ID3DX11EffectMatrixVariable Direct3D 11, метод Сетматрикстранспосе
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daf77b6e2e9578dcbc6c9cfe80f57b149097c32
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986933"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtranspose-method"></a><span data-ttu-id="ae82c-106">Метод ID3DX11EffectMatrixVariable:: Сетматрикстранспосе</span><span class="sxs-lookup"><span data-stu-id="ae82c-106">ID3DX11EffectMatrixVariable::SetMatrixTranspose method</span></span>

<span data-ttu-id="ae82c-107">Переставить и установить матрицу с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="ae82c-107">Transpose and set a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae82c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae82c-108">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="ae82c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae82c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae82c-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="ae82c-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="ae82c-111">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="ae82c-111">Type: **float\***</span></span>

<span data-ttu-id="ae82c-112">Указатель на первый элемент матрицы.</span><span class="sxs-lookup"><span data-stu-id="ae82c-112">A pointer to the first element of a matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae82c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae82c-113">Return value</span></span>

<span data-ttu-id="ae82c-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae82c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae82c-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ae82c-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ae82c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae82c-116">Remarks</span></span>

<span data-ttu-id="ae82c-117">При перестановке матрицы порядок данных переупорядочивается из порядка строк в столбец в порядке строк (или наоборот).</span><span class="sxs-lookup"><span data-stu-id="ae82c-117">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="ae82c-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="ae82c-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ae82c-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="ae82c-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ae82c-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ae82c-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ae82c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ae82c-121">Requirements</span></span>



| <span data-ttu-id="ae82c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ae82c-122">Requirement</span></span> | <span data-ttu-id="ae82c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ae82c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae82c-124">Header</span><span class="sxs-lookup"><span data-stu-id="ae82c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ae82c-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae82c-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ae82c-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae82c-126">Library</span></span><br/> | <dl> <span data-ttu-id="ae82c-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="ae82c-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae82c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae82c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae82c-129">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="ae82c-129">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





