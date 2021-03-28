---
description: В Windows 7 и более поздних версиях можно добавлять команды в папку с помощью Desktop.ini. Дополнительные сведения о Desktop.ini файлах см. в статье Настройка папок с помощью Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: Реализация пользовательских команд для папок с помощью Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133726133abe884863a0b4d2abc0cc76aab1310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985433"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="42cf4-104">Реализация пользовательских команд для папок с помощью Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="42cf4-104">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="42cf4-105">В Windows 7 и более поздних версиях можно добавлять команды в папку с помощью Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="42cf4-105">In Windows 7 and later, you can add verbs to a folder by using Desktop.ini.</span></span> <span data-ttu-id="42cf4-106">Дополнительные сведения о Desktop.ini файлах см. [в статье Настройка папок с помощью Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="42cf4-106">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="42cf4-107">Desktop.ini файлы всегда должны быть помечены как   +  **скрытые** системой, чтобы они не отображались для пользователей.</span><span class="sxs-lookup"><span data-stu-id="42cf4-107">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="42cf4-108">Чтобы добавить пользовательские команды для папок с помощью файла Desktop.ini, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="42cf4-108">To add custom verbs for folders through a Desktop.ini file, perform the following steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="42cf4-109">Инструкции</span><span class="sxs-lookup"><span data-stu-id="42cf4-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="42cf4-110">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="42cf4-110">Step 1:</span></span>

<span data-ttu-id="42cf4-111">Создайте папку, которая помечена как доступная **только для чтения** или как **система**.</span><span class="sxs-lookup"><span data-stu-id="42cf4-111">Create a folder that is marked **Read-only** or **System**.</span></span>

### <a name="step-2"></a><span data-ttu-id="42cf4-112">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="42cf4-112">Step 2:</span></span>

<span data-ttu-id="42cf4-113">Создайте файл Desktop.ini, содержащий \[ . Шеллклассинфо \] директорикласс = ProgID папки.</span><span class="sxs-lookup"><span data-stu-id="42cf4-113">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>

### <a name="step-3"></a><span data-ttu-id="42cf4-114">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="42cf4-114">Step 3:</span></span>

<span data-ttu-id="42cf4-115">В реестре создайте **классы hKey \_ с \_ корневой** \\ **папкой ProgID** со значением канусефордиректори.</span><span class="sxs-lookup"><span data-stu-id="42cf4-115">In the registry, create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="42cf4-116">Значение Канусефордиректори позволяет избежать неправильного использования ProgID, которые не участвуют в реализации пользовательских команд для папок с помощью Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="42cf4-116">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>

### <a name="step-4"></a><span data-ttu-id="42cf4-117">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="42cf4-117">Step 4:</span></span>

<span data-ttu-id="42cf4-118">Добавьте команды в подключе ProgID **папки** , например:</span><span class="sxs-lookup"><span data-stu-id="42cf4-118">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a><span data-ttu-id="42cf4-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="42cf4-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="42cf4-120">Эти команды могут быть глаголами по умолчанию. в этом случае двойной щелчок папки активирует команду.</span><span class="sxs-lookup"><span data-stu-id="42cf4-120">These verbs can be the default verbs, in which case double-clicking the folder activates the verb.</span></span>

 

 

 



