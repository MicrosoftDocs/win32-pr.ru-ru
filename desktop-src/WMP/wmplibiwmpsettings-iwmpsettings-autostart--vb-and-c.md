---
title: Свойство автозапуска Ивмпсеттингс
description: Свойство автозапуска получает или задает значение, указывающее, начинается ли воспроизведение текущего элемента мультимедиа автоматически.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- свойство "Автозапуск" проигрывателя Windows Media
- свойство "Автозапуск" проигрывателя Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, свойство "Автозапуск"
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718030"
---
# <a name="iwmpsettingsautostart-property"></a><span data-ttu-id="dee85-106">Свойство Ивмпсеттингс:: Автозапуск</span><span class="sxs-lookup"><span data-stu-id="dee85-106">IWMPSettings::autoStart property</span></span>

<span data-ttu-id="dee85-107">Свойство **автозапуска** получает или задает значение, указывающее, начинается ли воспроизведение текущего элемента мультимедиа автоматически.</span><span class="sxs-lookup"><span data-stu-id="dee85-107">The **autoStart** property gets or sets a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee85-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dee85-108">Syntax</span></span>


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="dee85-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dee85-109">Property value</span></span>

<span data-ttu-id="dee85-110">Значение **System. Boolean** , указывающее, начинается ли воспроизведение текущего элемента мультимедиа автоматически.</span><span class="sxs-lookup"><span data-stu-id="dee85-110">A **System.Boolean** value that indicates whether the current media item begins playing automatically.</span></span> <span data-ttu-id="dee85-111">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="dee85-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dee85-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dee85-112">Remarks</span></span>

<span data-ttu-id="dee85-113">Если параметру **автозапуска** присвоено значение **true**, воспроизведение элемента мультимедиа начнется при установке **аксвиндовсмедиаплайер. URL**, **аксвиндовсмедиаплайер. куррентплайлист** или **аксвиндовсмедиаплайер. currentMedia** .</span><span class="sxs-lookup"><span data-stu-id="dee85-113">If **autoStart** is set to **true**, the media item will begin playing when **AxWindowsMediaPlayer.URL**, **AxWindowsMediaPlayer.currentPlaylist**, or **AxWindowsMediaPlayer.currentMedia** is set.</span></span> <span data-ttu-id="dee85-114">В противном случае воспроизведение элемента мультимедиа не начнется до тех пор, пока не будет вызван метод **ивмпконтролс. Play** .</span><span class="sxs-lookup"><span data-stu-id="dee85-114">Otherwise, the media item will not start playing until the **IWMPControls.play** method is called.</span></span>

<span data-ttu-id="dee85-115">Если не задать для параметра **Автозапуск** значение **true** непосредственно перед указанием элемента мультимедиа, не следует полагаться на этот параметр в качестве замены с помощью метода **ивмпконтролс. Play** .</span><span class="sxs-lookup"><span data-stu-id="dee85-115">Unless you set **autoStart** to **true** immediately before specifying a media item, you should not rely on this setting as a substitute for using the **IWMPControls.play** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee85-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dee85-116">Requirements</span></span>



| <span data-ttu-id="dee85-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dee85-117">Requirement</span></span> | <span data-ttu-id="dee85-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dee85-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee85-119">Версия</span><span class="sxs-lookup"><span data-stu-id="dee85-119">Version</span></span><br/>   | <span data-ttu-id="dee85-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="dee85-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dee85-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dee85-121">Namespace</span></span><br/> | <span data-ttu-id="dee85-122">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="dee85-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dee85-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="dee85-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dee85-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dee85-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dee85-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dee85-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee85-126">**Аксвиндовсмедиаплайер. Куррентмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dee85-126">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dee85-127">**Аксвиндовсмедиаплайер. Куррентплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dee85-127">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dee85-128">**Аксвиндовсмедиаплайер. URL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dee85-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dee85-129">**Ивмпконтролс. Play (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dee85-129">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dee85-130">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dee85-130">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





