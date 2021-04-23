---
title: Метод CDROM. EJECT
description: Метод Eject извлекает компакт-диск или DVD-диск из накопителя. | Метод CDROM. EJECT
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- метод извлечения Windows Media Player
- метод извлечения Windows Media Player, класс CDROM
- Класс CDROM проигрыватель Windows Media Player, метод reeject
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693984"
---
# <a name="cdromeject-method"></a><span data-ttu-id="60202-107">Метод CDROM. EJECT</span><span class="sxs-lookup"><span data-stu-id="60202-107">Cdrom.eject method</span></span>

<span data-ttu-id="60202-108">Метод **Eject** извлекает компакт-диск или DVD-диск из накопителя.</span><span class="sxs-lookup"><span data-stu-id="60202-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="60202-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60202-109">Syntax</span></span>


```JScript
Cdrom.eject()
```



## <a name="parameters"></a><span data-ttu-id="60202-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="60202-110">Parameters</span></span>

<span data-ttu-id="60202-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="60202-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="60202-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60202-112">Return value</span></span>

<span data-ttu-id="60202-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="60202-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60202-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60202-114">Remarks</span></span>

<span data-ttu-id="60202-115">Если дверца диска открыта, этот метод закрывает дверцу.</span><span class="sxs-lookup"><span data-stu-id="60202-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="60202-116">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="60202-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="60202-117">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="60202-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="60202-118">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="60202-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="60202-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="60202-119">Examples</span></span>

<span data-ttu-id="60202-120">В следующем примере создается HTML-элемент Button, который использует *CDROM*. **Извлеките** , чтобы открыть дверцу диска с нулевым индексом описателя.</span><span class="sxs-lookup"><span data-stu-id="60202-120">The following example creates an HTML button element that uses *Cdrom*.**eject** to open the door of the drive that has drive specifier index zero.</span></span> <span data-ttu-id="60202-121">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="60202-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a><span data-ttu-id="60202-122">Требования</span><span class="sxs-lookup"><span data-stu-id="60202-122">Requirements</span></span>



| <span data-ttu-id="60202-123">Требование</span><span class="sxs-lookup"><span data-stu-id="60202-123">Requirement</span></span> | <span data-ttu-id="60202-124">Значение</span><span class="sxs-lookup"><span data-stu-id="60202-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60202-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60202-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60202-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="60202-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60202-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60202-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60202-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="60202-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="60202-129">Версия</span><span class="sxs-lookup"><span data-stu-id="60202-129">Version</span></span><br/>                  | <span data-ttu-id="60202-130">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="60202-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="60202-131">DLL</span><span class="sxs-lookup"><span data-stu-id="60202-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60202-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60202-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60202-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60202-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60202-134">**Объект CDROM**</span><span class="sxs-lookup"><span data-stu-id="60202-134">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="60202-135">**Player. Плайстате**</span><span class="sxs-lookup"><span data-stu-id="60202-135">**Player.playState**</span></span>](player-playstate.md)
</dt> <dt>

[<span data-ttu-id="60202-136">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="60202-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="60202-137">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="60202-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





