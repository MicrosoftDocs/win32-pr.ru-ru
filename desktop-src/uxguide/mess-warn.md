---
title: Предупреждающие сообщения
description: Предупреждающее сообщение — это модальное диалоговое окно, сообщение на месте, уведомление или всплывающее оповещение, которое предупреждает пользователя о том, что условие может привести к возникновению проблемы в будущем.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 42f7c669a68790ec290f931165b4aa937b5008d5
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524508"
---
# <a name="warning-messages"></a><span data-ttu-id="a3721-103">Предупреждающие сообщения</span><span class="sxs-lookup"><span data-stu-id="a3721-103">Warning Messages</span></span>

> [!NOTE]
> <span data-ttu-id="a3721-104">Это руководство по проектированию было создано для Windows 7 и не Обновлено для более новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="a3721-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="a3721-105">Многие рекомендации по-прежнему применяются в принципе, но презентация и примеры не соответствуют нашим [текущим руководствам по проектированию](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="a3721-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="a3721-106">Предупреждающее сообщение — это модальное диалоговое окно, сообщение на месте, уведомление или всплывающее оповещение, которое предупреждает пользователя о том, что условие может привести к возникновению проблемы в будущем.</span><span class="sxs-lookup"><span data-stu-id="a3721-106">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span>

![снимок экрана типичного предупреждающего сообщения](images/mess-warn-image1.png)

<span data-ttu-id="a3721-108">Типичное модальное предупреждающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="a3721-108">A typical modal warning message.</span></span>

<span data-ttu-id="a3721-109">Основная характеристика предупреждений заключается в том, что они связаны с риском потери одного или нескольких из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="a3721-109">The fundamental characteristic of warnings is that they involve the risk of losing one or more of the following:</span></span>

-   <span data-ttu-id="a3721-110">Ценный ресурс, например важные финансовые или другие данные.</span><span class="sxs-lookup"><span data-stu-id="a3721-110">A valuable asset, such as important financial or other data.</span></span>
-   <span data-ttu-id="a3721-111">Системный доступ или целостность.</span><span class="sxs-lookup"><span data-stu-id="a3721-111">System access or integrity.</span></span>
-   <span data-ttu-id="a3721-112">Конфиденциальность или контроль над конфиденциальной информацией.</span><span class="sxs-lookup"><span data-stu-id="a3721-112">Privacy or control over confidential information.</span></span>
-   <span data-ttu-id="a3721-113">Время пользователя (значительный объем, например 30 секунд или более).</span><span class="sxs-lookup"><span data-stu-id="a3721-113">User's time (a significant amount, such as 30 seconds or more).</span></span>

<span data-ttu-id="a3721-114">В отличие от этого, подтверждение — это модальное диалоговое окно с запросом о том, что пользователь хочет продолжить работу с действием.</span><span class="sxs-lookup"><span data-stu-id="a3721-114">By contrast, a confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span> <span data-ttu-id="a3721-115">Некоторые типы предупреждений представляются в виде подтверждений, и если да, то также применяются рекомендации по подтверждению.</span><span class="sxs-lookup"><span data-stu-id="a3721-115">Some types of warnings are presented as confirmations, and if so, the confirmation guidelines also apply.</span></span>

