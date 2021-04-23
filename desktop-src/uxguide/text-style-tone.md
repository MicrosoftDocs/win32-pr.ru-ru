---
title: Стиль и тон
description: Сигнал в написании — это отношение, которое модуль записи передает читателю.
ms.assetid: b9a03709-301f-46de-b4b4-0dd1214c0ed7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6009491b54de9035b253a10b9fd48f2233947104
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104554387"
---
# <a name="style-and-tone"></a><span data-ttu-id="b5c80-103">Стиль и тон</span><span class="sxs-lookup"><span data-stu-id="b5c80-103">Style and Tone</span></span>

> [!NOTE]
> <span data-ttu-id="b5c80-104">Это руководство по проектированию было создано для Windows 7 и не Обновлено для более новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="b5c80-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="b5c80-105">Многие рекомендации по-прежнему применяются в принципе, но презентация и примеры не соответствуют нашим [текущим руководствам по проектированию](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="b5c80-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="b5c80-106">Сигнал в написании — это отношение, которое модуль записи передает читателю.</span><span class="sxs-lookup"><span data-stu-id="b5c80-106">Tone in writing is the attitude that the writer conveys to the reader.</span></span> <span data-ttu-id="b5c80-107">Это не обязательно то, что вы говорите, но как вы говорите.</span><span class="sxs-lookup"><span data-stu-id="b5c80-107">It's not necessarily what you say, but how you say it.</span></span> <span data-ttu-id="b5c80-108">Тон предназначен для создания конкретного ответа или распознавания эмоций в модуле чтения; Он создает индивидуального пользователя, который может привлекать или стоек пользователей.</span><span class="sxs-lookup"><span data-stu-id="b5c80-108">Tone is intended to create a specific response or emotion in the reader; it creates a personality that can either engage or repel users.</span></span>

<span data-ttu-id="b5c80-109">**Примечание.** Рекомендации, связанные с [текстом пользовательского интерфейса](text-ui.md) , представлены в отдельной статье.</span><span class="sxs-lookup"><span data-stu-id="b5c80-109">**Note:** Guidelines related to [user interface text](text-ui.md) are presented in a separate article.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="b5c80-110">Принципы проектирования</span><span class="sxs-lookup"><span data-stu-id="b5c80-110">Design concepts</span></span>

### <a name="the-windows-tone"></a><span data-ttu-id="b5c80-111">Тон Windows</span><span class="sxs-lookup"><span data-stu-id="b5c80-111">The Windows tone</span></span>

<span data-ttu-id="b5c80-112">Используйте тон Windows, чтобы вдохновить уверенность, выполнив обмен данными с пользователями на личном уровне.</span><span class="sxs-lookup"><span data-stu-id="b5c80-112">Use the Windows tone to inspire confidence by communicating to users on a personal level by being accurate, encouraging, insightful, objective, and user focused.</span></span> <span data-ttu-id="b5c80-113">Тон Windows также стремится вдохновляющие, просто и заслуживает доверия.</span><span class="sxs-lookup"><span data-stu-id="b5c80-113">The Windows tone also strives to be light, inspiring, straightforward, and trustworthy.</span></span>

<span data-ttu-id="b5c80-114">Не используйте оттенок, по убыванию или аррогант.</span><span class="sxs-lookup"><span data-stu-id="b5c80-114">Don't use a distracting, condescending, or arrogant tone.</span></span> <span data-ttu-id="b5c80-115">Старайтесь не использовать голосовую передачу "машины" (где динамик удаляется из языка) и голос "Торговый представитель" (где написание попытается продать нам что-нибудь, чтобы кажоле нам, чтобы не усложнять нас, чтобы обойти все как "простые").</span><span class="sxs-lookup"><span data-stu-id="b5c80-115">Avoid the extremes of the "machine" voice (where the speaker is removed from the language) and the "sales rep" voice (where the writing tries to sell us something, to cajole us, to cheer us up, to gloss over everything as "simple.")</span></span>

<span data-ttu-id="b5c80-116">Исследование от корпорации Майкрософт показывает, что в программном обеспечении часто возникают следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="b5c80-116">Research from Microsoft shows that in software, there is often:</span></span>

-   <span data-ttu-id="b5c80-117">**Чрезмерное употребление терминологии компьютера и жаргоне,** которые многие пользователи не понимают или неверно распознает.</span><span class="sxs-lookup"><span data-stu-id="b5c80-117">**Overuse of computer terminology and jargon,** which many users don't understand or misinterpret.</span></span>
-   <span data-ttu-id="b5c80-118">**Несовместимость использования терминологии.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-118">**Inconsistent use of terminology.**</span></span>
-   <span data-ttu-id="b5c80-119">**Импенетрабле, часто непреднамеренно патронизинг сообщения,** которые пользователи испытывают при расшифровке.</span><span class="sxs-lookup"><span data-stu-id="b5c80-119">**Impenetrable, often unintentionally patronizing messages,** which users struggle to decipher.</span></span>

<span data-ttu-id="b5c80-120">Эти проблемы делают пользователей запутанными, неинтеллектуальными, дишеартенед и в конечном итоге отменяют их опыт работы с программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="b5c80-120">These problems make users feel confused, unintelligent, disheartened, and ultimately disengaged from their experience with software.</span></span>

<span data-ttu-id="b5c80-121">Обратите внимание на качество сообщения, включая тон текста, подразумевает, что сам язык является важным ингредиентом в общем удовлетворении клиента.</span><span class="sxs-lookup"><span data-stu-id="b5c80-121">Renewed attention to message quality, including the tone of the text, implies that language itself is an important ingredient in overall customer satisfaction.</span></span> <span data-ttu-id="b5c80-122">Поддержка пользователей с различными уровнями технических знаний, в частности новичков пользователей, для использования всех возможностей, которые может выполнять программа.</span><span class="sxs-lookup"><span data-stu-id="b5c80-122">Support users with different levels of technical knowledge, especially novice users, to take advantage of all the things your program can do.</span></span>

<span data-ttu-id="b5c80-123">**Если вы выполняете только одно действие...**</span><span class="sxs-lookup"><span data-stu-id="b5c80-123">**If you do only one thing...**</span></span>

<span data-ttu-id="b5c80-124">Убедитесь в том, что текст является точным, поощрением, объективным и ориентированным на пользователя.</span><span class="sxs-lookup"><span data-stu-id="b5c80-124">Make sure that your text is accurate, encouraging, insightful, objective, and user-focused.</span></span> <span data-ttu-id="b5c80-125">Будьте простыми и надежными и при необходимости используйте светло-и вдохновляющиеный тон.</span><span class="sxs-lookup"><span data-stu-id="b5c80-125">Be straightforward and trustworthy, and where appropriate use a light and inspiring tone.</span></span>

## <a name="guidelines"></a><span data-ttu-id="b5c80-126">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="b5c80-126">Guidelines</span></span>

