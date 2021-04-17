---
title: Метод шага IWMPControls2
description: Метод Step заставляет текущий элемент мультимедиа перейти к следующему кадру или предыдущему кадру и заморозить воспроизведение.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- Пошаговый метод проигрывателя Windows Media
- Пошаговый метод проигрывателя Windows Media Player, интерфейс IWMPControls2
- Интерфейс IWMPControls2 Windows Media Player, метод Step
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689293"
---
# <a name="iwmpcontrols2step-method"></a><span data-ttu-id="4ae55-106">Метод IWMPControls2:: Step</span><span class="sxs-lookup"><span data-stu-id="4ae55-106">IWMPControls2::step method</span></span>

<span data-ttu-id="4ae55-107">Метод **Step** заставляет текущий элемент мультимедиа перейти к следующему кадру или предыдущему кадру и заморозить воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="4ae55-107">The **step** method causes the current video media item to step to the next frame or the previous frame and freeze playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae55-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ae55-108">Syntax</span></span>


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a><span data-ttu-id="4ae55-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ae55-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ae55-110">*лстеп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ae55-110">*lStep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae55-111">Значение **System. Int32** , указывающее, сколько кадров необходимо выполнить перед замораживанием.</span><span class="sxs-lookup"><span data-stu-id="4ae55-111">A **System.Int32** value indicating how many frames to step before freezing.</span></span> <span data-ttu-id="4ae55-112">Необходимо задать значение 1 или-1.</span><span class="sxs-lookup"><span data-stu-id="4ae55-112">Must be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ae55-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ae55-113">Return value</span></span>

<span data-ttu-id="4ae55-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4ae55-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ae55-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ae55-115">Remarks</span></span>

<span data-ttu-id="4ae55-116">В настоящее время этот метод поддерживает только параметры 1 или-1, поэтому можно пошаговым образом выполнять только один кадр.</span><span class="sxs-lookup"><span data-stu-id="4ae55-116">This method currently supports only the parameters 1 or -1, so you can only step one frame at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae55-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4ae55-117">Requirements</span></span>



| <span data-ttu-id="4ae55-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4ae55-118">Requirement</span></span> | <span data-ttu-id="4ae55-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4ae55-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae55-120">Версия</span><span class="sxs-lookup"><span data-stu-id="4ae55-120">Version</span></span><br/>   | <span data-ttu-id="4ae55-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4ae55-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4ae55-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4ae55-122">Namespace</span></span><br/> | <span data-ttu-id="4ae55-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="4ae55-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4ae55-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="4ae55-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4ae55-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4ae55-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ae55-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ae55-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae55-127">**Интерфейс IWMPControls2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4ae55-127">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ae55-128">**Интерфейс ИВМПДВД (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4ae55-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





