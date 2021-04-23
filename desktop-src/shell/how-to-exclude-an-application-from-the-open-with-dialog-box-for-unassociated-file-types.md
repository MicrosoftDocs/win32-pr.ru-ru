---
description: Исключение приложения из диалогового окна "Открыть с помощью" для несвязанного типа файла.
title: Исключение приложения из диалогового окна "Открыть с помощью" для несвязанных типов файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9443416e95fca112623d487bf58f4fce1d51d13d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557496"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a><span data-ttu-id="6820c-103">Исключение приложения из диалогового окна "Открыть с помощью" для несвязанных типов файлов</span><span class="sxs-lookup"><span data-stu-id="6820c-103">How to Exclude an Application from the Open With Dialog Box for Unassociated File Types</span></span>

<span data-ttu-id="6820c-104">Когда пользователь пытается открыть файл, который не является членом какого-либо зарегистрированного типа файла (то есть неизвестного типа файла), или когда пользователь выбирает пункт **Открыть с** помощью или **открыть с использованием > выбрать программу по умолчанию** в контекстном меню файла, оболочка представляет подменю или диалоговое окно, позволяющее пользователю указать программу, используемую для открытия файла.</span><span class="sxs-lookup"><span data-stu-id="6820c-104">When a user attempts to open a file that is not a member of any registered file type (that is, an unknown file type), or when a user selects **Open with** or **Open with -> Choose default program** from a file's shortcut menu, the Shell presents a submenu or dialog box that enables the user to specify the program used to open the file.</span></span>

<span data-ttu-id="6820c-105">По умолчанию любое приложение, зарегистрированное в качестве подраздела для **\_ \_ корневых приложений классов hKey**, \\  представлено в диалоговом окне **Открыть с помощью** .</span><span class="sxs-lookup"><span data-stu-id="6820c-105">By default, any application registered as a subkey of **HKEY\_CLASSES\_ROOT**\\**Applications** is presented in the **Open with** dialog box.</span></span> <span data-ttu-id="6820c-106">Эти приложения представлены в **открытом** виде независимо от того, зарегистрировано ли приложение для работы с типом файлов.</span><span class="sxs-lookup"><span data-stu-id="6820c-106">These applications are presented in **Open with** regardless of whether the application is registered to handle the file type.</span></span>

<span data-ttu-id="6820c-107">Чтобы приложение не отображалось в диалоговом окне **Открыть с помощью** , если приложение не должно быть открыто или не может использоваться для открытия определенных типов файлов, используйте один из двух методов, описанных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="6820c-107">To prevent an application from appearing in the **Open with** dialog box when the application should not or cannot be used to open certain file types, use one of the two techniques described in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="6820c-108">Инструкции</span><span class="sxs-lookup"><span data-stu-id="6820c-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="6820c-109">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="6820c-109">Step 1:</span></span>

<span data-ttu-id="6820c-110">Добавьте запись Нупенвис в подраздел приложения.</span><span class="sxs-lookup"><span data-stu-id="6820c-110">Add a NoOpenWith entry to the application's subkey.</span></span> <span data-ttu-id="6820c-111">Если приложение использует тип файла, Windows записывает эти сведения для создания списка **рекомендуемых программ** .</span><span class="sxs-lookup"><span data-stu-id="6820c-111">When an application uses a file type, Windows records that information to build the **Recommended Programs** list.</span></span> <span data-ttu-id="6820c-112">Этот список представлен в подменю **Открыть с помощью** , как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="6820c-112">This list is presented in the **Open with** submenu as shown in the following screen shot.</span></span>

![снимок экрана контекстного меню с отображаемым подменю «открыть с помощью»](images/file-assoc/openwithsubmenu.png)

<span data-ttu-id="6820c-114">Эти Рекомендуемые приложения также отображаются в разделе **Рекомендуемые программы** диалогового окна **Открыть с помощью** , как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="6820c-114">These recommended applications are also shown in the **Recommended Programs** portion of the **Open with** dialog box as shown in the following screen shot.</span></span>

![снимок экрана с диалоговым окном "Открыть с помощью" с рекомендуемыми программами](images/file-assoc/openwithdialog.png)

> [!Note]  
> <span data-ttu-id="6820c-116">Если приложение зарегистрировано в [опенвислист](fa-file-types.md) или опенвиспрогидс для типа файла, оно появится в списке **рекомендуемых программ** , даже если задана запись нупенвис.</span><span class="sxs-lookup"><span data-stu-id="6820c-116">If an application has registered itself in the [OpenWithList](fa-file-types.md) or OpenWithProgIDs for the file type, it will appear in the **Recommended Programs** list even if the NoOpenWith entry is set.</span></span> <span data-ttu-id="6820c-117">Кроме того, помните, что независимо от того, предлагается ли приложение в списке рекомендуемых программ, пользователь может вручную перейти к любому исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="6820c-117">Also, remember that regardless of whether an application is offered in a list of recommended programs, a user can manually browse to any executable file.</span></span>

 

<span data-ttu-id="6820c-118">Приложения могут отключить это отслеживание, указав значение Нупенвис в подразделе приложения.</span><span class="sxs-lookup"><span data-stu-id="6820c-118">Applications can disable this tracking by specifying a NoOpenWith value under the application's subkey.</span></span>

