---
title: Player. Плайераппликатион
description: Свойство Плайераппликатион извлекает объект Плайераппликатион при запуске удаленного элемента управления проигрывателя Windows Media.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Проигрыватель проигрывателя Windows Media Player. Плайераппликатион
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704406"
---
# <a name="playerplayerapplication"></a><span data-ttu-id="4ea67-104">Player. Плайераппликатион</span><span class="sxs-lookup"><span data-stu-id="4ea67-104">Player.playerApplication</span></span>

<span data-ttu-id="4ea67-105">Свойство **плайераппликатион** извлекает объект **плайераппликатион** при запуске удаленного элемента управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4ea67-105">The **playerApplication** property retrieves the **PlayerApplication** object when a remoted Windows Media Player control is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea67-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ea67-106">Syntax</span></span>

<span data-ttu-id="4ea67-107">**плайераппликатион**</span><span class="sxs-lookup"><span data-stu-id="4ea67-107">**playerApplication**</span></span>

## <a name="possible-values"></a><span data-ttu-id="4ea67-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="4ea67-108">Possible Values</span></span>

<span data-ttu-id="4ea67-109">Это свойство является объектом **плайераппликатион** , предназначенным только для чтения, или значением NULL.</span><span class="sxs-lookup"><span data-stu-id="4ea67-109">This property is a read-only **PlayerApplication** object or the null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ea67-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ea67-110">Remarks</span></span>

<span data-ttu-id="4ea67-111">Это свойство используется только при удаленном взаимодействии с Windows Media Плайерконтрол.</span><span class="sxs-lookup"><span data-stu-id="4ea67-111">This property is used only when remoting the Windows Media Playercontrol.</span></span> <span data-ttu-id="4ea67-112">Если значение равно null, Плайерконтрол Windows Media не внедряется в удаленном режиме.</span><span class="sxs-lookup"><span data-stu-id="4ea67-112">If the value is null, the Windows Media Playercontrol is not embedded in remote mode.</span></span>

<span data-ttu-id="4ea67-113">Это свойство доступно только в коде C++ или в коде скрипта в обложек через глобальную переменную Плайераппликатион.</span><span class="sxs-lookup"><span data-stu-id="4ea67-113">This property is only accessible in C++ code or in script code in skins through the playerApplication global variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ea67-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4ea67-114">Requirements</span></span>



| <span data-ttu-id="4ea67-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4ea67-115">Requirement</span></span> | <span data-ttu-id="4ea67-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4ea67-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea67-117">Версия</span><span class="sxs-lookup"><span data-stu-id="4ea67-117">Version</span></span><br/> | <span data-ttu-id="4ea67-118">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="4ea67-118">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="4ea67-119">DLL</span><span class="sxs-lookup"><span data-stu-id="4ea67-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="4ea67-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ea67-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ea67-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ea67-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea67-122">**Глобальные атрибуты**</span><span class="sxs-lookup"><span data-stu-id="4ea67-122">**Global Attributes**</span></span>](global-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ea67-123">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="4ea67-123">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="4ea67-124">**Объект Плайераппликатион**</span><span class="sxs-lookup"><span data-stu-id="4ea67-124">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="4ea67-125">**Реализация удаленного управления проигрывателем Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4ea67-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





