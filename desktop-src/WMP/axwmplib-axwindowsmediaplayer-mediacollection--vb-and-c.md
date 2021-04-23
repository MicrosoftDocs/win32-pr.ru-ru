---
title: Аксвиндовсмедиаплайер. Медиаколлектион, свойство
description: Свойство Медиаколлектион получает интерфейс Ивмпмедиаколлектион, который предоставляет способ организации большой коллекции элементов мультимедиа.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- Проигрыватель Windows Media для свойства Медиаколлектион
- Медиаколлектион свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Медиаколлектион
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6501dd5dda8e60b8ba1a5f2667f6b581cbdfd90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699018"
---
# <a name="axwindowsmediaplayermediacollection-property"></a><span data-ttu-id="9b49d-106">Аксвиндовсмедиаплайер. Медиаколлектион, свойство</span><span class="sxs-lookup"><span data-stu-id="9b49d-106">AxWindowsMediaPlayer.mediaCollection property</span></span>

<span data-ttu-id="9b49d-107">Свойство Медиаколлектион получает интерфейс **ивмпмедиаколлектион** , который предоставляет способ организации большой коллекции элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9b49d-107">The mediaCollection property gets an **IWMPMediaCollection** interface that provides a way to organize a large collection of media items.</span></span>

<span data-ttu-id="9b49d-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9b49d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b49d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b49d-109">Syntax</span></span>


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a><span data-ttu-id="9b49d-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9b49d-110">Property value</span></span>

<span data-ttu-id="9b49d-111">Интерфейс Вмплиб. Ивмпмедиаколлектион к коллекции элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9b49d-111">The WMPLib.IWMPMediaCollection interface to a collection of media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b49d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b49d-112">Remarks</span></span>

<span data-ttu-id="9b49d-113">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="9b49d-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="9b49d-114">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9b49d-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b49d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9b49d-115">Requirements</span></span>



| <span data-ttu-id="9b49d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9b49d-116">Requirement</span></span> | <span data-ttu-id="9b49d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9b49d-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b49d-118">Версия</span><span class="sxs-lookup"><span data-stu-id="9b49d-118">Version</span></span><br/>   | <span data-ttu-id="9b49d-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9b49d-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="9b49d-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9b49d-120">Namespace</span></span><br/> | <span data-ttu-id="9b49d-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="9b49d-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9b49d-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="9b49d-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9b49d-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9b49d-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b49d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b49d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b49d-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9b49d-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b49d-126">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9b49d-126">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b49d-127">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9b49d-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b49d-128">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9b49d-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





