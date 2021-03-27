---
title: Метод ID3DX11EffectGroup-desc (D3dx11effect. h)
description: Возвращает описание группы.
ms.assetid: 04bb707a-be21-43d1-8d9d-5a84d29fda74
keywords:
- Метод DESC Direct3D 11
- Метод DESC Direct3D 11, интерфейс ID3DX11EffectGroup
- ID3DX11EffectGroup интерфейс Direct3D 11, метод DESC
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c32d44e215a6c89a7d71e899d9839509cbe39417
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000450"
---
# <a name="id3dx11effectgroupgetdesc-method"></a><span data-ttu-id="26ca4-106">Метод ID3DX11EffectGroup:: DESC</span><span class="sxs-lookup"><span data-stu-id="26ca4-106">ID3DX11EffectGroup::GetDesc method</span></span>

<span data-ttu-id="26ca4-107">Возвращает описание группы.</span><span class="sxs-lookup"><span data-stu-id="26ca4-107">Gets a group description.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ca4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26ca4-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_GROUP_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="26ca4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="26ca4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26ca4-110">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="26ca4-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="26ca4-111">Тип: **[ **D3DX11 \_ Группа \_ DESC**](d3dx11-group-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="26ca4-111">Type: **[**D3DX11\_GROUP\_DESC**](d3dx11-group-desc.md)\***</span></span>

<span data-ttu-id="26ca4-112">Указатель на структуру [**\_ \_ DESC группы D3DX11**](d3dx11-group-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="26ca4-112">A pointer to a [**D3DX11\_GROUP\_DESC**](d3dx11-group-desc.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26ca4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26ca4-113">Return value</span></span>

<span data-ttu-id="26ca4-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26ca4-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26ca4-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="26ca4-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26ca4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="26ca4-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="26ca4-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="26ca4-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="26ca4-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="26ca4-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="26ca4-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="26ca4-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26ca4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="26ca4-120">Requirements</span></span>



| <span data-ttu-id="26ca4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="26ca4-121">Requirement</span></span> | <span data-ttu-id="26ca4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="26ca4-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26ca4-123">Header</span><span class="sxs-lookup"><span data-stu-id="26ca4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="26ca4-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="26ca4-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="26ca4-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="26ca4-125">Library</span></span><br/> | <dl> <span data-ttu-id="26ca4-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="26ca4-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ca4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26ca4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ca4-128">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="26ca4-128">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

 





