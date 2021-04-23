---
title: Метод DVD. Топмену
description: Метод Топмену останавливает воспроизведение заголовка и отображает верхнее (или корневое) меню для текущего заголовка.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- Топмену метод Windows Media Player
- метод Топмену проигрывателя Windows Media Player, класс DVD
- Класс DVD проигрыватель Windows Media Player, метод Топмену
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491271"
---
# <a name="dvdtopmenu-method"></a><span data-ttu-id="5d405-106">Метод DVD. Топмену</span><span class="sxs-lookup"><span data-stu-id="5d405-106">DVD.topMenu method</span></span>

<span data-ttu-id="5d405-107">Метод **топмену** останавливает воспроизведение заголовка и отображает верхнее (или корневое) меню для текущего заголовка.</span><span class="sxs-lookup"><span data-stu-id="5d405-107">The **topMenu** method stops title playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d405-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d405-108">Syntax</span></span>


```JScript
DVD.topMenu()
```



## <a name="parameters"></a><span data-ttu-id="5d405-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d405-109">Parameters</span></span>

<span data-ttu-id="5d405-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5d405-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5d405-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d405-111">Return value</span></span>

<span data-ttu-id="5d405-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5d405-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d405-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d405-113">Remarks</span></span>

<span data-ttu-id="5d405-114">Каждый DVD-диск создан по-другому.</span><span class="sxs-lookup"><span data-stu-id="5d405-114">Every DVD is authored differently.</span></span> <span data-ttu-id="5d405-115">Чтобы этот метод работал, DVD-диск должен содержать меню.</span><span class="sxs-lookup"><span data-stu-id="5d405-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="5d405-116">Некоторые DVD-диски созданы таким образом, чтобы методы **топмену** и **титлемену** открывали одно и то же меню.</span><span class="sxs-lookup"><span data-stu-id="5d405-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="5d405-117">Метод **топмену** обычно вызывает верхнее (или корневое) меню, но вместо этого может вызвать меню заголовка, если нет доступного корневого меню.</span><span class="sxs-lookup"><span data-stu-id="5d405-117">The **topMenu** method usually invokes the top (or root) menu but it may invoke the title menu instead, if there is no root menu available.</span></span>

<span data-ttu-id="5d405-118">**Проигрыватель Windows Media 10 Mobile:** Этот метод всегда выполняется, но не выполняет требуемую операцию.</span><span class="sxs-lookup"><span data-stu-id="5d405-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d405-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5d405-119">Requirements</span></span>



| <span data-ttu-id="5d405-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5d405-120">Requirement</span></span> | <span data-ttu-id="5d405-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5d405-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d405-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d405-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5d405-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5d405-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d405-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d405-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5d405-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5d405-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5d405-126">Версия</span><span class="sxs-lookup"><span data-stu-id="5d405-126">Version</span></span><br/>                  | <span data-ttu-id="5d405-127">Проигрыватель Windows Media для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5d405-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="5d405-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5d405-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d405-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d405-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d405-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d405-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d405-131">**Объект DVD**</span><span class="sxs-lookup"><span data-stu-id="5d405-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="5d405-132">**DVD. Титлемену**</span><span class="sxs-lookup"><span data-stu-id="5d405-132">**DVD.titleMenu**</span></span>](dvd-titlemenu.md)
</dt> </dl>

 

 





