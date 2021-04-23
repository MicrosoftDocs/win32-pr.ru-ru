---
title: Событие Player. Домаинчанже
description: Событие Домаинчанже возникает при смене домена DVD. | Событие Player. Домаинчанже
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Проигрыватель Windows Media Event Домаинчанже
- Проигрыватель Windows Media Event Домаинчанже, класс Player
- Класс проигрывателя Windows Media Player, событие Домаинчанже
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708318"
---
# <a name="playerdomainchange-event"></a><span data-ttu-id="9a0d2-107">Событие Player. Домаинчанже</span><span class="sxs-lookup"><span data-stu-id="9a0d2-107">Player.DomainChange event</span></span>

<span data-ttu-id="9a0d2-108">Событие **домаинчанже** возникает при смене домена DVD.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-108">The **DomainChange** event occurs when the DVD domain changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a0d2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a0d2-109">Syntax</span></span>


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a><span data-ttu-id="9a0d2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a0d2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a0d2-111">*стрдомаин*</span><span class="sxs-lookup"><span data-stu-id="9a0d2-111">*strDomain*</span></span> 
</dt> <dd>

<span data-ttu-id="9a0d2-112">**Строка** , указывающая новый домен.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-112">**String** indicating the new domain.</span></span> <span data-ttu-id="9a0d2-113">Содержит одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="9a0d2-113">Contains one of the following values.</span></span>



| <span data-ttu-id="9a0d2-114">Строка</span><span class="sxs-lookup"><span data-stu-id="9a0d2-114">String</span></span>            | <span data-ttu-id="9a0d2-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9a0d2-115">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="9a0d2-116">фирстплай</span><span class="sxs-lookup"><span data-stu-id="9a0d2-116">firstplay</span></span>         | <span data-ttu-id="9a0d2-117">Выполнение инициализации DVD-диска по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-117">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="9a0d2-118">видеоманажермену</span><span class="sxs-lookup"><span data-stu-id="9a0d2-118">videoManagerMenu</span></span>  | <span data-ttu-id="9a0d2-119">Отображение меню для всего диска. Также называется корневым меню или Топмену.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-119">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="9a0d2-120">видеотитлесетмену</span><span class="sxs-lookup"><span data-stu-id="9a0d2-120">videoTitleSetMenu</span></span> | <span data-ttu-id="9a0d2-121">Отображение меню для текущего набора заголовков.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-121">Displaying menus for current title set.</span></span> <span data-ttu-id="9a0d2-122">Также называется Титлемену.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-122">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="9a0d2-123">title</span><span class="sxs-lookup"><span data-stu-id="9a0d2-123">title</span></span>             | <span data-ttu-id="9a0d2-124">Отображение текущего заголовка.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-124">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="9a0d2-125">stop</span><span class="sxs-lookup"><span data-stu-id="9a0d2-125">stop</span></span>              | <span data-ttu-id="9a0d2-126">Навигатор DVD находится в области DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-126">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a0d2-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a0d2-127">Return value</span></span>

<span data-ttu-id="9a0d2-128">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-128">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a0d2-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a0d2-129">Remarks</span></span>

<span data-ttu-id="9a0d2-130">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-130">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="9a0d2-131">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-131">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="9a0d2-132">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-132">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0d2-133">Требования</span><span class="sxs-lookup"><span data-stu-id="9a0d2-133">Requirements</span></span>



| <span data-ttu-id="9a0d2-134">Требование</span><span class="sxs-lookup"><span data-stu-id="9a0d2-134">Requirement</span></span> | <span data-ttu-id="9a0d2-135">Значение</span><span class="sxs-lookup"><span data-stu-id="9a0d2-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0d2-136">Версия</span><span class="sxs-lookup"><span data-stu-id="9a0d2-136">Version</span></span><br/> | <span data-ttu-id="9a0d2-137">Проигрыватель Windows Media для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9a0d2-137">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="9a0d2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9a0d2-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="9a0d2-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a0d2-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a0d2-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a0d2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0d2-141">**Объект DVD**</span><span class="sxs-lookup"><span data-stu-id="9a0d2-141">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="9a0d2-142">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="9a0d2-142">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





