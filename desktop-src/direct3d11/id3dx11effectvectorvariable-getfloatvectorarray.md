---
title: Метод ID3DX11EffectVectorVariable Жетфлоатвектораррай (D3dx11effect. h)
description: Получите массив векторов из четырех компонентов, содержащих данные с плавающей запятой.
ms.assetid: 30ecbd97-c16d-4ea9-b7d9-364887f42a04
keywords:
- Метод Жетфлоатвектораррай Direct3D 11
- Метод Жетфлоатвектораррай Direct3D 11, интерфейс ID3DX11EffectVectorVariable
- Интерфейс ID3DX11EffectVectorVariable Direct3D 11, метод Жетфлоатвектораррай
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a4c53b884c623ca3d11fb4a9a44660ce21d8a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987074"
---
# <a name="id3dx11effectvectorvariablegetfloatvectorarray-method"></a><span data-ttu-id="64aa5-106">Метод ID3DX11EffectVectorVariable:: Жетфлоатвектораррай</span><span class="sxs-lookup"><span data-stu-id="64aa5-106">ID3DX11EffectVectorVariable::GetFloatVectorArray method</span></span>

<span data-ttu-id="64aa5-107">Получите массив векторов из четырех компонентов, содержащих данные с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="64aa5-107">Get an array of four-component vectors that contain floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="64aa5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64aa5-108">Syntax</span></span>


```C++
HRESULT GetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="64aa5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="64aa5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64aa5-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="64aa5-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="64aa5-111">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="64aa5-111">Type: **float\***</span></span>

<span data-ttu-id="64aa5-112">Указатель на начало данных, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="64aa5-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="64aa5-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="64aa5-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="64aa5-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="64aa5-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="64aa5-115">Необходимо задать значение 0; это зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="64aa5-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="64aa5-116">*Количество*</span><span class="sxs-lookup"><span data-stu-id="64aa5-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="64aa5-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="64aa5-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="64aa5-118">Число заданных элементов массива.</span><span class="sxs-lookup"><span data-stu-id="64aa5-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64aa5-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64aa5-119">Return value</span></span>

<span data-ttu-id="64aa5-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64aa5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64aa5-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="64aa5-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="64aa5-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="64aa5-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="64aa5-123">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="64aa5-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="64aa5-124">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="64aa5-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="64aa5-125">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="64aa5-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64aa5-126">Требования</span><span class="sxs-lookup"><span data-stu-id="64aa5-126">Requirements</span></span>



| <span data-ttu-id="64aa5-127">Требование</span><span class="sxs-lookup"><span data-stu-id="64aa5-127">Requirement</span></span> | <span data-ttu-id="64aa5-128">Значение</span><span class="sxs-lookup"><span data-stu-id="64aa5-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64aa5-129">Header</span><span class="sxs-lookup"><span data-stu-id="64aa5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="64aa5-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="64aa5-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="64aa5-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="64aa5-131">Library</span></span><br/> | <dl> <span data-ttu-id="64aa5-132"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="64aa5-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64aa5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64aa5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64aa5-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="64aa5-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

