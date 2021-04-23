---
title: Метод ID3DX11EffectScalarVariable Сетбул (D3dx11effect. h)
description: Задайте логическую переменную.
ms.assetid: b5385ed3-6e65-4d65-bb8e-835967e6f610
keywords:
- Метод Сетбул Direct3D 11
- Метод Сетбул Direct3D 11, интерфейс ID3DX11EffectScalarVariable
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11, метод Сетбул
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1d3670b3a41f47bf1b5ec7ac3d2fb93441e72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987086"
---
# <a name="id3dx11effectscalarvariablesetbool-method"></a><span data-ttu-id="96815-106">Метод ID3DX11EffectScalarVariable:: Сетбул</span><span class="sxs-lookup"><span data-stu-id="96815-106">ID3DX11EffectScalarVariable::SetBool method</span></span>

<span data-ttu-id="96815-107">Задайте логическую переменную.</span><span class="sxs-lookup"><span data-stu-id="96815-107">Set a boolean variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="96815-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96815-108">Syntax</span></span>


```C++
HRESULT SetBool(
   BOOL Value
);
```



## <a name="parameters"></a><span data-ttu-id="96815-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="96815-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96815-110">*Значение*</span><span class="sxs-lookup"><span data-stu-id="96815-110">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="96815-111">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96815-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="96815-112">Указатель на переменную.</span><span class="sxs-lookup"><span data-stu-id="96815-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96815-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96815-113">Return value</span></span>

<span data-ttu-id="96815-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96815-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96815-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="96815-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="96815-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="96815-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="96815-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="96815-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="96815-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="96815-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="96815-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="96815-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96815-120">Требования</span><span class="sxs-lookup"><span data-stu-id="96815-120">Requirements</span></span>



| <span data-ttu-id="96815-121">Требование</span><span class="sxs-lookup"><span data-stu-id="96815-121">Requirement</span></span> | <span data-ttu-id="96815-122">Значение</span><span class="sxs-lookup"><span data-stu-id="96815-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96815-123">Header</span><span class="sxs-lookup"><span data-stu-id="96815-123">Header</span></span><br/>  | <dl> <span data-ttu-id="96815-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="96815-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="96815-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96815-125">Library</span></span><br/> | <dl> <span data-ttu-id="96815-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="96815-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96815-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96815-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96815-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="96815-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

