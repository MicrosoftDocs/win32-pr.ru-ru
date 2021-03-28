---
description: Для типа файла необходимо назначить пользовательский значок, чтобы предоставить визуальное представление пользователю этого типа файла или приложению, с которым связан этот тип файла.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Назначение пользовательского значка типу файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985469"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a><span data-ttu-id="0f92a-103">Назначение пользовательского значка типу файла</span><span class="sxs-lookup"><span data-stu-id="0f92a-103">How to Assign a Custom Icon to a File Type</span></span>

<span data-ttu-id="0f92a-104">Если тип файла не назначен пользовательскому значку по умолчанию, Рабочий стол и проводник Windows отображают все файлы этого типа со стандартным значком по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f92a-104">When no custom default icon is assigned to a file type, the desktop and Windows Explorer display all files of that type with a generic default icon.</span></span> <span data-ttu-id="0f92a-105">Например, на следующем снимке экрана показан этот значок по умолчанию, используемый с файлом MyDocs4. МИП.</span><span class="sxs-lookup"><span data-stu-id="0f92a-105">For example, the following screen shot shows this default icon used with the MyDocs4.myp file.</span></span>

![снимок экрана со значком по умолчанию](images/icon.png)

<span data-ttu-id="0f92a-107">Хотя все файлы, отображаемые на этом снимке экрана, являются простыми текстовыми файлами, только MyDocs4. МИП отображает значок Windows по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f92a-107">While all the files displayed in this screen shot are simple text files, only MyDocs4.myp displays the Windows default icon.</span></span> <span data-ttu-id="0f92a-108">Это связано с тем, что расширение txt является зарегистрированным типом файла с пользовательским значком по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f92a-108">This is because the .txt extension is a registered file type that has a custom default icon.</span></span>

<span data-ttu-id="0f92a-109">На следующем снимке экрана показан пользовательский значок, назначенный типу файла МИП.</span><span class="sxs-lookup"><span data-stu-id="0f92a-109">The following screen shot shows a custom icon that has been assigned to the .myp file type.</span></span>

![снимок экрана: пользовательский значок для файлов. МИП](images/context4.png)

> [!Note]  
> <span data-ttu-id="0f92a-111">Значки также могут назначаться для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="0f92a-111">Icons can also be assigned on an application-specific basis.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="0f92a-112">Инструкции</span><span class="sxs-lookup"><span data-stu-id="0f92a-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="0f92a-113">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="0f92a-113">Step 1:</span></span>

<span data-ttu-id="0f92a-114">Создайте подраздел с именем **дефаултикон** в одном из следующих двух расположений:</span><span class="sxs-lookup"><span data-stu-id="0f92a-114">Create a subkey named **DefaultIcon** in one of the following two locations:</span></span>

-   <span data-ttu-id="0f92a-115">Для назначения типа файла, **\_ классы hKey \_ root** \\ *. extension*</span><span class="sxs-lookup"><span data-stu-id="0f92a-115">For a file-type assignment, **HKEY\_CLASSES\_ROOT**\\ *.extension*</span></span>
-   <span data-ttu-id="0f92a-116">Для назначения приложения **\_ \_ корневой** \\ *идентификатор ProgID* классов hKey</span><span class="sxs-lookup"><span data-stu-id="0f92a-116">For an application assignment, **HKEY\_CLASSES\_ROOT**\\*ProgID*</span></span>

### <a name="step-2"></a><span data-ttu-id="0f92a-117">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="0f92a-117">Step 2:</span></span>

<span data-ttu-id="0f92a-118">Назначьте подразделу **дефаултикон** значение по умолчанию с типом **reg \_ SZ** , которое указывает полный путь к файлу, содержащему значок.</span><span class="sxs-lookup"><span data-stu-id="0f92a-118">Assign the **DefaultIcon** subkey a default value of type **REG\_SZ** that specifies the fully qualified path for the file that contains the icon.</span></span>

### <a name="step-3"></a><span data-ttu-id="0f92a-119">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="0f92a-119">Step 3:</span></span>

<span data-ttu-id="0f92a-120">Вызовите функцию [**шчанженотифи**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) , чтобы уведомить оболочку о необходимости обновления своего кэша значков.</span><span class="sxs-lookup"><span data-stu-id="0f92a-120">Call the [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) function to notify the Shell to update its icon cache.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f92a-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="0f92a-121">Remarks</span></span>

<span data-ttu-id="0f92a-122">В следующем примере показано подробное представление записей реестра, необходимых для назначения значка типа файла.</span><span class="sxs-lookup"><span data-stu-id="0f92a-122">The following example shows a detailed view of the registry entries that are required for a file-type icon assignment.</span></span> <span data-ttu-id="0f92a-123">Расширение имени файла связано с приложением, но его назначение — это расширение имени файла, чтобы связанное приложение не определяло значок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f92a-123">The file name extension is associated with an application, but the icon assignment is to the file name extension itself so that the associated application does not dictate the default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="0f92a-124">В следующем примере показано подробное представление записей реестра, необходимых для назначения значка приложения.</span><span class="sxs-lookup"><span data-stu-id="0f92a-124">The following example shows a detailed view of the registry entries that are required for an application icon assignment.</span></span> <span data-ttu-id="0f92a-125">Расширение имени файла МИП сначала связано с приложением MyProgram. 1.</span><span class="sxs-lookup"><span data-stu-id="0f92a-125">The .myp file name extension is first associated with the MyProgram.1 application.</span></span> <span data-ttu-id="0f92a-126">Затем подразделу ProgID MyProgram. 1 назначается пользовательский значок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0f92a-126">The MyProgram.1 ProgID subkey is then assigned the custom default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="0f92a-127">Любой файл, содержащий значок, допустим, включая файлы ICO, exe и DLL.</span><span class="sxs-lookup"><span data-stu-id="0f92a-127">Any file that contains an icon is acceptable, including .ico, .exe, and .dll files.</span></span> <span data-ttu-id="0f92a-128">Если в файле содержится более одного значка, за ним следует запятая, а затем индекс значка.</span><span class="sxs-lookup"><span data-stu-id="0f92a-128">If there is more than one icon in the file, the path should be followed by a comma, and then the index of the icon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f92a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0f92a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f92a-130">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="0f92a-130">File Types</span></span>](fa-file-types.md)
</dt> </dl>

 

 



