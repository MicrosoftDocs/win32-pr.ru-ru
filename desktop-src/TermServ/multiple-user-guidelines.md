---
title: Рекомендации для нескольких пользователей
description: Рекомендации по разработке приложений для нескольких пользователей в среде службы удаленных рабочих столов.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681524"
---
# <a name="multiple-user-guidelines"></a><span data-ttu-id="7909e-103">Рекомендации для нескольких пользователей</span><span class="sxs-lookup"><span data-stu-id="7909e-103">Multiple-user guidelines</span></span>

<span data-ttu-id="7909e-104">В следующих разделах приводятся рекомендации по разработке приложений для нескольких пользователей в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7909e-104">The following sections provide guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7909e-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="7909e-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="7909e-106">Настройка приложения</span><span class="sxs-lookup"><span data-stu-id="7909e-106">Application setup</span></span>](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="7909e-107">Установка приложения для одного пользователя может привести к возникновению проблем в многопользовательской службы удаленных рабочих столов среде.</span><span class="sxs-lookup"><span data-stu-id="7909e-107">Installing an application for a single user can create problems in a multiuser Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="7909e-108">Хранение сведений, относящихся к пользователю</span><span class="sxs-lookup"><span data-stu-id="7909e-108">Storing user-specific information</span></span>](storing-user-specific-information.md)
</dt> <dd>

<span data-ttu-id="7909e-109">Приложения должны хранить данные пользователя в определенных пользователем расположениях отдельно от глобальной информации, которая относится ко всем пользователям.</span><span class="sxs-lookup"><span data-stu-id="7909e-109">Applications should store user-specific information in user-specific locations, separately from global information that applies to all users.</span></span>

</dd> <dt>

[<span data-ttu-id="7909e-110">Пространства имен объектов ядра</span><span class="sxs-lookup"><span data-stu-id="7909e-110">Kernel object namespaces</span></span>](kernel-object-namespaces.md)
</dt> <dd>

<span data-ttu-id="7909e-111">Службы удаленных рабочих столов использует несколько пространств имен для объектов ядра; глобальное пространство имен используется главным образом службами в клиентских и серверных приложениях.</span><span class="sxs-lookup"><span data-stu-id="7909e-111">Remote Desktop Services uses multiple namespaces for kernel objects; a global namespace is used primarily by services in client/server applications.</span></span>

</dd> <dt>

[<span data-ttu-id="7909e-112">IP-адреса и имена компьютеров</span><span class="sxs-lookup"><span data-stu-id="7909e-112">IP addresses and computer names</span></span>](ip-addresses-and-computer-names.md)
</dt> <dd>

<span data-ttu-id="7909e-113">Небезопасно предполагать, что имя компьютера или IP-адрес , назначенные компьютеру, связаны с одним пользователем, так как на сервере узла сеансов удаленных рабочих столов могут одновременно находиться несколько пользователей.</span><span class="sxs-lookup"><span data-stu-id="7909e-113">It is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user because multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> </dl>

<span data-ttu-id="7909e-114">Как всегда, следует блокировать файлы и базы данных во время внесения изменений во избежание случайной потери данных.</span><span class="sxs-lookup"><span data-stu-id="7909e-114">As always, lock files and databases while making changes to prevent inadvertent loss of data.</span></span>

<span data-ttu-id="7909e-115">Приложение не должно блокировать файлы приложения времени выполнения, которые не являются файлами отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="7909e-115">Your application must not lock any run-time application files that are not per-user files.</span></span> <span data-ttu-id="7909e-116">Заблокированные файлы времени выполнения могут удерживать несколько экземпляров приложения или процессы в приложении, такие как мастера, от выполнения.</span><span class="sxs-lookup"><span data-stu-id="7909e-116">Locked run-time files can keep multiple instances of the application, or processes under the application such as wizards, from running.</span></span> <span data-ttu-id="7909e-117">Хорошим способом проверки файлов, которые являются файлами приложения во время выполнения, является запись файлов, устанавливаемых программой установки приложения.</span><span class="sxs-lookup"><span data-stu-id="7909e-117">A good way to test which files are run-time application files is to track which files are installed by the application setup.</span></span> <span data-ttu-id="7909e-118">Файлы отдельных пользователей редко устанавливаются программой установки; Поэтому большинство файлов, устанавливаемых программой установки, представляют собой файлы приложения времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="7909e-118">Per-user files are rarely installed by setup; therefore, most files installed by setup are run-time application files.</span></span>

 

 