### <a name="use-the-windows-tone"></a><span data-ttu-id="b5c80-127">Использование тона Windows</span><span class="sxs-lookup"><span data-stu-id="b5c80-127">Use the Windows tone</span></span>

<span data-ttu-id="b5c80-128">Звук в программе должен быть следующим:</span><span class="sxs-lookup"><span data-stu-id="b5c80-128">Tone in your program should be:</span></span>

-   <span data-ttu-id="b5c80-129">**Правильность.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-129">**Accurate.**</span></span> <span data-ttu-id="b5c80-130">Пользователи должны быть уверены в том, что данные технически точны.</span><span class="sxs-lookup"><span data-stu-id="b5c80-130">Users should feel reassured that the information is technically accurate.</span></span> <span data-ttu-id="b5c80-131">Если информация не точна, то опыт пользователя с этой конкретной задачей — развратил, и он теряется в случае любой другой помощи, читающей данные из этого источника.</span><span class="sxs-lookup"><span data-stu-id="b5c80-131">If the information isn't accurate, the user's experience with that specific task is spoiled, and he loses faith in any other assistance he reads from that source.</span></span>
-   <span data-ttu-id="b5c80-132">**Поощря.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-132">**Encouraging.**</span></span> <span data-ttu-id="b5c80-133">Используйте язык, который передает пользователям возможность выполнять нужные действия, а не позволяет им выполнять нужные действия.</span><span class="sxs-lookup"><span data-stu-id="b5c80-133">Use language that conveys that the software empowers users to do things, rather than allows them to do things.</span></span> <span data-ttu-id="b5c80-134">Например, можно использовать «можно», а не «Windows позволяет» или «эта функция позволяет».</span><span class="sxs-lookup"><span data-stu-id="b5c80-134">For example, use "you can" rather than "Windows lets you" or "this feature allows you."</span></span> <span data-ttu-id="b5c80-135">(Исключение: можно использовать "Allow" при ссылке на функции, такие как функции безопасности, которые разрешают или отклоняют действие.)</span><span class="sxs-lookup"><span data-stu-id="b5c80-135">(Exception: it's okay to use "allow" when referring to features—such as security features—that permit or deny an action.)</span></span>
-   <span data-ttu-id="b5c80-136">**Информативные.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-136">**Insightful.**</span></span> <span data-ttu-id="b5c80-137">Пользователи должны быть уверены, что вы (и расширение вашего приложения) узнаете, когда определенная задача осложняется и что вы будете с ними пошаговыми инструкциями.</span><span class="sxs-lookup"><span data-stu-id="b5c80-137">Users should believe that you (and by extension your application) know when a certain task is complicated and that you will guide them through it.</span></span> <span data-ttu-id="b5c80-138">В то же время рассматривайте пользователей как интеллектуальные пользователи, которым требуется помощь с определенной проблемой.</span><span class="sxs-lookup"><span data-stu-id="b5c80-138">At the same time, treat users as intelligent people who happen to need help with a particular problem.</span></span>
-   <span data-ttu-id="b5c80-139">**Функции.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-139">**Objective.**</span></span> <span data-ttu-id="b5c80-140">Иногда пользователям требуется более подробное объяснение. часто они просто хотят знать, что им нужно.</span><span class="sxs-lookup"><span data-stu-id="b5c80-140">Sometimes users want a richer explanation; often though they just want to know what they need to move on.</span></span> <span data-ttu-id="b5c80-141">Для этого требуется объективность, чтобы понять, что цель (производительность, любопытство, полноценному) является целью пользователя, а не модуля записи.</span><span class="sxs-lookup"><span data-stu-id="b5c80-141">This requires objectivity—to recognize that the goal (productivity, curiosity, enjoyment) is the user's goal, not the writer's.</span></span> <span data-ttu-id="b5c80-142">Также необходимо пролить все предуничтоженные идеи о пользователе.</span><span class="sxs-lookup"><span data-stu-id="b5c80-142">It also requires that you shed any predisposed notions about the user.</span></span>
-   <span data-ttu-id="b5c80-143">**Ориентированный на пользователя.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-143">**User-focused.**</span></span> <span data-ttu-id="b5c80-144">Напишите с точки зрения пользователя и предпочтительно с того, что можно сделать для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b5c80-144">Write from the user's perspective and preferably from the perspective of what you can do for the user.</span></span> <span data-ttu-id="b5c80-145">Пользователи должны иметь представление о том, что они могут найти важные и доступные для них сведения.</span><span class="sxs-lookup"><span data-stu-id="b5c80-145">Users should feel that they will find information that is relevant and accessible to them.</span></span>

<span data-ttu-id="b5c80-146">Вы можете дополнительно разрабатывать взаимодействие с пользователями, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b5c80-146">You can further develop communication with your users by being:</span></span>

-   <span data-ttu-id="b5c80-147">**Источник.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-147">**Light.**</span></span> <span data-ttu-id="b5c80-148">Легкая речь накажется легко работать с и быстро понимать.</span><span class="sxs-lookup"><span data-stu-id="b5c80-148">A light voice feels easy to deal with and quick to comprehend.</span></span> <span data-ttu-id="b5c80-149">Это не трудно или не утомительным, и это позволяет избежать снижения или серьезности сложности.</span><span class="sxs-lookup"><span data-stu-id="b5c80-149">It isn't difficult or burdensome, and it avoids straining to be profound or serious.</span></span>
-   <span data-ttu-id="b5c80-150">**Вдохновляющие.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-150">**Inspiring.**</span></span> <span data-ttu-id="b5c80-151">Вдохновляющиеный голоса мотивация для пользователей, плодотворного их для выполнения действий.</span><span class="sxs-lookup"><span data-stu-id="b5c80-151">An inspiring voice motivates users, stimulating them to take action.</span></span> <span data-ttu-id="b5c80-152">Определенный радуются помечает этот тип голоса, давая ему более привлекательную личность, чем у пользователей, похожих на компьютер, часто приходится ждать с компьютеров.</span><span class="sxs-lookup"><span data-stu-id="b5c80-152">A certain enthusiasm marks this kind of voice, giving it a more engaging personality than the machine-like tone users have often come to expect from their computers.</span></span>
-   <span data-ttu-id="b5c80-153">**Простым.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-153">**Straightforward.**</span></span> <span data-ttu-id="b5c80-154">Простая речь кандида и открыта бесплатно из предвременных или децеит.</span><span class="sxs-lookup"><span data-stu-id="b5c80-154">A straightforward voice is candid and open, free from pretense or deceit.</span></span>
-   <span data-ttu-id="b5c80-155">**Надежности.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-155">**Trustworthy.**</span></span> <span data-ttu-id="b5c80-156">Надежная речь — это достойной надежности, надежности, точности и честности.</span><span class="sxs-lookup"><span data-stu-id="b5c80-156">A trustworthy voice is worthy of confidence, reliable, accurate, and honest.</span></span> <span data-ttu-id="b5c80-157">Для потери доверия пользователя требуется лишь несколько неточностей, но получение доверия может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="b5c80-157">It only takes only a few inaccuracies to lose the user's trust, but it may take a long time to earn that trust back.</span></span>

