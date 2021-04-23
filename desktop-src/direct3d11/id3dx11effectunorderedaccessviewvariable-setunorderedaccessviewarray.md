---
title: Метод ID3DX11EffectUnorderedAccessViewVariable Сетунордередакцессвиеваррай (D3dx11effect. h)
description: Установите массив неупорядоченных представлений доступа.
ms.assetid: 12d0da06-990a-42b2-9566-cc5136f48781
keywords:
- Метод Сетунордередакцессвиеваррай Direct3D 11
- Метод Сетунордередакцессвиеваррай Direct3D 11, интерфейс ID3DX11EffectUnorderedAccessViewVariable
- Интерфейс ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, метод Сетунордередакцессвиеваррай
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053856f294906cf56acf1f38ca90663ebcc34051
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998342"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessviewarray-method"></a><span data-ttu-id="ff2e8-106">Метод ID3DX11EffectUnorderedAccessViewVariable:: Сетунордередакцессвиеваррай</span><span class="sxs-lookup"><span data-stu-id="ff2e8-106">ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="ff2e8-107">Установите массив неупорядоченных представлений доступа.</span><span class="sxs-lookup"><span data-stu-id="ff2e8-107">Set an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff2e8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff2e8-108">Syntax</span></span>


```C++
HRESULT SetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="ff2e8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff2e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff2e8-110">*ппресаурцес*</span><span class="sxs-lookup"><span data-stu-id="ff2e8-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="ff2e8-111">Тип: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="ff2e8-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="ff2e8-112">Массив указателей [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) .</span><span class="sxs-lookup"><span data-stu-id="ff2e8-112">An array of [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="ff2e8-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="ff2e8-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="ff2e8-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ff2e8-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ff2e8-115">Индекс первого неупорядоченного представления доступа.</span><span class="sxs-lookup"><span data-stu-id="ff2e8-115">Index of the first unordered-access-view.</span></span>

</dd> <dt>

<span data-ttu-id="ff2e8-116">*Количество*</span><span class="sxs-lookup"><span data-stu-id="ff2e8-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="ff2e8-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ff2e8-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ff2e8-118">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="ff2e8-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff2e8-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff2e8-119">Return value</span></span>

<span data-ttu-id="ff2e8-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ff2e8-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ff2e8-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ff2e8-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ff2e8-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff2e8-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ff2e8-123">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="ff2e8-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ff2e8-124">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="ff2e8-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ff2e8-125">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ff2e8-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ff2e8-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ff2e8-126">Requirements</span></span>



| <span data-ttu-id="ff2e8-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ff2e8-127">Requirement</span></span> | <span data-ttu-id="ff2e8-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ff2e8-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff2e8-129">Header</span><span class="sxs-lookup"><span data-stu-id="ff2e8-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ff2e8-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff2e8-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ff2e8-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ff2e8-131">Library</span></span><br/> | <dl> <span data-ttu-id="ff2e8-132"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="ff2e8-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff2e8-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff2e8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff2e8-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="ff2e8-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

