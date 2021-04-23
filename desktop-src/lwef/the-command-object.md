---
title: Объект Command
description: Объект Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710275"
---
# <a name="the-command-object"></a><span data-ttu-id="19d52-103">Объект Command</span><span class="sxs-lookup"><span data-stu-id="19d52-103">The Command Object</span></span>

<span data-ttu-id="19d52-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="19d52-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="19d52-105">Объект [**Command**](/windows/desktop/lwef/the-command-object) — это элемент в коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="19d52-105">A [**Command**](/windows/desktop/lwef/the-command-object) object is an item in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="19d52-106">Сервер предоставляет пользователю доступ к объектам **команды** , когда клиентское приложение преобразуется в входные данные.</span><span class="sxs-lookup"><span data-stu-id="19d52-106">The server provides the user access to your **Command** objects when your client application becomes input-active.</span></span>

-   [<span data-ttu-id="19d52-107">Свойства объекта Command</span><span class="sxs-lookup"><span data-stu-id="19d52-107">Command Object Properties</span></span>](command-object-properties.md)

<span data-ttu-id="19d52-108">Чтобы получить доступ к свойству объекта [**Command**](/windows/desktop/lwef/the-command-object) , вы ссылаетесь на него в своей коллекции, используя свойство [**Name**](name-property.md) .</span><span class="sxs-lookup"><span data-stu-id="19d52-108">To access the property of a [**Command**](/windows/desktop/lwef/the-command-object) object, you reference it in its collection using its [**Name**](name-property.md) property.</span></span> <span data-ttu-id="19d52-109">В VBScript и Visual Basic можно использовать свойство **Name** напрямую:</span><span class="sxs-lookup"><span data-stu-id="19d52-109">In VBScript and Visual Basic you can use the **Name** property directly:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="19d52-110">Для языков программирования, которые не поддерживают коллекции, используйте [**Командный**](command-method.md) метод:</span><span class="sxs-lookup"><span data-stu-id="19d52-110">For programming languages that don't support collections, use the [**Command**](command-method.md) method:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="19d52-111">Вы также можете ссылаться на объект Command, создав ссылку на него.</span><span class="sxs-lookup"><span data-stu-id="19d52-111">You can also reference a Command object by creating a reference to it.</span></span> <span data-ttu-id="19d52-112">В Visual Basic объявите объектную переменную и используйте инструкцию SET для создания ссылки:</span><span class="sxs-lookup"><span data-stu-id="19d52-112">In Visual Basic, declare an object variable and use the Set statement to create the reference:</span></span>


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="19d52-113">В Visual Basic 5,0 можно также объявить объект как тип [**иажентктлкоммандекс**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) и создать ссылку.</span><span class="sxs-lookup"><span data-stu-id="19d52-113">In Visual Basic 5.0, you can also declare the object as type [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) and create the reference.</span></span> <span data-ttu-id="19d52-114">Это соглашение включает раннее связывание, что приводит к лучшей производительности:</span><span class="sxs-lookup"><span data-stu-id="19d52-114">This convention enables early binding, which results in better performance:</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="19d52-115">В VBScript можно объявить ссылку как конкретный тип, но вы по-прежнему можете объявить переменную и задать ее для [**команды**](/windows/desktop/lwef/the-command-object) в коллекции:</span><span class="sxs-lookup"><span data-stu-id="19d52-115">In VBScript, you can declare a reference as a particular type, but you can still declare the variable and set it to the [**Command**](/windows/desktop/lwef/the-command-object) in the collection:</span></span>


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="19d52-116">Команда может отображаться во всплывающем меню символа, в окне команд или в обоих окнах.</span><span class="sxs-lookup"><span data-stu-id="19d52-116">A command may appear in either the character's pop-up menu and the Commands Window, or in both.</span></span> <span data-ttu-id="19d52-117">Для отображения во всплывающем меню он должен иметь заголовок и иметь свойство [**Visible**](visible-property.md) со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="19d52-117">To appear in the pop-up menu it must have a caption and have the [**Visible**](visible-property.md) property set to **True**.</span></span> <span data-ttu-id="19d52-118">Кроме того, свойство **Visible** объекта коллекции Commands также должно иметь значение **true**.</span><span class="sxs-lookup"><span data-stu-id="19d52-118">In addition, its Commands collection object **Visible** property must also be set to **True**.</span></span> <span data-ttu-id="19d52-119">Для отображения в окне команды в [**команде**](/windows/desktop/lwef/the-command-object) должны быть заданы свойства [**Caption**](caption-property.md) и [**Voice**](voice-property.md) .</span><span class="sxs-lookup"><span data-stu-id="19d52-119">To appear in the Commands Window, a [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Caption**](caption-property.md) and [**Voice**](voice-property.md) properties set.</span></span> <span data-ttu-id="19d52-120">Обратите внимание, что во время отображения меню записи всплывающего меню не меняются.</span><span class="sxs-lookup"><span data-stu-id="19d52-120">Note that a character's pop-up menu entries do not change while the menu displays.</span></span> <span data-ttu-id="19d52-121">При добавлении или удалении команд или изменении их свойств во время отображения всплывающего меню символа меню отображает эти изменения при каждом отображении пользователем.</span><span class="sxs-lookup"><span data-stu-id="19d52-121">If you add or remove commands or change their properties while the character's pop-up menu is displayed, the menu displays those changes whenever the user next displays it.</span></span> <span data-ttu-id="19d52-122">Однако окно команды динамически отражает любые внесенные изменения.</span><span class="sxs-lookup"><span data-stu-id="19d52-122">However, the Commands Window dynamically reflects any changes you make.</span></span>

