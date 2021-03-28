---
description: По умолчанию элементы панели управления Windows Vista не отображаются при работе Windows в защищенном режиме.
title: Доступ к панели управления в защищенном режиме
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984368"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a><span data-ttu-id="6d2b8-103">Доступ к панели управления в защищенном режиме</span><span class="sxs-lookup"><span data-stu-id="6d2b8-103">Accessing the Control Panel in Safe Mode</span></span>

<span data-ttu-id="6d2b8-104">По умолчанию элементы панели управления Windows Vista не отображаются при работе Windows в защищенном режиме.</span><span class="sxs-lookup"><span data-stu-id="6d2b8-104">By default, as of Windows Vista Control Panel items are not shown when Windows is run in safe mode.</span></span> <span data-ttu-id="6d2b8-105">Чтобы разрешить просмотр нового элемента панели управления в защищенном режиме, можно задать значения реестра, соответствующие типу элемента.</span><span class="sxs-lookup"><span data-stu-id="6d2b8-105">To allow a new Control Panel item to be viewed in safe mode, registry values appropriate to the item type can be set.</span></span> <span data-ttu-id="6d2b8-106">Значения интерпретируется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6d2b8-106">The values are interpreted as follows:</span></span>



| <span data-ttu-id="6d2b8-107">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2b8-107">Value</span></span> | <span data-ttu-id="6d2b8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2b8-108">Meaning</span></span>                                                            |
|-------|--------------------------------------------------------------------|
| <span data-ttu-id="6d2b8-109">1</span><span class="sxs-lookup"><span data-stu-id="6d2b8-109">1</span></span>     | <span data-ttu-id="6d2b8-110">Элемент должен отображаться только в режиме минимального безопасного режима.</span><span class="sxs-lookup"><span data-stu-id="6d2b8-110">The item should appear in minimal safe mode only.</span></span>                  |
| <span data-ttu-id="6d2b8-111">2</span><span class="sxs-lookup"><span data-stu-id="6d2b8-111">2</span></span>     | <span data-ttu-id="6d2b8-112">Элемент должен отображаться в защищенном режиме только при включенной сети.</span><span class="sxs-lookup"><span data-stu-id="6d2b8-112">The item should appear in safe mode only if networking is enabled.</span></span> |
| <span data-ttu-id="6d2b8-113">3</span><span class="sxs-lookup"><span data-stu-id="6d2b8-113">3</span></span>     | <span data-ttu-id="6d2b8-114">Элемент всегда должен отображаться в любом формате безопасного режима.</span><span class="sxs-lookup"><span data-stu-id="6d2b8-114">The item should always appear in any form of safe mode.</span></span>            |



 

<span data-ttu-id="6d2b8-115">В этом примере показаны записи, необходимые для элемента, реализованного в виде файла. cpl или. dll.</span><span class="sxs-lookup"><span data-stu-id="6d2b8-115">This example shows the entries required for an item implemented as a .cpl or .dll file.</span></span> <span data-ttu-id="6d2b8-116">Он указывает, что элемент должен отображаться в защищенном режиме с сетевыми подключениями.</span><span class="sxs-lookup"><span data-stu-id="6d2b8-116">It specifies that the item should appear in safe mode with networking.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

<span data-ttu-id="6d2b8-117">В этом примере показаны записи, необходимые для элемента, реализованного в виде EXE-файла.</span><span class="sxs-lookup"><span data-stu-id="6d2b8-117">This example shows the entries required for an item implemented as a .exe file.</span></span> <span data-ttu-id="6d2b8-118">Он указывает, что элемент должен отображаться в любой форме безопасного режима.</span><span class="sxs-lookup"><span data-stu-id="6d2b8-118">It specifies that the item should appear in any form of safe mode.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a><span data-ttu-id="6d2b8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="6d2b8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d2b8-120">Элементы панели управления</span><span class="sxs-lookup"><span data-stu-id="6d2b8-120">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="6d2b8-121">Руководство по работе пользователей</span><span class="sxs-lookup"><span data-stu-id="6d2b8-121">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="6d2b8-122">Регистрация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="6d2b8-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="6d2b8-123">Использование Кплапплет</span><span class="sxs-lookup"><span data-stu-id="6d2b8-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="6d2b8-124">Обработка сообщений в панели управления</span><span class="sxs-lookup"><span data-stu-id="6d2b8-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="6d2b8-125">Исполнение элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="6d2b8-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="6d2b8-126">Расширение элементов панели управления "система"</span><span class="sxs-lookup"><span data-stu-id="6d2b8-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="6d2b8-127">Назначение категорий панели управления</span><span class="sxs-lookup"><span data-stu-id="6d2b8-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="6d2b8-128">Создание ссылок на задачи с возможностью поиска для элемента панели управления</span><span class="sxs-lookup"><span data-stu-id="6d2b8-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> </dl>

 

 



