---
title: ID3DX11Effect-метод IsValid (D3dx11effect. h)
description: Протестируйте результат, чтобы проверить, содержит ли он допустимый синтаксис. | ID3DX11Effect-метод IsValid (D3dx11effect. h)
ms.assetid: 42bf0069-1828-4f55-99f5-d0f81eb04336
keywords:
- Метод IsValid Direct3D 11
- Метод IsValid Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод IsValid
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88aef9e3864fc77380b3459860178c8537a6a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998606"
---
# <a name="id3dx11effectisvalid-method"></a><span data-ttu-id="e70de-107">Метод ID3DX11Effect:: IsValid</span><span class="sxs-lookup"><span data-stu-id="e70de-107">ID3DX11Effect::IsValid method</span></span>

<span data-ttu-id="e70de-108">Протестируйте результат, чтобы проверить, содержит ли он допустимый синтаксис.</span><span class="sxs-lookup"><span data-stu-id="e70de-108">Test an effect to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70de-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e70de-109">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="e70de-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e70de-110">Parameters</span></span>

<span data-ttu-id="e70de-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e70de-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e70de-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e70de-112">Return value</span></span>

<span data-ttu-id="e70de-113">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e70de-113">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e70de-114">**Значение true** , если синтаксис кода допустим; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="e70de-114">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e70de-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="e70de-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e70de-116">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="e70de-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e70de-117">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="e70de-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e70de-118">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e70de-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e70de-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e70de-119">Requirements</span></span>



| <span data-ttu-id="e70de-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e70de-120">Requirement</span></span> | <span data-ttu-id="e70de-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e70de-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e70de-122">Header</span><span class="sxs-lookup"><span data-stu-id="e70de-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e70de-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e70de-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e70de-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e70de-124">Library</span></span><br/> | <dl> <span data-ttu-id="e70de-125"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="e70de-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e70de-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e70de-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70de-127">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="e70de-127">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

