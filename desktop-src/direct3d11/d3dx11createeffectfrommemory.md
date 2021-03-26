---
title: Функция D3DX11CreateEffectFromMemory (D3dx11effect. h)
description: Создает результат из бинарного действия или файла.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- D3DX11CreateEffectFromMemory функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998525"
---
# <a name="d3dx11createeffectfrommemory-function"></a><span data-ttu-id="8faa3-104">Функция D3DX11CreateEffectFromMemory</span><span class="sxs-lookup"><span data-stu-id="8faa3-104">D3DX11CreateEffectFromMemory function</span></span>

<span data-ttu-id="8faa3-105">Создает результат из бинарного действия или файла.</span><span class="sxs-lookup"><span data-stu-id="8faa3-105">Creates an effect from a binary effect or file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8faa3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8faa3-106">Syntax</span></span>


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="8faa3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8faa3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8faa3-108">*pData*</span><span class="sxs-lookup"><span data-stu-id="8faa3-108">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="8faa3-109">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="8faa3-109">Type: **void\***</span></span>

<span data-ttu-id="8faa3-110">Большой двоичный объект данных скомпилированных эффектов.</span><span class="sxs-lookup"><span data-stu-id="8faa3-110">Blob of compiled effect data.</span></span>

</dd> <dt>

<span data-ttu-id="8faa3-111">*DataLength*</span><span class="sxs-lookup"><span data-stu-id="8faa3-111">*DataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="8faa3-112">Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8faa3-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8faa3-113">Длина большого двоичного объекта данных.</span><span class="sxs-lookup"><span data-stu-id="8faa3-113">Length of the data blob.</span></span>

</dd> <dt>

<span data-ttu-id="8faa3-114">*фксфлагс*</span><span class="sxs-lookup"><span data-stu-id="8faa3-114">*FXFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="8faa3-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8faa3-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8faa3-116">Флаги влияния не существуют.</span><span class="sxs-lookup"><span data-stu-id="8faa3-116">No effect flags exist.</span></span> <span data-ttu-id="8faa3-117">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8faa3-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="8faa3-118">*пдевице*</span><span class="sxs-lookup"><span data-stu-id="8faa3-118">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="8faa3-119">Тип: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="8faa3-119">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="8faa3-120">Указатель на [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) , для которого необходимо создать ресурсы эффектов.</span><span class="sxs-lookup"><span data-stu-id="8faa3-120">Pointer to the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) on which to create Effect resources.</span></span>

</dd> <dt>

<span data-ttu-id="8faa3-121">*ппеффект*</span><span class="sxs-lookup"><span data-stu-id="8faa3-121">*ppEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="8faa3-122">Тип: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8faa3-122">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="8faa3-123">Адрес вновь созданного интерфейса [**ID3DX11Effect**](id3dx11effect.md) .</span><span class="sxs-lookup"><span data-stu-id="8faa3-123">Address of the newly created [**ID3DX11Effect**](id3dx11effect.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8faa3-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8faa3-124">Return value</span></span>

<span data-ttu-id="8faa3-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8faa3-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8faa3-126">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8faa3-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8faa3-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="8faa3-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8faa3-128">Для создания приложения типа Effects необходимо использовать [Исходный текст Effects 11](https://github.com/Microsoft/FX11) .</span><span class="sxs-lookup"><span data-stu-id="8faa3-128">You must use [Effects 11 source](https://github.com/Microsoft/FX11) to build your effects-type application.</span></span> <span data-ttu-id="8faa3-129">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8faa3-129">For more info about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8faa3-130">Требования</span><span class="sxs-lookup"><span data-stu-id="8faa3-130">Requirements</span></span>



| <span data-ttu-id="8faa3-131">Требование</span><span class="sxs-lookup"><span data-stu-id="8faa3-131">Requirement</span></span> | <span data-ttu-id="8faa3-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8faa3-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8faa3-133">Header</span><span class="sxs-lookup"><span data-stu-id="8faa3-133">Header</span></span><br/> | <dl> <span data-ttu-id="8faa3-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8faa3-134"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8faa3-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8faa3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8faa3-136">Эффекты 11 функций</span><span class="sxs-lookup"><span data-stu-id="8faa3-136">Effects 11 Functions</span></span>](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

