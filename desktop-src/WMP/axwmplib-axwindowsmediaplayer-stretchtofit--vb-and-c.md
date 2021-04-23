---
title: Аксвиндовсмедиаплайер. Стретчтофит, свойство
description: Свойство Стретчтофит получает или задает значение, указывающее, будет ли видео, отображаемое элементом управления проигрывателя Windows Media, автоматически соответствовать размеру окна видео, если видеоокно больше размеров изображения видео.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- Проигрыватель Windows Media для свойства Стретчтофит
- Стретчтофит свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Стретчтофит
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698818"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a><span data-ttu-id="3dd7e-106">Аксвиндовсмедиаплайер. Стретчтофит, свойство</span><span class="sxs-lookup"><span data-stu-id="3dd7e-106">AxWindowsMediaPlayer.stretchToFit property</span></span>

<span data-ttu-id="3dd7e-107">Свойство Стретчтофит получает или задает значение, указывающее, будет ли видео, отображаемое элементом управления проигрывателя Windows Media, автоматически соответствовать размеру окна видео, если видеоокно больше размеров изображения видео.</span><span class="sxs-lookup"><span data-stu-id="3dd7e-107">The stretchToFit property gets or sets a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd7e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dd7e-108">Syntax</span></span>


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="3dd7e-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3dd7e-109">Property value</span></span>

<span data-ttu-id="3dd7e-110">Значение System. Boolean, указывающее, будет ли видео растягиваться в соответствии с размерами окна.</span><span class="sxs-lookup"><span data-stu-id="3dd7e-110">The System.Boolean value that indicates whether the video will stretch to fit the window.</span></span> <span data-ttu-id="3dd7e-111">Значением по умолчанию является false.</span><span class="sxs-lookup"><span data-stu-id="3dd7e-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd7e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3dd7e-112">Remarks</span></span>

<span data-ttu-id="3dd7e-113">Если **стретчтофит** имеет значение true, элемент управления проигрывателя Windows Media сохраняет исходные пропорции видео.</span><span class="sxs-lookup"><span data-stu-id="3dd7e-113">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="3dd7e-114">Если пропорции видео не соответствуют пропорциям видеоокна, то области с черной маской могут отображаться в верхней и нижней, левой и правой частях изображения видео.</span><span class="sxs-lookup"><span data-stu-id="3dd7e-114">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="3dd7e-115">Это свойство применяется к элементу управления проигрывателя Windows Media только при его внедрении в веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="3dd7e-115">This property applies to the Windows Media Player control only when it is embedded in a webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd7e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3dd7e-116">Requirements</span></span>



| <span data-ttu-id="3dd7e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3dd7e-117">Requirement</span></span> | <span data-ttu-id="3dd7e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3dd7e-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd7e-119">Версия</span><span class="sxs-lookup"><span data-stu-id="3dd7e-119">Version</span></span><br/>   | <span data-ttu-id="3dd7e-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3dd7e-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="3dd7e-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3dd7e-121">Namespace</span></span><br/> | <span data-ttu-id="3dd7e-122">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="3dd7e-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3dd7e-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="3dd7e-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3dd7e-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3dd7e-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd7e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dd7e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd7e-126">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3dd7e-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





