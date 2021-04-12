---
title: Объект Плайераппликатион
description: Объект Плайераппликатион предоставляет способ координации переключения между удаленным элементом управления проигрывателя Windows Media и полноэкранным режимом проигрывателя Windows Media.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Проигрыватель Windows Media Object Плайераппликатион
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104334952"
---
# <a name="playerapplication-object"></a><span data-ttu-id="73731-104">Объект Плайераппликатион</span><span class="sxs-lookup"><span data-stu-id="73731-104">PlayerApplication Object</span></span>

<span data-ttu-id="73731-105">Объект **плайераппликатион** предоставляет способ координации переключения между удаленным элементом управления проигрывателя Windows Media и полноэкранным режимом проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="73731-105">The **PlayerApplication** object provides a way to coordinate switching between a remoted Windows Media Player control and the full mode of Windows Media Player.</span></span> <span data-ttu-id="73731-106">Этот объект используется только с программами C++, которые реализуют интерфейс **ивмпремотемедиасервицес** и внедряют элемент управления Player в удаленном режиме.</span><span class="sxs-lookup"><span data-stu-id="73731-106">This object is used only with C++ programs that implement the **IWMPRemoteMediaServices** interface and embed the Player control in remote mode.</span></span> <span data-ttu-id="73731-107">Файлы обложки, используемые в качестве пользовательских интерфейсов для удаленного управления проигрывателем Windows Media, обращаются к этому объекту в коде скрипта через глобальный атрибут **плайераппликатион** .</span><span class="sxs-lookup"><span data-stu-id="73731-107">Skin files used as custom interfaces for the remoted Windows Media Player control access this object in script code through the **playerApplication** global attribute.</span></span>

<span data-ttu-id="73731-108">Объект **плайераппликатион** поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="73731-108">The **PlayerApplication** object supports the following properties.</span></span>



| <span data-ttu-id="73731-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="73731-109">Property</span></span>                                           | <span data-ttu-id="73731-110">Описание</span><span class="sxs-lookup"><span data-stu-id="73731-110">Description</span></span>                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73731-111">хасдисплай</span><span class="sxs-lookup"><span data-stu-id="73731-111">hasDisplay</span></span>](playerapplication-hasdisplay.md)     | <span data-ttu-id="73731-112">Получает значение, указывающее, может ли видео отображаться с помощью удаленного элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="73731-112">Retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span> |
| [<span data-ttu-id="73731-113">плайердоккед</span><span class="sxs-lookup"><span data-stu-id="73731-113">playerDocked</span></span>](playerapplication-playerdocked.md) | <span data-ttu-id="73731-114">Извлекает значение, указывающее, находится ли проигрыватель Windows Media в закрепленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="73731-114">Retrieves a value indicating whether Windows Media Player is in a docked state.</span></span>                          |



 

<span data-ttu-id="73731-115">Объект **плайераппликатион** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="73731-115">The **PlayerApplication** object supports the following methods.</span></span>



| <span data-ttu-id="73731-116">Метод</span><span class="sxs-lookup"><span data-stu-id="73731-116">Method</span></span>                                                                       | <span data-ttu-id="73731-117">Описание</span><span class="sxs-lookup"><span data-stu-id="73731-117">Description</span></span>                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="73731-118">свитчтоконтрол</span><span class="sxs-lookup"><span data-stu-id="73731-118">switchToControl</span></span>](playerapplication-switchtocontrol.md)                     | <span data-ttu-id="73731-119">Переключает удаленный элемент управления проигрывателя Windows Media в закрепленное состояние.</span><span class="sxs-lookup"><span data-stu-id="73731-119">Switches a remoted Windows Media Player control to the docked state.</span></span>            |
| [<span data-ttu-id="73731-120">свитчтоплайераппликатион</span><span class="sxs-lookup"><span data-stu-id="73731-120">switchToPlayerApplication</span></span>](playerapplication-switchtoplayerapplication.md) | <span data-ttu-id="73731-121">Переключает удаленный элемент управления проигрывателя Windows Media в полный режим проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="73731-121">Switches a remoted Windows Media Player control to the full mode of the Player.</span></span> |



 

<span data-ttu-id="73731-122">Доступ к объекту **плайераппликатион** осуществляется через следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="73731-122">The **PlayerApplication** object is accessed through the following property.</span></span>



| <span data-ttu-id="73731-123">Объект</span><span class="sxs-lookup"><span data-stu-id="73731-123">Object</span></span>                      | <span data-ttu-id="73731-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="73731-124">Property</span></span>                                          |
|-----------------------------|---------------------------------------------------|
| [<span data-ttu-id="73731-125">Игрок</span><span class="sxs-lookup"><span data-stu-id="73731-125">Player</span></span>](player-object.md) | [<span data-ttu-id="73731-126">плайераппликатион</span><span class="sxs-lookup"><span data-stu-id="73731-126">playerApplication</span></span>](player-playerapplication.md) |



 

## <a name="see-also"></a><span data-ttu-id="73731-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73731-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73731-128">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="73731-128">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="73731-129">**Реализация удаленного управления проигрывателем Windows Media**</span><span class="sxs-lookup"><span data-stu-id="73731-129">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




