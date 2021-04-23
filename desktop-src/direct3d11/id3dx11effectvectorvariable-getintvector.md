---
title: Метод ID3DX11EffectVectorVariable Жетинтвектор (D3dx11effect. h)
description: Получение вектора из четырех компонентов, содержащего целочисленные данные.
ms.assetid: 27c75cfb-7c6f-43f4-9489-186006a60203
keywords:
- Метод Жетинтвектор Direct3D 11
- Метод Жетинтвектор Direct3D 11, интерфейс ID3DX11EffectVectorVariable
- Интерфейс ID3DX11EffectVectorVariable Direct3D 11, метод Жетинтвектор
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetIntVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e661ecce642cae4cf94a1bc35f92dc1afad16a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548039"
---
# <a name="id3dx11effectvectorvariablegetintvector-method"></a><span data-ttu-id="b0684-106">Метод ID3DX11EffectVectorVariable:: Жетинтвектор</span><span class="sxs-lookup"><span data-stu-id="b0684-106">ID3DX11EffectVectorVariable::GetIntVector method</span></span>

<span data-ttu-id="b0684-107">Получение вектора из четырех компонентов, содержащего целочисленные данные.</span><span class="sxs-lookup"><span data-stu-id="b0684-107">Get a four-component vector that contains integer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0684-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0684-108">Syntax</span></span>


```C++
HRESULT GetIntVector(
   int *pData
);
```



## <a name="parameters"></a><span data-ttu-id="b0684-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0684-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0684-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="b0684-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="b0684-111">Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="b0684-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="b0684-112">Указатель на первый компонент.</span><span class="sxs-lookup"><span data-stu-id="b0684-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0684-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0684-113">Return value</span></span>

<span data-ttu-id="b0684-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0684-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0684-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b0684-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0684-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0684-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b0684-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="b0684-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b0684-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="b0684-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b0684-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b0684-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b0684-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b0684-120">Requirements</span></span>



| <span data-ttu-id="b0684-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b0684-121">Requirement</span></span> | <span data-ttu-id="b0684-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b0684-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0684-123">Header</span><span class="sxs-lookup"><span data-stu-id="b0684-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b0684-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0684-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b0684-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b0684-125">Library</span></span><br/> | <dl> <span data-ttu-id="b0684-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="b0684-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0684-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0684-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0684-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="b0684-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

