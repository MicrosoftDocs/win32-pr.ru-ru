---
title: ID3DX11EffectGroup-метод IsValid (D3dx11effect. h)
description: Протестируйте результат, чтобы проверить, содержит ли он допустимый синтаксис. | ID3DX11EffectGroup-метод IsValid (D3dx11effect. h)
ms.assetid: 05829749-cef0-40ed-beab-556a65a1ac96
keywords:
- Метод IsValid Direct3D 11
- Метод IsValid Direct3D 11, интерфейс ID3DX11EffectGroup
- Интерфейс ID3DX11EffectGroup Direct3D 11, метод IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d1fd110a0f35f8a288517d72b69a6f5ad9f0ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986957"
---
# <a name="id3dx11effectgroupisvalid-method"></a><span data-ttu-id="c0584-107">Метод ID3DX11EffectGroup:: IsValid</span><span class="sxs-lookup"><span data-stu-id="c0584-107">ID3DX11EffectGroup::IsValid method</span></span>

<span data-ttu-id="c0584-108">Протестируйте результат, чтобы проверить, содержит ли он допустимый синтаксис.</span><span class="sxs-lookup"><span data-stu-id="c0584-108">Test an effect to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0584-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0584-109">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="c0584-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0584-110">Parameters</span></span>

<span data-ttu-id="c0584-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c0584-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0584-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0584-112">Return value</span></span>

<span data-ttu-id="c0584-113">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0584-113">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c0584-114">**Значение true** , если синтаксис кода допустим; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="c0584-114">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0584-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0584-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c0584-116">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="c0584-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c0584-117">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="c0584-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c0584-118">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c0584-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0584-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c0584-119">Requirements</span></span>



| <span data-ttu-id="c0584-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c0584-120">Requirement</span></span> | <span data-ttu-id="c0584-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c0584-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0584-122">Header</span><span class="sxs-lookup"><span data-stu-id="c0584-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c0584-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0584-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c0584-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0584-124">Library</span></span><br/> | <dl> <span data-ttu-id="c0584-125"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="c0584-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0584-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0584-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0584-127">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="c0584-127">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

