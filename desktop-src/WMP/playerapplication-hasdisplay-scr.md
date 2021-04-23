---
title: ПЛАЙЕРАППЛИКАТИОН. Хасдисплай, атрибут
description: Атрибут Хасдисплай извлекает значение, указывающее, может ли видео отображаться через удаленный элемент управления проигрывателя Windows Media.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- Проигрыватель Windows Media ПЛАЙЕРАППЛИКАТИОН. Хасдисплай
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704334"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="f56c6-104">ПЛАЙЕРАППЛИКАТИОН. Хасдисплай</span><span class="sxs-lookup"><span data-stu-id="f56c6-104">PLAYERAPPLICATION.hasDisplay</span></span>

<span data-ttu-id="f56c6-105">Атрибут **хасдисплай** извлекает значение, указывающее, может ли видео отображаться через удаленный элемент управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f56c6-105">The **hasDisplay** attribute retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span>

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a><span data-ttu-id="f56c6-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="f56c6-106">Possible Values</span></span>

<span data-ttu-id="f56c6-107">Этот атрибут является **логическим значением**, доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f56c6-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="f56c6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f56c6-108">Value</span></span> | <span data-ttu-id="f56c6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f56c6-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="f56c6-110">True</span><span class="sxs-lookup"><span data-stu-id="f56c6-110">True</span></span>  | <span data-ttu-id="f56c6-111">Видео может отображаться.</span><span class="sxs-lookup"><span data-stu-id="f56c6-111">The video can display.</span></span>    |
| <span data-ttu-id="f56c6-112">Неверно</span><span class="sxs-lookup"><span data-stu-id="f56c6-112">False</span></span> | <span data-ttu-id="f56c6-113">Не удается отобразить видео.</span><span class="sxs-lookup"><span data-stu-id="f56c6-113">The video cannot display.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f56c6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f56c6-114">Remarks</span></span>

<span data-ttu-id="f56c6-115">Этот атрибут используется только при удаленном взаимодействии с элементом управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f56c6-115">This attribute is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="f56c6-116">Несколько элементов управления проигрывателем Windows Media могут выполняться удаленно одновременно, но видео может отображаться в одном расположении одновременно либо в полноэкранном режиме проигрывателя, либо в одном из удаленных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="f56c6-116">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted controls.</span></span> <span data-ttu-id="f56c6-117">Используйте это свойство, чтобы определить, является ли текущий элемент управления элементом, с помощью которого можно отобразить видео.</span><span class="sxs-lookup"><span data-stu-id="f56c6-117">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f56c6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f56c6-118">Requirements</span></span>



| <span data-ttu-id="f56c6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f56c6-119">Requirement</span></span> | <span data-ttu-id="f56c6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f56c6-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="f56c6-121">Версия</span><span class="sxs-lookup"><span data-stu-id="f56c6-121">Version</span></span><br/> | <span data-ttu-id="f56c6-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f56c6-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f56c6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f56c6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f56c6-124">**ПЛАЙЕРАППЛИКАТИОН, элемент**</span><span class="sxs-lookup"><span data-stu-id="f56c6-124">**PLAYERAPPLICATION Element**</span></span>](playerapplication-element.md)
</dt> <dt>

[<span data-ttu-id="f56c6-125">**Реализация удаленного управления проигрывателем Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f56c6-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





