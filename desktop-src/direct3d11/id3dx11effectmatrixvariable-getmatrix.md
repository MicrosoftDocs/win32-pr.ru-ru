---
title: Метод ID3DX11EffectMatrixVariable-Matrix (D3dx11effect. h)
description: Получение матрицы.
ms.assetid: 1d0b20f2-6e43-414d-a161-65ce13bef1e0
keywords:
- Метод Matrix Direct3D 11
- Метод Matrix Direct3D 11, интерфейс ID3DX11EffectMatrixVariable
- Интерфейс ID3DX11EffectMatrixVariable Direct3D 11, метод Matrix
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14c2f196c4072d7f81a75045fe4703bf51ea338
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081895"
---
# <a name="id3dx11effectmatrixvariablegetmatrix-method"></a><span data-ttu-id="8619e-106">Метод ID3DX11EffectMatrixVariable:: Matrix</span><span class="sxs-lookup"><span data-stu-id="8619e-106">ID3DX11EffectMatrixVariable::GetMatrix method</span></span>

<span data-ttu-id="8619e-107">Получение матрицы.</span><span class="sxs-lookup"><span data-stu-id="8619e-107">Get a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8619e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8619e-108">Syntax</span></span>


```C++
HRESULT GetMatrix(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="8619e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8619e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8619e-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="8619e-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="8619e-111">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="8619e-111">Type: **float\***</span></span>

<span data-ttu-id="8619e-112">Указатель на первый элемент в матрице.</span><span class="sxs-lookup"><span data-stu-id="8619e-112">A pointer to the first element in a matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8619e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8619e-113">Return value</span></span>

<span data-ttu-id="8619e-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8619e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8619e-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8619e-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8619e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8619e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8619e-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="8619e-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8619e-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="8619e-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8619e-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8619e-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8619e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8619e-120">Requirements</span></span>



| <span data-ttu-id="8619e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8619e-121">Requirement</span></span> | <span data-ttu-id="8619e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8619e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8619e-123">Header</span><span class="sxs-lookup"><span data-stu-id="8619e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8619e-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8619e-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8619e-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8619e-125">Library</span></span><br/> | <dl> <span data-ttu-id="8619e-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="8619e-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8619e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8619e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8619e-128">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="8619e-128">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





