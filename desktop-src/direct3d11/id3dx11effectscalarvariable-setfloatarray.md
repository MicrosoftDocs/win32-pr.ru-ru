---
title: Метод ID3DX11EffectScalarVariable Сетфлоатаррай (D3dx11effect. h)
description: Задайте массив переменных с плавающей запятой.
ms.assetid: af7f3fb1-e5a8-43c9-8c8a-5ee7b3b01242
keywords:
- Метод Сетфлоатаррай Direct3D 11
- Метод Сетфлоатаррай Direct3D 11, интерфейс ID3DX11EffectScalarVariable
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11, метод Сетфлоатаррай
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetFloatArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591efd87026caeaadb8de7f29a2741dfccd5028a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000316"
---
# <a name="id3dx11effectscalarvariablesetfloatarray-method"></a><span data-ttu-id="09f0a-106">Метод ID3DX11EffectScalarVariable:: Сетфлоатаррай</span><span class="sxs-lookup"><span data-stu-id="09f0a-106">ID3DX11EffectScalarVariable::SetFloatArray method</span></span>

<span data-ttu-id="09f0a-107">Задайте массив переменных с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="09f0a-107">Set an array of floating-point variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="09f0a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09f0a-108">Syntax</span></span>


```C++
HRESULT SetFloatArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="09f0a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="09f0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09f0a-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="09f0a-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="09f0a-111">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="09f0a-111">Type: **float\***</span></span>

<span data-ttu-id="09f0a-112">Указатель на начало данных, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="09f0a-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="09f0a-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="09f0a-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="09f0a-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="09f0a-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="09f0a-115">Необходимо задать значение 0; это зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="09f0a-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="09f0a-116">*Количество*</span><span class="sxs-lookup"><span data-stu-id="09f0a-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="09f0a-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="09f0a-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="09f0a-118">Число заданных элементов массива.</span><span class="sxs-lookup"><span data-stu-id="09f0a-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09f0a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09f0a-119">Return value</span></span>

<span data-ttu-id="09f0a-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09f0a-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09f0a-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="09f0a-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="09f0a-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="09f0a-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="09f0a-123">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="09f0a-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="09f0a-124">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="09f0a-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="09f0a-125">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="09f0a-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="09f0a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="09f0a-126">Requirements</span></span>



| <span data-ttu-id="09f0a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="09f0a-127">Requirement</span></span> | <span data-ttu-id="09f0a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="09f0a-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09f0a-129">Header</span><span class="sxs-lookup"><span data-stu-id="09f0a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="09f0a-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="09f0a-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="09f0a-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="09f0a-131">Library</span></span><br/> | <dl> <span data-ttu-id="09f0a-132"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="09f0a-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09f0a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09f0a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f0a-134">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="09f0a-134">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

