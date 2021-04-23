---
title: Player. Remote
description: Свойство «Remote» извлекает значение, указывающее, выполняется ли элемент управления проигрывателя Windows Media в удаленном режиме.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Проигрыватель проигрывателя Windows Media Player
topic_type:
- apiref
api_name:
- Player.isRemote
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c8d97ba212e032db16b43299d2a3a8a836f9b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648059"
---
# <a name="playerisremote"></a><span data-ttu-id="1df78-104">Player. Remote</span><span class="sxs-lookup"><span data-stu-id="1df78-104">Player.isRemote</span></span>

<span data-ttu-id="1df78-105">Свойство « **Remote** » извлекает значение, указывающее, выполняется ли элемент управления проигрывателя Windows Media в удаленном режиме.</span><span class="sxs-lookup"><span data-stu-id="1df78-105">The **isRemote** property retrieves a value indicating whether the Windows Media Player control is running in remote mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df78-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1df78-106">Syntax</span></span>

<span data-ttu-id="1df78-107">*проигрыватель* . **Удаленный**</span><span class="sxs-lookup"><span data-stu-id="1df78-107">*player* .**isRemote**</span></span>

## <a name="possible-values"></a><span data-ttu-id="1df78-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1df78-108">Possible Values</span></span>

<span data-ttu-id="1df78-109">Это свойство является **логическим значением**, доступным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1df78-109">This property is a read-only **Boolean**.</span></span>



| <span data-ttu-id="1df78-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1df78-110">Value</span></span> | <span data-ttu-id="1df78-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1df78-111">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="1df78-112">true</span><span class="sxs-lookup"><span data-stu-id="1df78-112">true</span></span>  | <span data-ttu-id="1df78-113">Элемент управления "проигрыватель" работает в удаленном режиме.</span><span class="sxs-lookup"><span data-stu-id="1df78-113">The Player control is running in remote mode.</span></span> |
| <span data-ttu-id="1df78-114">false</span><span class="sxs-lookup"><span data-stu-id="1df78-114">false</span></span> | <span data-ttu-id="1df78-115">Элемент управления "проигрыватель" выполняется в локальном режиме.</span><span class="sxs-lookup"><span data-stu-id="1df78-115">The Player control is running in local mode.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="1df78-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1df78-116">Remarks</span></span>

<span data-ttu-id="1df78-117">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="1df78-117">**Windows Media Player 10 Mobile:** This property always returns false.</span></span>

## <a name="requirements"></a><span data-ttu-id="1df78-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1df78-118">Requirements</span></span>



| <span data-ttu-id="1df78-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1df78-119">Requirement</span></span> | <span data-ttu-id="1df78-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1df78-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1df78-121">Версия</span><span class="sxs-lookup"><span data-stu-id="1df78-121">Version</span></span><br/> | <span data-ttu-id="1df78-122">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="1df78-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="1df78-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1df78-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="1df78-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1df78-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df78-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1df78-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df78-126">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="1df78-126">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="1df78-127">**Реализация удаленного управления проигрывателем Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1df78-127">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





