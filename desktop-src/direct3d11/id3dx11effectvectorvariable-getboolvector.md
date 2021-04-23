---
title: Метод ID3DX11EffectVectorVariable Жетбулвектор (D3dx11effect. h)
description: Получение вектора из четырех компонентов, содержащего логические данные.
ms.assetid: ecaf5705-d13b-4d61-9766-d2ff183af789
keywords:
- Метод Жетбулвектор Direct3D 11
- Метод Жетбулвектор Direct3D 11, интерфейс ID3DX11EffectVectorVariable
- Интерфейс ID3DX11EffectVectorVariable Direct3D 11, метод Жетбулвектор
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetBoolVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a24563bd7c685579115e3b10309fb0a1c158c2e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987077"
---
# <a name="id3dx11effectvectorvariablegetboolvector-method"></a><span data-ttu-id="cafe4-106">Метод ID3DX11EffectVectorVariable:: Жетбулвектор</span><span class="sxs-lookup"><span data-stu-id="cafe4-106">ID3DX11EffectVectorVariable::GetBoolVector method</span></span>

<span data-ttu-id="cafe4-107">Получение вектора из четырех компонентов, содержащего логические данные.</span><span class="sxs-lookup"><span data-stu-id="cafe4-107">Get a four-component vector that contains boolean data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cafe4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cafe4-108">Syntax</span></span>


```C++
HRESULT GetBoolVector(
   BOOL *pData
);
```



## <a name="parameters"></a><span data-ttu-id="cafe4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cafe4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cafe4-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="cafe4-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="cafe4-111">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="cafe4-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cafe4-112">Указатель на первый компонент.</span><span class="sxs-lookup"><span data-stu-id="cafe4-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cafe4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cafe4-113">Return value</span></span>

<span data-ttu-id="cafe4-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cafe4-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cafe4-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="cafe4-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cafe4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="cafe4-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cafe4-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="cafe4-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cafe4-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="cafe4-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cafe4-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cafe4-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cafe4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cafe4-120">Requirements</span></span>



| <span data-ttu-id="cafe4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cafe4-121">Requirement</span></span> | <span data-ttu-id="cafe4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cafe4-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cafe4-123">Header</span><span class="sxs-lookup"><span data-stu-id="cafe4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cafe4-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cafe4-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cafe4-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cafe4-125">Library</span></span><br/> | <dl> <span data-ttu-id="cafe4-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="cafe4-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cafe4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cafe4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cafe4-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="cafe4-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

