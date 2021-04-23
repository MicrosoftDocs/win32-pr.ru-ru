---
description: Завершает активный метод.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'Метод ID3DXEffect:: end (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355013"
---
# <a name="id3dxeffectend-method"></a><span data-ttu-id="e7615-103">Метод ID3DXEffect:: end</span><span class="sxs-lookup"><span data-stu-id="e7615-103">ID3DXEffect::End method</span></span>

<span data-ttu-id="e7615-104">Завершает активный метод.</span><span class="sxs-lookup"><span data-stu-id="e7615-104">Ends an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7615-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7615-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="e7615-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7615-106">Parameters</span></span>

<span data-ttu-id="e7615-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e7615-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7615-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7615-108">Return value</span></span>

<span data-ttu-id="e7615-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7615-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7615-110">Этот метод всегда возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e7615-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7615-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7615-111">Remarks</span></span>

<span data-ttu-id="e7615-112">Все отрисовки в результате выполняются в соответствующей паре вызовов [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) и **ID3DXEffect:: end** .</span><span class="sxs-lookup"><span data-stu-id="e7615-112">All rendering in an effect is done within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and **ID3DXEffect::End** calls.</span></span> <span data-ttu-id="e7615-113">После отрисовки всех проходов необходимо вызвать **ID3DXEffect:: end** , чтобы завершить активный метод.</span><span class="sxs-lookup"><span data-stu-id="e7615-113">After all passes are rendered, **ID3DXEffect::End** must be called to end the active technique.</span></span> <span data-ttu-id="e7615-114">Система эффектов отвечает с помощью блока State, созданного при вызове **ID3DXEffect:: Begin** , для автоматического восстановления состояния конвейера перед **ID3DXEffect:: Begin**.</span><span class="sxs-lookup"><span data-stu-id="e7615-114">The effect system responds by using the state block created when **ID3DXEffect::Begin** was called, to automatically restore the pipeline state before **ID3DXEffect::Begin**.</span></span>

<span data-ttu-id="e7615-115">По умолчанию система эффектов осуществляет сохранение состояния перед приемом и восстановление состояния после приемки.</span><span class="sxs-lookup"><span data-stu-id="e7615-115">By default, the effect system takes care of saving state prior to a technique, and restoring state after a technique.</span></span> <span data-ttu-id="e7615-116">Если вы решили отключить эту функцию сохранения и восстановления, см. раздел [D3DXFX \_ донотсавесамплерстате](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="e7615-116">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7615-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e7615-117">Requirements</span></span>



| <span data-ttu-id="e7615-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e7615-118">Requirement</span></span> | <span data-ttu-id="e7615-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e7615-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7615-120">Header</span><span class="sxs-lookup"><span data-stu-id="e7615-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e7615-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7615-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e7615-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e7615-122">Library</span></span><br/> | <dl> <span data-ttu-id="e7615-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7615-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e7615-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7615-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7615-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="e7615-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




