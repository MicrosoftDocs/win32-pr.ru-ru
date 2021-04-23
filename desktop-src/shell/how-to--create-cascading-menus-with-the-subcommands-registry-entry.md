---
description: В Windows 7 и более поздних версиях можно использовать запись подкоманд в реестре для создания каскадных меню с помощью процедуры, приведенной в этом разделе.
title: Создание каскадных меню с записью реестра "подкоманды"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b1168daae5ea927f079c66eb436c099f8b3d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997714"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="e87e7-103">Создание каскадных меню с помощью записи реестра "подкоманды"</span><span class="sxs-lookup"><span data-stu-id="e87e7-103">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="e87e7-104">В Windows 7 и более поздних версиях можно использовать запись подкоманд в реестре для создания каскадных меню с помощью процедуры, приведенной в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="e87e7-104">In Windows 7 and later, you can use the SubCommands entry in the registry to create cascading menus by using the procedure given in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="e87e7-105">Инструкции</span><span class="sxs-lookup"><span data-stu-id="e87e7-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="e87e7-106">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="e87e7-106">Step 1:</span></span>

<span data-ttu-id="e87e7-107">Создайте новый подраздел в разделе **\_ классы hKey \_ root** \\ *ProgID* \\ **Shell**, где *ProgID* — это тип файла, для которого необходимо добавить каскадное меню.</span><span class="sxs-lookup"><span data-stu-id="e87e7-107">Create a new subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**, where *ProgID* is the file type for which you want to add a cascading menu.</span></span> <span data-ttu-id="e87e7-108">Этот новый подраздел можно назвать любым нужным образом.</span><span class="sxs-lookup"><span data-stu-id="e87e7-108">You can name this new subkey anything you'd like.</span></span> <span data-ttu-id="e87e7-109">В оставшейся части этого раздела мы назовем его *каскадемену*, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="e87e7-109">For the remainder of this topic, we'll call it *CascadeMenu*, as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a><span data-ttu-id="e87e7-110">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="e87e7-110">Step 2:</span></span>

<span data-ttu-id="e87e7-111">Добавьте запись с именем "Муиверб" типа **reg \_ SZ** или **reg \_ expand \_ SZ** в подраздел *каскадемену* .</span><span class="sxs-lookup"><span data-stu-id="e87e7-111">Add an entry named "MUIVerb", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="e87e7-112">Назначьте этой записи строковое значение, например "проверить каскадное меню".</span><span class="sxs-lookup"><span data-stu-id="e87e7-112">Assign this entry a string value such as "Test Cascade Menu".</span></span> <span data-ttu-id="e87e7-113">Как правило, эта строка предоставляется в виде ссылки на ресурс в виде " @file , ресурса".</span><span class="sxs-lookup"><span data-stu-id="e87e7-113">Normally, this string is provided as a resource reference in the form "@file, resource".</span></span> <span data-ttu-id="e87e7-114">Значение (по умолчанию) для подраздела *каскадемену* не должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="e87e7-114">The (Default) value for the *CascadeMenu* subkey should not be set.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a><span data-ttu-id="e87e7-115">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="e87e7-115">Step 3:</span></span>

<span data-ttu-id="e87e7-116">Добавьте в подраздел *каскадемену* запись с именем "подкоманды", введите **reg \_ SZ** или **reg \_ expand \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="e87e7-116">Add an entry named "SubCommands", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="e87e7-117">Присвойте этой записи разделенный точками с запятой список команд, которые должны отображаться в меню в нужном порядке их отображения.</span><span class="sxs-lookup"><span data-stu-id="e87e7-117">Assign this entry a semicolon-delimited list of the verbs that should appear on the menu, in their desired order of appearance.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a><span data-ttu-id="e87e7-118">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="e87e7-118">Step 4:</span></span>

<span data-ttu-id="e87e7-119">Заполните подраздел **коммандсторе** с реализацией глаголов для любых методов реализации пользовательских статических глаголов, которые использовались в записи подкоманд. Например:</span><span class="sxs-lookup"><span data-stu-id="e87e7-119">Populate the **CommandStore** subkey with verb implementations for any custom static verb implementation methods that you've used in your SubCommands entry; for example:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  CommandStore
                     Shell
                        VerbName
                           command
                              (Default) = notepad.exe %1
```

## <a name="related-topics"></a><span data-ttu-id="e87e7-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e87e7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e87e7-121">Создание статических каскадных меню</span><span class="sxs-lookup"><span data-stu-id="e87e7-121">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
</dt> </dl>

 

 