<span data-ttu-id="b5c80-158">В отличие от этого, следует избегать следующих тонов, которые, скорее всего, получит отрицательную реакцию:</span><span class="sxs-lookup"><span data-stu-id="b5c80-158">By contrast, be sure to avoid the following tones, which are much more likely to receive a negative reaction:</span></span>

-   <span data-ttu-id="b5c80-159">**Компьютерный гудок.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-159">**Machine tone.**</span></span> <span data-ttu-id="b5c80-160">Похоже, у вас есть некоторая, негибкая система Exchange с компьютером или роботом.</span><span class="sxs-lookup"><span data-stu-id="b5c80-160">Feels like having an impersonal, inflexible exchange with a computer or robot.</span></span>
-   <span data-ttu-id="b5c80-161">**Корпоративный тон.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-161">**Corporate tone.**</span></span> <span data-ttu-id="b5c80-162">Похоже, что у вас есть монологуе с любым мощным, хорошо работающим корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b5c80-162">Feels like having a monologue with an all-powerful, all-knowing, impersonal corporation.</span></span>
-   <span data-ttu-id="b5c80-163">**Тон правоохранительных органов.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-163">**Law enforcement tone.**</span></span> <span data-ttu-id="b5c80-164">Вам кажется, что вы подписываетесь на ненавязчивые вопросы.</span><span class="sxs-lookup"><span data-stu-id="b5c80-164">Feels like being interrogated with a barrage of intrusive questions.</span></span>
-   <span data-ttu-id="b5c80-165">**Тон лаверли.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-165">**Lawyerly tone.**</span></span> <span data-ttu-id="b5c80-166">Вам кажется, что у вас есть запрос на выполнение некоторых законных значимых действий.</span><span class="sxs-lookup"><span data-stu-id="b5c80-166">Feels like being asked to perform some legally significant act.</span></span>
-   <span data-ttu-id="b5c80-167">**Сигнал торгового представителя.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-167">**Sales rep tone.**</span></span> <span data-ttu-id="b5c80-168">Вам кажется, что вам нужно купить или попробовать что-нибудь, и все возможные проблемы.</span><span class="sxs-lookup"><span data-stu-id="b5c80-168">Feels like being asked to buy or try something, with any concerns being glossed over.</span></span>
-   <span data-ttu-id="b5c80-169">**Старший, нисходящий или злостьный тон.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-169">**Superior, condescending, or angry tone.**</span></span> <span data-ttu-id="b5c80-170">Похоже, что это программное обеспечение белиттлинг пользователей, говорите с ними или обеспокоен с ними.</span><span class="sxs-lookup"><span data-stu-id="b5c80-170">Feels like the software is belittling users, talking down to them, or upset with them.</span></span> <span data-ttu-id="b5c80-171">Как правило, этот сигнал является очень техническим, выводит ненужное внимание на ошибки пользователя и является грубым.</span><span class="sxs-lookup"><span data-stu-id="b5c80-171">Typically, this tone is very technical, draws unnecessary attention to the user's mistakes, and feels rude.</span></span>
-   <span data-ttu-id="b5c80-172">**Тон боастфул.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-172">**Boastful tone.**</span></span> <span data-ttu-id="b5c80-173">Похоже, что программное обеспечение авторитетом о своих достижениях или иным образом может привлечь внимание к самому себе.</span><span class="sxs-lookup"><span data-stu-id="b5c80-173">Feels like the software is bragging about its accomplishments or otherwise drawing too much attention to itself.</span></span>
-   <span data-ttu-id="b5c80-174">**Перевернутый тон.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-174">**Flippant tone.**</span></span> <span data-ttu-id="b5c80-175">Кажется, что цели пользователей и эмоции не используются серьезно или их использование программой принимается для предоставления.</span><span class="sxs-lookup"><span data-stu-id="b5c80-175">Feels like users' goals and emotions aren't being taken seriously, or their use of the program is being take for granted.</span></span>

### <a name="use-real-world-language"></a><span data-ttu-id="b5c80-176">Использование реального языка</span><span class="sxs-lookup"><span data-stu-id="b5c80-176">Use real-world language</span></span>

-   <span data-ttu-id="b5c80-177">**Используйте повседневные слова, когда можете избежать слов, которые вы не хотите сказать другому пользователю.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-177">**Use everyday words when you can and avoid words you wouldn't say to someone else in person.**</span></span> <span data-ttu-id="b5c80-178">Это особенно эффективно, если вы объясняем сложную техническую концепцию или действие.</span><span class="sxs-lookup"><span data-stu-id="b5c80-178">This is especially effective if you are explaining a complex technical concept or action.</span></span> <span data-ttu-id="b5c80-179">Представьте себе, что вы просматриваете свое право пользователя и объясняете, как выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="b5c80-179">Imagine yourself looking over the user's shoulder and explaining how to accomplish the task.</span></span>

    <span data-ttu-id="b5c80-180">**Хорошо:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-180">**Acceptable:**</span></span>

    <span data-ttu-id="b5c80-181">Используйте эту процедуру для изменения пароля.</span><span class="sxs-lookup"><span data-stu-id="b5c80-181">Use this procedure to change your password.</span></span>

    <span data-ttu-id="b5c80-182">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-182">**Better:**</span></span>

    <span data-ttu-id="b5c80-183">Чтобы изменить пароль, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b5c80-183">Follow these steps to change your password.</span></span>

-   <span data-ttu-id="b5c80-184">**При возможности используйте короткие, простые слова.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-184">**Use short, plain words whenever possible.**</span></span> <span data-ttu-id="b5c80-185">Более короткие слова — это дополнительные беседы, экономия пространства на экране и их легче сканировать.</span><span class="sxs-lookup"><span data-stu-id="b5c80-185">Shorter words are more conversational, save space on screen, and are easier to scan.</span></span>

    <span data-ttu-id="b5c80-186">**Хорошо:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-186">**Acceptable:**</span></span>

    <span data-ttu-id="b5c80-187">Кроме того, в этом разделе показано...</span><span class="sxs-lookup"><span data-stu-id="b5c80-187">In addition, this section shows you...</span></span>

    <span data-ttu-id="b5c80-188">Цифровые камеры используют немелкие микросхемы...</span><span class="sxs-lookup"><span data-stu-id="b5c80-188">Digital cameras employ tiny microchips...</span></span>

    <span data-ttu-id="b5c80-189">Цифровые камеры используют крошечные микросхемы...</span><span class="sxs-lookup"><span data-stu-id="b5c80-189">Digital cameras utilize tiny microchips...</span></span>

    <span data-ttu-id="b5c80-190">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-190">**Better:**</span></span>

    <span data-ttu-id="b5c80-191">В этом разделе также показано...</span><span class="sxs-lookup"><span data-stu-id="b5c80-191">This section also shows you...</span></span>

    <span data-ttu-id="b5c80-192">Цифровые камеры используют немелкие микросхемы...</span><span class="sxs-lookup"><span data-stu-id="b5c80-192">Digital cameras use tiny microchips...</span></span>

