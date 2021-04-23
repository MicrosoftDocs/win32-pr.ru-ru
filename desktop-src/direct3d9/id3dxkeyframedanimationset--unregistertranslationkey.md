---
description: Удаляет данные перевода в указанном опорном кадре.
ms.assetid: 58cadf5d-f687-4644-83b0-e124ef2bcb5a
title: 'Метод ID3DXKeyframedAnimationSet:: Унрегистертранслатионкэй (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 127aaa707c364e51815af09b8222d73102281b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674755"
---
# <a name="id3dxkeyframedanimationsetunregistertranslationkey-method"></a><span data-ttu-id="b2beb-103">Метод ID3DXKeyframedAnimationSet:: Унрегистертранслатионкэй</span><span class="sxs-lookup"><span data-stu-id="b2beb-103">ID3DXKeyframedAnimationSet::UnregisterTranslationKey method</span></span>

<span data-ttu-id="b2beb-104">Удаляет данные перевода в указанном опорном кадре.</span><span class="sxs-lookup"><span data-stu-id="b2beb-104">Removes the translation data at the specified key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2beb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2beb-105">Syntax</span></span>


```C++
HRESULT UnregisterTranslationKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a><span data-ttu-id="b2beb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2beb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2beb-107">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2beb-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2beb-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2beb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2beb-109">Идентификатор анимации.</span><span class="sxs-lookup"><span data-stu-id="b2beb-109">Animation identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b2beb-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2beb-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2beb-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2beb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2beb-112">Ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="b2beb-112">Key frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2beb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2beb-113">Return value</span></span>

<span data-ttu-id="b2beb-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2beb-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2beb-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="b2beb-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b2beb-116">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="b2beb-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2beb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2beb-117">Remarks</span></span>

<span data-ttu-id="b2beb-118">Этот метод работает достаточно долго и не должен использоваться после начала воспроизведения анимации.</span><span class="sxs-lookup"><span data-stu-id="b2beb-118">This method is slow and should not be used after an animation has begun to play.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2beb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b2beb-119">Requirements</span></span>



| <span data-ttu-id="b2beb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b2beb-120">Requirement</span></span> | <span data-ttu-id="b2beb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b2beb-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2beb-122">Header</span><span class="sxs-lookup"><span data-stu-id="b2beb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b2beb-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2beb-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b2beb-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b2beb-124">Library</span></span><br/> | <dl> <span data-ttu-id="b2beb-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2beb-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2beb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2beb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2beb-127">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="b2beb-127">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
