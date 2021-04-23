---
title: Метод ID3DX11EffectRasterizerVariable Ундосетрастеризерстате (D3dx11effect. h)
description: Возвращает ранее установленное состояние средства отображения программной прорисовки.
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- Метод Ундосетрастеризерстате Direct3D 11
- Метод Ундосетрастеризерстате Direct3D 11, интерфейс ID3DX11EffectRasterizerVariable
- Интерфейс ID3DX11EffectRasterizerVariable Direct3D 11, метод Ундосетрастеризерстате
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed05aa7380a1fb08bbd12d36328d33fa64fb7500
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273979"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a><span data-ttu-id="511af-106">Метод ID3DX11EffectRasterizerVariable:: Ундосетрастеризерстате</span><span class="sxs-lookup"><span data-stu-id="511af-106">ID3DX11EffectRasterizerVariable::UndoSetRasterizerState method</span></span>

<span data-ttu-id="511af-107">Возвращает ранее установленное состояние средства отображения программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="511af-107">Reverts a previously set rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="511af-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="511af-108">Syntax</span></span>


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="511af-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="511af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="511af-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="511af-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="511af-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="511af-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="511af-112">Индексировать в массив интерфейсов средства прорисовки.</span><span class="sxs-lookup"><span data-stu-id="511af-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="511af-113">Если имеется только один интерфейс, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="511af-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="511af-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="511af-114">Return value</span></span>

<span data-ttu-id="511af-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="511af-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="511af-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="511af-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="511af-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="511af-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="511af-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="511af-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="511af-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="511af-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="511af-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="511af-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="511af-121">Требования</span><span class="sxs-lookup"><span data-stu-id="511af-121">Requirements</span></span>



| <span data-ttu-id="511af-122">Требование</span><span class="sxs-lookup"><span data-stu-id="511af-122">Requirement</span></span> | <span data-ttu-id="511af-123">Значение</span><span class="sxs-lookup"><span data-stu-id="511af-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="511af-124">Header</span><span class="sxs-lookup"><span data-stu-id="511af-124">Header</span></span><br/>  | <dl> <span data-ttu-id="511af-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="511af-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="511af-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="511af-126">Library</span></span><br/> | <dl> <span data-ttu-id="511af-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="511af-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="511af-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="511af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="511af-129">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="511af-129">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