-   <span data-ttu-id="b5c80-193">**Не выводят слова и не применяйте новые значения к стандартным словам.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-193">**Don't invent words or apply new meanings to standard words.**</span></span> <span data-ttu-id="b5c80-194">Предположим, что пользователи более знакомы с установленным словом, а не специальным значением, заданным в технологической отрасли.</span><span class="sxs-lookup"><span data-stu-id="b5c80-194">Assume that users are more familiar with a word's established meaning than with a special meaning given it by the technology industry.</span></span> <span data-ttu-id="b5c80-195">Если требуется термин отрасли, укажите в качестве определения в контексте.</span><span class="sxs-lookup"><span data-stu-id="b5c80-195">When an industry term is required, provide an in-context definition.</span></span> <span data-ttu-id="b5c80-196">Старайтесь не жаргоне, но помните, что некоторые выражения, характерные для использования компьютером (Хакер, запись компакт-диска и т. д.), уже являются частью повседневного распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="b5c80-196">Avoid jargon, but remember that some expressions specific to computer usage—hacker, burn a CD, and so on—are already part of everyday speech.</span></span>

    <span data-ttu-id="b5c80-197">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="b5c80-197">**Incorrect:**</span></span>

    <span data-ttu-id="b5c80-198">Папки можно использовать для разбить избранного.</span><span class="sxs-lookup"><span data-stu-id="b5c80-198">You can use folders to bucketize your favorites.</span></span>

    <span data-ttu-id="b5c80-199">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-199">**Correct:**</span></span>

    <span data-ttu-id="b5c80-200">Папки можно использовать для категоризации избранного.</span><span class="sxs-lookup"><span data-stu-id="b5c80-200">You can use folders to categorize your favorites.</span></span>

-   <span data-ttu-id="b5c80-201">**Не используйте символы в качестве замены для простых слов.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-201">**Don't use symbols as a substitute for simple words.**</span></span>

    <span data-ttu-id="b5c80-202">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="b5c80-202">**Incorrect:**</span></span>

    <span data-ttu-id="b5c80-203">Пользователи & компьютеры</span><span class="sxs-lookup"><span data-stu-id="b5c80-203">users & computers</span></span>

    <span data-ttu-id="b5c80-204">Пользователи и компьютеры</span><span class="sxs-lookup"><span data-stu-id="b5c80-204">users + computers</span></span>

    <span data-ttu-id="b5c80-205">домен или Рабочая группа</span><span class="sxs-lookup"><span data-stu-id="b5c80-205">domain / workgroup</span></span>

    <span data-ttu-id="b5c80-206">\# пользователей</span><span class="sxs-lookup"><span data-stu-id="b5c80-206">\# of users</span></span>

    <span data-ttu-id="b5c80-207">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-207">**Correct:**</span></span>

    <span data-ttu-id="b5c80-208">Пользователи и компьютеры</span><span class="sxs-lookup"><span data-stu-id="b5c80-208">users and computers</span></span>

    <span data-ttu-id="b5c80-209">домен или Рабочая группа</span><span class="sxs-lookup"><span data-stu-id="b5c80-209">domain or workgroup</span></span>

    <span data-ttu-id="b5c80-210">число пользователей</span><span class="sxs-lookup"><span data-stu-id="b5c80-210">number of users</span></span>

### <a name="be-precise"></a><span data-ttu-id="b5c80-211">Быть точным</span><span class="sxs-lookup"><span data-stu-id="b5c80-211">Be precise</span></span>

-   <span data-ttu-id="b5c80-212">Выберите слова с четким значением.</span><span class="sxs-lookup"><span data-stu-id="b5c80-212">Choose words with a clear meaning.</span></span>

    <span data-ttu-id="b5c80-213">**Хорошо:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-213">**Acceptable:**</span></span>

    <span data-ttu-id="b5c80-214">После создания таблицы можно внести в нее изменения.</span><span class="sxs-lookup"><span data-stu-id="b5c80-214">Since you created the table, you can make changes to it.</span></span>

    <span data-ttu-id="b5c80-215">Обеспечьте, чтобы брандмауэр был включен, так как его отключение может создать угрозу безопасности.</span><span class="sxs-lookup"><span data-stu-id="b5c80-215">Keep your firewall turned on, as turning it off could create a security risk.</span></span>

    <span data-ttu-id="b5c80-216">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-216">**Better:**</span></span>

    <span data-ttu-id="b5c80-217">Так как вы создали таблицу, вы можете внести в нее изменения.</span><span class="sxs-lookup"><span data-stu-id="b5c80-217">Because you created the table, you can make changes to it.</span></span>

    <span data-ttu-id="b5c80-218">Включите брандмауэр, так как его отключение может создать угрозу безопасности.</span><span class="sxs-lookup"><span data-stu-id="b5c80-218">Keep your firewall turned on, because turning it off could create a security risk.</span></span>

-   <span data-ttu-id="b5c80-219">Пропуск ненужных слов — не используйте два или три слова, когда оно будет сделано.</span><span class="sxs-lookup"><span data-stu-id="b5c80-219">Omit needless words—don't use two or three words when one will do.</span></span>

    <span data-ttu-id="b5c80-220">**Verbose**</span><span class="sxs-lookup"><span data-stu-id="b5c80-220">**Verbose:**</span></span>

    <span data-ttu-id="b5c80-221">Чтобы изменить пароль, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b5c80-221">Follow these steps in order to change your password:</span></span>

    <span data-ttu-id="b5c80-222">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-222">**Better:**</span></span>

    <span data-ttu-id="b5c80-223">Чтобы изменить пароль, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b5c80-223">To change your password:</span></span>

-   <span data-ttu-id="b5c80-224">Избегайте ненужных модификаторам.</span><span class="sxs-lookup"><span data-stu-id="b5c80-224">Avoid unnecessary adverbs.</span></span>

    <span data-ttu-id="b5c80-225">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="b5c80-225">**Incorrect:**</span></span>

    <span data-ttu-id="b5c80-226">Изменить пароль не так уж сложно.</span><span class="sxs-lookup"><span data-stu-id="b5c80-226">It isn't terribly hard to change your password.</span></span>

    <span data-ttu-id="b5c80-227">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-227">**Correct:**</span></span>

    <span data-ttu-id="b5c80-228">Изменить пароль несложно.</span><span class="sxs-lookup"><span data-stu-id="b5c80-228">It isn't hard to change your password.</span></span>

