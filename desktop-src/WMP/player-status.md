---
title: Player. status
description: Свойство Status извлекает значение, указывающее состояние проигрывателя Windows Media.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Проигрыватель проигрывателя Windows Media. status
topic_type:
- apiref
api_name:
- Player.status
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d54c71e6ab8ece61fb97960bd2956393b1ae584
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704151"
---
# <a name="playerstatus"></a><span data-ttu-id="8c727-104">Player. status</span><span class="sxs-lookup"><span data-stu-id="8c727-104">Player.status</span></span>

<span data-ttu-id="8c727-105">Свойство **Status** извлекает значение, указывающее состояние проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8c727-105">The **status** property retrieves a value indicating the status of Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c727-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c727-106">Syntax</span></span>

<span data-ttu-id="8c727-107">*проигрыватель* . **состояние**</span><span class="sxs-lookup"><span data-stu-id="8c727-107">*player* .**status**</span></span>

## <a name="possible-values"></a><span data-ttu-id="8c727-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="8c727-108">Possible Values</span></span>

<span data-ttu-id="8c727-109">Это свойство является строкой, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8c727-109">This property is a read-only String.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c727-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c727-110">Remarks</span></span>

<span data-ttu-id="8c727-111">Значения, содержащиеся в этом свойстве, могут быть изменены в любое время, и их следует использовать только в целях вывода.</span><span class="sxs-lookup"><span data-stu-id="8c727-111">The values contained in this property are subject to change at any time, and should be used for display purposes only.</span></span>

<span data-ttu-id="8c727-112">Событие **StatusChange** срабатывает при каждом изменении значения свойства.</span><span class="sxs-lookup"><span data-stu-id="8c727-112">The **StatusChange** event is fired whenever this property changes value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c727-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8c727-113">Requirements</span></span>



| <span data-ttu-id="8c727-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8c727-114">Requirement</span></span> | <span data-ttu-id="8c727-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8c727-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c727-116">Версия</span><span class="sxs-lookup"><span data-stu-id="8c727-116">Version</span></span><br/> | <span data-ttu-id="8c727-117">Проигрыватель Windows Media 7,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="8c727-117">Windows Media Player 7.0 or later.</span></span><br/>                                      |
| <span data-ttu-id="8c727-118">DLL</span><span class="sxs-lookup"><span data-stu-id="8c727-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c727-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c727-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c727-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c727-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c727-121">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="8c727-121">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="8c727-122">**Событие Player. StatusChange**</span><span class="sxs-lookup"><span data-stu-id="8c727-122">**Player.StatusChange Event**</span></span>](player-player-statuschange.md)
</dt> </dl>

 

 





