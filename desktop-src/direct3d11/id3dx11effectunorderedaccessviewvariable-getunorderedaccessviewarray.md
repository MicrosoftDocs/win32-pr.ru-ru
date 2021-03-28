---
title: Метод ID3DX11EffectUnorderedAccessViewVariable Жетунордередакцессвиеваррай (D3dx11effect. h)
description: Получение массива неупорядоченных представлений доступа.
ms.assetid: 38f838bb-cdcb-43c2-8b98-a188f479e93d
keywords:
- Метод Жетунордередакцессвиеваррай Direct3D 11
- Метод Жетунордередакцессвиеваррай Direct3D 11, интерфейс ID3DX11EffectUnorderedAccessViewVariable
- Интерфейс ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, метод Жетунордередакцессвиеваррай
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c264b5652287676d0792027f4f0ea8921bdb92f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273853"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessviewarray-method"></a><span data-ttu-id="adfef-106">Метод ID3DX11EffectUnorderedAccessViewVariable:: Жетунордередакцессвиеваррай</span><span class="sxs-lookup"><span data-stu-id="adfef-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="adfef-107">Получение массива неупорядоченных представлений доступа.</span><span class="sxs-lookup"><span data-stu-id="adfef-107">Get an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="adfef-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adfef-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="adfef-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="adfef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adfef-110">*ппресаурцес*</span><span class="sxs-lookup"><span data-stu-id="adfef-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="adfef-111">Тип: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="adfef-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="adfef-112">Указатель на указатель [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) , который будет установлен в массив UAV при возврате.</span><span class="sxs-lookup"><span data-stu-id="adfef-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set to the UAV array on return.</span></span>

</dd> <dt>

<span data-ttu-id="adfef-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="adfef-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="adfef-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="adfef-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="adfef-115">Индекс первого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="adfef-115">Index of the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="adfef-116">*Количество*</span><span class="sxs-lookup"><span data-stu-id="adfef-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="adfef-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="adfef-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="adfef-118">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="adfef-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adfef-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adfef-119">Return value</span></span>

<span data-ttu-id="adfef-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="adfef-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="adfef-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="adfef-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="adfef-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="adfef-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="adfef-123">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="adfef-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="adfef-124">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="adfef-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="adfef-125">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="adfef-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="adfef-126">Требования</span><span class="sxs-lookup"><span data-stu-id="adfef-126">Requirements</span></span>



| <span data-ttu-id="adfef-127">Требование</span><span class="sxs-lookup"><span data-stu-id="adfef-127">Requirement</span></span> | <span data-ttu-id="adfef-128">Значение</span><span class="sxs-lookup"><span data-stu-id="adfef-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adfef-129">Header</span><span class="sxs-lookup"><span data-stu-id="adfef-129">Header</span></span><br/>  | <dl> <span data-ttu-id="adfef-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="adfef-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="adfef-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="adfef-131">Library</span></span><br/> | <dl> <span data-ttu-id="adfef-132"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="adfef-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adfef-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adfef-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adfef-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="adfef-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

