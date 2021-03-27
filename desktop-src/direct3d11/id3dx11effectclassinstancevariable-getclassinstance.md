---
title: Метод ID3DX11EffectClassInstanceVariable Жетклассинстанце (D3dx11effect. h)
description: Возвращает экземпляр класса.
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- Метод Жетклассинстанце Direct3D 11
- Метод Жетклассинстанце Direct3D 11, интерфейс ID3DX11EffectClassInstanceVariable
- Интерфейс ID3DX11EffectClassInstanceVariable Direct3D 11, метод Жетклассинстанце
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dae96d42a0088adc683ca93d7e3215c12912a87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356040"
---
# <a name="id3dx11effectclassinstancevariablegetclassinstance-method"></a><span data-ttu-id="9716b-106">Метод ID3DX11EffectClassInstanceVariable:: Жетклассинстанце</span><span class="sxs-lookup"><span data-stu-id="9716b-106">ID3DX11EffectClassInstanceVariable::GetClassInstance method</span></span>

<span data-ttu-id="9716b-107">Возвращает экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="9716b-107">Gets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="9716b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9716b-108">Syntax</span></span>


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="9716b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9716b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9716b-110">*ппклассинстанце*</span><span class="sxs-lookup"><span data-stu-id="9716b-110">*ppClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="9716b-111">Тип: **[ **ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***</span><span class="sxs-lookup"><span data-stu-id="9716b-111">Type: **[**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***</span></span>

<span data-ttu-id="9716b-112">Указатель на указатель [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) , который будет установлен в экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="9716b-112">Pointer to an [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointer that will be set to class instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9716b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9716b-113">Return value</span></span>

<span data-ttu-id="9716b-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9716b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9716b-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9716b-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9716b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9716b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9716b-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="9716b-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9716b-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="9716b-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9716b-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9716b-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9716b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9716b-120">Requirements</span></span>



| <span data-ttu-id="9716b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9716b-121">Requirement</span></span> | <span data-ttu-id="9716b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9716b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9716b-123">Header</span><span class="sxs-lookup"><span data-stu-id="9716b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9716b-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9716b-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9716b-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9716b-125">Library</span></span><br/> | <dl> <span data-ttu-id="9716b-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="9716b-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9716b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9716b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9716b-128">ID3DX11EffectClassInstanceVariable</span><span class="sxs-lookup"><span data-stu-id="9716b-128">ID3DX11EffectClassInstanceVariable</span></span>](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 