<span data-ttu-id="19d52-123">В следующей таблице показано, как свойства [**команды**](/windows/desktop/lwef/the-command-object) влияют на ее представление.</span><span class="sxs-lookup"><span data-stu-id="19d52-123">The following table summarizes how the properties of a [**Command**](/windows/desktop/lwef/the-command-object) affect its presentation:</span></span>



<span data-ttu-id="19d52-124">Свойство Caption</span><span class="sxs-lookup"><span data-stu-id="19d52-124">Caption Property</span></span>

<span data-ttu-id="19d52-125">Voice-Caption, свойство</span><span class="sxs-lookup"><span data-stu-id="19d52-125">Voice-Caption Property</span></span>

<span data-ttu-id="19d52-126">Свойство Voice</span><span class="sxs-lookup"><span data-stu-id="19d52-126">Voice Property</span></span>

<span data-ttu-id="19d52-127">Свойство Visible</span><span class="sxs-lookup"><span data-stu-id="19d52-127">Visible Property</span></span>

<span data-ttu-id="19d52-128">Свойство Enabled</span><span class="sxs-lookup"><span data-stu-id="19d52-128">Enabled Property</span></span>

<span data-ttu-id="19d52-129">Отображается во всплывающем меню "символ"</span><span class="sxs-lookup"><span data-stu-id="19d52-129">Appears in Character's Pop-up Menu</span></span>

<span data-ttu-id="19d52-130">Отображается в окне "команды"</span><span class="sxs-lookup"><span data-stu-id="19d52-130">Appears in Commands Window</span></span>

<span data-ttu-id="19d52-131">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-131">Yes</span></span>

<span data-ttu-id="19d52-132">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-132">Yes</span></span>

<span data-ttu-id="19d52-133">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-133">Yes</span></span>

<span data-ttu-id="19d52-134">True</span><span class="sxs-lookup"><span data-stu-id="19d52-134">True</span></span>

<span data-ttu-id="19d52-135">True</span><span class="sxs-lookup"><span data-stu-id="19d52-135">True</span></span>

