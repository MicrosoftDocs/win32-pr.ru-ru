---
title: Метод DVD. Титлемену
description: Метод Титлемену останавливает воспроизведение заголовка и отображает меню заголовка.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- Титлемену метод Windows Media Player
- метод Титлемену проигрывателя Windows Media Player, класс DVD
- Класс DVD проигрыватель Windows Media Player, метод Титлемену
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340590"
---
# <a name="dvdtitlemenu-method"></a><span data-ttu-id="f003d-106">Метод DVD. Титлемену</span><span class="sxs-lookup"><span data-stu-id="f003d-106">DVD.titleMenu method</span></span>

<span data-ttu-id="f003d-107">Метод **титлемену** останавливает воспроизведение заголовка и отображает меню заголовка.</span><span class="sxs-lookup"><span data-stu-id="f003d-107">The **titleMenu** method stops title playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="f003d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f003d-108">Syntax</span></span>


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a><span data-ttu-id="f003d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f003d-109">Parameters</span></span>

<span data-ttu-id="f003d-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f003d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f003d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f003d-111">Return value</span></span>

<span data-ttu-id="f003d-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f003d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f003d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f003d-113">Remarks</span></span>

<span data-ttu-id="f003d-114">Каждый DVD-диск создан по-другому.</span><span class="sxs-lookup"><span data-stu-id="f003d-114">Every DVD is authored differently.</span></span> <span data-ttu-id="f003d-115">Чтобы этот метод работал, DVD-диск должен содержать меню.</span><span class="sxs-lookup"><span data-stu-id="f003d-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="f003d-116">Некоторые DVD-диски созданы таким образом, чтобы методы **топмену** и **титлемену** открывали одно и то же меню.</span><span class="sxs-lookup"><span data-stu-id="f003d-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="f003d-117">Метод **титлемену** обычно вызывает меню заголовка, но он может вызвать верхнее меню, если нет доступного меню заголовка.</span><span class="sxs-lookup"><span data-stu-id="f003d-117">The **titleMenu** method usually invokes the title menu but it may invoke the top menu instead, if there is no title menu available.</span></span>

<span data-ttu-id="f003d-118">**Проигрыватель Windows Media 10 Mobile:** Этот метод всегда выполняется, но не выполняет требуемую операцию.</span><span class="sxs-lookup"><span data-stu-id="f003d-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f003d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f003d-119">Requirements</span></span>



| <span data-ttu-id="f003d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f003d-120">Requirement</span></span> | <span data-ttu-id="f003d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f003d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f003d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f003d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f003d-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f003d-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f003d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f003d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f003d-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f003d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f003d-126">Версия</span><span class="sxs-lookup"><span data-stu-id="f003d-126">Version</span></span><br/>                  | <span data-ttu-id="f003d-127">Проигрыватель Windows Media для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f003d-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="f003d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f003d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f003d-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f003d-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f003d-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f003d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f003d-131">**Объект DVD**</span><span class="sxs-lookup"><span data-stu-id="f003d-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="f003d-132">**DVD. Топмену**</span><span class="sxs-lookup"><span data-stu-id="f003d-132">**DVD.topMenu**</span></span>](dvd-topmenu.md)
</dt> </dl>

 

 





