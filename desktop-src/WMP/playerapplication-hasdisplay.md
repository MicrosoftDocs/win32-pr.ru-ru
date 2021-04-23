---
title: Плайераппликатион. Хасдисплай
description: Свойство Хасдисплай извлекает значение, указывающее, может ли видео отображаться с помощью удаленного элемента управления Player.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- Проигрыватель Windows Media Плайераппликатион. Хасдисплай
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704333"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="b09b2-104">Плайераппликатион. Хасдисплай</span><span class="sxs-lookup"><span data-stu-id="b09b2-104">PlayerApplication.hasDisplay</span></span>

<span data-ttu-id="b09b2-105">Свойство **хасдисплай** извлекает значение, указывающее, может ли видео отображаться с помощью удаленного элемента управления Player.</span><span class="sxs-lookup"><span data-stu-id="b09b2-105">The **hasDisplay** property retrieves a value indicating whether video can display through the remoted Player control.</span></span>

## <a name="syntax"></a><span data-ttu-id="b09b2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b09b2-106">Syntax</span></span>

<span data-ttu-id="b09b2-107">*плайераппликатион*. **хасдисплай**</span><span class="sxs-lookup"><span data-stu-id="b09b2-107">*playerApplication*.**hasDisplay**</span></span>

## <a name="possible-values"></a><span data-ttu-id="b09b2-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b09b2-108">Possible Values</span></span>

<span data-ttu-id="b09b2-109">Это свойство является **логическим значением**, доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b09b2-109">This property is a read-only **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b09b2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b09b2-110">Remarks</span></span>

<span data-ttu-id="b09b2-111">Это свойство используется только при удаленном взаимодействии с элементом управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b09b2-111">This property is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="b09b2-112">Несколько элементов управления проигрывателем Windows Media могут выполняться удаленно одновременно, но видео может отображаться в одном расположении одновременно либо в полноэкранном режиме проигрывателя, либо в одном из удаленных элементов управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b09b2-112">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted Windows Media Player controls.</span></span> <span data-ttu-id="b09b2-113">Используйте это свойство, чтобы определить, является ли текущий элемент управления элементом, с помощью которого можно отобразить видео.</span><span class="sxs-lookup"><span data-stu-id="b09b2-113">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

<span data-ttu-id="b09b2-114">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="b09b2-114">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b09b2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b09b2-115">Requirements</span></span>



| <span data-ttu-id="b09b2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b09b2-116">Requirement</span></span> | <span data-ttu-id="b09b2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b09b2-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b09b2-118">Версия</span><span class="sxs-lookup"><span data-stu-id="b09b2-118">Version</span></span><br/> | <span data-ttu-id="b09b2-119">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b09b2-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="b09b2-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b09b2-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="b09b2-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b09b2-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b09b2-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b09b2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b09b2-123">**Объект Плайераппликатион**</span><span class="sxs-lookup"><span data-stu-id="b09b2-123">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="b09b2-124">**Реализация удаленного управления проигрывателем Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b09b2-124">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





