---
title: IManipulationProcessor Минимумскалеротатерадиус, свойство
description: Указывает, насколько велика дистанция контактов на жесте масштабирования или вращения для запуска манипуляций.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- Сенсорный ввод окон свойств Минимумскалеротатерадиус
- Минимумскалеротатерадиус свойств Windows Touch, интерфейс IManipulationProcessor
- IManipulationProcessor интерфейса Windows, свойство Минимумскалеротатерадиус
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784155"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a><span data-ttu-id="3a4e0-106">Свойство IManipulationProcessor:: Минимумскалеротатерадиус</span><span class="sxs-lookup"><span data-stu-id="3a4e0-106">IManipulationProcessor::MinimumScaleRotateRadius property</span></span>

<span data-ttu-id="3a4e0-107">Указывает, насколько велика дистанция контактов на жесте масштабирования или вращения для запуска манипуляций.</span><span class="sxs-lookup"><span data-stu-id="3a4e0-107">Specifies how large the distance contacts on a scale or rotate gesture need to be to trigger manipulation.</span></span>

<span data-ttu-id="3a4e0-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3a4e0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a4e0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a4e0-109">Syntax</span></span>


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a><span data-ttu-id="3a4e0-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3a4e0-110">Property value</span></span>

<span data-ttu-id="3a4e0-111">Указывает минимальное расстояние между контактами для триггеров масштабирования или вращения.</span><span class="sxs-lookup"><span data-stu-id="3a4e0-111">Specifies the minimum distance between contacts to trigger scale or rotate gestures.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3a4e0-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3a4e0-112">Error codes</span></span>

## <a name="remarks"></a><span data-ttu-id="3a4e0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a4e0-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3a4e0-114">Это свойство задается в центипикселс (100ths пикселей).</span><span class="sxs-lookup"><span data-stu-id="3a4e0-114">This property is set in centipixels (100ths of a pixel).</span></span>

 

<span data-ttu-id="3a4e0-115">При задании этого значения процессор манипуляции будет игнорировать жесты, которые имеют слишком маленький радиус.</span><span class="sxs-lookup"><span data-stu-id="3a4e0-115">Setting this value will make the manipulation processor ignore gestures that have too small of a radius.</span></span> <span data-ttu-id="3a4e0-116">Это полезно, если вы хотите запретить пользователю манипулировать объектом слишком маленьким радиусом.</span><span class="sxs-lookup"><span data-stu-id="3a4e0-116">This is useful if you want to prevent a user from manipulating an object to too small of a radius.</span></span> <span data-ttu-id="3a4e0-117">Например, если вы используете процессор манипуляции с кругом и хотите обеспечить поддержку радиуса, превышающего 100 пикселей, это значение можно задать равным 10000.</span><span class="sxs-lookup"><span data-stu-id="3a4e0-117">For example, if you are using a manipulation processor with a circle and want the ensure that it maintains a radius greater than 100 pixels, you would set this value to 10000.</span></span>

## <a name="examples"></a><span data-ttu-id="3a4e0-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="3a4e0-118">Examples</span></span>


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a><span data-ttu-id="3a4e0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a4e0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4e0-120">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="3a4e0-120">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




