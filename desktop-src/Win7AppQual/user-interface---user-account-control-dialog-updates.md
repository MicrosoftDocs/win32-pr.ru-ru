---
description: Пользовательский интерфейс — обновления диалогового окна управления учетными записями пользователей
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Пользовательский интерфейс — обновления диалогового окна управления учетными записями пользователей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cd6cc6709283c7bd9cba3e26bd2df29bb02ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094422"
---
# <a name="user-interface---user-account-control-dialog-updates"></a><span data-ttu-id="9f36a-103">Пользовательский интерфейс — обновления диалогового окна управления учетными записями пользователей</span><span class="sxs-lookup"><span data-stu-id="9f36a-103">User Interface - User Account Control Dialog Updates</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="9f36a-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="9f36a-104">Affected Platforms</span></span>

<span data-ttu-id="9f36a-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="9f36a-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="9f36a-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f36a-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="9f36a-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="9f36a-107">Feature Impact</span></span>

<span data-ttu-id="9f36a-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="9f36a-108">**Severity** - Low</span></span>  
<span data-ttu-id="9f36a-109">**Частота** — средний</span><span class="sxs-lookup"><span data-stu-id="9f36a-109">**Frequency** - Medium</span></span>  











## <a name="description"></a><span data-ttu-id="9f36a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9f36a-110">Description</span></span>

<span data-ttu-id="9f36a-111">В Windows 7 выбраны стандартизированные возможности диалогового окна UAC.</span><span class="sxs-lookup"><span data-stu-id="9f36a-111">In Windows 7, we have standardized the UAC dialog box choices.</span></span> <span data-ttu-id="9f36a-112">Ранее пользователям пришлось выбирать из нескольких вариантов, например "продолжить", "Отмена" и т. д.</span><span class="sxs-lookup"><span data-stu-id="9f36a-112">Previously, users had to select from multiple options, for example, "Continue," "Cancel," and so on.</span></span> <span data-ttu-id="9f36a-113">Теперь все диалоговые окна предоставляют пользователям простые «Yes» и «No».</span><span class="sxs-lookup"><span data-stu-id="9f36a-113">Now all dialog boxes give users a simple "Yes" or "No."</span></span> <span data-ttu-id="9f36a-114">Теперь в макете диалогового окна также ясно отображается имя программы, издатель и источник.</span><span class="sxs-lookup"><span data-stu-id="9f36a-114">The dialog layout now also clearly shows the program name, publisher, and origin.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="9f36a-115">Использование возможностей функций</span><span class="sxs-lookup"><span data-stu-id="9f36a-115">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="9f36a-116">Требования к разработке приложений в Windows 7 для обеспечения совместимости UAC аналогичны требованиям Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9f36a-116">The application development requirements in Windows 7 for UAC compatibility are the same as in Windows Vista.</span></span> <span data-ttu-id="9f36a-117">Приложения, совместимые с Windows Vista, будут взаимодействовать с UAC в Windows 7 без каких-либо изменений.</span><span class="sxs-lookup"><span data-stu-id="9f36a-117">Windows Vista-compatible applications will interact with UAC in Windows 7 without any modifications.</span></span> <span data-ttu-id="9f36a-118">Сведения о том, как обеспечить правильную работу приложений Windows XP в Windows 7, см. в разделе Управление учетными записями пользователей в *Cookbook совместимости приложений Windows Vista* .</span><span class="sxs-lookup"><span data-stu-id="9f36a-118">See the User Account Control topics in the *Windows Vista Application Compatibility Cookbook* for information about how to make Windows XP applications work correctly on Windows 7.</span></span> <span data-ttu-id="9f36a-119">Хотя улучшения UAC для Windows 7 влияют на взаимодействие с пользователем, они не повлияют на интерфейс приложения.</span><span class="sxs-lookup"><span data-stu-id="9f36a-119">While the UAC improvements for Windows 7 will impact the user's experience, they will not impact the application interface.</span></span> <span data-ttu-id="9f36a-120">Однако при наличии содержимого справки, связанного с диалоговыми окнами UAC, может потребоваться обновить снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="9f36a-120">However, if there is any help content linked to the UAC dialogs, you may need to update the screenshots.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="9f36a-121">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="9f36a-121">Links to Other Resources</span></span>

-   <span data-ttu-id="9f36a-122">[Cookbook совместимости приложений Windows Vista](/previous-versions/bb757005(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9f36a-122">[Windows Vista Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10))</span></span>
-   [<span data-ttu-id="9f36a-123">Загрузка набора средств для обеспечения совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="9f36a-123">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="9f36a-124">[Анализатор Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="9f36a-124">[Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span></span>

> [!Note]  
> <span data-ttu-id="9f36a-125">Эти ресурсы могут быть недоступны в некоторых языках и странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="9f36a-125">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
