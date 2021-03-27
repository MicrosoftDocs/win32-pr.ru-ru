---
title: ID3DX11EffectType-метод IsValid (D3dx11effect. h)
description: Проверяет допустимость типа воздействия.
ms.assetid: 3c1d93a0-92a1-4969-a561-5156e2cd2f3b
keywords:
- Метод IsValid Direct3D 11
- Метод IsValid Direct3D 11, интерфейс ID3DX11EffectType
- Интерфейс ID3DX11EffectType Direct3D 11, метод IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectType.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9254513622ff7c0705c01b0ee15262126c096ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821004"
---
# <a name="id3dx11effecttypeisvalid-method"></a><span data-ttu-id="30b93-106">Метод ID3DX11EffectType:: IsValid</span><span class="sxs-lookup"><span data-stu-id="30b93-106">ID3DX11EffectType::IsValid method</span></span>

<span data-ttu-id="30b93-107">Проверяет допустимость типа воздействия.</span><span class="sxs-lookup"><span data-stu-id="30b93-107">Tests that the effect type is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b93-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30b93-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="30b93-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="30b93-109">Parameters</span></span>

<span data-ttu-id="30b93-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="30b93-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30b93-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30b93-111">Return value</span></span>

<span data-ttu-id="30b93-112">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30b93-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="30b93-113">**Значение true** , если оно является допустимым; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="30b93-113">**TRUE** if it is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="30b93-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="30b93-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30b93-115">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="30b93-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="30b93-116">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="30b93-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="30b93-117">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="30b93-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30b93-118">Требования</span><span class="sxs-lookup"><span data-stu-id="30b93-118">Requirements</span></span>



| <span data-ttu-id="30b93-119">Требование</span><span class="sxs-lookup"><span data-stu-id="30b93-119">Requirement</span></span> | <span data-ttu-id="30b93-120">Значение</span><span class="sxs-lookup"><span data-stu-id="30b93-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b93-121">Header</span><span class="sxs-lookup"><span data-stu-id="30b93-121">Header</span></span><br/>  | <dl> <span data-ttu-id="30b93-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="30b93-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="30b93-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="30b93-123">Library</span></span><br/> | <dl> <span data-ttu-id="30b93-124"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="30b93-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b93-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30b93-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b93-126">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="30b93-126">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

