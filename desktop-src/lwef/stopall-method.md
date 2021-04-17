---
title: Метод Стопалл
description: Метод Стопалл
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c99a687c2481d9686e84b7fa5c198e7a4273a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700843"
---
# <a name="stopall-method"></a><span data-ttu-id="b5e60-103">Метод Стопалл</span><span class="sxs-lookup"><span data-stu-id="b5e60-103">StopAll Method</span></span>

<span data-ttu-id="b5e60-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b5e60-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b5e60-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="b5e60-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b5e60-106">Останавливает все запросы анимации или заданные типы запросов для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="b5e60-106">Stops all animation requests or specified types of requests for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="b5e60-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="b5e60-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b5e60-108">\*Агент ***. Символы ("*** чарактерид \* \* *").* \*  \[ *Тип* стопалл\]</span><span class="sxs-lookup"><span data-stu-id="b5e60-108">*agent ***.Characters ("*** CharacterID\*\*\*").StopAll*\* \[*Type*\]</span></span>



| <span data-ttu-id="b5e60-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="b5e60-109">Part</span></span>   | <span data-ttu-id="b5e60-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b5e60-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5e60-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="b5e60-111">*Type*</span></span> | <span data-ttu-id="b5e60-112">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="b5e60-112">Optional.</span></span> <span data-ttu-id="b5e60-113">Чтобы использовать этот параметр, можно использовать любое из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b5e60-113">To use this parameter you can use any of the following values.</span></span> <span data-ttu-id="b5e60-114">Можно также указать несколько типов, разделяя их запятыми.</span><span class="sxs-lookup"><span data-stu-id="b5e60-114">You can also specify multiple types by separating them with commas.</span></span> <br/> <span data-ttu-id="b5e60-115">"**Get**"</span><span class="sxs-lookup"><span data-stu-id="b5e60-115">"**Get**"</span></span> <br/> <span data-ttu-id="b5e60-116">Для отмены всех запросов [**Get**](get-method.md) , помещенных в очередь.</span><span class="sxs-lookup"><span data-stu-id="b5e60-116">To stop all queued [**Get**](get-method.md) requests.</span></span><br/> <span data-ttu-id="b5e60-117">"**Нонкуеуеджет**"</span><span class="sxs-lookup"><span data-stu-id="b5e60-117">"**NonQueuedGet**"</span></span> <br/> <span data-ttu-id="b5e60-118">Для отмены всех запросов [**Get**](get-method.md) , не относящихся к очереди (метод **Get** с параметром **Queue** имеет значение **false**).</span><span class="sxs-lookup"><span data-stu-id="b5e60-118">To stop all non-queued [**Get**](get-method.md) requests (**Get** method with **Queue** parameter set to **False**).</span></span><br/> <span data-ttu-id="b5e60-119">"**Переместить**"</span><span class="sxs-lookup"><span data-stu-id="b5e60-119">"**Move**"</span></span> <br/> <span data-ttu-id="b5e60-120">Для отмены всех запросов [**MoveTo**](moveto-method.md) , помещенных в очередь.</span><span class="sxs-lookup"><span data-stu-id="b5e60-120">To stop all queued [**MoveTo**](moveto-method.md) requests.</span></span><br/> <span data-ttu-id="b5e60-121">"**Воспроизвести**"</span><span class="sxs-lookup"><span data-stu-id="b5e60-121">"**Play**"</span></span> <br/> <span data-ttu-id="b5e60-122">Для отмены всех запросов на [**Воспроизведение**](play-method.md) в очереди.</span><span class="sxs-lookup"><span data-stu-id="b5e60-122">To stop all queued [**Play**](play-method.md) requests.</span></span><br/> <span data-ttu-id="b5e60-123">«**Говорите**»</span><span class="sxs-lookup"><span data-stu-id="b5e60-123">"**Speak**"</span></span> <br/> <span data-ttu-id="b5e60-124">Чтобы прерывать все запросы, находящиеся в очереди, [**обговаривает**](speak-method.md) .</span><span class="sxs-lookup"><span data-stu-id="b5e60-124">To stop all queued [**Speak**](speak-method.md) requests.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5e60-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5e60-125">Remarks</span></span>

<span data-ttu-id="b5e60-126">Если параметр **типа** не задан, сервер останавливает все анимации для символа, включая очереди запросов на [**Получение**](get-method.md) , не являющиеся в очереди, и очищает ее очередь анимации.</span><span class="sxs-lookup"><span data-stu-id="b5e60-126">If you don't set the **Type** parameter, the server stops all animations for the character, including queued and non-queued [**Get**](get-method.md) requests, and clears its animation queue.</span></span> <span data-ttu-id="b5e60-127">Он также прекращает воспроизводить анимацию или скрытие символа.</span><span class="sxs-lookup"><span data-stu-id="b5e60-127">It also stops playing a character's Hiding or Showing animation.</span></span>

<span data-ttu-id="b5e60-128">Этот метод не создаст объект [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="b5e60-128">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5e60-129">См. также:</span><span class="sxs-lookup"><span data-stu-id="b5e60-129">See Also</span></span>

[<span data-ttu-id="b5e60-130">**Метод Stop**</span><span class="sxs-lookup"><span data-stu-id="b5e60-130">**Stop method**</span></span>](stop-method.md)


 