<span data-ttu-id="19d52-136">Обычная, использование [ **подписи**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-136">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="19d52-137">Да, с помощью [ **воицекаптион**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-137">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="19d52-138">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-138">Yes</span></span>

<span data-ttu-id="19d52-139">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-139">Yes</span></span>

<span data-ttu-id="19d52-140">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-140">Yes</span></span>

<span data-ttu-id="19d52-141">True</span><span class="sxs-lookup"><span data-stu-id="19d52-141">True</span></span>

<span data-ttu-id="19d52-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-142">False</span></span>

<span data-ttu-id="19d52-143">Отключено, используется [ **заголовок**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-143">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="19d52-144">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-144">No</span></span>

<span data-ttu-id="19d52-145">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-145">Yes</span></span>

<span data-ttu-id="19d52-146">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-146">Yes</span></span>

<span data-ttu-id="19d52-147">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-147">Yes</span></span>

<span data-ttu-id="19d52-148">False</span><span class="sxs-lookup"><span data-stu-id="19d52-148">False</span></span>

<span data-ttu-id="19d52-149">True</span><span class="sxs-lookup"><span data-stu-id="19d52-149">True</span></span>

<span data-ttu-id="19d52-150">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-150">Does not appear</span></span>

<span data-ttu-id="19d52-151">Да, с помощью [ **воицекаптион**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-151">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="19d52-152">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-152">Yes</span></span>

<span data-ttu-id="19d52-153">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-153">Yes</span></span>

<span data-ttu-id="19d52-154">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-154">Yes</span></span>

<span data-ttu-id="19d52-155">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-155">False</span></span>

<span data-ttu-id="19d52-156">False</span><span class="sxs-lookup"><span data-stu-id="19d52-156">False</span></span>

<span data-ttu-id="19d52-157">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-157">Does not appear</span></span>

<span data-ttu-id="19d52-158">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-158">No</span></span>

<span data-ttu-id="19d52-159">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-159">Yes</span></span>

<span data-ttu-id="19d52-160">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-160">Yes</span></span>

<span data-ttu-id="19d52-161">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-161">No</span></span> 

<span data-ttu-id="19d52-162">True</span><span class="sxs-lookup"><span data-stu-id="19d52-162">True</span></span>

<span data-ttu-id="19d52-163">True</span><span class="sxs-lookup"><span data-stu-id="19d52-163">True</span></span>

<span data-ttu-id="19d52-164">Обычная, использование [ **подписи**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-164">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="19d52-165">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-165">No</span></span>

<span data-ttu-id="19d52-166">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-166">Yes</span></span>

<span data-ttu-id="19d52-167">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-167">Yes</span></span>

<span data-ttu-id="19d52-168">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-168">No</span></span> 

<span data-ttu-id="19d52-169">True</span><span class="sxs-lookup"><span data-stu-id="19d52-169">True</span></span>

<span data-ttu-id="19d52-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-170">False</span></span>

<span data-ttu-id="19d52-171">Отключено, используется [ **заголовок**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-171">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="19d52-172">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-172">No</span></span>

<span data-ttu-id="19d52-173">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-173">Yes</span></span>

<span data-ttu-id="19d52-174">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-174">Yes</span></span>

<span data-ttu-id="19d52-175">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-175">No</span></span> 

<span data-ttu-id="19d52-176">False</span><span class="sxs-lookup"><span data-stu-id="19d52-176">False</span></span>

<span data-ttu-id="19d52-177">True</span><span class="sxs-lookup"><span data-stu-id="19d52-177">True</span></span>

<span data-ttu-id="19d52-178">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-178">Does not appear</span></span>

<span data-ttu-id="19d52-179">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-179">No</span></span>

<span data-ttu-id="19d52-180">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-180">Yes</span></span>

<span data-ttu-id="19d52-181">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-181">Yes</span></span>

<span data-ttu-id="19d52-182">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-182">No</span></span> 

<span data-ttu-id="19d52-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-183">False</span></span>

<span data-ttu-id="19d52-184">False</span><span class="sxs-lookup"><span data-stu-id="19d52-184">False</span></span>

<span data-ttu-id="19d52-185">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-185">Does not appear</span></span>

<span data-ttu-id="19d52-186">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-186">No</span></span>

<span data-ttu-id="19d52-187">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-187">No</span></span> 

<span data-ttu-id="19d52-188">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-188">Yes</span></span>

<span data-ttu-id="19d52-189">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-189">Yes</span></span>

<span data-ttu-id="19d52-190">True</span><span class="sxs-lookup"><span data-stu-id="19d52-190">True</span></span>

<span data-ttu-id="19d52-191">True</span><span class="sxs-lookup"><span data-stu-id="19d52-191">True</span></span>

<span data-ttu-id="19d52-192">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-192">Does not appear</span></span>

<span data-ttu-id="19d52-193">Да, с помощью [ **воицекаптион**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-193">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="19d52-194">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-194">No</span></span> 

<span data-ttu-id="19d52-195">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-195">Yes</span></span>

<span data-ttu-id="19d52-196">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-196">Yes</span></span>

<span data-ttu-id="19d52-197">True</span><span class="sxs-lookup"><span data-stu-id="19d52-197">True</span></span>

<span data-ttu-id="19d52-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-198">False</span></span>

<span data-ttu-id="19d52-199">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-199">Does not appear</span></span>

<span data-ttu-id="19d52-200">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-200">No</span></span>

<span data-ttu-id="19d52-201">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-201">No</span></span> 

<span data-ttu-id="19d52-202">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-202">Yes</span></span>

<span data-ttu-id="19d52-203">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-203">Yes</span></span>

<span data-ttu-id="19d52-204">False</span><span class="sxs-lookup"><span data-stu-id="19d52-204">False</span></span>

<span data-ttu-id="19d52-205">True</span><span class="sxs-lookup"><span data-stu-id="19d52-205">True</span></span>

<span data-ttu-id="19d52-206">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-206">Does not appear</span></span>

<span data-ttu-id="19d52-207">Да, с помощью [ **воицекаптион**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-207">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="19d52-208">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-208">No</span></span> 

<span data-ttu-id="19d52-209">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-209">Yes</span></span>

<span data-ttu-id="19d52-210">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-210">Yes</span></span>

<span data-ttu-id="19d52-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-211">False</span></span>

<span data-ttu-id="19d52-212">False</span><span class="sxs-lookup"><span data-stu-id="19d52-212">False</span></span>

<span data-ttu-id="19d52-213">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-213">Does not appear</span></span>

<span data-ttu-id="19d52-214">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-214">No</span></span>

<span data-ttu-id="19d52-215">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-215">No</span></span> 

<span data-ttu-id="19d52-216">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-216">Yes</span></span>

<span data-ttu-id="19d52-217">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-217">No</span></span> 

<span data-ttu-id="19d52-218">True</span><span class="sxs-lookup"><span data-stu-id="19d52-218">True</span></span>

<span data-ttu-id="19d52-219">True</span><span class="sxs-lookup"><span data-stu-id="19d52-219">True</span></span>

<span data-ttu-id="19d52-220">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-220">Does not appear</span></span>

<span data-ttu-id="19d52-221">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-221">No</span></span>

<span data-ttu-id="19d52-222">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-222">No</span></span> 

<span data-ttu-id="19d52-223">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-223">Yes</span></span>

<span data-ttu-id="19d52-224">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-224">No</span></span> 

<span data-ttu-id="19d52-225">True</span><span class="sxs-lookup"><span data-stu-id="19d52-225">True</span></span>

<span data-ttu-id="19d52-226">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-226">False</span></span>

<span data-ttu-id="19d52-227">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-227">Does not appear</span></span>

<span data-ttu-id="19d52-228">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-228">No</span></span>

<span data-ttu-id="19d52-229">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-229">No</span></span> 

<span data-ttu-id="19d52-230">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-230">Yes</span></span>

<span data-ttu-id="19d52-231">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-231">No</span></span> 

<span data-ttu-id="19d52-232">False</span><span class="sxs-lookup"><span data-stu-id="19d52-232">False</span></span>

<span data-ttu-id="19d52-233">True</span><span class="sxs-lookup"><span data-stu-id="19d52-233">True</span></span>

<span data-ttu-id="19d52-234">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-234">Does not appear</span></span>

<span data-ttu-id="19d52-235">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-235">No</span></span>

<span data-ttu-id="19d52-236">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-236">No</span></span> 

<span data-ttu-id="19d52-237">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-237">Yes</span></span>

<span data-ttu-id="19d52-238">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-238">No</span></span> 

<span data-ttu-id="19d52-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-239">False</span></span>

<span data-ttu-id="19d52-240">False</span><span class="sxs-lookup"><span data-stu-id="19d52-240">False</span></span>

<span data-ttu-id="19d52-241">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-241">Does not appear</span></span>

<span data-ttu-id="19d52-242">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-242">No</span></span>

<span data-ttu-id="19d52-243">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-243">Yes</span></span>

<span data-ttu-id="19d52-244">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-244">No</span></span> 

<span data-ttu-id="19d52-245">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-245">Yes</span></span>

<span data-ttu-id="19d52-246">True</span><span class="sxs-lookup"><span data-stu-id="19d52-246">True</span></span>

<span data-ttu-id="19d52-247">True</span><span class="sxs-lookup"><span data-stu-id="19d52-247">True</span></span>

<span data-ttu-id="19d52-248">Обычная, использование [ **подписи**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-248">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="19d52-249">Да, с использованием [ **заголовка**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-249">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="19d52-250">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-250">Yes</span></span>

<span data-ttu-id="19d52-251">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-251">No</span></span> 

<span data-ttu-id="19d52-252">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-252">Yes</span></span>

<span data-ttu-id="19d52-253">True</span><span class="sxs-lookup"><span data-stu-id="19d52-253">True</span></span>

<span data-ttu-id="19d52-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-254">False</span></span>

<span data-ttu-id="19d52-255">Отключено, используется [ **заголовок**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-255">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="19d52-256">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-256">No</span></span>

<span data-ttu-id="19d52-257">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-257">Yes</span></span>

<span data-ttu-id="19d52-258">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-258">No</span></span> 

<span data-ttu-id="19d52-259">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-259">Yes</span></span>

<span data-ttu-id="19d52-260">False</span><span class="sxs-lookup"><span data-stu-id="19d52-260">False</span></span>

<span data-ttu-id="19d52-261">True</span><span class="sxs-lookup"><span data-stu-id="19d52-261">True</span></span>

<span data-ttu-id="19d52-262">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-262">Does not appear</span></span>

<span data-ttu-id="19d52-263">Да, с использованием [ **заголовка**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-263">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="19d52-264">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-264">Yes</span></span>

<span data-ttu-id="19d52-265">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-265">No</span></span> 

<span data-ttu-id="19d52-266">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-266">Yes</span></span>

<span data-ttu-id="19d52-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-267">False</span></span>

<span data-ttu-id="19d52-268">False</span><span class="sxs-lookup"><span data-stu-id="19d52-268">False</span></span>

<span data-ttu-id="19d52-269">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-269">Does not appear</span></span>

<span data-ttu-id="19d52-270">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-270">No</span></span>

<span data-ttu-id="19d52-271">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-271">Yes</span></span>

<span data-ttu-id="19d52-272">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-272">No</span></span> 

<span data-ttu-id="19d52-273">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-273">No</span></span> 

<span data-ttu-id="19d52-274">True</span><span class="sxs-lookup"><span data-stu-id="19d52-274">True</span></span>

<span data-ttu-id="19d52-275">True</span><span class="sxs-lookup"><span data-stu-id="19d52-275">True</span></span>

<span data-ttu-id="19d52-276">Обычная, использование [ **подписи**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-276">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="19d52-277">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-277">No</span></span>

<span data-ttu-id="19d52-278">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-278">Yes</span></span>

<span data-ttu-id="19d52-279">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-279">No</span></span> 

<span data-ttu-id="19d52-280">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-280">No</span></span> 

<span data-ttu-id="19d52-281">True</span><span class="sxs-lookup"><span data-stu-id="19d52-281">True</span></span>

<span data-ttu-id="19d52-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-282">False</span></span>

<span data-ttu-id="19d52-283">Отключено, используется [ **заголовок**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="19d52-283">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="19d52-284">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-284">No</span></span>

<span data-ttu-id="19d52-285">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-285">Yes</span></span>

<span data-ttu-id="19d52-286">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-286">No</span></span> 

<span data-ttu-id="19d52-287">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-287">No</span></span> 

<span data-ttu-id="19d52-288">False</span><span class="sxs-lookup"><span data-stu-id="19d52-288">False</span></span>

<span data-ttu-id="19d52-289">True</span><span class="sxs-lookup"><span data-stu-id="19d52-289">True</span></span>

<span data-ttu-id="19d52-290">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-290">Does not appear</span></span>

<span data-ttu-id="19d52-291">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-291">No</span></span>

<span data-ttu-id="19d52-292">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-292">Yes</span></span>

<span data-ttu-id="19d52-293">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-293">No</span></span> 

<span data-ttu-id="19d52-294">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-294">No</span></span> 

<span data-ttu-id="19d52-295">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-295">False</span></span>

<span data-ttu-id="19d52-296">False</span><span class="sxs-lookup"><span data-stu-id="19d52-296">False</span></span>

<span data-ttu-id="19d52-297">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-297">Does not appear</span></span>

<span data-ttu-id="19d52-298">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-298">No</span></span>

<span data-ttu-id="19d52-299">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-299">No</span></span> 

<span data-ttu-id="19d52-300">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-300">No</span></span> 

<span data-ttu-id="19d52-301">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-301">Yes</span></span>

<span data-ttu-id="19d52-302">True</span><span class="sxs-lookup"><span data-stu-id="19d52-302">True</span></span>

<span data-ttu-id="19d52-303">True</span><span class="sxs-lookup"><span data-stu-id="19d52-303">True</span></span>

<span data-ttu-id="19d52-304">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-304">Does not appear</span></span>

<span data-ttu-id="19d52-305">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-305">No</span></span> 

<span data-ttu-id="19d52-306">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-306">No</span></span> 

<span data-ttu-id="19d52-307">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-307">No</span></span> 

<span data-ttu-id="19d52-308">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-308">Yes</span></span>

<span data-ttu-id="19d52-309">True</span><span class="sxs-lookup"><span data-stu-id="19d52-309">True</span></span>

<span data-ttu-id="19d52-310">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-310">False</span></span>

<span data-ttu-id="19d52-311">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-311">Does not appear</span></span>

<span data-ttu-id="19d52-312">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-312">No</span></span>

<span data-ttu-id="19d52-313">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-313">No</span></span> 

<span data-ttu-id="19d52-314">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-314">No</span></span> 

<span data-ttu-id="19d52-315">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-315">Yes</span></span>

<span data-ttu-id="19d52-316">False</span><span class="sxs-lookup"><span data-stu-id="19d52-316">False</span></span>

<span data-ttu-id="19d52-317">True</span><span class="sxs-lookup"><span data-stu-id="19d52-317">True</span></span>

<span data-ttu-id="19d52-318">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-318">Does not appear</span></span>

<span data-ttu-id="19d52-319">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-319">No</span></span> 

<span data-ttu-id="19d52-320">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-320">No</span></span> 

<span data-ttu-id="19d52-321">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-321">No</span></span> 

<span data-ttu-id="19d52-322">Да</span><span class="sxs-lookup"><span data-stu-id="19d52-322">Yes</span></span>

<span data-ttu-id="19d52-323">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-323">False</span></span>

<span data-ttu-id="19d52-324">False</span><span class="sxs-lookup"><span data-stu-id="19d52-324">False</span></span>

<span data-ttu-id="19d52-325">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-325">Does not appear</span></span>

<span data-ttu-id="19d52-326">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-326">No</span></span>

<span data-ttu-id="19d52-327">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-327">No</span></span> 

<span data-ttu-id="19d52-328">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-328">No</span></span> 

<span data-ttu-id="19d52-329">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-329">No</span></span> 

<span data-ttu-id="19d52-330">True</span><span class="sxs-lookup"><span data-stu-id="19d52-330">True</span></span>

<span data-ttu-id="19d52-331">True</span><span class="sxs-lookup"><span data-stu-id="19d52-331">True</span></span>

<span data-ttu-id="19d52-332">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-332">Does not appear</span></span>

<span data-ttu-id="19d52-333">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-333">No</span></span>

<span data-ttu-id="19d52-334">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-334">No</span></span> 

<span data-ttu-id="19d52-335">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-335">No</span></span> 

<span data-ttu-id="19d52-336">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-336">No</span></span> 

<span data-ttu-id="19d52-337">True</span><span class="sxs-lookup"><span data-stu-id="19d52-337">True</span></span>

<span data-ttu-id="19d52-338">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-338">False</span></span>

<span data-ttu-id="19d52-339">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-339">Does not appear</span></span>

<span data-ttu-id="19d52-340">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-340">No</span></span>

<span data-ttu-id="19d52-341">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-341">No</span></span> 

<span data-ttu-id="19d52-342">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-342">No</span></span> 

<span data-ttu-id="19d52-343">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-343">No</span></span> 

<span data-ttu-id="19d52-344">False</span><span class="sxs-lookup"><span data-stu-id="19d52-344">False</span></span>

<span data-ttu-id="19d52-345">True</span><span class="sxs-lookup"><span data-stu-id="19d52-345">True</span></span>

<span data-ttu-id="19d52-346">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-346">Does not appear</span></span>

<span data-ttu-id="19d52-347">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-347">No</span></span>

<span data-ttu-id="19d52-348">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-348">No</span></span> 

<span data-ttu-id="19d52-349">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-349">No</span></span> 

<span data-ttu-id="19d52-350">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-350">No</span></span> 

<span data-ttu-id="19d52-351">Неверно</span><span class="sxs-lookup"><span data-stu-id="19d52-351">False</span></span>

<span data-ttu-id="19d52-352">False</span><span class="sxs-lookup"><span data-stu-id="19d52-352">False</span></span>

<span data-ttu-id="19d52-353">Не отображается</span><span class="sxs-lookup"><span data-stu-id="19d52-353">Does not appear</span></span>

<span data-ttu-id="19d52-354">Нет</span><span class="sxs-lookup"><span data-stu-id="19d52-354">No</span></span>

 <span data-ttu-id="19d52-355">Значение, если значение свойства равно null.</span><span class="sxs-lookup"><span data-stu-id="19d52-355">If the property setting is null.</span></span> <span data-ttu-id="19d52-356">В некоторых языках программирования пустая строка не может интерпретироваться как строка со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="19d52-356">In some programming languages, an empty string may not be interpreted the same as a null string.</span></span>  <span data-ttu-id="19d52-357">Команда по-прежнему доступна для передачи голоса.</span><span class="sxs-lookup"><span data-stu-id="19d52-357">The command is still voice-accessible.</span></span><br/>



 

<span data-ttu-id="19d52-358">Когда сервер получает входные данные для одной из команд, он отправляет [**командное**](/windows/desktop/lwef/the-command-object) событие и передает имя **команды** в виде атрибута объекта [**UserInput**](/windows/desktop/lwef/iagentuserinput) .</span><span class="sxs-lookup"><span data-stu-id="19d52-358">When the server receives input for one of your commands, it sends a [**Command**](/windows/desktop/lwef/the-command-object) event, and passes back the name of the **Command** as an attribute of the [**UserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="19d52-359">Затем можно использовать условные операторы для сопоставления и обработки **команды**.</span><span class="sxs-lookup"><span data-stu-id="19d52-359">You can then use conditional statements to match and process the **Command**.</span></span>

 

