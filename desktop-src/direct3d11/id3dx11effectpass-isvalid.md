---
title: ID3DX11EffectPass-метод IsValid (D3dx11effect. h)
description: Протестируйте пройденный тест, чтобы увидеть, содержит ли он допустимый синтаксис.
ms.assetid: 3c6ddcef-1303-4161-889c-c3ca271b6ad0
keywords:
- Метод IsValid Direct3D 11
- Метод IsValid Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50db900d3cea82197fb56ce3a57a5a548220ca1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986918"
---
# <a name="id3dx11effectpassisvalid-method"></a><span data-ttu-id="0e25d-106">Метод ID3DX11EffectPass:: IsValid</span><span class="sxs-lookup"><span data-stu-id="0e25d-106">ID3DX11EffectPass::IsValid method</span></span>

<span data-ttu-id="0e25d-107">Протестируйте пройденный тест, чтобы увидеть, содержит ли он допустимый синтаксис.</span><span class="sxs-lookup"><span data-stu-id="0e25d-107">Test a pass to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e25d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e25d-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="0e25d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e25d-109">Parameters</span></span>

<span data-ttu-id="0e25d-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0e25d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e25d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e25d-111">Return value</span></span>

<span data-ttu-id="0e25d-112">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0e25d-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0e25d-113">**Значение true** , если синтаксис кода допустим; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="0e25d-113">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e25d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e25d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0e25d-115">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="0e25d-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0e25d-116">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="0e25d-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0e25d-117">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0e25d-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e25d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0e25d-118">Requirements</span></span>



| <span data-ttu-id="0e25d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0e25d-119">Requirement</span></span> | <span data-ttu-id="0e25d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0e25d-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e25d-121">Header</span><span class="sxs-lookup"><span data-stu-id="0e25d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0e25d-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e25d-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0e25d-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0e25d-123">Library</span></span><br/> | <dl> <span data-ttu-id="0e25d-124"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="0e25d-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e25d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e25d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e25d-126">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="0e25d-126">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

