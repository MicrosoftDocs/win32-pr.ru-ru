---
title: Метод Player. Лаунчурл
description: Метод Лаунчурл отправляет URL-адрес браузеру пользователя по умолчанию для подготовки к просмотру. | Метод Player. Лаунчурл
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- Лаунчурл метод Windows Media Player
- метод Лаунчурл проигрывателя Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, метод Лаунчурл
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685272"
---
# <a name="playerlaunchurl-method"></a><span data-ttu-id="48022-107">Метод Player. Лаунчурл</span><span class="sxs-lookup"><span data-stu-id="48022-107">Player.launchURL method</span></span>

<span data-ttu-id="48022-108">Метод **лаунчурл** отправляет URL-адрес браузеру пользователя по умолчанию для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="48022-108">The **launchURL** method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="48022-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48022-109">Syntax</span></span>


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="48022-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="48022-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48022-111">*URL-адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48022-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48022-112">**Строковое** значение, представляющее URL-адрес для запуска.</span><span class="sxs-lookup"><span data-stu-id="48022-112">**String** value representing the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48022-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48022-113">Return value</span></span>

<span data-ttu-id="48022-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="48022-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48022-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48022-115">Remarks</span></span>

<span data-ttu-id="48022-116">Этот метод открывает только веб-страницы с использованием протоколов HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="48022-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="48022-117">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="48022-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="48022-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="48022-118">Examples</span></span>

<span data-ttu-id="48022-119">В следующем примере создается элемент кнопки HTML, который при нажатии отображает веб-сайт Майкрософт в новом окне браузера.</span><span class="sxs-lookup"><span data-stu-id="48022-119">The following example creates an HTML BUTTON element that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="48022-120">Был создан элемент **Player** с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="48022-120">The **Player** element was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a><span data-ttu-id="48022-121">Требования</span><span class="sxs-lookup"><span data-stu-id="48022-121">Requirements</span></span>



| <span data-ttu-id="48022-122">Требование</span><span class="sxs-lookup"><span data-stu-id="48022-122">Requirement</span></span> | <span data-ttu-id="48022-123">Значение</span><span class="sxs-lookup"><span data-stu-id="48022-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="48022-124">Версия</span><span class="sxs-lookup"><span data-stu-id="48022-124">Version</span></span><br/> | <span data-ttu-id="48022-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="48022-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="48022-126">DLL</span><span class="sxs-lookup"><span data-stu-id="48022-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="48022-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48022-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48022-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48022-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48022-129">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="48022-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





