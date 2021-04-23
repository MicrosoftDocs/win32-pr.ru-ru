---
title: Метод ID3DX11ThreadPump Процессдевицеворкитемс (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Задает рабочие элементы для устройства после завершения загрузки и обработки.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Метод Процессдевицеворкитемс Direct3D 11
- Метод Процессдевицеворкитемс Direct3D 11, интерфейс ID3DX11ThreadPump
- Интерфейс ID3DX11ThreadPump Direct3D 11, метод Процессдевицеворкитемс
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986900"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="d64ed-107">ID3DX11ThreadPump: метод:P Роцессдевицеворкитемс</span><span class="sxs-lookup"><span data-stu-id="d64ed-107">ID3DX11ThreadPump::ProcessDeviceWorkItems method</span></span>

> [!Note]  
> <span data-ttu-id="d64ed-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="d64ed-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="d64ed-109">Задает рабочие элементы для устройства после завершения загрузки и обработки.</span><span class="sxs-lookup"><span data-stu-id="d64ed-109">Sets work items to the device after they have finished loading and processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="d64ed-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d64ed-110">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="d64ed-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d64ed-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d64ed-112">*иворкитемкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d64ed-112">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d64ed-113">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d64ed-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d64ed-114">Число рабочих элементов, которое будет задано для устройства.</span><span class="sxs-lookup"><span data-stu-id="d64ed-114">The number of work items to set to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d64ed-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d64ed-115">Return value</span></span>

<span data-ttu-id="d64ed-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d64ed-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d64ed-117">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d64ed-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d64ed-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="d64ed-118">Remarks</span></span>

<span data-ttu-id="d64ed-119">Когда конвейер потока закончит загрузку и обработку ресурса или шейдера, он будет хранить его в очереди до вызова этого API, после чего обработанные элементы будут установлены на устройство.</span><span class="sxs-lookup"><span data-stu-id="d64ed-119">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="d64ed-120">Это полезно для управления объемом обработки, который тратится на привязку ресурсов к устройству для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="d64ed-120">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span>

<span data-ttu-id="d64ed-121">В качестве примера того, как один из них может использовать этот API, скажем, вы приближаетесь к концу одного уровня в игре и хотите начать предварительную загрузку текстур, шейдеров и других ресурсов для следующего уровня.</span><span class="sxs-lookup"><span data-stu-id="d64ed-121">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="d64ed-122">Конвейер потока начнет загрузку, распаковку и обработку ресурсов и шейдеров в отдельном потоке, пока они не будут готовы к установке устройству, и в этом случае они покидают их в очереди.</span><span class="sxs-lookup"><span data-stu-id="d64ed-122">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="d64ed-123">Один из них может не захотеть одновременно устанавливать все ресурсы и шейдеры, так как это может привести к заметному временному снижению производительности игры.</span><span class="sxs-lookup"><span data-stu-id="d64ed-123">One may not want to set all the resources and shaders to the device at once because this may cause a noticeable temporary slow down in the game's performance.</span></span> <span data-ttu-id="d64ed-124">Таким образом, этот API может вызываться один раз для каждого кадра, чтобы в каждом кадре было установлено только небольшое число рабочих элементов, таким образом распределяя рабочую нагрузку привязок ресурсов на устройство в нескольких кадрах.</span><span class="sxs-lookup"><span data-stu-id="d64ed-124">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="d64ed-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d64ed-125">Requirements</span></span>



| <span data-ttu-id="d64ed-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d64ed-126">Requirement</span></span> | <span data-ttu-id="d64ed-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d64ed-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d64ed-128">Header</span><span class="sxs-lookup"><span data-stu-id="d64ed-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d64ed-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d64ed-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="d64ed-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d64ed-130">Library</span></span><br/> | <dl> <span data-ttu-id="d64ed-131"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d64ed-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d64ed-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d64ed-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d64ed-133">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="d64ed-133">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="d64ed-134">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="d64ed-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

