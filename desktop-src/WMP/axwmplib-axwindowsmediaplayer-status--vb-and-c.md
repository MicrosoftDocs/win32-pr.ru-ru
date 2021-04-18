---
title: Аксвиндовсмедиаплайер. status, свойство
description: Свойство Status получает значение, указывающее состояние проигрывателя Windows Media.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- Свойство Status проигрыватель Windows Media
- Свойство Status проигрыватель Windows Media, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Status
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695039"
---
# <a name="axwindowsmediaplayerstatus-property"></a><span data-ttu-id="924c4-106">Аксвиндовсмедиаплайер. status, свойство</span><span class="sxs-lookup"><span data-stu-id="924c4-106">AxWindowsMediaPlayer.status property</span></span>

<span data-ttu-id="924c4-107">Свойство Status получает значение, указывающее состояние проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="924c4-107">The status property gets a value indicating the status of Windows Media Player.</span></span>

<span data-ttu-id="924c4-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="924c4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="924c4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="924c4-109">Syntax</span></span>


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a><span data-ttu-id="924c4-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="924c4-110">Property value</span></span>

<span data-ttu-id="924c4-111">Строка System. String, которая является состоянием.</span><span class="sxs-lookup"><span data-stu-id="924c4-111">The System.String that is the status.</span></span>

## <a name="remarks"></a><span data-ttu-id="924c4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="924c4-112">Remarks</span></span>

<span data-ttu-id="924c4-113">Значения, содержащиеся в этом свойстве, могут быть изменены в любое время, и их следует использовать только в целях вывода.</span><span class="sxs-lookup"><span data-stu-id="924c4-113">The values contained in this property are subject to change at any time, and should be used for display purposes only.</span></span>

<span data-ttu-id="924c4-114">Аксвиндовсмедиаплайер. Событие **StatusChange** срабатывает при каждом изменении значения свойства.</span><span class="sxs-lookup"><span data-stu-id="924c4-114">The AxWindowsMediaPlayer.**StatusChange** event is fired whenever this property changes value.</span></span>

## <a name="requirements"></a><span data-ttu-id="924c4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="924c4-115">Requirements</span></span>



| <span data-ttu-id="924c4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="924c4-116">Requirement</span></span> | <span data-ttu-id="924c4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="924c4-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="924c4-118">Версия</span><span class="sxs-lookup"><span data-stu-id="924c4-118">Version</span></span><br/>   | <span data-ttu-id="924c4-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="924c4-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="924c4-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="924c4-120">Namespace</span></span><br/> | <span data-ttu-id="924c4-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="924c4-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="924c4-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="924c4-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="924c4-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="924c4-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="924c4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="924c4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="924c4-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="924c4-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="924c4-126">**Событие Аксвиндовсмедиаплайер. StatusChange (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="924c4-126">**AxWindowsMediaPlayer.StatusChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





