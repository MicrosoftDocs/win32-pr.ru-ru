---
description: Укажите пользовательский значок и метку для диска.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Назначить букве диска пользовательский значок и метку
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985476"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a><span data-ttu-id="24ccb-103">Как назначить букву диска пользовательский значок и метку</span><span class="sxs-lookup"><span data-stu-id="24ccb-103">How to Assign a Custom Icon and Label to a Drive Letter</span></span>

<span data-ttu-id="24ccb-104">Укажите пользовательский значок и метку для диска.</span><span class="sxs-lookup"><span data-stu-id="24ccb-104">Specify a custom icon and label for a drive.</span></span>

## <a name="instructions"></a><span data-ttu-id="24ccb-105">Инструкции</span><span class="sxs-lookup"><span data-stu-id="24ccb-105">Instructions</span></span>

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a><span data-ttu-id="24ccb-106">Шаг 1. Замена стандартного значка диска на пользовательский значок в Windows 2000</span><span class="sxs-lookup"><span data-stu-id="24ccb-106">Step 1: Replacing the standard drive icon with a custom icon in Windows 2000</span></span>

<span data-ttu-id="24ccb-107">Чтобы заменить стандартный значок диска на пользовательский значок в Windows 2000, добавьте подраздел с именем для буквы диска в следующий раздел.</span><span class="sxs-lookup"><span data-stu-id="24ccb-107">To replace the standard drive icon with a custom icon in Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

<span data-ttu-id="24ccb-108">В следующем примере задается пользовательский значок и метка для диска E:.</span><span class="sxs-lookup"><span data-stu-id="24ccb-108">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="24ccb-109">Значок находится в файле C: \\ MyDir \\MyDrive.exe с нулевым индексом, начинающимся с нуля.</span><span class="sxs-lookup"><span data-stu-id="24ccb-109">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="24ccb-110">Для Windows 2000:</span><span class="sxs-lookup"><span data-stu-id="24ccb-110">For Windows 2000:</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a><span data-ttu-id="24ccb-111">Шаг 2. Замена стандартного значка диска на пользовательский значок во всех остальных версиях Windows</span><span class="sxs-lookup"><span data-stu-id="24ccb-111">Step 2: Replacing the standard drive icon with a custom icon in all other versions of Windows</span></span>

<span data-ttu-id="24ccb-112">Чтобы заменить стандартный значок диска на пользовательский значок во всех версиях Windows, отличных от Windows 2000, добавьте подраздел с именем для буквы диска в следующий раздел.</span><span class="sxs-lookup"><span data-stu-id="24ccb-112">To replace the standard drive icon with a custom icon in all versions of Windows other than Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

<span data-ttu-id="24ccb-113">В следующем примере задается пользовательский значок и метка для диска E:.</span><span class="sxs-lookup"><span data-stu-id="24ccb-113">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="24ccb-114">Значок находится в файле C: \\ MyDir \\MyDrive.exe с нулевым индексом, начинающимся с нуля.</span><span class="sxs-lookup"><span data-stu-id="24ccb-114">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="24ccb-115">Для всех остальных версий Windows:</span><span class="sxs-lookup"><span data-stu-id="24ccb-115">For all other versions of Windows:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a><span data-ttu-id="24ccb-116">Шаг 3. вызов события Шупдатеимаже</span><span class="sxs-lookup"><span data-stu-id="24ccb-116">Step 3: Calling the SHUpdateImage Event</span></span>

<span data-ttu-id="24ccb-117">Во всех версиях Windows при изменении типа файла или значка диска необходимо также вызвать Шупдатеимаже, чтобы уведомить оболочку о необходимости обновления значков, отображаемых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="24ccb-117">In all versions of Windows, if you change a file type or drive icon you must also call SHUpdateImage to notify the Shell to update any icons that are currently displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="24ccb-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="24ccb-118">Remarks</span></span>

<span data-ttu-id="24ccb-119">За буквой диска не следует ставить двоеточие (:).</span><span class="sxs-lookup"><span data-stu-id="24ccb-119">The drive letter should not be followed by a colon (:).</span></span> <span data-ttu-id="24ccb-120">Добавьте подраздел **дефаултикон** в подраздел букв диска и задайте в качестве значения по умолчанию строку, содержащую расположение значка.</span><span class="sxs-lookup"><span data-stu-id="24ccb-120">Add a **DefaultIcon** subkey to the drive letter subkey and set its default value to a string that contains the location of the icon.</span></span> <span data-ttu-id="24ccb-121">Первая часть строки содержит полный путь к файлу значка.</span><span class="sxs-lookup"><span data-stu-id="24ccb-121">The first part of the string contains the fully-qualified path of the icon's file.</span></span> <span data-ttu-id="24ccb-122">Если в файле содержится более одного значка, за ним следует запятая, а затем — Отсчитываемый от нуля индекс значка.</span><span class="sxs-lookup"><span data-stu-id="24ccb-122">If there is more than one icon in the file, the path is followed by a comma, and then by the zero-based index of the icon.</span></span>

 

 



