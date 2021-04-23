---
description: Задание рабочих элементов для устройства после завершения загрузки и обработки.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: 'ID3DX10ThreadPump: метод:P Роцессдевицеворкитемс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157262"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="822b9-103">ID3DX10ThreadPump: метод:P Роцессдевицеворкитемс</span><span class="sxs-lookup"><span data-stu-id="822b9-103">ID3DX10ThreadPump::ProcessDeviceWorkItems method</span></span>

<span data-ttu-id="822b9-104">Задание рабочих элементов для устройства после завершения загрузки и обработки.</span><span class="sxs-lookup"><span data-stu-id="822b9-104">Set work items to the device after they have finished loading and processing.</span></span> <span data-ttu-id="822b9-105">Когда конвейер потока закончит загрузку и обработку ресурса или шейдера, он будет хранить его в очереди до вызова этого API, после чего обработанные элементы будут установлены на устройство.</span><span class="sxs-lookup"><span data-stu-id="822b9-105">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="822b9-106">Это полезно для управления объемом обработки, который тратится на привязку ресурсов к устройству для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="822b9-106">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span> <span data-ttu-id="822b9-107">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="822b9-107">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="822b9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="822b9-108">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="822b9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="822b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="822b9-110">*иворкитемкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="822b9-110">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="822b9-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="822b9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="822b9-112">Число рабочих элементов, которое будет задано для устройства.</span><span class="sxs-lookup"><span data-stu-id="822b9-112">The number of work items to set to the device.</span></span> <span data-ttu-id="822b9-113">Процессдевицеобжекткреатион создаст не более Иворкитемкаунт объектов.</span><span class="sxs-lookup"><span data-stu-id="822b9-113">ProcessDeviceObjectCreation will create at most iWorkItemCount objects.</span></span> <span data-ttu-id="822b9-114">Если в очереди недостаточно рабочих элементов для обработки объектов Иворкитемкаунт, Процессдевицеобжекткреатион создаст столько объектов устройств, сколько есть элементов в очереди.</span><span class="sxs-lookup"><span data-stu-id="822b9-114">If there are not enough work items in the queue to process iWorkItemCount objects, ProcessDeviceObjectCreation will create as many device objects as there are items in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="822b9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="822b9-115">Return value</span></span>

<span data-ttu-id="822b9-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="822b9-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="822b9-117">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="822b9-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="822b9-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="822b9-118">Remarks</span></span>

<span data-ttu-id="822b9-119">В качестве примера того, как один из них может использовать этот API, скажем, вы приближаетесь к концу одного уровня в игре и хотите начать предварительную загрузку текстур, шейдеров и других ресурсов для следующего уровня.</span><span class="sxs-lookup"><span data-stu-id="822b9-119">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="822b9-120">Конвейер потока начнет загрузку, распаковку и обработку ресурсов и шейдеров в отдельном потоке, пока они не будут готовы к установке устройству, и в этом случае они покидают их в очереди.</span><span class="sxs-lookup"><span data-stu-id="822b9-120">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="822b9-121">Один из них может не захотеть одновременно устанавливать все ресурсы и шейдеры, так как это может привести к снижению производительности игры.</span><span class="sxs-lookup"><span data-stu-id="822b9-121">One may not want to set all the resources and shaders to the device at once because this may cause a noticable temporary slow down in the game's performance.</span></span> <span data-ttu-id="822b9-122">Таким образом, этот API может вызываться один раз для каждого кадра, чтобы в каждом кадре было установлено только небольшое число рабочих элементов, что позволяет распределять рабочую нагрузку привязок ресурсов на устройство в нескольких кадрах и свести к минимуму вероятность снижения вероятности потери данных в игре.</span><span class="sxs-lookup"><span data-stu-id="822b9-122">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames and minimizing the possibility of a noticable slow down in the game's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="822b9-123">Требования</span><span class="sxs-lookup"><span data-stu-id="822b9-123">Requirements</span></span>



| <span data-ttu-id="822b9-124">Требование</span><span class="sxs-lookup"><span data-stu-id="822b9-124">Requirement</span></span> | <span data-ttu-id="822b9-125">Значение</span><span class="sxs-lookup"><span data-stu-id="822b9-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="822b9-126">Header</span><span class="sxs-lookup"><span data-stu-id="822b9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="822b9-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="822b9-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="822b9-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="822b9-128">Library</span></span><br/> | <dl> <span data-ttu-id="822b9-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="822b9-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="822b9-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="822b9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="822b9-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="822b9-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="822b9-132">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="822b9-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
