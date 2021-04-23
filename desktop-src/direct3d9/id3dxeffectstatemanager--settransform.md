---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки преобразования.
ms.assetid: 5d886554-ddb6-4b8a-a7fd-453e94b9516f
title: 'Метод ID3DXEffectStateManager:: Сеттрансформ (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTransform
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b19a060cfeb09d5d1a92e5e7a1a1f25b58e64f4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000424"
---
# <a name="id3dxeffectstatemanagersettransform-method"></a><span data-ttu-id="d18bc-103">Метод ID3DXEffectStateManager:: Сеттрансформ</span><span class="sxs-lookup"><span data-stu-id="d18bc-103">ID3DXEffectStateManager::SetTransform method</span></span>

<span data-ttu-id="d18bc-104">Функция обратного вызова, которая должна быть реализована пользователем для установки преобразования.</span><span class="sxs-lookup"><span data-stu-id="d18bc-104">A callback function that must be implemented by a user to set a transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="d18bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d18bc-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in]       D3DTRANSFORMSTATETYPE State,
  [in] const D3DMATRIX             *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="d18bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d18bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d18bc-107">*Состояние* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d18bc-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d18bc-108">Тип: **[ **D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="d18bc-108">Type: **[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span></span>

<span data-ttu-id="d18bc-109">Тип преобразования, к которому применяется матрица.</span><span class="sxs-lookup"><span data-stu-id="d18bc-109">The type of transform to apply the matrix to.</span></span> <span data-ttu-id="d18bc-110">См. [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="d18bc-110">See [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="d18bc-111">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d18bc-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d18bc-112">Тип: **const [**D3DMATRIX**](d3dmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d18bc-112">Type: **const [**D3DMATRIX**](d3dmatrix.md)\***</span></span>

<span data-ttu-id="d18bc-113">Матрица преобразования.</span><span class="sxs-lookup"><span data-stu-id="d18bc-113">A transformation matrix.</span></span> <span data-ttu-id="d18bc-114">См. [**D3DMATRIX**](d3dmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="d18bc-114">See [**D3DMATRIX**](d3dmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d18bc-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d18bc-115">Return value</span></span>

<span data-ttu-id="d18bc-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d18bc-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d18bc-117">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d18bc-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="d18bc-118">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="d18bc-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="d18bc-119">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="d18bc-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="d18bc-120">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сеттрансформ**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d18bc-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="d18bc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d18bc-121">Requirements</span></span>



| <span data-ttu-id="d18bc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d18bc-122">Requirement</span></span> | <span data-ttu-id="d18bc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d18bc-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d18bc-124">Header</span><span class="sxs-lookup"><span data-stu-id="d18bc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d18bc-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d18bc-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d18bc-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d18bc-126">Library</span></span><br/> | <dl> <span data-ttu-id="d18bc-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d18bc-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d18bc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d18bc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18bc-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="d18bc-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
