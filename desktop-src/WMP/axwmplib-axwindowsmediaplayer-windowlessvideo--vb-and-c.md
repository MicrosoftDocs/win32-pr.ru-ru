---
title: Аксвиндовсмедиаплайер. Виндовлессвидео, свойство
description: Свойство Виндовлессвидео получает или задает значение, указывающее, визуализирует ли элемент управления проигрывателем Windows Media видео в режиме без окон.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- Проигрыватель Windows Media для свойства Виндовлессвидео
- Виндовлессвидео свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Виндовлессвидео
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699254"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a><span data-ttu-id="1ad81-106">Аксвиндовсмедиаплайер. Виндовлессвидео, свойство</span><span class="sxs-lookup"><span data-stu-id="1ad81-106">AxWindowsMediaPlayer.windowlessVideo property</span></span>

<span data-ttu-id="1ad81-107">Свойство Виндовлессвидео получает или задает значение, указывающее, визуализирует ли элемент управления проигрывателем Windows Media видео в режиме без окон.</span><span class="sxs-lookup"><span data-stu-id="1ad81-107">The windowlessVideo property gets or sets a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad81-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ad81-108">Syntax</span></span>


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="1ad81-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1ad81-109">Property value</span></span>

<span data-ttu-id="1ad81-110">Значение System. Boolean, указывающее, визуализирует ли элемент управления проигрывателем Windows Media видео в режиме без окон.</span><span class="sxs-lookup"><span data-stu-id="1ad81-110">A System.Boolean value indicating whether the Windows Media Player control renders video in windowless mode.</span></span> <span data-ttu-id="1ad81-111">Значением по умолчанию является false.</span><span class="sxs-lookup"><span data-stu-id="1ad81-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad81-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ad81-112">Remarks</span></span>

<span data-ttu-id="1ad81-113">По умолчанию встроенный элемент управления проигрывателя Windows Media визуализирует видео в отдельном окне в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="1ad81-113">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="1ad81-114">Если для **виндовлессвидео** задано значение true, объект проигрывателя Windows Media визуализирует видео непосредственно в клиентской области, поэтому можно применять специальные эффекты или распространять видео с текстом.</span><span class="sxs-lookup"><span data-stu-id="1ad81-114">When **windowlessVideo** is set to true, the Windows Media Player object renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="1ad81-115">В Windows Vista отрисовка видео в режиме без окон может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="1ad81-115">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="1ad81-116">Получение значения для этого свойства не поддерживается для Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="1ad81-116">Getting a value for this property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="1ad81-117">Установка значения этого свойства в Netscape Navigator может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="1ad81-117">Setting a value for this property in Netscape Navigator may yield unexpected results.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ad81-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1ad81-118">Requirements</span></span>



| <span data-ttu-id="1ad81-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1ad81-119">Requirement</span></span> | <span data-ttu-id="1ad81-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1ad81-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad81-121">Версия</span><span class="sxs-lookup"><span data-stu-id="1ad81-121">Version</span></span><br/>   | <span data-ttu-id="1ad81-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1ad81-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="1ad81-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1ad81-123">Namespace</span></span><br/> | <span data-ttu-id="1ad81-124">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="1ad81-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="1ad81-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="1ad81-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1ad81-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1ad81-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ad81-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ad81-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad81-128">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="1ad81-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





