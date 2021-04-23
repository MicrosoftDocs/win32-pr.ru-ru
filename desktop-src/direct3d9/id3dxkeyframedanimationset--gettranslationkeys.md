---
description: Заполняет массив данными ключа, используемыми для анимации ключевых кадров.
ms.assetid: ecb791ad-e586-4057-9239-facd37a47637
title: 'Метод ID3DXKeyframedAnimationSet:: Жеттранслатионкэйс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6cc56e5538eb45c01ba7c35115e94719119bc4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713946"
---
# <a name="id3dxkeyframedanimationsetgettranslationkeys-method"></a><span data-ttu-id="78a37-103">Метод ID3DXKeyframedAnimationSet:: Жеттранслатионкэйс</span><span class="sxs-lookup"><span data-stu-id="78a37-103">ID3DXKeyframedAnimationSet::GetTranslationKeys method</span></span>

<span data-ttu-id="78a37-104">Заполняет массив данными ключа, используемыми для анимации ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="78a37-104">Fills an array with translational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="78a37-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78a37-105">Syntax</span></span>


```C++
HRESULT GetTranslationKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pTranslationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="78a37-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78a37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78a37-107">*Анимация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78a37-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78a37-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78a37-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78a37-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="78a37-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="78a37-110">*птранслатионкэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78a37-110">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78a37-111">Тип: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="78a37-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="78a37-112">Указатель на выделенный пользователем массив векторов [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) , который метод должен заполнять данными преобразования анимации.</span><span class="sxs-lookup"><span data-stu-id="78a37-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation translation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78a37-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78a37-113">Return value</span></span>

<span data-ttu-id="78a37-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78a37-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78a37-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="78a37-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="78a37-116">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="78a37-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="78a37-117">Требования</span><span class="sxs-lookup"><span data-stu-id="78a37-117">Requirements</span></span>



| <span data-ttu-id="78a37-118">Требование</span><span class="sxs-lookup"><span data-stu-id="78a37-118">Requirement</span></span> | <span data-ttu-id="78a37-119">Значение</span><span class="sxs-lookup"><span data-stu-id="78a37-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78a37-120">Header</span><span class="sxs-lookup"><span data-stu-id="78a37-120">Header</span></span><br/>  | <dl> <span data-ttu-id="78a37-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="78a37-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="78a37-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="78a37-122">Library</span></span><br/> | <dl> <span data-ttu-id="78a37-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78a37-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78a37-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78a37-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a37-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="78a37-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="78a37-126">**ID3DXKeyframedAnimationSet:: Жетнумтранслатионкэйс**</span><span class="sxs-lookup"><span data-stu-id="78a37-126">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