-   <span data-ttu-id="b5c80-229">Выберите команды, сопоставленные с одним словом, по командам из нескольких слов.</span><span class="sxs-lookup"><span data-stu-id="b5c80-229">Choose single-word verbs over multi-word verbs.</span></span>

    <span data-ttu-id="b5c80-230">**Хорошо:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-230">**Acceptable:**</span></span>

    <span data-ttu-id="b5c80-231">При блокировке компьютера...</span><span class="sxs-lookup"><span data-stu-id="b5c80-231">When you lock down your computer, ...</span></span>

    <span data-ttu-id="b5c80-232">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-232">**Better:**</span></span>

    <span data-ttu-id="b5c80-233">При блокировке компьютера...</span><span class="sxs-lookup"><span data-stu-id="b5c80-233">When you lock your computer, ...</span></span>

-   <span data-ttu-id="b5c80-234">Не преобразуйте глаголы в существительные и существительные в глаголы.</span><span class="sxs-lookup"><span data-stu-id="b5c80-234">Don't convert verbs to nouns and nouns to verbs.</span></span>

    <span data-ttu-id="b5c80-235">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="b5c80-235">**Incorrect:**</span></span>

    <span data-ttu-id="b5c80-236">Защита компьютера с помощью пароля...</span><span class="sxs-lookup"><span data-stu-id="b5c80-236">To password-protect your computer...</span></span>

    <span data-ttu-id="b5c80-237">Чтобы установить подключение...</span><span class="sxs-lookup"><span data-stu-id="b5c80-237">To establish connectivity...</span></span>

    <span data-ttu-id="b5c80-238">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-238">**Correct:**</span></span>

    <span data-ttu-id="b5c80-239">Защита компьютера с помощью пароля...</span><span class="sxs-lookup"><span data-stu-id="b5c80-239">To protect your computer with a password...</span></span>

    <span data-ttu-id="b5c80-240">Для подключения...</span><span class="sxs-lookup"><span data-stu-id="b5c80-240">To connect...</span></span>

### <a name="be-consistent"></a><span data-ttu-id="b5c80-241">Соблюдать единообразие</span><span class="sxs-lookup"><span data-stu-id="b5c80-241">Be consistent</span></span>

-   <span data-ttu-id="b5c80-242">Единая терминология способствует освоению и более глубокому пониманию технических концепций.</span><span class="sxs-lookup"><span data-stu-id="b5c80-242">Consistent terminology promotes learning and a better understanding of technical concepts.</span></span> <span data-ttu-id="b5c80-243">Несогласованность заставляет пользователей определить, означают ли разные слова и действия одно и то же действие.</span><span class="sxs-lookup"><span data-stu-id="b5c80-243">Inconsistency forces users to figure out whether different words and actions mean the same thing.</span></span>

    <span data-ttu-id="b5c80-244">Примеры:</span><span class="sxs-lookup"><span data-stu-id="b5c80-244">Examples:</span></span>

    <span data-ttu-id="b5c80-245">переключатель, переключатель</span><span class="sxs-lookup"><span data-stu-id="b5c80-245">switch, toggle</span></span>

    <span data-ttu-id="b5c80-246">Запуск, запуск, запуск, Загрузка, выполнение</span><span class="sxs-lookup"><span data-stu-id="b5c80-246">start, run, launch, boot, execute</span></span>

    <span data-ttu-id="b5c80-247">включить, активировать, включить</span><span class="sxs-lookup"><span data-stu-id="b5c80-247">enable, activate, turn on</span></span>

    <span data-ttu-id="b5c80-248">запись, копирование</span><span class="sxs-lookup"><span data-stu-id="b5c80-248">burn, copy</span></span>

-   <span data-ttu-id="b5c80-249">Последовательный синтаксис помогает установить ожидания пользователей.</span><span class="sxs-lookup"><span data-stu-id="b5c80-249">Consistent syntax helps set users' expectations.</span></span> <span data-ttu-id="b5c80-250">После установки этих ожиданий пользователи могут быстрее анализировать текст, использующий единообразный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="b5c80-250">Once these expectations are set, users can more quickly parse text that uses consistent syntax.</span></span> <span data-ttu-id="b5c80-251">Например, если инструкции всегда написаны в императивной форме, пользователи узнают о необходимости более тщательного рассмотрения императивных предложений.</span><span class="sxs-lookup"><span data-stu-id="b5c80-251">For example, if instructions are always written in the imperative form, users will learn to pay closer attention to imperative sentences.</span></span>

### <a name="contractions"></a><span data-ttu-id="b5c80-252">Сокращения</span><span class="sxs-lookup"><span data-stu-id="b5c80-252">Contractions</span></span>

-   <span data-ttu-id="b5c80-253">Контракты выдают более короткий, шустрее и более цикл для написания.</span><span class="sxs-lookup"><span data-stu-id="b5c80-253">Contractions lend a shorter, snappier, more conversational rhythm to writing.</span></span> <span data-ttu-id="b5c80-254">Используйте их в качестве подходящих и в контексте.</span><span class="sxs-lookup"><span data-stu-id="b5c80-254">Use them as appropriate and in context.</span></span> <span data-ttu-id="b5c80-255">Не используйте контракты с названиями продуктов или другими соответствующими существительными.</span><span class="sxs-lookup"><span data-stu-id="b5c80-255">Don't use contractions with product names or other proper nouns.</span></span>

### <a name="colloquialisms-idioms-and-slang"></a><span data-ttu-id="b5c80-256">Коллокуиалисмс, идиомы и сленговых выражений</span><span class="sxs-lookup"><span data-stu-id="b5c80-256">Colloquialisms, idioms, and slang</span></span>

-   <span data-ttu-id="b5c80-257">Рекомендуется использовать коллокуиалисмс или сленговых выражений только в особых ситуациях, таких как обзоры продуктов, экраны настройки или содержимое, которое не будет локализовано.</span><span class="sxs-lookup"><span data-stu-id="b5c80-257">Consider using colloquialisms or slang only in special situations, such as product tours, setup screens, or content that won't be localized.</span></span> <span data-ttu-id="b5c80-258">Последние исследования показали, что пользователи получили удовольствие от непредвиденного слова или знакомой фразы.</span><span class="sxs-lookup"><span data-stu-id="b5c80-258">Recent studies have shown that users enjoy the unexpected word or familiar phrase.</span></span> <span data-ttu-id="b5c80-259">Помните, что использование коллокуиалисмс и сленговых выражений может быть трудным и дорогостоящим для эффективного преобразования, поэтому такой язык лучше использовать разумно.</span><span class="sxs-lookup"><span data-stu-id="b5c80-259">Bear in mind that using colloquialisms and slang can be difficult and costly to translate effectively, so such language is best used judiciously.</span></span>

    <span data-ttu-id="b5c80-260">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-260">**Examples:**</span></span>

    <span data-ttu-id="b5c80-261">С другой стороны, в реестре есть определенные значения, которые не должны изменяться.</span><span class="sxs-lookup"><span data-stu-id="b5c80-261">On the other hand, there are certain values in the registry that shouldn't be changed.</span></span>

    <span data-ttu-id="b5c80-262">При использовании СДСЛ эта линия выделяется для использования в Интернете, поэтому вы не сможете использовать ДТП трафик в Интернете, как и в случае со службой кабелей.</span><span class="sxs-lookup"><span data-stu-id="b5c80-262">With SDSL, the line is dedicated to your Internet use, so you won't experience rush-hour traffic jams on the Internet, as you might with cable service.</span></span>

