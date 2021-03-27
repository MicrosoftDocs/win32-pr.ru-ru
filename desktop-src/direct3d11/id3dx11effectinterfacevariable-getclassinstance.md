---
title: Метод ID3DX11EffectInterfaceVariable Жетклассинстанце (D3dx11effect. h)
description: Получение экземпляра класса.
ms.assetid: a965f4e7-1761-45f1-a72e-7ad0ed1ad671
keywords:
- Метод Жетклассинстанце Direct3D 11
- Метод Жетклассинстанце Direct3D 11, интерфейс ID3DX11EffectInterfaceVariable
- Интерфейс ID3DX11EffectInterfaceVariable Direct3D 11, метод Жетклассинстанце
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f729da6ee84d76dd37a40a7946438e367c1a4cbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000427"
---
# <a name="id3dx11effectinterfacevariablegetclassinstance-method"></a><span data-ttu-id="6f61e-106">Метод ID3DX11EffectInterfaceVariable:: Жетклассинстанце</span><span class="sxs-lookup"><span data-stu-id="6f61e-106">ID3DX11EffectInterfaceVariable::GetClassInstance method</span></span>

<span data-ttu-id="6f61e-107">Получение экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="6f61e-107">Get a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f61e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f61e-108">Syntax</span></span>


```C++
HRESULT GetClassInstance(
   ID3DX11EffectClassInstanceVariable **ppEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="6f61e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f61e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f61e-110">*ппеффектклассинстанце*</span><span class="sxs-lookup"><span data-stu-id="6f61e-110">*ppEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6f61e-111">Тип: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6f61e-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span></span>

<span data-ttu-id="6f61e-112">Указатель на указатель [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) , который будет установлен в экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="6f61e-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) pointer that will be set to the class instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f61e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f61e-113">Return value</span></span>

<span data-ttu-id="6f61e-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f61e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f61e-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6f61e-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f61e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="6f61e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6f61e-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="6f61e-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6f61e-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="6f61e-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6f61e-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6f61e-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f61e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6f61e-120">Requirements</span></span>



| <span data-ttu-id="6f61e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6f61e-121">Requirement</span></span> | <span data-ttu-id="6f61e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6f61e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f61e-123">Header</span><span class="sxs-lookup"><span data-stu-id="6f61e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6f61e-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f61e-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6f61e-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6f61e-125">Library</span></span><br/> | <dl> <span data-ttu-id="6f61e-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="6f61e-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f61e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f61e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f61e-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="6f61e-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





