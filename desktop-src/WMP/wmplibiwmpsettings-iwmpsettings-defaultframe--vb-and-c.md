---
title: Ивмпсеттингс Дефаултфраме, свойство
description: Свойство Дефаултфраме Возвращает или задает имя кадра, используемого для вывода URL-адреса, полученного в \_ \_ событии аксвиндовсмедиаплайер вмпокксевентс скрипткоммандевент.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- Проигрыватель Windows Media для свойства Дефаултфраме
- Дефаултфраме свойство проигрывателя Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, свойство Дефаултфраме
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717848"
---
# <a name="iwmpsettingsdefaultframe-property"></a><span data-ttu-id="9e868-106">Ивмпсеттингс: свойство Ефаултфраме:d</span><span class="sxs-lookup"><span data-stu-id="9e868-106">IWMPSettings::defaultFrame property</span></span>

<span data-ttu-id="9e868-107">Свойство **дефаултфраме** Возвращает или задает имя кадра, используемого для вывода URL-адреса, полученного в событии **аксвиндовсмедиаплайер \_ вмпокксевентс \_ скрипткоммандевент** .</span><span class="sxs-lookup"><span data-stu-id="9e868-107">The **defaultFrame** property gets or sets the name of the frame used to display a URL that is received in an **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e868-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e868-108">Syntax</span></span>


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a><span data-ttu-id="9e868-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9e868-109">Property value</span></span>

<span data-ttu-id="9e868-110">**Строка System. String** , которая является значением атрибута Name целевого элемента **Frame** .</span><span class="sxs-lookup"><span data-stu-id="9e868-110">A **System.String** that is the value of the name attribute of the target **FRAME** element.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e868-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e868-111">Remarks</span></span>

<span data-ttu-id="9e868-112">Если целевой кадр указан в самом событии **\_ вмпокксевентс \_ скрипткоммандевент** , это свойство игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9e868-112">If a target frame is specified in the **\_WMPOCXEvents\_ScriptCommandEvent** event itself, this property is ignored.</span></span>

<span data-ttu-id="9e868-113">Это свойство игнорируется при использовании приложения Netscape Navigator Java.</span><span class="sxs-lookup"><span data-stu-id="9e868-113">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="9e868-114">В Netscape Navigator каждая полученная команда сценария URL-адреса будет отображать URL-адрес в новом окне браузера, независимо от значения **дефаултфраме**.</span><span class="sxs-lookup"><span data-stu-id="9e868-114">In Netscape Navigator, each URL script command received will display the URL in a new browser window, regardless of the value of **defaultFrame**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e868-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9e868-115">Requirements</span></span>



| <span data-ttu-id="9e868-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9e868-116">Requirement</span></span> | <span data-ttu-id="9e868-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9e868-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e868-118">Версия</span><span class="sxs-lookup"><span data-stu-id="9e868-118">Version</span></span><br/>   | <span data-ttu-id="9e868-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9e868-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9e868-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9e868-120">Namespace</span></span><br/> | <span data-ttu-id="9e868-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="9e868-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9e868-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="9e868-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9e868-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9e868-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e868-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e868-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e868-125">**Событие Аксвиндовсмедиаплайер. команду скрипта (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9e868-125">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="9e868-126">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9e868-126">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





