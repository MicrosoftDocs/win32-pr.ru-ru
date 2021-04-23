---
title: DVD. домен
description: Свойство Domain извлекает текущий домен DVD-диска.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. проигрыватель Windows Media Player
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340595"
---
# <a name="dvddomain"></a><span data-ttu-id="696f3-104">DVD. домен</span><span class="sxs-lookup"><span data-stu-id="696f3-104">DVD.domain</span></span>

<span data-ttu-id="696f3-105">Свойство **domain** извлекает текущий домен DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="696f3-105">The **domain** property retrieves the current domain of the DVD.</span></span>

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a><span data-ttu-id="696f3-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="696f3-106">Possible Values</span></span>

<span data-ttu-id="696f3-107">Это свойство является **строкой** только для чтения, содержащей одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="696f3-107">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="696f3-108">Строка</span><span class="sxs-lookup"><span data-stu-id="696f3-108">String</span></span>            | <span data-ttu-id="696f3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="696f3-109">Description</span></span>                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="696f3-110">фирстплай</span><span class="sxs-lookup"><span data-stu-id="696f3-110">firstPlay</span></span>         | <span data-ttu-id="696f3-111">Выполнение инициализации DVD-диска по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="696f3-111">Performing default initialization of a DVD disc.</span></span>                                                                                      |
| <span data-ttu-id="696f3-112">видеоманажермену</span><span class="sxs-lookup"><span data-stu-id="696f3-112">videoManagerMenu</span></span>  | <span data-ttu-id="696f3-113">Отображение меню для всего диска. Также известен как Топмену для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="696f3-113">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="696f3-114">Обычно называется меню заголовка или верхним меню.</span><span class="sxs-lookup"><span data-stu-id="696f3-114">Commonly called the title menu or the top menu.</span></span> |
| <span data-ttu-id="696f3-115">видеотитлесетмену</span><span class="sxs-lookup"><span data-stu-id="696f3-115">videoTitleSetMenu</span></span> | <span data-ttu-id="696f3-116">Отображение меню для текущего набора заголовков.</span><span class="sxs-lookup"><span data-stu-id="696f3-116">Displaying menus for current title set.</span></span> <span data-ttu-id="696f3-117">Также известен как Титлемену для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="696f3-117">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="696f3-118">Обычно называется корневым меню.</span><span class="sxs-lookup"><span data-stu-id="696f3-118">Commonly called the root menu.</span></span>              |
| <span data-ttu-id="696f3-119">title</span><span class="sxs-lookup"><span data-stu-id="696f3-119">title</span></span>             | <span data-ttu-id="696f3-120">Обычно отображается текущее название.</span><span class="sxs-lookup"><span data-stu-id="696f3-120">Usually displaying the current title.</span></span>                                                                                                 |
| <span data-ttu-id="696f3-121">stop</span><span class="sxs-lookup"><span data-stu-id="696f3-121">stop</span></span>              | <span data-ttu-id="696f3-122">Навигатор DVD находится в области DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="696f3-122">The DVD Navigator is in the DVD Stop domain.</span></span>                                                                                          |
| <span data-ttu-id="696f3-123">неопределенный</span><span class="sxs-lookup"><span data-stu-id="696f3-123">undefined</span></span>         | <span data-ttu-id="696f3-124">Проигрыватель не находится ни в одном DVD-домене.</span><span class="sxs-lookup"><span data-stu-id="696f3-124">Player is not in any DVD domain.</span></span>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="696f3-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="696f3-125">Remarks</span></span>

<span data-ttu-id="696f3-126">Каждый DVD-диск создан по-другому.</span><span class="sxs-lookup"><span data-stu-id="696f3-126">Every DVD is authored differently.</span></span> <span data-ttu-id="696f3-127">Некоторые DVD-диски не содержат домены Фирстплай, Видеоманажермену или Видеотитлесетмену.</span><span class="sxs-lookup"><span data-stu-id="696f3-127">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

<span data-ttu-id="696f3-128">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="696f3-128">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="696f3-129">Требования</span><span class="sxs-lookup"><span data-stu-id="696f3-129">Requirements</span></span>



| <span data-ttu-id="696f3-130">Требование</span><span class="sxs-lookup"><span data-stu-id="696f3-130">Requirement</span></span> | <span data-ttu-id="696f3-131">Значение</span><span class="sxs-lookup"><span data-stu-id="696f3-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="696f3-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="696f3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="696f3-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="696f3-133">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="696f3-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="696f3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="696f3-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="696f3-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="696f3-136">Версия</span><span class="sxs-lookup"><span data-stu-id="696f3-136">Version</span></span><br/>                  | <span data-ttu-id="696f3-137">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="696f3-137">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="696f3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="696f3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="696f3-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="696f3-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="696f3-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="696f3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="696f3-141">**Объект DVD**</span><span class="sxs-lookup"><span data-stu-id="696f3-141">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





