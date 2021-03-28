---
description: Расширение пространства имен можно использовать, чтобы пользователи могли просматривать содержимое файла, а не представлять его в виде папки. Расширения этой сортировки обычно используются для вывода содержимого элементов типа файла.
title: Отображение корневого представления файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ee16f3ce50cd79800dd98aa53256591d1f79d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909547"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a><span data-ttu-id="5a6ad-104">Отображение корневого представления файла</span><span class="sxs-lookup"><span data-stu-id="5a6ad-104">How to Display a Rooted View of a File</span></span>

<span data-ttu-id="5a6ad-105">Расширение пространства имен можно использовать, чтобы пользователи могли просматривать содержимое файла, а не представлять его в виде папки.</span><span class="sxs-lookup"><span data-stu-id="5a6ad-105">You can use a namespace extension to allow users to browse the contents of a file rather than have it presented as a folder.</span></span> <span data-ttu-id="5a6ad-106">Расширения этой сортировки обычно используются для вывода содержимого элементов [типа файла](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="5a6ad-106">Extensions of this sort are typically used to display the contents of the members of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="5a6ad-107">Например, элементы типа файла могут содержать несколько сжатых файлов или изображений, организованных в иерархии.</span><span class="sxs-lookup"><span data-stu-id="5a6ad-107">For instance, the members of a file type might contain multiple compressed files or images, organized in a hierarchy.</span></span> <span data-ttu-id="5a6ad-108">Вместо того чтобы создавать приложение, позволяющее пользователю просматривать содержимое такого файла, можно написать расширение пространства имен и позволить проводнику работать с экраном.</span><span class="sxs-lookup"><span data-stu-id="5a6ad-108">Rather than write an application to allow the user to view the contents of such a file, you can instead write a namespace extension and let Windows Explorer handle the display.</span></span>

<span data-ttu-id="5a6ad-109">Чтобы расширение отображало содержимое файла, необходимо использовать корневое представление.</span><span class="sxs-lookup"><span data-stu-id="5a6ad-109">You must use a rooted view in order to have an extension display the contents of a file.</span></span> <span data-ttu-id="5a6ad-110">Наиболее распространенным способом предоставления корневого представления членов типа файла является определение [команды контекстного меню](context.md) , запускающей экземпляр Explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="5a6ad-110">The most common way to provide a rooted view of the members of a file type is to define a [shortcut menu verb](context.md) that launches an instance of Explorer.exe.</span></span> <span data-ttu-id="5a6ad-111">Если сделать эту команду командой по умолчанию, при двойном щелчке также будет открыто корневое представление файла.</span><span class="sxs-lookup"><span data-stu-id="5a6ad-111">By making this verb the default verb, a double-click will also open a rooted view of the file.</span></span> <span data-ttu-id="5a6ad-112">Можно либо определить команду для всех элементов типа файлов, [изменив реестр](context.md), либо динамически определять глаголы по отдельности в файлах, реализовав [обработчик контекстного меню](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="5a6ad-112">You can either define a verb for all members of the file type by [modifying the registry](context.md), or dynamically define verbs on a file-by-file basis by implementing a [shortcut menu handler](context-menu-handlers.md).</span></span>

## <a name="instructions"></a><span data-ttu-id="5a6ad-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="5a6ad-113">Instructions</span></span>


<span data-ttu-id="5a6ad-114">В следующем примере показано, как использовать реестр для предоставления корневого представления элементов типа файла путем изменения реестра.</span><span class="sxs-lookup"><span data-stu-id="5a6ad-114">The following example illustrates how to use the registry to provide a rooted view of the members of a file type by modifying the registry.</span></span> <span data-ttu-id="5a6ad-115">Пример записи реестра является изменением одного из примеров в разделе [расширение контекстных меню](context.md).</span><span class="sxs-lookup"><span data-stu-id="5a6ad-115">The sample registry entry is a modification of one of the examples in [Extending Shortcut Menus](context.md).</span></span> <span data-ttu-id="5a6ad-116">Записи реестра определяют файлы с расширением МИП в виде файлов и используют команду **обзора** для запуска корневого представления членов этого типа.</span><span class="sxs-lookup"><span data-stu-id="5a6ad-116">The registry entries define files with an .myp file name extension as a file type, and use the **browse** verb to launch a rooted view of members of that type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = browse
         browse
            command
               (Default) = %SYSTEMROOT%\explorer.exe /e,/root,{Extension CLSID}, "%1"
```

<span data-ttu-id="5a6ad-117">Одну и ту же команду можно использовать для программного запуска корневого представления элемента типа файла путем вызова функции [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="5a6ad-117">You can use the same verb to programmatically launch a rooted view of a member of the file type by calling the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a6ad-118">См. также</span><span class="sxs-lookup"><span data-stu-id="5a6ad-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a6ad-119">Указание расположения расширения пространства имен</span><span class="sxs-lookup"><span data-stu-id="5a6ad-119">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="5a6ad-120">Открытие корневого представления точки соединения в реестре</span><span class="sxs-lookup"><span data-stu-id="5a6ad-120">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="5a6ad-121">Открытие корневого представления точки соединения через файл ярлыка</span><span class="sxs-lookup"><span data-stu-id="5a6ad-121">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="5a6ad-122">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="5a6ad-122">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



