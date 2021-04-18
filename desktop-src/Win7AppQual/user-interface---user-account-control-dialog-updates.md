---
description: .
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Пользовательский интерфейс — обновления диалогового окна управления учетными записями пользователей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5711f8bbed029102bea81e0f4cfcbd4649b5a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713205"
---
# <a name="user-interface---user-account-control-dialog-updates"></a><span data-ttu-id="e7078-103">Пользовательский интерфейс — обновления диалогового окна управления учетными записями пользователей</span><span class="sxs-lookup"><span data-stu-id="e7078-103">User Interface - User Account Control Dialog Updates</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e7078-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="e7078-104">Affected Platforms</span></span>

<span data-ttu-id="e7078-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7078-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="e7078-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7078-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="e7078-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="e7078-107">Feature Impact</span></span>

<span data-ttu-id="e7078-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="e7078-108">**Severity** - Low</span></span>  
<span data-ttu-id="e7078-109">**Частота** — средний</span><span class="sxs-lookup"><span data-stu-id="e7078-109">**Frequency** - Medium</span></span>  











## <a name="description"></a><span data-ttu-id="e7078-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e7078-110">Description</span></span>

<span data-ttu-id="e7078-111">В Windows 7 выбраны стандартизированные возможности диалогового окна UAC.</span><span class="sxs-lookup"><span data-stu-id="e7078-111">In Windows 7, we have standardized the UAC dialog box choices.</span></span> <span data-ttu-id="e7078-112">Ранее пользователям пришлось выбирать из нескольких вариантов, например "продолжить", "Отмена" и т. д.</span><span class="sxs-lookup"><span data-stu-id="e7078-112">Previously, users had to select from multiple options, for example, "Continue," "Cancel," and so on.</span></span> <span data-ttu-id="e7078-113">Теперь все диалоговые окна предоставляют пользователям простые «Yes» и «No».</span><span class="sxs-lookup"><span data-stu-id="e7078-113">Now all dialog boxes give users a simple "Yes" or "No."</span></span> <span data-ttu-id="e7078-114">Теперь в макете диалогового окна также ясно отображается имя программы, издатель и источник.</span><span class="sxs-lookup"><span data-stu-id="e7078-114">The dialog layout now also clearly shows the program name, publisher, and origin.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="e7078-115">Использование возможностей функций</span><span class="sxs-lookup"><span data-stu-id="e7078-115">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="e7078-116">Требования к разработке приложений в Windows 7 для обеспечения совместимости UAC аналогичны требованиям Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e7078-116">The application development requirements in Windows 7 for UAC compatibility are the same as in Windows Vista.</span></span> <span data-ttu-id="e7078-117">Приложения, совместимые с Windows Vista, будут взаимодействовать с UAC в Windows 7 без каких-либо изменений.</span><span class="sxs-lookup"><span data-stu-id="e7078-117">Windows Vista-compatible applications will interact with UAC in Windows 7 without any modifications.</span></span> <span data-ttu-id="e7078-118">Сведения о том, как обеспечить правильную работу приложений Windows XP в Windows 7, см. в разделе Управление учетными записями пользователей в *Cookbook совместимости приложений Windows Vista* .</span><span class="sxs-lookup"><span data-stu-id="e7078-118">See the User Account Control topics in the *Windows Vista Application Compatibility Cookbook* for information about how to make Windows XP applications work correctly on Windows 7.</span></span> <span data-ttu-id="e7078-119">Хотя улучшения UAC для Windows 7 влияют на взаимодействие с пользователем, они не повлияют на интерфейс приложения.</span><span class="sxs-lookup"><span data-stu-id="e7078-119">While the UAC improvements for Windows 7 will impact the user's experience, they will not impact the application interface.</span></span> <span data-ttu-id="e7078-120">Однако при наличии содержимого справки, связанного с диалоговыми окнами UAC, может потребоваться обновить снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="e7078-120">However, if there is any help content linked to the UAC dialogs, you may need to update the screenshots.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="e7078-121">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="e7078-121">Links to Other Resources</span></span>

-   <span data-ttu-id="e7078-122">[Cookbook совместимости приложений Windows Vista](/previous-versions/bb757005(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e7078-122">[Windows Vista Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10))</span></span>
-   [<span data-ttu-id="e7078-123">Загрузка набора средств для обеспечения совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="e7078-123">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="e7078-124">[Анализатор Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="e7078-124">[Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span></span>

> [!Note]  
> <span data-ttu-id="e7078-125">Эти ресурсы могут быть недоступны в некоторых языках и странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="e7078-125">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
