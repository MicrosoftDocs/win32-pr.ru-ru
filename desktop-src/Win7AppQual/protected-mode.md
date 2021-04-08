---
description: .
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Защищенный режим
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace82e27bbec3bb97a9ffbd3b64c9c6cee9e11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910584"
---
# <a name="protected-mode"></a><span data-ttu-id="b8025-103">Защищенный режим</span><span class="sxs-lookup"><span data-stu-id="b8025-103">Protected Mode</span></span>

<span data-ttu-id="b8025-104">Большинство функций безопасности Windows Internet Explorer 8 доступны в Internet Explorer 8 для операционных систем Windows XP с пакетом обновления 2 (SP2) и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="b8025-104">Most Windows Internet Explorer 8 security features are available in Internet Explorer 8 for the Windows XP with Service Pack 2 (SP2) operating system and later versions.</span></span> <span data-ttu-id="b8025-105">Защищенный режим доступен только для Windows Vista или более поздних версий, поскольку он основан на следующих функциях безопасности, впервые реализованных в Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="b8025-105">Protected Mode is available only for Windows Vista or later versions because it is based on the following security features that are new to Windows Vista:</span></span>

-   <span data-ttu-id="b8025-106">[Управление учетными записями пользователей (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) упрощает запуск без прав администратора.</span><span class="sxs-lookup"><span data-stu-id="b8025-106">[User Account Control (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) makes it easy to run without administrator privileges.</span></span> <span data-ttu-id="b8025-107">Когда пользователи запускают программы с ограниченными правами пользователя, они более безопасны от атак, чем при запуске с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="b8025-107">When users run programs with limited user privileges, they are safer from an attack than when they run with administrator privileges.</span></span> <span data-ttu-id="b8025-108">Операционная система Windows может ограничить вредоносным кодом выполнение невредных действий.</span><span class="sxs-lookup"><span data-stu-id="b8025-108">The Windows operating system can restrict the malicious code from carrying out damaging actions.</span></span>
-   <span data-ttu-id="b8025-109">Механизм целостности запрещает доступ на запись к [защищаемым объектам](../secauthz/securable-objects.md) с помощью процессов более низкого уровня целостности, точно так же, как членство в группе учетных записей пользователя запрещает пользователям доступ к важным системным компонентам.</span><span class="sxs-lookup"><span data-stu-id="b8025-109">An integrity mechanism restricts write access to [securable objects](../secauthz/securable-objects.md) by lower-integrity processes, in the same way that user account group membership restricts the rights of users to access sensitive system components.</span></span>
-   <span data-ttu-id="b8025-110">[Изоляция прав пользовательского интерфейса (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) предотвращает отправку сообщений выбранных окон и других пользовательских API процессам, работающим с более высокой целостностью.</span><span class="sxs-lookup"><span data-stu-id="b8025-110">[User Interface Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) prevents processes from sending selected window messages and other USER APIs to processes that are running with higher integrity.</span></span>

<span data-ttu-id="b8025-111">Инфраструктура безопасности механизмов целостности Windows позволяет защищенному режиму предоставить Windows Internet Explorer привилегии, необходимые пользователям для просмотра веб-страниц, а также подлинность полномочий, необходимых пользователям для автоматической установки программ или изменения конфиденциальных системных данных.</span><span class="sxs-lookup"><span data-stu-id="b8025-111">The Windows Integrity Mechanism security infrastructure allows Protected Mode to provide Windows Internet Explorer with the privileges that users need to browse the web, while withholding privileges that users need to install programs silently or modify sensitive system data.</span></span>

<span data-ttu-id="b8025-112">Пользователи могут отключить эту функцию с помощью флажка, и администраторы могут отключить ее, используя групповая политика.</span><span class="sxs-lookup"><span data-stu-id="b8025-112">Users can disable this feature through a check box, and administrators can disable it by using Group Policy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8025-113">Эту функцию следует отключить только в качестве временной меры во время устранения неполадок, чтобы сравнить поведение приложения, когда эта функция включена.</span><span class="sxs-lookup"><span data-stu-id="b8025-113">You should disable the feature only as a temporary measure during troubleshooting to compare behavior of the application when the feature is enabled or not.</span></span> <span data-ttu-id="b8025-114">Мы рекомендуем постоянно включать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="b8025-114">We recommended that you keep this feature permanently enabled.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b8025-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b8025-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8025-116">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="b8025-116">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
