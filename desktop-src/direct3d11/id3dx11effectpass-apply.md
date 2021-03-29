---
title: Метод Apply ID3DX11EffectPass (D3dx11effect. h)
description: Задайте состояние, которое содержится в передаче на устройство.
ms.assetid: d67fe968-bfb2-4f3a-b393-3f72f680211f
keywords:
- Применение метода Direct3D 11
- Применение метода Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод Apply
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.Apply
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a061609953e164524e16722222a5ecea81f275b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986924"
---
# <a name="id3dx11effectpassapply-method"></a><span data-ttu-id="59ace-106">Метод ID3DX11EffectPass:: Apply</span><span class="sxs-lookup"><span data-stu-id="59ace-106">ID3DX11EffectPass::Apply method</span></span>

<span data-ttu-id="59ace-107">Задайте состояние, которое содержится в передаче на устройство.</span><span class="sxs-lookup"><span data-stu-id="59ace-107">Set the state contained in a pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="59ace-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59ace-108">Syntax</span></span>


```C++
HRESULT Apply(
   UINT                Flags,
   ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="59ace-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="59ace-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59ace-110">*Флаги*</span><span class="sxs-lookup"><span data-stu-id="59ace-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="59ace-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="59ace-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="59ace-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="59ace-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="59ace-113">*pContext*</span><span class="sxs-lookup"><span data-stu-id="59ace-113">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="59ace-114">Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="59ace-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="59ace-115">[**Ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) , к которому применяется передача.</span><span class="sxs-lookup"><span data-stu-id="59ace-115">The [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) to apply the pass to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59ace-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59ace-116">Return value</span></span>

<span data-ttu-id="59ace-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59ace-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59ace-118">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="59ace-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="59ace-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="59ace-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="59ace-120">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="59ace-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="59ace-121">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="59ace-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="59ace-122">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="59ace-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="59ace-123">Требования</span><span class="sxs-lookup"><span data-stu-id="59ace-123">Requirements</span></span>



| <span data-ttu-id="59ace-124">Требование</span><span class="sxs-lookup"><span data-stu-id="59ace-124">Requirement</span></span> | <span data-ttu-id="59ace-125">Значение</span><span class="sxs-lookup"><span data-stu-id="59ace-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59ace-126">Header</span><span class="sxs-lookup"><span data-stu-id="59ace-126">Header</span></span><br/>  | <dl> <span data-ttu-id="59ace-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="59ace-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="59ace-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59ace-128">Library</span></span><br/> | <dl> <span data-ttu-id="59ace-129"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="59ace-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59ace-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59ace-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ace-131">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="59ace-131">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

