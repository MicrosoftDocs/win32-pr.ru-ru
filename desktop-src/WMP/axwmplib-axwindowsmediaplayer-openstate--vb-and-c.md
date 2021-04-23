---
title: Аксвиндовсмедиаплайер. Опенстате, свойство
description: Свойство Опенстате возвращает значение перечисления, указывающее состояние источника содержимого.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- Проигрыватель Windows Media для свойства Опенстате
- Опенстате свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Опенстате
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694728"
---
# <a name="axwindowsmediaplayeropenstate-property"></a><span data-ttu-id="7b56d-106">Аксвиндовсмедиаплайер. Опенстате, свойство</span><span class="sxs-lookup"><span data-stu-id="7b56d-106">AxWindowsMediaPlayer.openState property</span></span>

<span data-ttu-id="7b56d-107">Свойство Опенстате возвращает значение перечисления, указывающее состояние источника содержимого.</span><span class="sxs-lookup"><span data-stu-id="7b56d-107">The openState property gets an enumeration value indicating the state of the content source.</span></span>

<span data-ttu-id="7b56d-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7b56d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b56d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b56d-109">Syntax</span></span>


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a><span data-ttu-id="7b56d-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7b56d-110">Property value</span></span>

<span data-ttu-id="7b56d-111">Значение перечисления Вмплиб. Вмпопенстате.</span><span class="sxs-lookup"><span data-stu-id="7b56d-111">The WMPLib.WMPOpenState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b56d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b56d-112">Remarks</span></span>

<span data-ttu-id="7b56d-113">Состояния проигрывателя Windows Media не гарантированно выполняются в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="7b56d-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="7b56d-114">Кроме того, не все состояния должны происходить во время последовательности событий.</span><span class="sxs-lookup"><span data-stu-id="7b56d-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="7b56d-115">Не следует писать код, зависящий от порядка состояний.</span><span class="sxs-lookup"><span data-stu-id="7b56d-115">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b56d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7b56d-116">Requirements</span></span>



| <span data-ttu-id="7b56d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7b56d-117">Requirement</span></span> | <span data-ttu-id="7b56d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7b56d-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b56d-119">Версия</span><span class="sxs-lookup"><span data-stu-id="7b56d-119">Version</span></span><br/>   | <span data-ttu-id="7b56d-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7b56d-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7b56d-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7b56d-121">Namespace</span></span><br/> | <span data-ttu-id="7b56d-122">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="7b56d-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7b56d-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="7b56d-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7b56d-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7b56d-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b56d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b56d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b56d-126">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7b56d-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7b56d-127">**Аксвиндовсмедиаплайер. Опенстатечанже, событие**</span><span class="sxs-lookup"><span data-stu-id="7b56d-127">**AxWindowsMediaPlayer.OpenStateChange Event**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="7b56d-128">**Вмплиб. Вмпопенстате**</span><span class="sxs-lookup"><span data-stu-id="7b56d-128">**WMPLib.WMPOpenState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





