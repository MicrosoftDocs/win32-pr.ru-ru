---
description: Задает для спрайта левое преобразование представления мира. Перед объявлением или сортировкой спрайтов необходимо вызвать этот метод.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: 'Метод ID3DXSprite:: Сетворлдвиевлх (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 397c3803f6d4e445f74a8b24a61e86e72e471648
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273840"
---
# <a name="id3dxspritesetworldviewlh-method"></a><span data-ttu-id="5aa15-104">Метод ID3DXSprite:: Сетворлдвиевлх</span><span class="sxs-lookup"><span data-stu-id="5aa15-104">ID3DXSprite::SetWorldViewLH method</span></span>

<span data-ttu-id="5aa15-105">Задает для спрайта левое преобразование представления мира.</span><span class="sxs-lookup"><span data-stu-id="5aa15-105">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="5aa15-106">Перед объявлением или сортировкой спрайтов необходимо вызвать этот метод.</span><span class="sxs-lookup"><span data-stu-id="5aa15-106">A call to this method is required before billboarding or sorting sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa15-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5aa15-107">Syntax</span></span>


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a><span data-ttu-id="5aa15-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5aa15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa15-109">*пворлд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5aa15-109">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa15-110">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5aa15-110">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5aa15-111">Указатель на [**D3DXMATRIX**](d3dxmatrix.md) , содержащий универсальное преобразование.</span><span class="sxs-lookup"><span data-stu-id="5aa15-111">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a world transform.</span></span> <span data-ttu-id="5aa15-112">Если **значение равно NULL**, то для универсального преобразования используется матрица идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="5aa15-112">If **NULL**, the identity matrix is used for the world transform.</span></span>

</dd> <dt>

<span data-ttu-id="5aa15-113">*pView* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5aa15-113">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa15-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5aa15-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5aa15-115">Указатель на [**D3DXMATRIX**](d3dxmatrix.md) , содержащий преобразование представления.</span><span class="sxs-lookup"><span data-stu-id="5aa15-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a view transform.</span></span> <span data-ttu-id="5aa15-116">Если **значение равно NULL**, то для преобразования представления используется матрица идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="5aa15-116">If **NULL**, the identity matrix is used for the view transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa15-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5aa15-117">Return value</span></span>

<span data-ttu-id="5aa15-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5aa15-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5aa15-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="5aa15-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5aa15-120">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="5aa15-120">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="5aa15-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5aa15-121">Remarks</span></span>

<span data-ttu-id="5aa15-122">Вызов этого метода (или to [**ID3DXSprite:: сетворлдвиеврх**](id3dxsprite--setworldviewrh.md)) требуется, если спрайт будет подготовлен к просмотру с помощью [ \_ \_ объявления D3DXSprite](d3dxsprite.md), D3DXSprite \_ \_ сортировки \_ глубины \_ Фронттобакк или D3DXSprite \_ \_ сортировки \_ глубины \_ бакктофронт в [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="5aa15-122">A call to this method (or to [**ID3DXSprite::SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) is required if the sprite will be rendered with the [D3DXSprite\_\_BILLBOARD](d3dxsprite.md), D3DXSprite\_\_SORT\_DEPTH\_FRONTTOBACK, or D3DXSprite\_\_SORT\_DEPTH\_BACKTOFRONT flag value in [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa15-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5aa15-123">Requirements</span></span>



| <span data-ttu-id="5aa15-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5aa15-124">Requirement</span></span> | <span data-ttu-id="5aa15-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5aa15-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa15-126">Header</span><span class="sxs-lookup"><span data-stu-id="5aa15-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5aa15-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aa15-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="5aa15-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5aa15-128">Library</span></span><br/> | <dl> <span data-ttu-id="5aa15-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5aa15-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5aa15-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5aa15-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa15-131">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="5aa15-131">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