### <a name="person"></a><span data-ttu-id="b5c80-263">Человек</span><span class="sxs-lookup"><span data-stu-id="b5c80-263">Person</span></span>

-   <span data-ttu-id="b5c80-264">**Непосредственное или косвенное обращение к пользователю.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-264">**Address the user as you, directly or indirectly.**</span></span>
-   <span data-ttu-id="b5c80-265">**Используйте второй человек (вы, ваш), чтобы сообщить пользователям, что делать.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-265">**Use the second person (you, your) to tell users what to do.**</span></span> <span data-ttu-id="b5c80-266">Часто используется второе лицо.</span><span class="sxs-lookup"><span data-stu-id="b5c80-266">Often the second person is implied.</span></span>

    <span data-ttu-id="b5c80-267">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-267">**Examples:**</span></span>

    <span data-ttu-id="b5c80-268">Выберите изображения, которые нужно напечатать.</span><span class="sxs-lookup"><span data-stu-id="b5c80-268">Choose the pictures you want to print.</span></span>

    <span data-ttu-id="b5c80-269">Выберите учетную запись.</span><span class="sxs-lookup"><span data-stu-id="b5c80-269">Choose an account.</span></span> <span data-ttu-id="b5c80-270">предполагаем</span><span class="sxs-lookup"><span data-stu-id="b5c80-270">(implied)</span></span>

-   <span data-ttu-id="b5c80-271">**Используйте первого пользователя (I, Me, My), чтобы позволить пользователям сообщить программе, что делать.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-271">**Use the first person (I, me, my) to let users tell the program what to do.**</span></span>

    <span data-ttu-id="b5c80-272">**Пример**.</span><span class="sxs-lookup"><span data-stu-id="b5c80-272">**Example:**</span></span>

    <span data-ttu-id="b5c80-273">Печать фотографий на камере.</span><span class="sxs-lookup"><span data-stu-id="b5c80-273">Print the photos on my camera.</span></span>

-   <span data-ttu-id="b5c80-274">**Используйте с осторожностью.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-274">**Use we judiciously.**</span></span> <span data-ttu-id="b5c80-275">Во множественном числе первых пользователей можно предложить нетрудное корпоративное присутствие.</span><span class="sxs-lookup"><span data-stu-id="b5c80-275">The first-person plural can suggest a daunting corporate presence.</span></span> <span data-ttu-id="b5c80-276">Однако может быть предпочтительнее использовать имя приложения.</span><span class="sxs-lookup"><span data-stu-id="b5c80-276">However, it can be preferable to using the name of your application.</span></span> <span data-ttu-id="b5c80-277">Рекомендуется использовать вместо него рекомендуемый вариант.</span><span class="sxs-lookup"><span data-stu-id="b5c80-277">Use we recommend rather than it is recommended.</span></span>
-   <span data-ttu-id="b5c80-278">**Не используйте ссылки на сторонние лица (пользователь)** , так как они создают более формальный, менее личный тон.</span><span class="sxs-lookup"><span data-stu-id="b5c80-278">**Avoid third-person references (the user)** because they create a more formal, less personal tone.</span></span>

### <a name="voice"></a><span data-ttu-id="b5c80-279">Голосовая связь</span><span class="sxs-lookup"><span data-stu-id="b5c80-279">Voice</span></span>

-   <span data-ttu-id="b5c80-280">**Используйте активный голосовое значение,** которое подчеркивает пользователя или предмет действия.</span><span class="sxs-lookup"><span data-stu-id="b5c80-280">**Use the active voice,** which emphasizes the person or thing doing the action.</span></span> <span data-ttu-id="b5c80-281">Он является более прямым и личным по сравнению с пассивным голосовым, что может быть запутанным или формальным.</span><span class="sxs-lookup"><span data-stu-id="b5c80-281">It is more direct and personal than the passive voice, which can be confusing or sound formal.</span></span>

    <span data-ttu-id="b5c80-282">**Хорошо:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-282">**Acceptable:**</span></span>

    <span data-ttu-id="b5c80-283">Значки можно упорядочить по именам в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="b5c80-283">Icons can be arranged by name in alphabetical order.</span></span>

    <span data-ttu-id="b5c80-284">При подключении персонального цифрового помощника (PDA) или ноутбука...</span><span class="sxs-lookup"><span data-stu-id="b5c80-284">When a Personal Digital Assistant (PDA) or laptop is plugged in...</span></span>

    <span data-ttu-id="b5c80-285">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-285">**Better:**</span></span>

    <span data-ttu-id="b5c80-286">Значки можно упорядочить в алфавитном порядке по имени значка.</span><span class="sxs-lookup"><span data-stu-id="b5c80-286">You can arrange icons in alphabetical order by the icon name.</span></span>

    <span data-ttu-id="b5c80-287">При подключении любого личного цифрового помощника (PDA) или ноутбука...</span><span class="sxs-lookup"><span data-stu-id="b5c80-287">When you plug in any Personal Digital Assistant (PDA) or laptop...</span></span>

-   <span data-ttu-id="b5c80-288">Используйте пассивный голосовое значение, чтобы избежать появления слова или неудобного построения; когда фокус находится на предложении, а не на злодея. Если тема неизвестна; или в сообщениях об ошибках, когда пользователь является субъектом и может быть изменен на ошибку, если использовались Активные голоса.</span><span class="sxs-lookup"><span data-stu-id="b5c80-288">Use the passive voice only to avoid a wordy or awkward construction; when the action rather than the doer is the focus of the sentence; when the subject is unknown; or in error messages, when the user is the subject and might feel blamed for the error if the active voice were used.</span></span>

    <span data-ttu-id="b5c80-289">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-289">**Correct:**</span></span>

    <span data-ttu-id="b5c80-290">В левом верхнем углу должен появиться новый значок.</span><span class="sxs-lookup"><span data-stu-id="b5c80-290">The new icon should appear in the upper-left corner.</span></span>

    <span data-ttu-id="b5c80-291">Прежде чем они смогут работать, необходимо загрузить и установить обновления.</span><span class="sxs-lookup"><span data-stu-id="b5c80-291">Updates must be downloaded and installed before they can work.</span></span>

