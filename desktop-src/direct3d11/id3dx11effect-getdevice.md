---
title: Метод ID3DX11Effect-Device (D3dx11effect. h)
description: Получите устройство, которое создало этот результат.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- Метод WebMethod Direct3D 11
- Метод метода WebMethod Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод WebMethod
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25317740cade8a937aeeeac29f5a608bb4a43931
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273910"
---
# <a name="id3dx11effectgetdevice-method"></a><span data-ttu-id="0fd0e-106">Метод ID3DX11Effect:: of Device</span><span class="sxs-lookup"><span data-stu-id="0fd0e-106">ID3DX11Effect::GetDevice method</span></span>

<span data-ttu-id="0fd0e-107">Получите устройство, которое создало этот результат.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-107">Get the device that created the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd0e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fd0e-108">Syntax</span></span>


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="0fd0e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fd0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fd0e-110">*ппдевице*</span><span class="sxs-lookup"><span data-stu-id="0fd0e-110">*ppDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="0fd0e-111">Тип: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span><span class="sxs-lookup"><span data-stu-id="0fd0e-111">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span></span>

<span data-ttu-id="0fd0e-112">Указатель на [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span><span class="sxs-lookup"><span data-stu-id="0fd0e-112">A pointer to an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fd0e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fd0e-113">Return value</span></span>

<span data-ttu-id="0fd0e-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0fd0e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0fd0e-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0fd0e-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0fd0e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="0fd0e-116">Remarks</span></span>

<span data-ttu-id="0fd0e-117">Для конкретного устройства создается действие путем вызова функции, такой как [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="0fd0e-117">An effect is created for a specific device, by calling a function such as [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

> [!Note]  
> <span data-ttu-id="0fd0e-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0fd0e-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0fd0e-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0fd0e-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0fd0e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0fd0e-121">Requirements</span></span>



| <span data-ttu-id="0fd0e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0fd0e-122">Requirement</span></span> | <span data-ttu-id="0fd0e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0fd0e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd0e-124">Header</span><span class="sxs-lookup"><span data-stu-id="0fd0e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0fd0e-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd0e-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0fd0e-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0fd0e-126">Library</span></span><br/> | <dl> <span data-ttu-id="0fd0e-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="0fd0e-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fd0e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fd0e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd0e-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="0fd0e-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