<span data-ttu-id="6820c-119">Запись Нупенвис представляет собой пустое значение **reg \_ SZ** , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="6820c-119">The NoOpenWith entry is an empty **REG\_SZ** value as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

<span data-ttu-id="6820c-120">Настройка записи Нупенвис также включает следующие эффекты:</span><span class="sxs-lookup"><span data-stu-id="6820c-120">Setting the NoOpenWith entry also has these effects:</span></span>

-   <span data-ttu-id="6820c-121">Предотвращает закрепление файла в списке переходов приложения с помощью перетаскивания, если только приложение не зарегистрировано для работы с этим типом файлов.</span><span class="sxs-lookup"><span data-stu-id="6820c-121">Prevents pinning a file to the application's Jump List through drag-and-drop, unless the application is specifically registered to handle that file type.</span></span>
-   <span data-ttu-id="6820c-122">Запрещает диалоговое окно Common File и любой вызов функции [**шаддторецентдокс**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) для добавления любого файла в список переходов приложения, если только приложение не зарегистрировано для работы с этим типом файлов.</span><span class="sxs-lookup"><span data-stu-id="6820c-122">Prevents the common file dialog box and any call to the [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) function from adding any file to the application's Jump List, unless the application is specifically registered to handle that file type.</span></span>

### <a name="step-2"></a><span data-ttu-id="6820c-123">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="6820c-123">Step 2:</span></span>

<span data-ttu-id="6820c-124">Второй способ предотвратить появление приложения в диалоговом окне **Открыть с помощью** заключается в использовании подраздела **суппортедтипес** для явного перечисления расширений типов файлов, которые может открыть приложение.</span><span class="sxs-lookup"><span data-stu-id="6820c-124">The second way to prevent an application from appearing in the **Open with** dialog box is to use the **SupportedTypes** subkey to explicitly list the extensions of file types that the application can open.</span></span> <span data-ttu-id="6820c-125">Это предотвращает отображение приложения в диалоговом окне **Открыть с помощью** для типов файлов, которые не удается открыть.</span><span class="sxs-lookup"><span data-stu-id="6820c-125">This prevents the application from appearing in the **Open with** dialog box for file types that it cannot open.</span></span> <span data-ttu-id="6820c-126">Это также приводит к тому, что приложение отображается в списке **рекомендуемых программ** , как описано выше.</span><span class="sxs-lookup"><span data-stu-id="6820c-126">It also causes the application to appear in the **Recommended Programs** list as discussed previously.</span></span>

<span data-ttu-id="6820c-127">Этот метод особенно полезен, если приложение может сохранить файл в файле определенного типа, но не может открыть этот тип файла.</span><span class="sxs-lookup"><span data-stu-id="6820c-127">This method is particularly useful if an application can save a file as a certain file type but cannot open that file type.</span></span> <span data-ttu-id="6820c-128">Приложение также должно установить \_ флаг Фос донтаддторецент с помощью [**ифиледиалог:: сетоптионс**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) при вызове диалогового окна **сохранить** .</span><span class="sxs-lookup"><span data-stu-id="6820c-128">An application should also set the FOS\_DONTADDTORECENT flag through [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) when calling the **Save** dialog box.</span></span> <span data-ttu-id="6820c-129">Это предотвращает добавление элемента к **последним** или **частым** частям списка переходов.</span><span class="sxs-lookup"><span data-stu-id="6820c-129">This keeps the item from being added to the **Recent** or **Frequent** portions of a Jump List.</span></span> <span data-ttu-id="6820c-130">Он также блокирует отслеживание приложения в разделе [опенвислист](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="6820c-130">It also blocks the application from being tracked under [OpenWithList](fa-file-types.md).</span></span>

<span data-ttu-id="6820c-131">Каждое поддерживаемое расширение добавляется в качестве записи в подраздел **суппортедтипес** , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="6820c-131">Each supported extension is added as an entry under the **SupportedTypes** subkey as shown in the following example.</span></span> <span data-ttu-id="6820c-132">Записи имеют тип **reg \_ SZ** или **reg \_ null** без связанных значений.</span><span class="sxs-lookup"><span data-stu-id="6820c-132">The entries are of type **REG\_SZ** or **REG\_NULL**, with no associated values.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

<span data-ttu-id="6820c-133">Если указан подраздел **суппортедтипес** , то только файлы с этими расширениями могут закрепляться в списке переходов приложения или в списке **недавних** или **часто** используемых приложений.</span><span class="sxs-lookup"><span data-stu-id="6820c-133">If a **SupportedTypes** subkey is provided, only files with those extensions are eligible for pinning to the application's Jump List or for being tracked in an application's **Recent** or **Frequent** destinations list.</span></span>

<span data-ttu-id="6820c-134">Запись Нупенвис переопределяет подраздел **суппортедтипес** и скрывает приложение в диалоговом окне " **Открыть с помощью** ".</span><span class="sxs-lookup"><span data-stu-id="6820c-134">The NoOpenWith entry overrides the **SupportedTypes** subkey and hides the application in the **Open with** dialog box.</span></span>

 

 