<span data-ttu-id="a3721-116">**Примечание.** Рекомендации, связанные с [диалоговыми окнами](win-dialog-box.md), [подтверждениями](mess-confirm.md), [сообщениями об ошибках](mess-error.md)[стандартные значки](vis-std-icons.md), [уведомления](mess-notif.md)и [Макет](vis-layout.md) , представлены в отдельных статьях.</span><span class="sxs-lookup"><span data-stu-id="a3721-116">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [confirmations](mess-confirm.md), [error messages](mess-error.md)[standard icons](vis-std-icons.md), [notifications](mess-notif.md), and [layout](vis-layout.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="a3721-117">Это правильный пользовательский интерфейс?</span><span class="sxs-lookup"><span data-stu-id="a3721-117">Is this the right user interface?</span></span>

<span data-ttu-id="a3721-118">Чтобы определиться, ответьте на вопросы:</span><span class="sxs-lookup"><span data-stu-id="a3721-118">To decide, consider these questions:</span></span>

-   <span data-ttu-id="a3721-119">**Пользователь оповещает о условии, что может привести к возникновению проблемы в будущем?**</span><span class="sxs-lookup"><span data-stu-id="a3721-119">**Is the user being alerted of a condition that might cause a problem in the future?**</span></span> <span data-ttu-id="a3721-120">В противном случае сообщение не является предупреждением.</span><span class="sxs-lookup"><span data-stu-id="a3721-120">If not, the message isn't a warning.</span></span>
-   <span data-ttu-id="a3721-121">**Отображается ли в пользовательском интерфейсе ошибка или проблема, которые уже произошли?**</span><span class="sxs-lookup"><span data-stu-id="a3721-121">**Is the UI presenting an error or problem that has already occurred?**</span></span> <span data-ttu-id="a3721-122">В этом случае следует использовать сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a3721-122">If so, use an error message instead.</span></span>
-   <span data-ttu-id="a3721-123">**Могут ли пользователи выполнить действие или изменить их поведение в результате сообщения?**</span><span class="sxs-lookup"><span data-stu-id="a3721-123">**Are users likely to perform an action or change their behavior as the result of the message?**</span></span> <span data-ttu-id="a3721-124">В противном случае условие не будет выдавать прерывание пользователя, поэтому лучше отключить это предупреждение.</span><span class="sxs-lookup"><span data-stu-id="a3721-124">If not, the condition doesn't justify interrupting the user so it's better to suppress the warning.</span></span>
-   <span data-ttu-id="a3721-125">**Является ли условие прямым результатом действия, инициированного пользователем?**</span><span class="sxs-lookup"><span data-stu-id="a3721-125">**Is the condition the direct result of an action initiated by the user?**</span></span> <span data-ttu-id="a3721-126">В противном случае рассмотрите возможность использования [некритических уведомлений о событиях](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="a3721-126">If not, consider using a [non-critical event notifications](mess-notif.md).</span></span>
-   <span data-ttu-id="a3721-127">**Является ли условие особым условием в элементе управления?**</span><span class="sxs-lookup"><span data-stu-id="a3721-127">**Is the condition a special condition in a control?**</span></span> <span data-ttu-id="a3721-128">Если это так, используйте [всплывающую подсказку](ctrl-balloons.md) .</span><span class="sxs-lookup"><span data-stu-id="a3721-128">If so, use a [balloon](ctrl-balloons.md) instead.</span></span>
-   <span data-ttu-id="a3721-129">**Для подтверждений пользователь собирается выполнить опасное действие?**</span><span class="sxs-lookup"><span data-stu-id="a3721-129">**For confirmations, is the user about to perform a risky action?**</span></span> <span data-ttu-id="a3721-130">Если это так, предупреждение подходит, если действие имеет значительные последствия или не может быть легко отменено.</span><span class="sxs-lookup"><span data-stu-id="a3721-130">If so, a warning is appropriate if the action has significant consequences or cannot be easily undone.</span></span>
-   <span data-ttu-id="a3721-131">**Для других типов предупреждений пользователь должен действовать сейчас или в немедленном будущем?**</span><span class="sxs-lookup"><span data-stu-id="a3721-131">**For other types of warnings, does the user need to act now or in the immediate future?**</span></span> <span data-ttu-id="a3721-132">Не отображать предупреждения, если пользователи могут продолжить работу без немедленной работы.</span><span class="sxs-lookup"><span data-stu-id="a3721-132">Don't display warnings if users can continue to work productively without immediate problems.</span></span> <span data-ttu-id="a3721-133">Отложите предупреждение, пока условие не станет более непосредственным и релевантным.</span><span class="sxs-lookup"><span data-stu-id="a3721-133">Postpone the warning until the condition is more immediate and relevant.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="a3721-134">Принципы проектирования</span><span class="sxs-lookup"><span data-stu-id="a3721-134">Design concepts</span></span>

### <a name="avoid-overwarning"></a><span data-ttu-id="a3721-135">Избегайте превышения пороговых предупреждений</span><span class="sxs-lookup"><span data-stu-id="a3721-135">Avoid overwarning</span></span>

<span data-ttu-id="a3721-136">Мы передавали предупреждение в программах Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a3721-136">We overwarn in Microsoft Windows programs.</span></span> <span data-ttu-id="a3721-137">Типичная программа Windows имеет предупреждения везде, что не слишком важно.</span><span class="sxs-lookup"><span data-stu-id="a3721-137">The typical Windows program has warnings seemingly everywhere, warning about things that have little significance.</span></span> <span data-ttu-id="a3721-138">В некоторых программах практически все вопросы представляются как предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a3721-138">In some programs, nearly every question is presented as a warning.</span></span> <span data-ttu-id="a3721-139">Перепредупреждение делает использование программы похоже на опасное действие, и оно рассылает от действительно значимых проблем.</span><span class="sxs-lookup"><span data-stu-id="a3721-139">Overwarning makes using a program feel like a hazardous activity, and it detracts from truly significant issues.</span></span>

<span data-ttu-id="a3721-140">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="a3721-140">**Incorrect:**</span></span>

![<span data-ttu-id="a3721-141">снимок экрана с ненужным предупреждающим сообщением</span><span class="sxs-lookup"><span data-stu-id="a3721-141">screen shot of an unnecessary warning message</span></span> ](images/mess-warn-image2.png)

<span data-ttu-id="a3721-142">Переупреждающее приложение делает вашу программу опасной и выглядит так, как она была разработана юристы беспокоились.</span><span class="sxs-lookup"><span data-stu-id="a3721-142">Overwarning makes your program feel hazardous and look like it was designed by lawyers.</span></span>

<span data-ttu-id="a3721-143">Достаточно возможной потери данных или только будущей проблемы недостаточно для вызова предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a3721-143">The mere potential for data loss or a future problem alone is insufficient to call for a warning.</span></span> <span data-ttu-id="a3721-144">Кроме того, нежелательные результаты должны быть непредвиденными или непреднамеренно, и их легко исправить.</span><span class="sxs-lookup"><span data-stu-id="a3721-144">Additionally, any undesirable results should be unexpected or unintended, and not easily corrected.</span></span> <span data-ttu-id="a3721-145">В противном случае, практически любая ошибка пользователя может быть вызвана потерей данных или потенциальной проблемой какого-либо рода и выдачи предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a3721-145">Otherwise, just about any user mistake could be construed to result in data loss or a potential problem of some kind and merit a warning.</span></span>

### <a name="characteristics-of-good-warnings"></a><span data-ttu-id="a3721-146">Характеристики хороших предупреждений</span><span class="sxs-lookup"><span data-stu-id="a3721-146">Characteristics of good warnings</span></span>

<span data-ttu-id="a3721-147">Хорошие предупреждения:</span><span class="sxs-lookup"><span data-stu-id="a3721-147">Good warnings:</span></span>

-   <span data-ttu-id="a3721-148">**Затрагивать риски.**</span><span class="sxs-lookup"><span data-stu-id="a3721-148">**Involve risk.**</span></span> <span data-ttu-id="a3721-149">Хорошие предупреждения предупреждают пользователей о значительных возможностях.</span><span class="sxs-lookup"><span data-stu-id="a3721-149">Good warnings alert users of something significant.</span></span>

<span data-ttu-id="a3721-150">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="a3721-150">**Incorrect:**</span></span>

![<span data-ttu-id="a3721-151">снимок экрана: "вы хотите выйти?"</span><span class="sxs-lookup"><span data-stu-id="a3721-151">screen shot of 'do you want to exit?'</span></span> <span data-ttu-id="a3721-152">warning</span><span class="sxs-lookup"><span data-stu-id="a3721-152">warning</span></span> ](images/mess-warn-image3.png)

<span data-ttu-id="a3721-153">Ну и что?</span><span class="sxs-lookup"><span data-stu-id="a3721-153">So what?</span></span> <span data-ttu-id="a3721-154">Это подтверждение предполагает, что пользователи часто завершают работу с программами.</span><span class="sxs-lookup"><span data-stu-id="a3721-154">This confirmation assumes that users often exit programs by accident.</span></span>

-   <span data-ttu-id="a3721-155">**Непосредственный релевантность.**</span><span class="sxs-lookup"><span data-stu-id="a3721-155">**Have immediate relevance.**</span></span> <span data-ttu-id="a3721-156">Пользователи не только должны соблюдать осторожность, но и сейчас.</span><span class="sxs-lookup"><span data-stu-id="a3721-156">Not only do users have to care, they have to care now.</span></span> <span data-ttu-id="a3721-157">Пользователи, как правило, не заинтересованы в проблемах, которые могут быть позже, пока они могут выполнить свою работу прямо сейчас.</span><span class="sxs-lookup"><span data-stu-id="a3721-157">Users typically aren't interested in problems they might have later as long as they can do their work now.</span></span>

<span data-ttu-id="a3721-158">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="a3721-158">**Incorrect:**</span></span>

![<span data-ttu-id="a3721-159">снимок экрана с предупреждением "батарея — меньше трех часов"</span><span class="sxs-lookup"><span data-stu-id="a3721-159">screen shot of battery-low-in-three-hours warning</span></span> ](images/mess-warn-image4.png)

<span data-ttu-id="a3721-160">В этом случае лучше всего предупредить пользователя за три часа.</span><span class="sxs-lookup"><span data-stu-id="a3721-160">In this case, it's better just to warn the user in three hours.</span></span>

-   <span data-ttu-id="a3721-161">**Приведут к действию.**</span><span class="sxs-lookup"><span data-stu-id="a3721-161">**Lead to action.**</span></span> <span data-ttu-id="a3721-162">Есть какие-либо пользователи, которые должны иметь в виду результат предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a3721-162">There is something users must do or be aware of as the result of the warning.</span></span> <span data-ttu-id="a3721-163">Возможно, они должны предпринять действие сейчас или в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="a3721-163">Perhaps they must take an action now or sometime in the immediate future.</span></span> <span data-ttu-id="a3721-164">Возможно, они будут выполнять задачу по-разному.</span><span class="sxs-lookup"><span data-stu-id="a3721-164">Perhaps they will perform a task differently as a result.</span></span> <span data-ttu-id="a3721-165">Результат игнорирования предупреждения должен быть четким.</span><span class="sxs-lookup"><span data-stu-id="a3721-165">The consequence of ignoring the warning should be clear.</span></span> <span data-ttu-id="a3721-166">Предупреждения без действий просто делают пользователей параноиков.</span><span class="sxs-lookup"><span data-stu-id="a3721-166">Warnings without actions just make users feel paranoid.</span></span>

<span data-ttu-id="a3721-167">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="a3721-167">**Incorrect:**</span></span>

![<span data-ttu-id="a3721-168">снимок экрана: предупреждение "запущена служба Live Messenger"</span><span class="sxs-lookup"><span data-stu-id="a3721-168">screen shot of 'live messenger is running' warning</span></span> ](images/mess-warn-image5.png)

<span data-ttu-id="a3721-169">Почему это уведомление является предупреждением?</span><span class="sxs-lookup"><span data-stu-id="a3721-169">Why is this notification a warning?</span></span> <span data-ttu-id="a3721-170">Что должны делать пользователи (рядом с заботами)?</span><span class="sxs-lookup"><span data-stu-id="a3721-170">What are users supposed to do (beside worry)?</span></span>

-   <span data-ttu-id="a3721-171">**Не очевидны.**</span><span class="sxs-lookup"><span data-stu-id="a3721-171">**Are not obvious.**</span></span> <span data-ttu-id="a3721-172">Не выводите предупреждение, чтобы определить очевидные последствия действия.</span><span class="sxs-lookup"><span data-stu-id="a3721-172">Don't display a warning to state the obvious consequence of an action.</span></span> <span data-ttu-id="a3721-173">Например, предположим, что пользователи понимают последствия невыполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="a3721-173">For example, assume users understand the consequences of not completing a task.</span></span>

<span data-ttu-id="a3721-174">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="a3721-174">**Incorrect:**</span></span>

![<span data-ttu-id="a3721-175">снимок экрана: выйти из мастера? !</span><span class="sxs-lookup"><span data-stu-id="a3721-175">screen shot of do you want to exit wizard? warning</span></span> ](images/mess-warn-image6.png)

<span data-ttu-id="a3721-176">Отмена незавершенного мастера означает, что задача не будет выполнена... кто знал?</span><span class="sxs-lookup"><span data-stu-id="a3721-176">Canceling an incomplete wizard means the task doesn't get done...who knew?</span></span>

-   <span data-ttu-id="a3721-177">**Происходят редко.**</span><span class="sxs-lookup"><span data-stu-id="a3721-177">**Occur infrequently.**</span></span> <span data-ttu-id="a3721-178">Постоянные предупреждения быстро становятся неэффективными и нетронутыми.</span><span class="sxs-lookup"><span data-stu-id="a3721-178">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="a3721-179">Пользователи часто получают больше внимания за тем, чтобы избавиться от предупреждения, чем устраняет проблему.</span><span class="sxs-lookup"><span data-stu-id="a3721-179">Users often become more focused on getting rid of the warning than addressing the problem.</span></span>

<span data-ttu-id="a3721-180">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="a3721-180">**Incorrect:**</span></span>

![<span data-ttu-id="a3721-181">снимок экрана с предупреждением "Обновление сигнатур вирусов"</span><span class="sxs-lookup"><span data-stu-id="a3721-181">screen shot of 'update virus signatures' warning</span></span> ](images/mess-warn-image7.png)

<span data-ttu-id="a3721-182">Пользователи, скорее всего, пососредоточусь на избавиться от предупреждения, чем исправить базовую проблему.</span><span class="sxs-lookup"><span data-stu-id="a3721-182">Users are more likely to focus on getting rid of the warning than fixing the underlying problem.</span></span>

<span data-ttu-id="a3721-183">Сообщение, не имеющее этих характеристик, может по-прежнему быть хорошим сообщением, но не очень хорошим предупреждением.</span><span class="sxs-lookup"><span data-stu-id="a3721-183">A message that doesn't have these characteristics might still be a good message, just not a good warning.</span></span>

### <a name="determine-the-appropriate-message-type"></a><span data-ttu-id="a3721-184">Определение соответствующего типа сообщений</span><span class="sxs-lookup"><span data-stu-id="a3721-184">Determine the appropriate message type</span></span>

<span data-ttu-id="a3721-185">Некоторые проблемы могут быть представлены как ошибки, предупреждения или сведения в зависимости от характера и формулировки.</span><span class="sxs-lookup"><span data-stu-id="a3721-185">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="a3721-186">Например, предположим, что веб-страница не может загрузить неподписанный элемент ActiveX на основе текущей конфигурации Windows Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="a3721-186">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

-   <span data-ttu-id="a3721-187">**План.**</span><span class="sxs-lookup"><span data-stu-id="a3721-187">**Error.**</span></span> <span data-ttu-id="a3721-188">"Эта страница не может загрузить неподписанный элемент ActiveX."</span><span class="sxs-lookup"><span data-stu-id="a3721-188">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="a3721-189">(С фразой в качестве существующей проблемы.)</span><span class="sxs-lookup"><span data-stu-id="a3721-189">(Phrased as an existing problem.)</span></span>
-   <span data-ttu-id="a3721-190">**!.**</span><span class="sxs-lookup"><span data-stu-id="a3721-190">**Warning.**</span></span> <span data-ttu-id="a3721-191">"Эта страница может работать неправильно, так как Windows Internet Explorer не настроен для загрузки неподписанных элементов ActiveX."</span><span class="sxs-lookup"><span data-stu-id="a3721-191">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="a3721-192">или "разрешить этой странице устанавливать неподписанный элемент ActiveX?</span><span class="sxs-lookup"><span data-stu-id="a3721-192">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="a3721-193">Это может повредить компьютер из ненадежных источников».</span><span class="sxs-lookup"><span data-stu-id="a3721-193">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="a3721-194">(Как и в случае с условиями, которые могут вызвать будущие проблемы.)</span><span class="sxs-lookup"><span data-stu-id="a3721-194">(Both phrased as conditions that may cause future problems.)</span></span>
-   <span data-ttu-id="a3721-195">**Об.**</span><span class="sxs-lookup"><span data-stu-id="a3721-195">**Information.**</span></span> <span data-ttu-id="a3721-196">«Вы настроили Windows Internet Explorer на блокировку неподписанных элементов ActiveX».</span><span class="sxs-lookup"><span data-stu-id="a3721-196">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="a3721-197">(С фразой в качестве оператора факта.)</span><span class="sxs-lookup"><span data-stu-id="a3721-197">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="a3721-198">**Чтобы определить подходящий тип сообщений, сосредоточьтесь на самом важном аспекте проблемы, которую пользователи должны знать или предпринять.**</span><span class="sxs-lookup"><span data-stu-id="a3721-198">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="a3721-199">Как правило, если ошибка блокирует продолжение работы пользователя, вы должны представлять его как ошибку; Если пользователь может продолжать работу, представьте его как предупреждение.</span><span class="sxs-lookup"><span data-stu-id="a3721-199">Typically, if an issue blocks the user from proceeding, you should present it as an error; if the user can proceed, present it as a warning.</span></span> <span data-ttu-id="a3721-200">Создайте [основную инструкцию](text-ui.md) или другой соответствующий текст на основе этого фокуса, а затем выберите значок ([стандартный](vis-std-icons.md) или другой), соответствующий тексту.</span><span class="sxs-lookup"><span data-stu-id="a3721-200">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, then choose an icon ([standard](vis-std-icons.md) or otherwise) that matches the text.</span></span> <span data-ttu-id="a3721-201">Основной текст и значки инструкций должны всегда совпадать.</span><span class="sxs-lookup"><span data-stu-id="a3721-201">The main instruction text and icons should always match.</span></span>

### <a name="be-specific"></a><span data-ttu-id="a3721-202">Быть конкретным</span><span class="sxs-lookup"><span data-stu-id="a3721-202">Be specific</span></span>

<span data-ttu-id="a3721-203">Предупреждения являются более привлекательными, если приведенные ниже сведения являются специфичными и понятны.</span><span class="sxs-lookup"><span data-stu-id="a3721-203">Warnings are more compelling when the following information is specific and clear:</span></span>

-   <span data-ttu-id="a3721-204">Источник предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a3721-204">The source of the warning.</span></span>
-   <span data-ttu-id="a3721-205">Конкретное условие и потенциальная проблема.</span><span class="sxs-lookup"><span data-stu-id="a3721-205">The specific condition and potential problem.</span></span>
-   <span data-ttu-id="a3721-206">Что должен делать пользователь.</span><span class="sxs-lookup"><span data-stu-id="a3721-206">What the user should do about it.</span></span>
-   <span data-ttu-id="a3721-207">Что происходит, если пользователь ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="a3721-207">What happens if the user doesn't do anything.</span></span>

<span data-ttu-id="a3721-208">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="a3721-208">**Incorrect:**</span></span>

![<span data-ttu-id="a3721-209">снимок экрана с неясным предупреждением о значимом риске</span><span class="sxs-lookup"><span data-stu-id="a3721-209">screen shot of vague warning of significant risk</span></span> ](images/mess-warn-image8.png)

<span data-ttu-id="a3721-210">В этом примере, какова потенциальная проблема?</span><span class="sxs-lookup"><span data-stu-id="a3721-210">In this example, what is the potential problem?</span></span> <span data-ttu-id="a3721-211">Что должен делать пользователь, помимо использования проектора по сети?</span><span class="sxs-lookup"><span data-stu-id="a3721-211">What is the user supposed to do, aside from not using the projector over the network?</span></span> <span data-ttu-id="a3721-212">Если не получить более конкретных сведений, то все, что может сделать пользователь, не будет работать.</span><span class="sxs-lookup"><span data-stu-id="a3721-212">Without more specific information, all the user can do is feel bad about proceeding.</span></span>

<span data-ttu-id="a3721-213">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="a3721-213">**Correct:**</span></span>

![<span data-ttu-id="a3721-214">снимок экрана с предупреждением о проблеме и последствиях</span><span class="sxs-lookup"><span data-stu-id="a3721-214">screen shot of warning of problem and consequences</span></span> ](images/mess-warn-image9.png)

<span data-ttu-id="a3721-215">В этом примере проблема и последствия очевидны.</span><span class="sxs-lookup"><span data-stu-id="a3721-215">In this example, the problem and consequences are clear.</span></span>

<span data-ttu-id="a3721-216">Иногда существует легальная потенциальная проблема, достойной о том, что пользователи должны знать, но решение и последствия не известны.</span><span class="sxs-lookup"><span data-stu-id="a3721-216">Sometimes there is a legitimate potential problem worthy of informing users about, but the solution and consequences aren't known for sure.</span></span> <span data-ttu-id="a3721-217">Вместо того, чтобы выдавать неопределенное предупреждение, следует присваивать наиболее вероятные сведения или наиболее распространенный пример.</span><span class="sxs-lookup"><span data-stu-id="a3721-217">Rather than give a vague warning, be specific by giving the most likely information or the most common example.</span></span>

<span data-ttu-id="a3721-218">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="a3721-218">**Correct:**</span></span>

![<span data-ttu-id="a3721-219">снимок экрана с предупреждением об ошибке сети и решениями</span><span class="sxs-lookup"><span data-stu-id="a3721-219">screen shot of network error warning and solutions</span></span> ](images/mess-warn-image10.png)

<span data-ttu-id="a3721-220">В этом примере предупреждение делается независимым, предоставляя наиболее вероятное решение.</span><span class="sxs-lookup"><span data-stu-id="a3721-220">In this example, the warning is made specific by providing the most likely solution.</span></span>

<span data-ttu-id="a3721-221">Однако в таких случаях используйте слова, которые указывают на наличие других возможностей.</span><span class="sxs-lookup"><span data-stu-id="a3721-221">However, in such cases, use wording that indicates that there are other possibilities.</span></span> <span data-ttu-id="a3721-222">В противном случае пользователи могут быть заблуждение.</span><span class="sxs-lookup"><span data-stu-id="a3721-222">Otherwise, users might be misled.</span></span>

<span data-ttu-id="a3721-223">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="a3721-223">**Incorrect:**</span></span>

![<span data-ttu-id="a3721-224">снимок экрана с сообщением о неподключенном сетевом кабеле</span><span class="sxs-lookup"><span data-stu-id="a3721-224">screen shot of network cable unplugged warning</span></span> ](images/mess-warn-image11.png)

<span data-ttu-id="a3721-225">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="a3721-225">**Correct:**</span></span>

![<span data-ttu-id="a3721-226">снимок экрана, возможно, отключено предупреждение о кабеле</span><span class="sxs-lookup"><span data-stu-id="a3721-226">screen shot of cable might be unplugged warning</span></span> ](images/mess-warn-image12.png)

<span data-ttu-id="a3721-227">В неправильном примере пользователи будут путать, если кабель явно подсоединен.</span><span class="sxs-lookup"><span data-stu-id="a3721-227">In the incorrect example, users will be confused if the cable is clearly plugged in.</span></span>

<span data-ttu-id="a3721-228">**Если вы выполняете только два действия...**</span><span class="sxs-lookup"><span data-stu-id="a3721-228">**If you do only two things...**</span></span>

1. <span data-ttu-id="a3721-229">Не передавать предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a3721-229">Don't overwarn.</span></span> <span data-ttu-id="a3721-230">Ограничьте предупреждения условиями, которые затрагивают риск и являются немедленно важными, практичными, неочевидными и редкими.</span><span class="sxs-lookup"><span data-stu-id="a3721-230">Limit warnings to conditions that involve risk and are immediately relevant, actionable, not obvious, and infrequent.</span></span> <span data-ttu-id="a3721-231">В противном случае удалите или зафразу сообщение.</span><span class="sxs-lookup"><span data-stu-id="a3721-231">Otherwise, remove or rephrase the message.</span></span>

2. <span data-ttu-id="a3721-232">Укажите конкретные полезные сведения.</span><span class="sxs-lookup"><span data-stu-id="a3721-232">Provide specific, useful information.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="a3721-233">Варианты использования</span><span class="sxs-lookup"><span data-stu-id="a3721-233">Usage patterns</span></span>

<span data-ttu-id="a3721-234">Предупреждения имеют несколько шаблонов использования:</span><span class="sxs-lookup"><span data-stu-id="a3721-234">Warnings have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3721-235"><strong>Сведения</strong></span><span class="sxs-lookup"><span data-stu-id="a3721-235"><strong>Awareness</strong></span></span><br/> <span data-ttu-id="a3721-236">Пользователь должен знать о условии или возможной проблеме, но в этом случае пользователю может быть не нужно ничего делать.</span><span class="sxs-lookup"><span data-stu-id="a3721-236">Make user aware of a condition or potential problem, but user may not have to do anything now.</span></span> <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> <span data-ttu-id="a3721-237">Примеры предупреждений о осведомленности.</span><span class="sxs-lookup"><span data-stu-id="a3721-237">Examples of awareness warnings.</span></span><br/> <span data-ttu-id="a3721-238">Предупреждения о осведомленности имеют следующую презентацию:</span><span class="sxs-lookup"><span data-stu-id="a3721-238">Awareness warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="a3721-239"><strong>Основная инструкция:</strong> Опишите условие или потенциальную проблему.</span><span class="sxs-lookup"><span data-stu-id="a3721-239"><strong>Main instruction:</strong> Describe the condition or potential problem.</span></span></li>
<li><span data-ttu-id="a3721-240"><strong>Дополнительная инструкция:</strong> Объясните смысл и почему это важно.</span><span class="sxs-lookup"><span data-stu-id="a3721-240"><strong>Supplemental instruction:</strong> Explain the implication and why it is important.</span></span></li>
<li><span data-ttu-id="a3721-241"><strong>Кнопки фиксации:</strong> Выхода.</span><span class="sxs-lookup"><span data-stu-id="a3721-241"><strong>Commit buttons:</strong> Close.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3721-242"><strong>Предотвращение ошибок</strong></span><span class="sxs-lookup"><span data-stu-id="a3721-242"><strong>Error prevention</strong></span></span><br/> <span data-ttu-id="a3721-243">Предоставление пользователю сведений о том, что может помешать проблеме, особенно при выборе варианта.</span><span class="sxs-lookup"><span data-stu-id="a3721-243">Make user aware of information that might prevent a problem, especially when making choices.</span></span> <br/></td>
<td><span data-ttu-id="a3721-244">Предупреждения предотвращения ошибок лучше представить с помощью значка предупреждения на месте и пояснительного текста.</span><span class="sxs-lookup"><span data-stu-id="a3721-244">Error prevention warnings are best presented using an in-place warning icon and explanatory text.</span></span> <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> <span data-ttu-id="a3721-245">Примеры предупреждений предотвращения ошибок.</span><span class="sxs-lookup"><span data-stu-id="a3721-245">Examples of error prevention warnings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3721-246"><strong>Приближающаяся проблема</strong></span><span class="sxs-lookup"><span data-stu-id="a3721-246"><strong>Imminent problem</strong></span></span><br/> <span data-ttu-id="a3721-247">Для предотвращения возможной проблемы пользователь должен сделать что-то еще.</span><span class="sxs-lookup"><span data-stu-id="a3721-247">The user needs to do something now to prevent an imminent problem.</span></span> <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> <span data-ttu-id="a3721-248">Пример приближенного к проблеме предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a3721-248">An example of an imminent problem warning.</span></span><br/> <span data-ttu-id="a3721-249">Выявление предупреждений о проблемах имеет следующую презентацию:</span><span class="sxs-lookup"><span data-stu-id="a3721-249">Imminent problem warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="a3721-250"><strong>Основная инструкция:</strong> Опишите, что нужно сделать пользователю.</span><span class="sxs-lookup"><span data-stu-id="a3721-250"><strong>Main instruction:</strong> Describe what the user needs to do now.</span></span></li>
<li><span data-ttu-id="a3721-251"><strong>Дополнительная инструкция:</strong> Объясните условие и его важность.</span><span class="sxs-lookup"><span data-stu-id="a3721-251"><strong>Supplemental instruction:</strong> Explain the condition and why it is important.</span></span></li>
<li><span data-ttu-id="a3721-252"><strong>Кнопки фиксации:</strong> Кнопка или ссылка на команду для каждого параметра или значение ОК, если действие выполняется за пределами этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a3721-252"><strong>Commit buttons:</strong> A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3721-253"><strong>Подтверждение нерискованного действия</strong></span><span class="sxs-lookup"><span data-stu-id="a3721-253"><strong>Risky action confirmation</strong></span></span><br/> <span data-ttu-id="a3721-254">Убедитесь, что пользователь хочет перейти к действию, которое имеет некоторый риск и не может быть легко отменено.</span><span class="sxs-lookup"><span data-stu-id="a3721-254">Confirm that the user wants to proceed with an action that has some risk and can't be easily undone.</span></span> <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> <span data-ttu-id="a3721-255">Пример подтверждения опасного действия.</span><span class="sxs-lookup"><span data-stu-id="a3721-255">An example of risky action confirmation.</span></span><br/> <span data-ttu-id="a3721-256">Подтверждение рискованных действий имеет следующую презентацию:</span><span class="sxs-lookup"><span data-stu-id="a3721-256">Risky action confirmations have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="a3721-257"><strong>Основная инструкция:</strong> Задайте вопрос, чтобы определить, желаете ли пользователь продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="a3721-257"><strong>Main instruction:</strong> Ask a question to determine if the user wants to proceed.</span></span></li>
<li><span data-ttu-id="a3721-258"><strong>Дополнительная инструкция:</strong> Объясните все неочевидные причины, по которым пользователю может не потребоваться продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="a3721-258"><strong>Supplemental instruction:</strong> Explain any non-obvious reasons why the user might not want to proceed.</span></span></li>
<li><span data-ttu-id="a3721-259"><strong>Кнопки фиксации:</strong> Да, нет.</span><span class="sxs-lookup"><span data-stu-id="a3721-259"><strong>Commit buttons:</strong> Yes, No.</span></span></li>
</ul>
<span data-ttu-id="a3721-260">Рекомендации по этому шаблону см. в разделе <a href="mess-confirm.md">подтверждения</a>.</span><span class="sxs-lookup"><span data-stu-id="a3721-260">For guidelines on this pattern, see <a href="mess-confirm.md">Confirmations</a>.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="a3721-261">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="a3721-261">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="a3721-262">Уровень представления</span><span class="sxs-lookup"><span data-stu-id="a3721-262">Presentation</span></span>

-   <span data-ttu-id="a3721-263">**Выберите пользовательский интерфейс представления в зависимости от типа информации:**</span><span class="sxs-lookup"><span data-stu-id="a3721-263">**Choose the presentation UI based on the type of information:**</span></span>



| <span data-ttu-id="a3721-264">Пользовательский интерфейс</span><span class="sxs-lookup"><span data-stu-id="a3721-264">User interface</span></span>  | <span data-ttu-id="a3721-265">Лучше использовать для</span><span class="sxs-lookup"><span data-stu-id="a3721-265">Best used for</span></span> |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3721-266">Модальные диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="a3721-266">Modal dialog boxes</span></span><br/> | <span data-ttu-id="a3721-267">Критические предупреждения (включая подтверждения), на которые пользователи должны ответить сейчас.</span><span class="sxs-lookup"><span data-stu-id="a3721-267">Critical warnings (including confirmations) that users must respond to now.</span></span><br/>                                                 |
| <span data-ttu-id="a3721-268">На месте</span><span class="sxs-lookup"><span data-stu-id="a3721-268">In-place</span></span><br/>           | <span data-ttu-id="a3721-269">Сведения, которые могут помешать возникновению проблемы, особенно при выборе пользователей.</span><span class="sxs-lookup"><span data-stu-id="a3721-269">Information that might prevent a problem, especially when users are making choices.</span></span><br/>                                         |
| <span data-ttu-id="a3721-270">Баннеров</span><span class="sxs-lookup"><span data-stu-id="a3721-270">Banners</span></span><br/>            | <span data-ttu-id="a3721-271">Сведения, которые могут помешать возникновению проблемы, особенно если они связаны с завершением задачи.</span><span class="sxs-lookup"><span data-stu-id="a3721-271">Information that might prevent a problem, especially when related to completing a task.</span></span><br/>                                     |
| <span data-ttu-id="a3721-272">Уведомления</span><span class="sxs-lookup"><span data-stu-id="a3721-272">Notifications</span></span><br/>      | <span data-ttu-id="a3721-273">Значимые события или состояние, которые можно спокойно игнорировать, по крайней мере временно.</span><span class="sxs-lookup"><span data-stu-id="a3721-273">Significant events or status that can be safely ignored, at least temporarily.</span></span><br/>                                              |
| <span data-ttu-id="a3721-274">Объекты Balloon</span><span class="sxs-lookup"><span data-stu-id="a3721-274">Balloons</span></span><br/>           | <span data-ttu-id="a3721-275">Элемент управления находится в состоянии, которое влияет на входные данные.</span><span class="sxs-lookup"><span data-stu-id="a3721-275">A control is in a state that affects input.</span></span> <span data-ttu-id="a3721-276">Это состояние, скорее всего, непреднамеренно, и пользователь может не реализовать ввод.</span><span class="sxs-lookup"><span data-stu-id="a3721-276">This state is likely unintended and the user may not realize input is affected.</span></span><br/> |



 

-   <span data-ttu-id="a3721-277">**Для модальных диалоговых окон:**</span><span class="sxs-lookup"><span data-stu-id="a3721-277">**For modal dialog boxes:**</span></span>
    -   <span data-ttu-id="a3721-278">**При необходимости используйте диалоговые окна задач, чтобы добиться согласованного вида и макета.**</span><span class="sxs-lookup"><span data-stu-id="a3721-278">**Use task dialogs whenever appropriate to achieve a consistent look and layout.**</span></span> <span data-ttu-id="a3721-279">В диалоговых окнах задач требуется Windows Vista или более поздней версии, поэтому они не подходят для более ранних версий Windows.</span><span class="sxs-lookup"><span data-stu-id="a3721-279">Task dialogs require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span>
    -   <span data-ttu-id="a3721-280">**Отображать только одно предупреждающее сообщение для каждого условия.**</span><span class="sxs-lookup"><span data-stu-id="a3721-280">**Display only one warning message per condition.**</span></span> <span data-ttu-id="a3721-281">Например, отобразится одно предупреждение, которое полностью описывает условие, вместо того чтобы описывать его по одному подробному сообщению за раз.</span><span class="sxs-lookup"><span data-stu-id="a3721-281">For example, display a single warning that completely explains a condition instead of describing it one detail at a time per message.</span></span> <span data-ttu-id="a3721-282">Отображение последовательности диалоговых окон предупреждений для одного условия — это путаница и неприятная проблема.</span><span class="sxs-lookup"><span data-stu-id="a3721-282">Displaying a sequence of warning dialogs for a single condition is confusing and annoying.</span></span>
    -   <span data-ttu-id="a3721-283">**Не отображать предупреждение более одного раза для каждого условия.**</span><span class="sxs-lookup"><span data-stu-id="a3721-283">**Don't display a warning more than once per condition.**</span></span> <span data-ttu-id="a3721-284">Постоянные предупреждения быстро становятся неэффективными и нетронутыми.</span><span class="sxs-lookup"><span data-stu-id="a3721-284">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="a3721-285">Пользователи часто получают больше внимания за тем, чтобы избавиться от предупреждения, чем устраняет проблему.</span><span class="sxs-lookup"><span data-stu-id="a3721-285">Users often become more focused on getting rid of the warning than addressing the problem.</span></span> <span data-ttu-id="a3721-286">Если необходимо регулярно выдавать предупреждение для одного условия, используйте [прогрессивное укрупнение](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="a3721-286">If you must warn repeatedly for a single condition, use [progressive escalation](mess-notif.md).</span></span>
-   <span data-ttu-id="a3721-287">**Не выводят предупреждения с помощью звукового эффекта или звукового сигнала.**</span><span class="sxs-lookup"><span data-stu-id="a3721-287">**Don't accompany warnings with a sound effect or beep.**</span></span> <span data-ttu-id="a3721-288">Это жарринг и не требуется.</span><span class="sxs-lookup"><span data-stu-id="a3721-288">Doing so is jarring and unnecessary.</span></span>
    -   <span data-ttu-id="a3721-289">**Исключение:** Если пользователь должен ответить немедленно, можно использовать звуковой эффекты.</span><span class="sxs-lookup"><span data-stu-id="a3721-289">**Exception:** If the user must respond immediately, you can use a sound effect.</span></span>

### <a name="icons"></a><span data-ttu-id="a3721-290">Значки</span><span class="sxs-lookup"><span data-stu-id="a3721-290">Icons</span></span>

-   <span data-ttu-id="a3721-291">Не размещайте значок предупреждения в заголовке диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a3721-291">Don't place a warning icon in the title bar of a dialog box.</span></span>
-   <span data-ttu-id="a3721-292">**Используйте значок предупреждения.**</span><span class="sxs-lookup"><span data-stu-id="a3721-292">**Use a warning icon.**</span></span> <span data-ttu-id="a3721-293">Исключения:</span><span class="sxs-lookup"><span data-stu-id="a3721-293">Exceptions:</span></span>
    -   <span data-ttu-id="a3721-294">Если предупреждение относится к компоненту, имеющему значок, можно использовать значок функции с наложением предупреждений.</span><span class="sxs-lookup"><span data-stu-id="a3721-294">If the warning is for a feature that has an icon, you can use the feature icon with a warning overlay.</span></span>

        <span data-ttu-id="a3721-295">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="a3721-295">**Correct:**</span></span>

        ![<span data-ttu-id="a3721-296">снимок экрана с изображением значка блокировки с наложением значка предупреждения</span><span class="sxs-lookup"><span data-stu-id="a3721-296">screen shot of lock icon with warning icon overlay</span></span> ](images/mess-warn-image21.png)

        <span data-ttu-id="a3721-297">В этом примере значок функции имеет наложение предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a3721-297">In this example, the feature icon has a warning overlay.</span></span>

-   <span data-ttu-id="a3721-298">Для модальных диалоговых окон, в которых появляется сноска предупреждения, вместо области содержимого следует разместить значок предупреждения в сноске.</span><span class="sxs-lookup"><span data-stu-id="a3721-298">For modal dialog boxes with a warning footnote, put the warning icon in the footnote instead of the content area.</span></span>

    <span data-ttu-id="a3721-299">**Правильно:**</span><span class="sxs-lookup"><span data-stu-id="a3721-299">**Correct:**</span></span>

    ![<span data-ttu-id="a3721-300">снимок экрана с значком предупреждения в сноске диалогового окна</span><span class="sxs-lookup"><span data-stu-id="a3721-300">screen shot of warning icon in dialog-box footnote</span></span> ](images/mess-warn-image22.png)

    <span data-ttu-id="a3721-301">В этом примере в сноске имеется значок предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a3721-301">In this example, the footnote has the warning icon.</span></span>

<span data-ttu-id="a3721-302">Дополнительные рекомендации и примеры см. в разделе [стандартные значки](vis-std-icons.md).</span><span class="sxs-lookup"><span data-stu-id="a3721-302">For more guidelines and examples, see [Standard Icons](vis-std-icons.md).</span></span>

### <a name="dont-show-this-message-again"></a><span data-ttu-id="a3721-303">Больше не показывать это сообщение</span><span class="sxs-lookup"><span data-stu-id="a3721-303">Don't show this message again</span></span>

-   <span data-ttu-id="a3721-304">**Если для этого параметра требуется диалоговое окно предупреждения, следует рассмотреть предупреждение и его частоту.**</span><span class="sxs-lookup"><span data-stu-id="a3721-304">**If a warning dialog box needs this option, reconsider the warning and its frequency.**</span></span> <span data-ttu-id="a3721-305">Если у него есть все характеристики хорошего предупреждения (в том что входит риск, и он является немедленно релевантным, практичным, неочевидным и редким), не следует иметь смысла подавлять его.</span><span class="sxs-lookup"><span data-stu-id="a3721-305">If it has all the characteristics of a good warning (involves risk, and is immediately relevant, actionable, not obvious, and infrequent), it shouldn't make sense for users to suppress it.</span></span>

<span data-ttu-id="a3721-306">Дополнительные рекомендации см. в разделе [диалоговые окна](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="a3721-306">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="a3721-307">Поэтапное представление информации</span><span class="sxs-lookup"><span data-stu-id="a3721-307">Progressive disclosure</span></span>

-   <span data-ttu-id="a3721-308">**Если необходимо включить дополнительные сведения в предупреждающее сообщение, раскроете его с помощью кнопок прогрессивной раскрытия** (например, "Показать подробности").</span><span class="sxs-lookup"><span data-stu-id="a3721-308">**If you must include advanced information in a warning message, reveal it by using progressive disclosure buttons** (for example, "Show details").</span></span> <span data-ttu-id="a3721-309">Это упрощает предупреждение для типичного использования.</span><span class="sxs-lookup"><span data-stu-id="a3721-309">Doing so simplifies the warning for typical usage.</span></span> <span data-ttu-id="a3721-310">Не скрывать необходимую информацию, так как пользователи могут их не найти.</span><span class="sxs-lookup"><span data-stu-id="a3721-310">Don't hide needed information because users might not find it.</span></span>
-   <span data-ttu-id="a3721-311">**Не используйте "Показывать подробности", если нет более подробной информации.**</span><span class="sxs-lookup"><span data-stu-id="a3721-311">**Don't use "Show details" unless there really is more detail.**</span></span> <span data-ttu-id="a3721-312">Не просто переформатируйте существующую информацию в другом формате.</span><span class="sxs-lookup"><span data-stu-id="a3721-312">Don't just restate the existing information in a different format.</span></span>

<span data-ttu-id="a3721-313">Рекомендации по созданию меток см. в разделе [прогрессивное раскрытие](ctrl-progressive-disclosure-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a3721-313">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="a3721-314">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a3721-314">Default values</span></span>

-   <span data-ttu-id="a3721-315">**Выберите самый безопасный, наименее разрушительный или наиболее безопасный ответ, который будет использоваться по умолчанию.**</span><span class="sxs-lookup"><span data-stu-id="a3721-315">**Select the safest, least destructive, or most secure response to be the default.**</span></span>

## <a name="text"></a><span data-ttu-id="a3721-316">text</span><span class="sxs-lookup"><span data-stu-id="a3721-316">Text</span></span>

### <a name="general"></a><span data-ttu-id="a3721-317">Общее</span><span class="sxs-lookup"><span data-stu-id="a3721-317">General</span></span>

-   <span data-ttu-id="a3721-318">**Удалите избыточный текст.**</span><span class="sxs-lookup"><span data-stu-id="a3721-318">**Remove redundant text.**</span></span> <span data-ttu-id="a3721-319">Ищите его в заголовках, основных инструкциях, дополнительных инструкциях, областях содержимого, ссылках на команды и кнопках фиксации.</span><span class="sxs-lookup"><span data-stu-id="a3721-319">Look for it in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="a3721-320">Как правило, оставьте весь текст в инструкциях и интерактивных элементах управления и удалите все избыточность из других мест.</span><span class="sxs-lookup"><span data-stu-id="a3721-320">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="a3721-321">**Не используйте термины «предупреждение» и «внимание» в тексте.**</span><span class="sxs-lookup"><span data-stu-id="a3721-321">**Don't use the terms "warning" or "caution" in the text.**</span></span> <span data-ttu-id="a3721-322">При [правильном использовании](vis-std-icons.md)значок предупреждения сообщает о том, что пользователи должны соблюдать осторожность.</span><span class="sxs-lookup"><span data-stu-id="a3721-322">When [used correctly](vis-std-icons.md), the warning icon sufficiently communicates that users must proceed with caution.</span></span>

<span data-ttu-id="a3721-323">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="a3721-323">**Incorrect:**</span></span>

![<span data-ttu-id="a3721-324">снимок экрана с ненужным использованием предупреждения в тексте</span><span class="sxs-lookup"><span data-stu-id="a3721-324">screen shot of unnecessary use of warning in text</span></span> ](images/mess-warn-image23.png)

<span data-ttu-id="a3721-325">В этом примере термин «предупреждение» не требуется.</span><span class="sxs-lookup"><span data-stu-id="a3721-325">In this example, the term "warning" is unnecessary.</span></span>

### <a name="titles"></a><span data-ttu-id="a3721-326">Заголовки</span><span class="sxs-lookup"><span data-stu-id="a3721-326">Titles</span></span>

-   <span data-ttu-id="a3721-327">**Используйте заголовок, чтобы указать команду или функцию, из которой поступило предупреждение.**</span><span class="sxs-lookup"><span data-stu-id="a3721-327">**Use the title to identify the command or feature where the warning came from.**</span></span> <span data-ttu-id="a3721-328">Исключения:</span><span class="sxs-lookup"><span data-stu-id="a3721-328">Exceptions:</span></span>
    -   <span data-ttu-id="a3721-329">Если предупреждение отображается многими различными командами, рекомендуется использовать имя программы.</span><span class="sxs-lookup"><span data-stu-id="a3721-329">If a warning is displayed by many different commands, consider using the program name instead.</span></span>
    -   <span data-ttu-id="a3721-330">Если этот заголовок будет избыточным или запутанным с помощью основной инструкции, используйте вместо этого имя программы.</span><span class="sxs-lookup"><span data-stu-id="a3721-330">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>

<span data-ttu-id="a3721-331">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="a3721-331">**Incorrect:**</span></span>

![<span data-ttu-id="a3721-332">снимок экрана с заголовком диалогового окна "предупреждение системы безопасности"</span><span class="sxs-lookup"><span data-stu-id="a3721-332">screen shot of security warning dialog box title</span></span> ](images/mess-warn-image24.png)

<span data-ttu-id="a3721-333">В этом примере "предупреждение системы безопасности" не определяет команду или функцию, из которой поступило предупреждение.</span><span class="sxs-lookup"><span data-stu-id="a3721-333">In this example, "Security Warning" doesn't identify the command or feature where the warning came from.</span></span>

-   <span data-ttu-id="a3721-334">**Не используйте заголовок, чтобы объяснить, что делать в диалоговом окне** , предназначенном для основной инструкции.</span><span class="sxs-lookup"><span data-stu-id="a3721-334">**Don't use the title to explain what to do in the dialog** that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="a3721-335">Используйте [прописные буквы в стиле заголовка](glossary.md)без закрывающих знаков препинания.</span><span class="sxs-lookup"><span data-stu-id="a3721-335">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="a3721-336">Основные инструкции</span><span class="sxs-lookup"><span data-stu-id="a3721-336">Main instructions</span></span>

-   <span data-ttu-id="a3721-337">Основная инструкция для предупреждения зависит от ее шаблона разработки:</span><span class="sxs-lookup"><span data-stu-id="a3721-337">The main instruction for a warning is based on its design pattern:</span></span>



| <span data-ttu-id="a3721-338">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a3721-338">Pattern</span></span>                        | <span data-ttu-id="a3721-339">Основная инструкция</span><span class="sxs-lookup"><span data-stu-id="a3721-339">Main instruction</span></span>                                               |
|--------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="a3721-340">Осведомленность</span><span class="sxs-lookup"><span data-stu-id="a3721-340">Awareness</span></span><br/>                 | <span data-ttu-id="a3721-341">Опишите условие или потенциальную проблему.</span><span class="sxs-lookup"><span data-stu-id="a3721-341">Describe the condition or potential problem.</span></span><br/>              |
| <span data-ttu-id="a3721-342">Приближающаяся проблема</span><span class="sxs-lookup"><span data-stu-id="a3721-342">Imminent problem</span></span><br/>          | <span data-ttu-id="a3721-343">Опишите, что нужно сделать пользователю.</span><span class="sxs-lookup"><span data-stu-id="a3721-343">Describe what the user needs to do now.</span></span><br/>                   |
| <span data-ttu-id="a3721-344">Подтверждение нерискованного действия</span><span class="sxs-lookup"><span data-stu-id="a3721-344">Risky action confirmation</span></span><br/> | <span data-ttu-id="a3721-345">Задайте вопрос, чтобы определить, желаете ли пользователь продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="a3721-345">Ask a question to determine if the user wants to proceed.</span></span><br/> |



 

-   ![<span data-ttu-id="a3721-346">снимок экрана с уведомлением о низком уровне заряда батареи</span><span class="sxs-lookup"><span data-stu-id="a3721-346">screen shot of a low-battery notification</span></span> ](images/mess-warn-image25.png)
-   <span data-ttu-id="a3721-347">В этом примере уведомление о низком уровне заряда батареи является предупреждением о осведомленности, поэтому основная инструкция описывает условие.</span><span class="sxs-lookup"><span data-stu-id="a3721-347">In this example, the low battery notification is an awareness warning, so the main instruction describes the condition.</span></span>
-   ![<span data-ttu-id="a3721-348">снимок экрана с предупреждением об изменении аккумулятора немедленно</span><span class="sxs-lookup"><span data-stu-id="a3721-348">screen shot of change battery immediately warning</span></span> ](images/mess-warn-image1.png)
-   <span data-ttu-id="a3721-349">В этом примере диалоговое окно низкого заряда батареи является приближающейся проблемой, поэтому основная инструкция описывает, что именно необходимо сделать пользователю.</span><span class="sxs-lookup"><span data-stu-id="a3721-349">In this example, the low battery dialog box is an imminent problem, so the main instruction describes what the user needs to do now.</span></span>
-   <span data-ttu-id="a3721-350">**Будьте кратко использовать только одно предложение целиком.**</span><span class="sxs-lookup"><span data-stu-id="a3721-350">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="a3721-351">Разбить основную инструкцию на основные сведения.</span><span class="sxs-lookup"><span data-stu-id="a3721-351">Strip the main instruction down to the essential information.</span></span> <span data-ttu-id="a3721-352">Если необходимо объяснить что-то еще, используйте дополнительную инструкцию.</span><span class="sxs-lookup"><span data-stu-id="a3721-352">If you must explain anything more, use a supplemental instruction.</span></span>
-   <span data-ttu-id="a3721-353">**Если пользователь должен действовать немедленно, используйте слова «Now» и «немедленно».**</span><span class="sxs-lookup"><span data-stu-id="a3721-353">**Use words like "now" and "immediately" if the user must act immediately.**</span></span> <span data-ttu-id="a3721-354">Не используйте эти слова, если нет срочности.</span><span class="sxs-lookup"><span data-stu-id="a3721-354">Don't use these words if there is no urgency.</span></span>
-   <span data-ttu-id="a3721-355">**Будьте специфичны, если есть задействованные объекты, присвойте их полные имена.**</span><span class="sxs-lookup"><span data-stu-id="a3721-355">**Be specific if there are objects involved, give their full names.**</span></span>
-   <span data-ttu-id="a3721-356">Используйте [прописные буквы в стиле предложения](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a3721-356">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="a3721-357">Дополнительные инструкции</span><span class="sxs-lookup"><span data-stu-id="a3721-357">Supplemental instructions</span></span>

-   <span data-ttu-id="a3721-358">Дополнительная инструкция для предупреждения зависит от ее шаблона разработки:</span><span class="sxs-lookup"><span data-stu-id="a3721-358">The supplemental instruction for a warning is based on its design pattern:</span></span>



| <span data-ttu-id="a3721-359">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a3721-359">Pattern</span></span>            | <span data-ttu-id="a3721-360">Дополнительная инструкция</span><span class="sxs-lookup"><span data-stu-id="a3721-360">Supplemental instruction</span></span>                                            |
|--------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3721-361">Осведомленность</span><span class="sxs-lookup"><span data-stu-id="a3721-361">Awareness</span></span><br/>                 | <span data-ttu-id="a3721-362">Объясните смысл и почему это важно.</span><span class="sxs-lookup"><span data-stu-id="a3721-362">Explain the implication and why it is important.</span></span><br/>                        |
| <span data-ttu-id="a3721-363">Приближающаяся проблема</span><span class="sxs-lookup"><span data-stu-id="a3721-363">Imminent problem</span></span><br/>          | <span data-ttu-id="a3721-364">Объясните условие и его важность.</span><span class="sxs-lookup"><span data-stu-id="a3721-364">Explain the condition and why it is important.</span></span><br/>                          |
| <span data-ttu-id="a3721-365">Подтверждение нерискованного действия</span><span class="sxs-lookup"><span data-stu-id="a3721-365">Risky action confirmation</span></span><br/> | <span data-ttu-id="a3721-366">Объясните все неочевидные причины, по которым пользователю может не потребоваться продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="a3721-366">Explain any non-obvious reasons why the user might not want to proceed.</span></span><br/> |



 

-   <span data-ttu-id="a3721-367">**Не повторяйте основную инструкцию с слегка отличающимися словами.**</span><span class="sxs-lookup"><span data-stu-id="a3721-367">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="a3721-368">Вместо этого пропустите вспомогательную инструкцию, если больше не нужно добавлять.</span><span class="sxs-lookup"><span data-stu-id="a3721-368">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="a3721-369">Используйте предложения Complete, прописные и закрывающие знаки пунктуации.</span><span class="sxs-lookup"><span data-stu-id="a3721-369">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="a3721-370">Кнопки фиксации</span><span class="sxs-lookup"><span data-stu-id="a3721-370">Commit buttons</span></span>

-   <span data-ttu-id="a3721-371">Для диалоговых окон предупреждений кнопки фиксации основываются на шаблоне разработки:</span><span class="sxs-lookup"><span data-stu-id="a3721-371">For warning dialog boxes, the commit buttons are based on its design pattern:</span></span>



| <span data-ttu-id="a3721-372">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a3721-372">Pattern</span></span>               | <span data-ttu-id="a3721-373">Кнопки фиксации</span><span class="sxs-lookup"><span data-stu-id="a3721-373">Commit buttons</span></span>        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3721-374">Осведомленность</span><span class="sxs-lookup"><span data-stu-id="a3721-374">Awareness</span></span><br/>                 | <span data-ttu-id="a3721-375">Близко.</span><span class="sxs-lookup"><span data-stu-id="a3721-375">Close.</span></span> <span data-ttu-id="a3721-376">Не используйте ОК, поскольку предполагается, что потенциальные проблемы являются нормальными.</span><span class="sxs-lookup"><span data-stu-id="a3721-376">Don't use OK because it suggests that potential problems are OK.</span></span><br/>                              |
| <span data-ttu-id="a3721-377">Приближающаяся проблема</span><span class="sxs-lookup"><span data-stu-id="a3721-377">Imminent problem</span></span><br/>          | <span data-ttu-id="a3721-378">Кнопка или ссылка на команду для каждого параметра или значение ОК, если действие выполняется за пределами этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a3721-378">A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span><br/> |
| <span data-ttu-id="a3721-379">Подтверждение нерискованного действия</span><span class="sxs-lookup"><span data-stu-id="a3721-379">Risky action confirmation</span></span><br/> | <span data-ttu-id="a3721-380">Да, нет.</span><span class="sxs-lookup"><span data-stu-id="a3721-380">Yes, No.</span></span><br/>                                                                                             |



 

-   <span data-ttu-id="a3721-381">**Неправильно**:</span><span class="sxs-lookup"><span data-stu-id="a3721-381">**Incorrect:**</span></span>
-   ![<span data-ttu-id="a3721-382">снимок экрана с диалоговым окном "предупреждение" с кнопкой "ОК"</span><span class="sxs-lookup"><span data-stu-id="a3721-382">screen shot of warning dialog box with ok button</span></span> ](images/mess-warn-image26.png)
-   <span data-ttu-id="a3721-383">Проблемы не работают, поэтому вместо них используйте Close.</span><span class="sxs-lookup"><span data-stu-id="a3721-383">Problems aren't OK, so use Close instead.</span></span>

## <a name="documentation"></a><span data-ttu-id="a3721-384">Документация</span><span class="sxs-lookup"><span data-stu-id="a3721-384">Documentation</span></span>

<span data-ttu-id="a3721-385">При ссылке на предупреждения:</span><span class="sxs-lookup"><span data-stu-id="a3721-385">When referring to warnings:</span></span>

-   <span data-ttu-id="a3721-386">Если предупреждение запрашивает вопрос, обратитесь к предупреждению по его вопросу. в противном случае используйте основную инструкцию.</span><span class="sxs-lookup"><span data-stu-id="a3721-386">If the warning asks a question, refer to a warning by its question; otherwise, use the main instruction.</span></span> <span data-ttu-id="a3721-387">Если вопрос или Основная инструкция являются длинными или подробными, обобщение их.</span><span class="sxs-lookup"><span data-stu-id="a3721-387">If the question or main instruction is long or detailed, summarize it.</span></span>
-   <span data-ttu-id="a3721-388">При необходимости в качестве сообщения может появиться диалоговое окно с предупреждением.</span><span class="sxs-lookup"><span data-stu-id="a3721-388">If necessary, you may refer to a warning dialog box as a message.</span></span>
-   <span data-ttu-id="a3721-389">По возможности отформатируйте текст, используя полужирный шрифт.</span><span class="sxs-lookup"><span data-stu-id="a3721-389">When possible, format the text using bold.</span></span> <span data-ttu-id="a3721-390">В противном случае заключите текст в кавычки, только если это необходимо для предотвращения путаницы.</span><span class="sxs-lookup"><span data-stu-id="a3721-390">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="a3721-391">Пример. сообщение о **незащищенных элементах?** нажмите кнопку Да.</span><span class="sxs-lookup"><span data-stu-id="a3721-391">Example: In the **Do you want to display the nonsecure items?** message, click Yes.</span></span>

 

