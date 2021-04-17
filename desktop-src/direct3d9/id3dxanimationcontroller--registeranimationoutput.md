---
description: Добавляет выходные данные анимации в контроллер анимации и регистрирует указатели для преобразований масштабирования, вращения и преобразования (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'Метод ID3DXAnimationController:: Регистераниматионаутпут (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670f8b311532d096b9957ebbefcf1f6fb15d952
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703923"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a><span data-ttu-id="e65f0-103">Метод ID3DXAnimationController:: Регистераниматионаутпут</span><span class="sxs-lookup"><span data-stu-id="e65f0-103">ID3DXAnimationController::RegisterAnimationOutput method</span></span>

<span data-ttu-id="e65f0-104">Добавляет выходные данные анимации в контроллер анимации и регистрирует указатели для преобразований масштабирования, вращения и преобразования (SRT).</span><span class="sxs-lookup"><span data-stu-id="e65f0-104">Adds an animation output to the animation controller and registers pointers for scale, rotate, and translate (SRT) transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e65f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e65f0-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="e65f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e65f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e65f0-107">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e65f0-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e65f0-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e65f0-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e65f0-109">Имя выходных данных анимации.</span><span class="sxs-lookup"><span data-stu-id="e65f0-109">Name of the animation output.</span></span>

</dd> <dt>

<span data-ttu-id="e65f0-110">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e65f0-110">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e65f0-111">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e65f0-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e65f0-112">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , содержащую данные преобразования SRT.</span><span class="sxs-lookup"><span data-stu-id="e65f0-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure containing SRT transformation data.</span></span> <span data-ttu-id="e65f0-113">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e65f0-113">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e65f0-114">*пскале* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e65f0-114">*pScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e65f0-115">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e65f0-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e65f0-116">Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , описывающий масштаб набора анимации.</span><span class="sxs-lookup"><span data-stu-id="e65f0-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span> <span data-ttu-id="e65f0-117">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e65f0-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e65f0-118"> \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e65f0-118">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e65f0-119">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e65f0-119">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e65f0-120">Указатель на кватернион [**D3DXQUATERNION**](d3dxquaternion.md) , описывающий поворот набора анимации.</span><span class="sxs-lookup"><span data-stu-id="e65f0-120">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span> <span data-ttu-id="e65f0-121">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e65f0-121">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e65f0-122">*птранслатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e65f0-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e65f0-123">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e65f0-123">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e65f0-124">Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , описывающий перевод набора анимации.</span><span class="sxs-lookup"><span data-stu-id="e65f0-124">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span> <span data-ttu-id="e65f0-125">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e65f0-125">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e65f0-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e65f0-126">Return value</span></span>

<span data-ttu-id="e65f0-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e65f0-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e65f0-128">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="e65f0-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e65f0-129">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e65f0-129">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e65f0-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e65f0-130">Remarks</span></span>

<span data-ttu-id="e65f0-131">Если выходные данные анимации уже зарегистрированы, Пматрикс будет заполнен данными преобразования входных данных.</span><span class="sxs-lookup"><span data-stu-id="e65f0-131">If the animation output is already registered, pMatrix will be filled with the input transformation data.</span></span>

<span data-ttu-id="e65f0-132">Наборы анимации, созданные с помощью [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) , автоматически регистрируют все загруженные наборы анимации.</span><span class="sxs-lookup"><span data-stu-id="e65f0-132">Animation sets created with [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) automatically register all loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="e65f0-133">Требования</span><span class="sxs-lookup"><span data-stu-id="e65f0-133">Requirements</span></span>



| <span data-ttu-id="e65f0-134">Требование</span><span class="sxs-lookup"><span data-stu-id="e65f0-134">Requirement</span></span> | <span data-ttu-id="e65f0-135">Значение</span><span class="sxs-lookup"><span data-stu-id="e65f0-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e65f0-136">Header</span><span class="sxs-lookup"><span data-stu-id="e65f0-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e65f0-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e65f0-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e65f0-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e65f0-138">Library</span></span><br/> | <dl> <span data-ttu-id="e65f0-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e65f0-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e65f0-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e65f0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e65f0-141">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="e65f0-141">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
