---
description: Active Directory является службой каталогов для Windows и является основой распределенных сетей Windows.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Доступ к Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272233"
---
# <a name="accessing-active-directory"></a><span data-ttu-id="234c6-103">Доступ к Active Directory</span><span class="sxs-lookup"><span data-stu-id="234c6-103">Accessing Active Directory</span></span>

<span data-ttu-id="234c6-104">Active Directory является службой каталогов для Windows и является основой распределенных сетей Windows.</span><span class="sxs-lookup"><span data-stu-id="234c6-104">Active Directory is the directory service for Windows and is the foundation of Windows distributed networks.</span></span> <span data-ttu-id="234c6-105">Active Directory можно использовать для нахождение объектов в доменной сети компьютера, таких как пользователи, политики безопасности, принтеры, распределенные компоненты и другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="234c6-105">You can use Active Directory to locate objects in a computer network domain, such as users, security policies, printers, distributed components, and other resources.</span></span> <span data-ttu-id="234c6-106">Имя Active Directory ссылается как на службу каталогов, так и на сам каталог.</span><span class="sxs-lookup"><span data-stu-id="234c6-106">The name Active Directory refers both to the directory service and the directory itself.</span></span>

> [!Note]  
> <span data-ttu-id="234c6-107">Дополнительные сведения о поддержке и установке этого компонента в определенной операционной системе см. в статье [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="234c6-107">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="234c6-108">Windows делает Active Directory доступными через WMI, создавая набор ссылок на каждый класс и объект, содержащийся в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="234c6-108">Windows makes Active Directory accessible through WMI by creating a set of references to every class and object contained in Active Directory.</span></span> <span data-ttu-id="234c6-109">Доступ к поставщику служб каталогов через инструментарий WMI позволяет создавать приложения с поддержкой WMI, которые могут получать доступ к обширным сведениям, содержащимся в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="234c6-109">By accessing the Directory Services provider through WMI, you can create WMI-enabled applications that can access the wealth of information contained in Active Directory.</span></span>

<span data-ttu-id="234c6-110">С помощью этих интерфейсов можно:</span><span class="sxs-lookup"><span data-stu-id="234c6-110">With these interfaces, you can:</span></span>

-   <span data-ttu-id="234c6-111">Извлечение классов и экземпляров.</span><span class="sxs-lookup"><span data-stu-id="234c6-111">Retrieve classes and instances.</span></span>
-   <span data-ttu-id="234c6-112">Перечисление классов и экземпляров.</span><span class="sxs-lookup"><span data-stu-id="234c6-112">Enumerate classes and instances.</span></span>
-   <span data-ttu-id="234c6-113">Создайте новые экземпляры.</span><span class="sxs-lookup"><span data-stu-id="234c6-113">Create new instances.</span></span>
-   <span data-ttu-id="234c6-114">Изменение существующих экземпляров.</span><span class="sxs-lookup"><span data-stu-id="234c6-114">Modify existing instances.</span></span>
-   <span data-ttu-id="234c6-115">Удаление существующих экземпляров.</span><span class="sxs-lookup"><span data-stu-id="234c6-115">Delete existing instances.</span></span>
-   <span data-ttu-id="234c6-116">Active Directory запроса.</span><span class="sxs-lookup"><span data-stu-id="234c6-116">Query Active Directory.</span></span>

<span data-ttu-id="234c6-117">Следующие разделы помогут вам в использовании Active Directory с WMI:</span><span class="sxs-lookup"><span data-stu-id="234c6-117">The following topics can assist you in using Active Directory with WMI:</span></span>

-   [<span data-ttu-id="234c6-118">Использование правильного синтаксиса Active Directory</span><span class="sxs-lookup"><span data-stu-id="234c6-118">Using the Proper Active Directory Syntax</span></span>](using-the-proper-active-directory-syntax.md)
-   [<span data-ttu-id="234c6-119">Сопоставление Active Directory WMI</span><span class="sxs-lookup"><span data-stu-id="234c6-119">Mapping Active Directory to WMI</span></span>](mapping-active-directory-to-wmi.md)

 

 



