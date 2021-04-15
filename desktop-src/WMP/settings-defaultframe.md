---
title: Settings. Дефаултфраме
description: Свойство Дефаултфраме указывает или получает имя кадра, используемого для вывода URL-адреса, полученного в событии команду скрипта.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Проигрыватель Windows Media Settings. Дефаултфраме
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648725"
---
# <a name="settingsdefaultframe"></a><span data-ttu-id="98c48-104">Settings. Дефаултфраме</span><span class="sxs-lookup"><span data-stu-id="98c48-104">Settings.defaultFrame</span></span>

<span data-ttu-id="98c48-105">Свойство **дефаултфраме** указывает или получает имя кадра, используемого для вывода URL-адреса, полученного в событии **команду скрипта** .</span><span class="sxs-lookup"><span data-stu-id="98c48-105">The **defaultFrame** property specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c48-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98c48-106">Syntax</span></span>

<span data-ttu-id="98c48-107">Player. Settings. Дефаултфраме</span><span class="sxs-lookup"><span data-stu-id="98c48-107">player.settings.defaultFrame</span></span>

## <a name="possible-values"></a><span data-ttu-id="98c48-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="98c48-108">Possible Values</span></span>

<span data-ttu-id="98c48-109">Это свойство является **строкой** для чтения и записи, соответствующей значению атрибута **Name** целевого элемента Frame.</span><span class="sxs-lookup"><span data-stu-id="98c48-109">This property is a read/write **String** corresponding to the value of the **name** attribute of the target FRAME element.</span></span>

## <a name="remarks"></a><span data-ttu-id="98c48-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98c48-110">Remarks</span></span>

<span data-ttu-id="98c48-111">Если целевой кадр указан в событии **команду скрипта** , это свойство игнорируется.</span><span class="sxs-lookup"><span data-stu-id="98c48-111">If a target frame is specified in the **ScriptCommand** event itself, this property is ignored.</span></span>

<span data-ttu-id="98c48-112">Это свойство игнорируется при использовании приложения Netscape Navigator Java.</span><span class="sxs-lookup"><span data-stu-id="98c48-112">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="98c48-113">В навигаторе каждая полученная команда сценария URL-адреса отображает URL-адрес в новом окне браузера, независимо от значения *параметров*. **дефаултфраме**.</span><span class="sxs-lookup"><span data-stu-id="98c48-113">In Navigator, each URL script command received displays the URL in a new browser window, regardless of the value of *Settings*.**defaultFrame**.</span></span>

<span data-ttu-id="98c48-114">**Проигрыватель Windows Media 10 Mobile**: это свойство доступно только для чтения и всегда возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="98c48-114">**Windows Media Player 10 Mobile**: This property is read only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="98c48-115">Требования</span><span class="sxs-lookup"><span data-stu-id="98c48-115">Requirements</span></span>



| <span data-ttu-id="98c48-116">Требование</span><span class="sxs-lookup"><span data-stu-id="98c48-116">Requirement</span></span> | <span data-ttu-id="98c48-117">Значение</span><span class="sxs-lookup"><span data-stu-id="98c48-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98c48-118">Версия</span><span class="sxs-lookup"><span data-stu-id="98c48-118">Version</span></span><br/> | <span data-ttu-id="98c48-119">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="98c48-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="98c48-120">DLL</span><span class="sxs-lookup"><span data-stu-id="98c48-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="98c48-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98c48-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98c48-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98c48-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c48-123">**Событие Player. команду скрипта**</span><span class="sxs-lookup"><span data-stu-id="98c48-123">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="98c48-124">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="98c48-124">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="98c48-125">**Использование проигрывателя Windows Media с Netscape 7.1**</span><span class="sxs-lookup"><span data-stu-id="98c48-125">**Using Windows Media Player with Netscape 7.1**</span></span>](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





