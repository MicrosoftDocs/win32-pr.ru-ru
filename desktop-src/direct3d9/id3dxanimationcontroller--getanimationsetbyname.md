---
description: Возвращает набор анимации по его имени.
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: 'Метод ID3DXAnimationController:: Жетаниматионсетбинаме (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSetByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d520625e457a50fe962ae74d6e25fc17e2beb729
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713857"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a><span data-ttu-id="2bb40-103">Метод ID3DXAnimationController:: Жетаниматионсетбинаме</span><span class="sxs-lookup"><span data-stu-id="2bb40-103">ID3DXAnimationController::GetAnimationSetByName method</span></span>

<span data-ttu-id="2bb40-104">Возвращает набор анимации по его имени.</span><span class="sxs-lookup"><span data-stu-id="2bb40-104">Gets an animation set, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb40-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bb40-105">Syntax</span></span>


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="2bb40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bb40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bb40-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2bb40-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bb40-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bb40-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2bb40-109">Строка, содержащая имя набора анимации.</span><span class="sxs-lookup"><span data-stu-id="2bb40-109">String containing the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="2bb40-110">*ппанимсет* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2bb40-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bb40-111">Тип: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="2bb40-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="2bb40-112">Указатель на набор эффектов анимации [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="2bb40-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bb40-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bb40-113">Return value</span></span>

<span data-ttu-id="2bb40-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2bb40-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2bb40-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="2bb40-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2bb40-116">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="2bb40-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bb40-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2bb40-117">Remarks</span></span>

<span data-ttu-id="2bb40-118">Контроллер анимации содержит массив наборов анимации.</span><span class="sxs-lookup"><span data-stu-id="2bb40-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="2bb40-119">Этот метод возвращает набор анимации с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="2bb40-119">This method returns an animation set that has the given name.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bb40-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2bb40-120">Requirements</span></span>



| <span data-ttu-id="2bb40-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2bb40-121">Requirement</span></span> | <span data-ttu-id="2bb40-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2bb40-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb40-123">Header</span><span class="sxs-lookup"><span data-stu-id="2bb40-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2bb40-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bb40-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2bb40-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2bb40-125">Library</span></span><br/> | <dl> <span data-ttu-id="2bb40-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bb40-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2bb40-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bb40-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bb40-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="2bb40-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
