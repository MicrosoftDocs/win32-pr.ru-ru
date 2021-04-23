---
title: Метод ID3DX11EffectScalarVariable SetFloat (D3dx11effect. h)
description: Задайте переменную с плавающей запятой.
ms.assetid: e13f3ba1-437a-47f0-bd08-4423ffc25ddb
keywords:
- Метод SetFloat Direct3D 11
- Метод SetFloat Direct3D 11, интерфейс ID3DX11EffectScalarVariable
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11, метод SetFloat
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad3c3e9f020e5094cd03f7b25ee907dcc6e2c2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081846"
---
# <a name="id3dx11effectscalarvariablesetfloat-method"></a><span data-ttu-id="31223-106">Метод ID3DX11EffectScalarVariable:: SetFloat</span><span class="sxs-lookup"><span data-stu-id="31223-106">ID3DX11EffectScalarVariable::SetFloat method</span></span>

<span data-ttu-id="31223-107">Задайте переменную с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="31223-107">Set a floating-point variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="31223-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31223-108">Syntax</span></span>


```C++
HRESULT SetFloat(
   float Value
);
```



## <a name="parameters"></a><span data-ttu-id="31223-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="31223-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31223-110">*Значение*</span><span class="sxs-lookup"><span data-stu-id="31223-110">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="31223-111">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="31223-111">Type: **float**</span></span>

<span data-ttu-id="31223-112">Указатель на переменную.</span><span class="sxs-lookup"><span data-stu-id="31223-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31223-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31223-113">Return value</span></span>

<span data-ttu-id="31223-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31223-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31223-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="31223-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="31223-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="31223-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="31223-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="31223-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="31223-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="31223-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="31223-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="31223-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="31223-120">Требования</span><span class="sxs-lookup"><span data-stu-id="31223-120">Requirements</span></span>



| <span data-ttu-id="31223-121">Требование</span><span class="sxs-lookup"><span data-stu-id="31223-121">Requirement</span></span> | <span data-ttu-id="31223-122">Значение</span><span class="sxs-lookup"><span data-stu-id="31223-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31223-123">Header</span><span class="sxs-lookup"><span data-stu-id="31223-123">Header</span></span><br/>  | <dl> <span data-ttu-id="31223-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="31223-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="31223-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31223-125">Library</span></span><br/> | <dl> <span data-ttu-id="31223-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="31223-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31223-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31223-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31223-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="31223-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

 





