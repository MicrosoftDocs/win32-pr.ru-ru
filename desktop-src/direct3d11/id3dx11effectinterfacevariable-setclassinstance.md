---
title: Метод ID3DX11EffectInterfaceVariable Сетклассинстанце (D3dx11effect. h)
description: Задает экземпляр класса.
ms.assetid: fc71a0d2-054a-48ed-86a5-54cf0017062a
keywords:
- Метод Сетклассинстанце Direct3D 11
- Метод Сетклассинстанце Direct3D 11, интерфейс ID3DX11EffectInterfaceVariable
- Интерфейс ID3DX11EffectInterfaceVariable Direct3D 11, метод Сетклассинстанце
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.SetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03d319d55b073393ff511b2e072aa07c244e5a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986948"
---
# <a name="id3dx11effectinterfacevariablesetclassinstance-method"></a><span data-ttu-id="ff5c1-106">Метод ID3DX11EffectInterfaceVariable:: Сетклассинстанце</span><span class="sxs-lookup"><span data-stu-id="ff5c1-106">ID3DX11EffectInterfaceVariable::SetClassInstance method</span></span>

<span data-ttu-id="ff5c1-107">Задает экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="ff5c1-107">Sets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff5c1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff5c1-108">Syntax</span></span>


```C++
HRESULT SetClassInstance(
   ID3DX11EffectClassInstanceVariable *pEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="ff5c1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff5c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff5c1-110">*пеффектклассинстанце*</span><span class="sxs-lookup"><span data-stu-id="ff5c1-110">*pEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ff5c1-111">Тип: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff5c1-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span></span>

<span data-ttu-id="ff5c1-112">Указатель на интерфейс [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) .</span><span class="sxs-lookup"><span data-stu-id="ff5c1-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff5c1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff5c1-113">Return value</span></span>

<span data-ttu-id="ff5c1-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ff5c1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ff5c1-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ff5c1-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ff5c1-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff5c1-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ff5c1-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="ff5c1-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ff5c1-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="ff5c1-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ff5c1-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ff5c1-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ff5c1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ff5c1-120">Requirements</span></span>



| <span data-ttu-id="ff5c1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ff5c1-121">Requirement</span></span> | <span data-ttu-id="ff5c1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ff5c1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff5c1-123">Header</span><span class="sxs-lookup"><span data-stu-id="ff5c1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ff5c1-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff5c1-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ff5c1-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ff5c1-125">Library</span></span><br/> | <dl> <span data-ttu-id="ff5c1-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="ff5c1-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff5c1-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff5c1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff5c1-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="ff5c1-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





