---
title: Метод ID3DX11EffectUnorderedAccessViewVariable Жетунордередакцессвиев (D3dx11effect. h)
description: Получите неупорядоченный доступ к представлению.
ms.assetid: 46f61c4f-b3ee-4058-99b9-a43ca6944fb2
keywords:
- Метод Жетунордередакцессвиев Direct3D 11
- Метод Жетунордередакцессвиев Direct3D 11, интерфейс ID3DX11EffectUnorderedAccessViewVariable
- Интерфейс ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, метод Жетунордередакцессвиев
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7743d15c2380ff4e38bdcae1d38bbd8905cbccda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998678"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessview-method"></a><span data-ttu-id="ae2f3-106">Метод ID3DX11EffectUnorderedAccessViewVariable:: Жетунордередакцессвиев</span><span class="sxs-lookup"><span data-stu-id="ae2f3-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessView method</span></span>

<span data-ttu-id="ae2f3-107">Получите неупорядоченный доступ к представлению.</span><span class="sxs-lookup"><span data-stu-id="ae2f3-107">Get an unordered-access-view.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2f3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae2f3-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessView(
   ID3D11UnorderedAccessView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="ae2f3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae2f3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae2f3-110">*ппресаурце*</span><span class="sxs-lookup"><span data-stu-id="ae2f3-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="ae2f3-111">Тип: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="ae2f3-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="ae2f3-112">Указатель на указатель [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) , который будет установлен при возврате.</span><span class="sxs-lookup"><span data-stu-id="ae2f3-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae2f3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae2f3-113">Return value</span></span>

<span data-ttu-id="ae2f3-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae2f3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae2f3-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ae2f3-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2f3-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae2f3-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ae2f3-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="ae2f3-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ae2f3-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="ae2f3-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ae2f3-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ae2f3-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ae2f3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ae2f3-120">Requirements</span></span>



| <span data-ttu-id="ae2f3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ae2f3-121">Requirement</span></span> | <span data-ttu-id="ae2f3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ae2f3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2f3-123">Header</span><span class="sxs-lookup"><span data-stu-id="ae2f3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ae2f3-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2f3-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ae2f3-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae2f3-125">Library</span></span><br/> | <dl> <span data-ttu-id="ae2f3-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="ae2f3-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae2f3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae2f3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2f3-128">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="ae2f3-128">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





