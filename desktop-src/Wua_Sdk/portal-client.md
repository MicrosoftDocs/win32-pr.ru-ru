---
description: API Центр обновления Windows Agent (WUA) — это набор COM-интерфейсов, которые позволяют системным администраторам и программистам получать доступ к Центр обновления Windows и Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: API агента Центр обновления Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808650"
---
# <a name="windows-update-agent-api"></a><span data-ttu-id="2a743-103">API агента Центр обновления Windows</span><span class="sxs-lookup"><span data-stu-id="2a743-103">Windows Update Agent API</span></span>

## <a name="purpose"></a><span data-ttu-id="2a743-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="2a743-104">Purpose</span></span>

<span data-ttu-id="2a743-105">API Центр обновления Windows Agent (WUA) — это набор COM-интерфейсов, которые позволяют системным администраторам и программистам получать доступ к Центр обновления Windows и [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a743-105">The Windows Update Agent (WUA) API is a set of COM interfaces that enable system administrators and programmers to access Windows Update and [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span></span> <span data-ttu-id="2a743-106">Сценарии и программы могут быть написаны для проверки того, какие обновления в настоящее время доступны для компьютера, а затем можно установить или удалить обновления.</span><span class="sxs-lookup"><span data-stu-id="2a743-106">Scripts and programs can be written to examine which updates are currently available for a computer, and then you can install or uninstall updates.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="2a743-107">Где применимо</span><span class="sxs-lookup"><span data-stu-id="2a743-107">Where applicable</span></span>

<span data-ttu-id="2a743-108">Системные администраторы могут использовать WUA для программного определения того, какие обновления следует применить к компьютеру, загружать эти обновления, а затем устанавливать их без вмешательства пользователя или без него.</span><span class="sxs-lookup"><span data-stu-id="2a743-108">System administrators can use WUA to programmatically determine which updates should be applied to a computer, download those updates, and then install them with little or no user intervention.</span></span>

<span data-ttu-id="2a743-109">Независимые поставщики программного обеспечения (ISV) и разработчики конечных пользователей могут интегрировать функции WUA в систему управления компьютерами или по для управления обновлениями, чтобы обеспечить удобную рабочую среду.</span><span class="sxs-lookup"><span data-stu-id="2a743-109">Independent software vendors (ISV) and end-user developers can integrate WUA features into computer management or update management software to provide a seamless operating environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2a743-110">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="2a743-110">Developer audience</span></span>

<span data-ttu-id="2a743-111">Вы можете писать приложения WUA на нескольких языках программирования.</span><span class="sxs-lookup"><span data-stu-id="2a743-111">You can write WUA applications in several programming languages.</span></span> <span data-ttu-id="2a743-112">WUA определяет интерфейсы и объекты, доступные из Visual Basic, Visual Basic Scripting Edition (VBScript), JScript и C и C++.</span><span class="sxs-lookup"><span data-stu-id="2a743-112">WUA defines interfaces and objects that are accessible from Visual Basic, Visual Basic Scripting Edition (VBScript), JScript, and from C and C++.</span></span> <span data-ttu-id="2a743-113">Знание программирования COM полезно для программиста WUA.</span><span class="sxs-lookup"><span data-stu-id="2a743-113">A familiarity with COM programming is useful to the WUA programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2a743-114">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="2a743-114">Run-time requirements</span></span>

<span data-ttu-id="2a743-115">WUA поддерживается начиная с Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2a743-115">WUA is supported starting with Windows XP.</span></span> <span data-ttu-id="2a743-116">WUA поддерживается на сервере, начиная с Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2a743-116">WUA is supported on the server starting with Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2a743-117">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="2a743-117">In this section</span></span>

-   [<span data-ttu-id="2a743-118">Использование API агента Центр обновления Windows</span><span class="sxs-lookup"><span data-stu-id="2a743-118">Using the Windows Update Agent API</span></span>](using-the-windows-update-agent-api.md)
-   [<span data-ttu-id="2a743-119">Справочник по API WUA</span><span class="sxs-lookup"><span data-stu-id="2a743-119">WUA API Reference</span></span>](windows-update-agent--wua--api-reference.md)

 

 
