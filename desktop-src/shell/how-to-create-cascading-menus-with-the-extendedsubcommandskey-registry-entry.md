---
description: В Windows 7 и более поздних версиях можно использовать подраздел Екстендедсубкоммандскэй для создания расширенных каскадных меню.
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: Создание каскадных меню с помощью записи реестра Екстендедсубкоммандскэй
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813712"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="4ec95-103">Создание каскадных меню с помощью записи реестра Екстендедсубкоммандскэй</span><span class="sxs-lookup"><span data-stu-id="4ec95-103">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="4ec95-104">В Windows 7 и более поздних версиях можно использовать подраздел **екстендедсубкоммандскэй** для создания расширенных каскадных меню.</span><span class="sxs-lookup"><span data-stu-id="4ec95-104">In Windows 7 and later, you can use the **ExtendedSubCommandsKey** subkey to create extended cascading menus.</span></span>

<span data-ttu-id="4ec95-105">На следующем снимке экрана показан пример расширенного каскадного меню.</span><span class="sxs-lookup"><span data-stu-id="4ec95-105">The following screen shot is an example of an extended cascading menu.</span></span>

![снимок экрана с расширенным каскадным меню для устройств](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="4ec95-107">Так **как \_ \_ корневые классы классов hKey** являются сочетанием **\_ текущего \_ пользователя hKey** и раздела **hKey \_ \_**, можно зарегистрировать подкоманды в подразделе " **классы \_ текущего \_ пользовательского** \\ **программного обеспечения** hKey" \\  .</span><span class="sxs-lookup"><span data-stu-id="4ec95-107">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register the subverbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="4ec95-108">Преимущество этого подхода в том, что повышенное разрешение не требуется.</span><span class="sxs-lookup"><span data-stu-id="4ec95-108">The advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="4ec95-109">Другие ассоциации файлов могут повторно использовать весь набор команд, указав тот же подраздел **екстендедсубкоммандскэй** .</span><span class="sxs-lookup"><span data-stu-id="4ec95-109">Other file associations can reuse this entire set of verbs by specifying the same **ExtendedSubCommandsKey** subkey.</span></span> <span data-ttu-id="4ec95-110">Если не нужно повторно использовать этот набор команд, можно вывести список команд в родительском элементе.</span><span class="sxs-lookup"><span data-stu-id="4ec95-110">If you do not need to reuse this set of verbs, you can list the verbs under the parent.</span></span> <span data-ttu-id="4ec95-111">В этом случае убедитесь, что значение по умолчанию родительского элемента пустое, как показано в примере записи реестра в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="4ec95-111">In this case, make sure the default value of the parent is empty, as illustrated in the registry entry example in this section.</span></span>

## <a name="instructions"></a><span data-ttu-id="4ec95-112">Инструкции</span><span class="sxs-lookup"><span data-stu-id="4ec95-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="4ec95-113">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="4ec95-113">Step 1:</span></span>

<span data-ttu-id="4ec95-114">Создайте подраздел в разделе **\_ Classes \_ root** \\ *ProgID* \\ **Shell** \\ *каскадеменукэй* и присвойте каскадеменукэй имя, например *каскадетест*, например.</span><span class="sxs-lookup"><span data-stu-id="4ec95-114">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**\\*CascadeMenuKey* and give the CascadeMenuKey a name such as *CascadeTest*, for example.</span></span> <span data-ttu-id="4ec95-115">Затем добавьте запись Муиверб типа **reg \_ SZ** и присвойте ей имя, такое как проверка каскадного меню 2, как показано в следующем примере реестра.</span><span class="sxs-lookup"><span data-stu-id="4ec95-115">Then add a MUIVerb entry of **REG\_SZ** type and give it a name such as Test Cascade Menu 2, as illustrated in the following registry example.</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a><span data-ttu-id="4ec95-116">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="4ec95-116">Step 2:</span></span>

<span data-ttu-id="4ec95-117">В созданном вами подразделе *каскадетест* добавьте подраздел **екстендедсубкоммандскэй** , а затем добавьте подкоманды Document (из типа **reg \_ SZ**), например:</span><span class="sxs-lookup"><span data-stu-id="4ec95-117">Under the *CascadeTest* subkey that you created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of type **REG\_SZ**); for example:</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Layout
               Properties
               Select all
```

<span data-ttu-id="4ec95-118">Убедитесь, что значение по умолчанию для подраздела *тест Cascade меню 2* пусто и отображается как **(значение не задано)**.</span><span class="sxs-lookup"><span data-stu-id="4ec95-118">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

### <a name="step-3"></a><span data-ttu-id="4ec95-119">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="4ec95-119">Step 3:</span></span>

<span data-ttu-id="4ec95-120">Заполните подкоманды с помощью любой из следующих статических реализаций глаголов.</span><span class="sxs-lookup"><span data-stu-id="4ec95-120">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="4ec95-121">Обратите внимание, что подраздел Коммандфлагс представляет значения ЕКСПКМДФЛАГС.</span><span class="sxs-lookup"><span data-stu-id="4ec95-121">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="4ec95-122">Если вы хотите добавить разделитель до или после пункта меню Cascade, используйте ЕКФ \_ сепараторбефоре (0x20) или ЕКФ \_ сепараторафтер (0x40).</span><span class="sxs-lookup"><span data-stu-id="4ec95-122">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="4ec95-123">Описание этих флагов Windows 7 и более поздних версий см. в разделе [**иексплореркомманд::-flags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="4ec95-123">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="4ec95-124">ЕКФ \_ сепараторбефоре работает только для пунктов меню верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4ec95-124">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="4ec95-125">Муиверб имеет тип **reg \_ SZ**, а Коммандфлагс имеет тип **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="4ec95-125">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Shell
                  cmd1
                     MUIVerb = Notepad
                     command
                        (Default) = %SystemRoot%\system32\notepad.exe %1
                  cmd2
                     MUIVerb = Wordpad
                     CommandFlags = 0x20
                     command
                        (Default) = C:\Program Files\Windows NT\Accessories\wordpad.exe %1
```

## <a name="remarks"></a><span data-ttu-id="4ec95-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="4ec95-126">Remarks</span></span>

<span data-ttu-id="4ec95-127">На следующем снимке экрана показан пример записи предыдущего раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="4ec95-127">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![снимок экрана, показывающий пример каскадного меню, в котором отображаются параметры блокнота и WordPad](images/file-assoc/testcascademenu2.png)

 

 