-   <span data-ttu-id="b5c80-292">**Инструкции фразы в положительной форме** и Акцентируйте внимание на том, что пользователи могут выполнять, а не на их невозможности.</span><span class="sxs-lookup"><span data-stu-id="b5c80-292">**Phrase statements in the positive form**, and emphasize what users can accomplish, rather than what they can't.</span></span>

### <a name="attitude-toward-the-user"></a><span data-ttu-id="b5c80-293">Отношение к пользователю</span><span class="sxs-lookup"><span data-stu-id="b5c80-293">Attitude toward the user</span></span>

-   <span data-ttu-id="b5c80-294">**Будьте в повежливо, поддержке и поощрении.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-294">**Be polite, supportive, and encouraging.**</span></span> <span data-ttu-id="b5c80-295">Пользователь никогда не должен иметь права на изменен или пугайтесь.</span><span class="sxs-lookup"><span data-stu-id="b5c80-295">The user should never feel condescended to, blamed, or intimidated.</span></span>

    <span data-ttu-id="b5c80-296">**Хорошо:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-296">**Acceptable:**</span></span>

    <span data-ttu-id="b5c80-297">Невозможно удалить новый текстовый документ: отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="b5c80-297">Cannot delete New Text Document: Access is denied.</span></span>

    <span data-ttu-id="b5c80-298">**Лучше:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-298">**Better:**</span></span>

    <span data-ttu-id="b5c80-299">Этот файл защищен и не может быть удален без конкретного разрешения.</span><span class="sxs-lookup"><span data-stu-id="b5c80-299">This file is protected and cannot be deleted without specific permission.</span></span>

-   <span data-ttu-id="b5c80-300">**Подчеркивание правильного баланса: Будьте в направлении к пользователю, не слишком глубоким или не имеющим в бизнесе.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-300">**Strike the right balance: be warm toward the user without being too intimate or too business-like.**</span></span> <span data-ttu-id="b5c80-301">Представьте, что вы помогаете другу использовать продукт в первый раз.</span><span class="sxs-lookup"><span data-stu-id="b5c80-301">Imagine that you are helping a friend use the product for the first time.</span></span> <span data-ttu-id="b5c80-302">Этот человек не является ни дружественным, ни существенным другим, а, наоборот, соседним или близким к другу.</span><span class="sxs-lookup"><span data-stu-id="b5c80-302">This person is not your best friend or significant other, but instead, a neighbor or family friend.</span></span> <span data-ttu-id="b5c80-303">Пользователи должны быть знакомы и дома при использовании программы, но язык не должен быть пресумптуаус или слишком знаком.</span><span class="sxs-lookup"><span data-stu-id="b5c80-303">Users should feel comfortable and at home when using your program, but the language should not feel presumptuous or too familiar.</span></span>
-   <span data-ttu-id="b5c80-304">**Предельное число ситуаций, в которых пользователь неудобство,** например:</span><span class="sxs-lookup"><span data-stu-id="b5c80-304">**Limit please to situations that inconvenience the user in some way,** such as:</span></span>

    -   <span data-ttu-id="b5c80-305">Пользователю предлагается сделать что-то неудобное, например подождать, повторить задачу или обновить программу.</span><span class="sxs-lookup"><span data-stu-id="b5c80-305">The user is asked to do something inconvenient, such as waiting, repeating a task or updating a program.</span></span>

        <span data-ttu-id="b5c80-306">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-306">**Correct:**</span></span>

        <span data-ttu-id="b5c80-307">Подождите, пока Windows скопирует файлы на компьютер.</span><span class="sxs-lookup"><span data-stu-id="b5c80-307">Please wait while Windows copies the files to your computer.</span></span>

    -   <span data-ttu-id="b5c80-308">Пользователь не может выполнить задачу из-за отсутствия компонента, недостатка проектирования или ошибки программы.</span><span class="sxs-lookup"><span data-stu-id="b5c80-308">The user can't complete a task because of a missing feature, design flaw, or program bug.</span></span>

        <span data-ttu-id="b5c80-309">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-309">**Correct:**</span></span>

        <span data-ttu-id="b5c80-310">Не удается сохранить с использованием указанного формата.</span><span class="sxs-lookup"><span data-stu-id="b5c80-310">Unable to save using the specified format.</span></span> <span data-ttu-id="b5c80-311">Выберите другой формат.</span><span class="sxs-lookup"><span data-stu-id="b5c80-311">Please select another format.</span></span>

    -   <span data-ttu-id="b5c80-312">Пользователь больше не должен быть полезен, так как участвует в программе обратной связи с клиентами или при составлении отчета об ошибках.</span><span class="sxs-lookup"><span data-stu-id="b5c80-312">The user has gone out of his or her way to be helpful, as by participating in a customer feedback program or filing a bug report.</span></span>

        <span data-ttu-id="b5c80-313">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-313">**Correct:**</span></span>

        <span data-ttu-id="b5c80-314">Чтобы улучшить процесс резервного копирования Fabrikam, примите участие в программе "Отзывы пользователей" компании Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="b5c80-314">To improve the Fabrikam Backup experience, please participate in the Fabrikam customer feedback program.</span></span>

    <span data-ttu-id="b5c80-315">Также следует использовать, если его отсутствие будет считаться Курт.</span><span class="sxs-lookup"><span data-stu-id="b5c80-315">You should also use please whenever its absence would be considered curt.</span></span>

    ![<span data-ttu-id="b5c80-316">снимок экрана с инструкциями, начинающимися с.</span><span class="sxs-lookup"><span data-stu-id="b5c80-316">screen shot of directions beginning with please</span></span> ](images/text-style-tone-image1.png)

    <span data-ttu-id="b5c80-317">В этом примере встроенные сообщения об ошибках будут Курт без.</span><span class="sxs-lookup"><span data-stu-id="b5c80-317">In this example, the inline error messages would be curt without please.</span></span>

