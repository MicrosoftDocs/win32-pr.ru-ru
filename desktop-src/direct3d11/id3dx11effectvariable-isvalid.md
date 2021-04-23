---
title: ID3DX11EffectVariable-метод IsValid (D3dx11effect. h)
description: Сравните тип данных с хранимыми данными.
ms.assetid: 3384afa3-6ae5-4c7c-b95d-4fe3c87cc2fe
keywords:
- Метод IsValid Direct3D 11
- Метод IsValid Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5136005e675a6f5e54cc3863ef2d80ffadfb7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998642"
---
# <a name="id3dx11effectvariableisvalid-method"></a><span data-ttu-id="ac6ec-106">Метод ID3DX11EffectVariable:: IsValid</span><span class="sxs-lookup"><span data-stu-id="ac6ec-106">ID3DX11EffectVariable::IsValid method</span></span>

<span data-ttu-id="ac6ec-107">Сравните тип данных с хранимыми данными.</span><span class="sxs-lookup"><span data-stu-id="ac6ec-107">Compare the data type with the data stored.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac6ec-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac6ec-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="ac6ec-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac6ec-109">Parameters</span></span>

<span data-ttu-id="ac6ec-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ac6ec-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac6ec-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac6ec-111">Return value</span></span>

<span data-ttu-id="ac6ec-112">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ac6ec-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ac6ec-113">**Значение true** , если синтаксис допустим; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="ac6ec-113">**TRUE** if the syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac6ec-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ac6ec-114">Remarks</span></span>

<span data-ttu-id="ac6ec-115">Этот метод проверяет, соответствует ли тип данных данным, хранящимся после приведения одного интерфейса к другому (с помощью любого из методов AS).</span><span class="sxs-lookup"><span data-stu-id="ac6ec-115">This method checks that the data type matches the data stored after casting one interface to another (using any of the As methods).</span></span>

> [!Note]  
> <span data-ttu-id="ac6ec-116">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="ac6ec-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ac6ec-117">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="ac6ec-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ac6ec-118">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ac6ec-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ac6ec-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ac6ec-119">Requirements</span></span>



| <span data-ttu-id="ac6ec-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ac6ec-120">Requirement</span></span> | <span data-ttu-id="ac6ec-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ac6ec-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac6ec-122">Header</span><span class="sxs-lookup"><span data-stu-id="ac6ec-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ac6ec-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac6ec-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ac6ec-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac6ec-124">Library</span></span><br/> | <dl> <span data-ttu-id="ac6ec-125"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="ac6ec-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac6ec-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac6ec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac6ec-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="ac6ec-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

