---
description: В Windows Vista и Windows Server 2008 изменились расположения по умолчанию для данных и системных данных пользователя.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Точки соединения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692912"
---
# <a name="junction-points"></a><span data-ttu-id="d2d06-103">Точки соединения</span><span class="sxs-lookup"><span data-stu-id="d2d06-103">Junction Points</span></span>

<span data-ttu-id="d2d06-104">В Windows Vista и Windows Server 2008 изменились расположения по умолчанию для данных и системных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="d2d06-104">In Windows Vista and Windows Server 2008, the default locations for user data and system data have changed.</span></span> <span data-ttu-id="d2d06-105">Например, данные пользователя, которые ранее хранились в каталоге% SystemDrive% \\ Documents and Settings, теперь хранятся в каталоге% systemdrive% \\ пользователей.</span><span class="sxs-lookup"><span data-stu-id="d2d06-105">For example, user data that was previously stored in the %SystemDrive%\\Documents and Settings directory is now stored in the %SystemDrive%\\Users directory.</span></span> <span data-ttu-id="d2d06-106">В целях обратной совместимости старые расположения имеют точки соединения, указывающие на новые расположения.</span><span class="sxs-lookup"><span data-stu-id="d2d06-106">For backward compatibility, the old locations have junction points that point to the new locations.</span></span> <span data-ttu-id="d2d06-107">Например, C: \\ документы и параметры теперь являются точкой соединения, указывающей на C: \\ Users.</span><span class="sxs-lookup"><span data-stu-id="d2d06-107">For example, C:\\Documents and Settings is now a junction point that points to C:\\Users.</span></span> <span data-ttu-id="d2d06-108">Приложения резервного копирования должны поддерживать резервное копирование и восстановление точек соединения.</span><span class="sxs-lookup"><span data-stu-id="d2d06-108">Backup applications must be capable of backing up and restoring junction points.</span></span>

<span data-ttu-id="d2d06-109">Эти точки соединения можно определить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d2d06-109">These junction points can be identified as follows:</span></span>

-   <span data-ttu-id="d2d06-110">Для них \_ \_ заданы точка повторного анализа атрибутов файлов \_ , \_ атрибут файла \_ Hidden и \_ \_ атрибуты системного файла атрибута файла.</span><span class="sxs-lookup"><span data-stu-id="d2d06-110">They have the FILE\_ATTRIBUTE\_REPARSE\_POINT, FILE\_ATTRIBUTE\_HIDDEN, and FILE\_ATTRIBUTE\_SYSTEM file attributes set.</span></span>
-   <span data-ttu-id="d2d06-111">В них также установлены списки управления доступом (ACL), запрещающие доступ на чтение для всех.</span><span class="sxs-lookup"><span data-stu-id="d2d06-111">They also have their access control lists (ACLs) set to deny read access to everyone.</span></span>

<span data-ttu-id="d2d06-112">Приложения, вызывающие конкретный путь, могут пройти по этим точкам соединения, если у них есть необходимые разрешения.</span><span class="sxs-lookup"><span data-stu-id="d2d06-112">Applications that call out a specific path can traverse these junction points if they have the required permissions.</span></span> <span data-ttu-id="d2d06-113">Однако попытки перечисления содержимого точек соединения приведут к сбоям.</span><span class="sxs-lookup"><span data-stu-id="d2d06-113">However, attempts to enumerate the contents of the junction points will result in failures.</span></span> <span data-ttu-id="d2d06-114">Важно, чтобы приложения резервного копирования не проводили эти точки соединения или попытались создать резервную копию данных по двум причинам.</span><span class="sxs-lookup"><span data-stu-id="d2d06-114">It is important that backup applications do not traverse these junction points, or attempt to backup data under them, for two reasons:</span></span>

-   <span data-ttu-id="d2d06-115">Это может привести к тому, что приложение резервного копирования будет выполнять резервное копирование одних и тех же данных более одного раза.</span><span class="sxs-lookup"><span data-stu-id="d2d06-115">Doing so can cause the backup application to back up the same data more than once.</span></span>
-   <span data-ttu-id="d2d06-116">Он также может привести к циклам (циклические ссылки).</span><span class="sxs-lookup"><span data-stu-id="d2d06-116">It can also lead to cycles (circular references).</span></span>

## <a name="per-user-junctions-and-system-junctions"></a><span data-ttu-id="d2d06-117">Per-User соединений и соединений системы</span><span class="sxs-lookup"><span data-stu-id="d2d06-117">Per-User Junctions and System Junctions</span></span>

<span data-ttu-id="d2d06-118">Точки соединения, используемые для обеспечения виртуализации файлов и реестра в Windows Vista и Windows Server 2008, можно разделить на два класса: соединения отдельных пользователей и соединения системы.</span><span class="sxs-lookup"><span data-stu-id="d2d06-118">The junction points that are used to provide file and registry virtualization in Windows Vista and Windows Server 2008 can be divided into two classes: per-user junctions and system junctions.</span></span>

<span data-ttu-id="d2d06-119">Соединения для каждого пользователя создаются внутри каждого профиля отдельного пользователя для обеспечения обратной совместимости с пользовательскими приложениями.</span><span class="sxs-lookup"><span data-stu-id="d2d06-119">Per-user junctions are created inside each individual user's profile to provide backward compatibility for user applications.</span></span> <span data-ttu-id="d2d06-120">Точка соединения на диске C: \\ Users \\  \\ My Documents, указывающая на C: \\ Users \\ *usernames*, \\ является примером соединения для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="d2d06-120">The junction point at C:\\Users\\*username*\\My Documents that points to C:\\Users\\*username*\\Documents is an example of a per-user junction.</span></span> <span data-ttu-id="d2d06-121">Соединения "на пользователя" создаются службой профилей при создании профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="d2d06-121">Per-user junctions are created by the Profile service when the user's profile is created.</span></span>

<span data-ttu-id="d2d06-122">Другие соединения являются соединениями системы, которые не находятся в каталоге User \\ *username* .</span><span class="sxs-lookup"><span data-stu-id="d2d06-122">The other junctions are system junctions that do not reside under the Users\\*username* directory.</span></span> <span data-ttu-id="d2d06-123">Ниже приведены примеры соединений системы.</span><span class="sxs-lookup"><span data-stu-id="d2d06-123">Examples of system junctions include:</span></span>

-   <span data-ttu-id="d2d06-124">Документы и параметры</span><span class="sxs-lookup"><span data-stu-id="d2d06-124">Documents and Settings</span></span>
-   <span data-ttu-id="d2d06-125">Точки соединения в профилях "все пользователи", "Открытый" и "по умолчанию"</span><span class="sxs-lookup"><span data-stu-id="d2d06-125">Junctions within the All Users, Public, and Default User profiles</span></span>

<span data-ttu-id="d2d06-126">Соединения системы создаются userenv.dll при вызове с помощью окна приветствия Windows (также называемого встроенным компьютером или Мубе).</span><span class="sxs-lookup"><span data-stu-id="d2d06-126">System junctions are created by userenv.dll when it is invoked by Windows Welcome (also called the machine out-of-box-experience, or mOOBE).</span></span>

> [!Note]  
> <span data-ttu-id="d2d06-127">Если пользователь меняет язык системы на язык, отличный от английского, то точки соединения для пользователя и системы будут созданы с локализованными именами.</span><span class="sxs-lookup"><span data-stu-id="d2d06-127">If the user changes the system language to a language other than English, the per-user and system junction points will be created with localized names.</span></span>

 

 

 