-   <span data-ttu-id="b5c80-318">**Приносим извинения только к сообщениям об ошибках, которые приводят к серьезным проблемам пользователя** (например, к потери данных, пользователь не может продолжать использовать компьютер, или пользователь должен получить помощь от технического представителя).</span><span class="sxs-lookup"><span data-stu-id="b5c80-318">**Use sorry only in error messages that result in serious problems for the user** (for example, data loss, the user can't continue to use the computer, or the user must get help from a technical representative).</span></span> <span data-ttu-id="b5c80-319">Не приносим извинения, если во время нормальной работы программы возникла ошибка (например, если пользователь должен дождаться обнаружения сетевого подключения).</span><span class="sxs-lookup"><span data-stu-id="b5c80-319">Don't apologize if the issue occurred during the normal functioning of the program (for example, if the user needs to wait for a network connection to be found).</span></span>

    <span data-ttu-id="b5c80-320">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-320">**Correct:**</span></span>

    <span data-ttu-id="b5c80-321">К сожалению, при резервном копировании Fabrikam возникла неустранимая проблема. работа была завершена.</span><span class="sxs-lookup"><span data-stu-id="b5c80-321">We're sorry, but Fabrikam Backup detected an unrecoverable problem and was shut down.</span></span>

### <a name="sentence-structure-and-length"></a><span data-ttu-id="b5c80-322">Структура и длина предложения</span><span class="sxs-lookup"><span data-stu-id="b5c80-322">Sentence structure and length</span></span>

-   <span data-ttu-id="b5c80-323">Так как пользователи часто проверяют текст, **вынимайте все слова.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-323">Because users often scan text, **make every word count.**</span></span> <span data-ttu-id="b5c80-324">Простые и краткие предложения (и абзацы) не только сохраняют место на экране, но и являются наиболее эффективными средствами передачи идеи или действия.</span><span class="sxs-lookup"><span data-stu-id="b5c80-324">Simple, concise sentences (and paragraphs) not only save space on the screen but are the most effective means of conveying that an idea or action is important.</span></span> <span data-ttu-id="b5c80-325">Используйте свои лучшие решения — делайте предложения строго, но не так плотнее, что тон кажется внезапно понятным и недружественным.</span><span class="sxs-lookup"><span data-stu-id="b5c80-325">Use your best judgment—make sentences tight, but not so tight that the tone seems abrupt and unfriendly.</span></span>
-   <span data-ttu-id="b5c80-326">**Избегайте повторения.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-326">**Avoid repetition.**</span></span> <span data-ttu-id="b5c80-327">Проверьте каждое окно и удалите дублирующиеся слова и инструкции.</span><span class="sxs-lookup"><span data-stu-id="b5c80-327">Review each window and eliminate duplicate words and statements.</span></span> <span data-ttu-id="b5c80-328">Не следует избегать важного текста — будьте явными при необходимости, но не должны быть избыточными и не объясним вещи, которые не говорят.</span><span class="sxs-lookup"><span data-stu-id="b5c80-328">Don't avoid important text—be explicit whenever necessary—but don't be redundant and don't explain things that go without saying.</span></span>
-   <span data-ttu-id="b5c80-329">**При необходимости используйте фрагменты предложений.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-329">**Use sentence fragments if appropriate.**</span></span> <span data-ttu-id="b5c80-330">Фрагменты предложений являются короткими и перфорациями — и, как правило, они принимают опросную форму, они являются хорошим способом непосредственного привлечения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b5c80-330">Sentence fragments are short and punchy—and, as they typically take the interrogative form, they are a good way of directly engaging the user.</span></span>

    <span data-ttu-id="b5c80-331">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-331">**Correct:**</span></span>

    <span data-ttu-id="b5c80-332">Сохранить изменения в "моих фотографиях"?</span><span class="sxs-lookup"><span data-stu-id="b5c80-332">Save changes to "My Photos"?</span></span>

    <span data-ttu-id="b5c80-333">Когда-либо сохраняли файл и не сохранили его там, где он был сохранен?</span><span class="sxs-lookup"><span data-stu-id="b5c80-333">Ever saved a file and then not remembered where you saved it?</span></span>

-   <span data-ttu-id="b5c80-334">При необходимости **начинайте предложения с помощью сочетании** (и, но или).</span><span class="sxs-lookup"><span data-stu-id="b5c80-334">**Start sentences with conjunctions** (and, but, or) if you need to.</span></span>
-   <span data-ttu-id="b5c80-335">**Подстановочные списки и таблицы для сложных предложений.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-335">**Substitute lists and tables for complex sentences.**</span></span> <span data-ttu-id="b5c80-336">Списки (нумерованные или маркированные) и таблицы более понятны и более просты для просмотра.</span><span class="sxs-lookup"><span data-stu-id="b5c80-336">Lists (whether numbered or bulleted) and tables are clearer and easier to scan.</span></span>
-   <span data-ttu-id="b5c80-337">**Используйте параллельные грамматические конструкции.**</span><span class="sxs-lookup"><span data-stu-id="b5c80-337">**Use parallel grammatical constructions.**</span></span> <span data-ttu-id="b5c80-338">Для параллелизма требуется, чтобы слова и фразы, имеющие одну и ту же функцию, имели одну и ту же форму.</span><span class="sxs-lookup"><span data-stu-id="b5c80-338">Parallelism requires that words and phrases that have the same function have the same form.</span></span> <span data-ttu-id="b5c80-339">Используйте параллельный язык, когда вы выражаете идеи одинакового веса и для элементов пользовательского интерфейса, которые работают параллельно (например, заголовки, метки, списки или заголовки страниц).</span><span class="sxs-lookup"><span data-stu-id="b5c80-339">Use parallel language whenever you express ideas of equal weight, and for UI elements that are parallel in function (such as headings, labels, lists, or page titles).</span></span>

    <span data-ttu-id="b5c80-340">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="b5c80-340">**Correct:**</span></span>

    <span data-ttu-id="b5c80-341">Прослушивание</span><span class="sxs-lookup"><span data-stu-id="b5c80-341">Listen</span></span>

    <span data-ttu-id="b5c80-342">Watch</span><span class="sxs-lookup"><span data-stu-id="b5c80-342">Watch</span></span>

    <span data-ttu-id="b5c80-343">Поделиться</span><span class="sxs-lookup"><span data-stu-id="b5c80-343">Share</span></span>

    <span data-ttu-id="b5c80-344">Collect</span><span class="sxs-lookup"><span data-stu-id="b5c80-344">Collect</span></span>

    <span data-ttu-id="b5c80-345">Эти элементы являются параллельными, так как все они являются одним словом, императивными глаголами.</span><span class="sxs-lookup"><span data-stu-id="b5c80-345">These items are parallel because they are all single-word, imperative verbs.</span></span>

    <span data-ttu-id="b5c80-346">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="b5c80-346">**Incorrect:**</span></span>

    <span data-ttu-id="b5c80-347">Музыка</span><span class="sxs-lookup"><span data-stu-id="b5c80-347">Music</span></span>

    <span data-ttu-id="b5c80-348">Видео</span><span class="sxs-lookup"><span data-stu-id="b5c80-348">Video</span></span>

    <span data-ttu-id="b5c80-349">Поделиться</span><span class="sxs-lookup"><span data-stu-id="b5c80-349">Share</span></span>

    <span data-ttu-id="b5c80-350">Прослушивание</span><span class="sxs-lookup"><span data-stu-id="b5c80-350">Listen</span></span>

    <span data-ttu-id="b5c80-351">Эти элементы не параллельны, так как музыкальные и видеозаписи являются существительными, а совместное использование и прослушивание являются глаголами.</span><span class="sxs-lookup"><span data-stu-id="b5c80-351">These items are not parallel because Music and Video are nouns, but Share and Listen are verbs.</span></span>

 

 