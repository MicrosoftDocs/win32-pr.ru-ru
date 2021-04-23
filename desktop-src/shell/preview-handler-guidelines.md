---
description: При предоставлении предварительного просмотра следует следовать приведенным ниже рекомендациям.
title: Рекомендации по обработчику предварительной версии
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e725d561056e78a88bd9eeabd00d90abda1f0343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910771"
---
# <a name="preview-handler-guidelines"></a><span data-ttu-id="a0039-103">Рекомендации по обработчику предварительной версии</span><span class="sxs-lookup"><span data-stu-id="a0039-103">Preview Handler Guidelines</span></span>

<span data-ttu-id="a0039-104">При предоставлении предварительного просмотра следует следовать приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="a0039-104">When you provide a preview, the following guidelines should be followed.</span></span>

-   <span data-ttu-id="a0039-105">Предварительный просмотр должен содержать минимальный пользовательский интерфейс — это просто Предварительная версия.</span><span class="sxs-lookup"><span data-stu-id="a0039-105">A preview should contain minimal UI—it is simply a preview.</span></span> <span data-ttu-id="a0039-106">Он должен отображать только содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="a0039-106">It should display only the file content.</span></span> <span data-ttu-id="a0039-107">Он не должен отображать диалоговые окна, экраны-заставки, панели инструментов и области задач.</span><span class="sxs-lookup"><span data-stu-id="a0039-107">It should not display dialogs, splash screens, toolbars, or task panes.</span></span> <span data-ttu-id="a0039-108">Область чтения обычно используется вместе с поиском для быстрого обнаружения файла.</span><span class="sxs-lookup"><span data-stu-id="a0039-108">The reading pane will commonly be used in conjunction with search to quickly identify a file.</span></span> <span data-ttu-id="a0039-109">Следует избегать все, что переводит область чтения или иным образом рассматривает содержимое файла или вызывает задержки на экране предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="a0039-109">Anything that clutters the reading pane or otherwise detracts from file content or causes delays in preview display should be avoided.</span></span>
-   <span data-ttu-id="a0039-110">Предварительный просмотр должен позволить пользователю перемещаться по документу.</span><span class="sxs-lookup"><span data-stu-id="a0039-110">The preview should allow the user to navigate in the document.</span></span> <span data-ttu-id="a0039-111">Пользователь также должен иметь возможность выбирать и копировать текст.</span><span class="sxs-lookup"><span data-stu-id="a0039-111">The user should also be able to select and copy text.</span></span>
-   <span data-ttu-id="a0039-112">Предварительный просмотр не должен быть ресурсоемким, должен потреблять минимальный объем ресурсов и иметь быстрое время запуска.</span><span class="sxs-lookup"><span data-stu-id="a0039-112">The preview should not be memory-intensive, should consume minimal resources, and should have a fast startup time.</span></span>
-   <span data-ttu-id="a0039-113">Все скрипты и макросы в файле, для которых выполняется предварительный просмотр, должны быть заблокированы в целях обеспечения безопасности и конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="a0039-113">All script and macros in the file being previewed should be blocked from running for security and privacy purposes.</span></span>
-   <span data-ttu-id="a0039-114">Предварительная версия должна поддерживать сочетания клавиш для навигации и выбора в соответствии с поддерживаемыми приложениями.</span><span class="sxs-lookup"><span data-stu-id="a0039-114">The preview should support keyboard accelerators for navigation and selection as supported by the application.</span></span> <span data-ttu-id="a0039-115">Он также должен отображать контекстное меню при щелчке правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="a0039-115">It should also display a context menu when right-clicked.</span></span>
-   <span data-ttu-id="a0039-116">Если файл отображается в режиме предварительного просмотра, предварительный просмотр не должен блокировать сам файл.</span><span class="sxs-lookup"><span data-stu-id="a0039-116">When a file is displayed as a preview, the preview should not lock the file itself.</span></span> <span data-ttu-id="a0039-117">Файл можно просмотреть и открыть в связанном с ним приложении одновременно.</span><span class="sxs-lookup"><span data-stu-id="a0039-117">A file can be previewed and opened in its associated application at the same time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0039-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a0039-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0039-119">Обработчик предварительной версии и узел предварительной версии оболочки</span><span class="sxs-lookup"><span data-stu-id="a0039-119">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="a0039-120">Создание обработчиков предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="a0039-120">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> </dl>

 

 



