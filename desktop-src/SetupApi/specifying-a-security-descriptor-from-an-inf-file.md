---
description: Можно управлять способностью процесса получать доступ к защищаемым объектам или выполнять задачи системного администрирования.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Указание дескриптора безопасности из INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999508"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a><span data-ttu-id="f0743-103">Указание дескриптора безопасности из INF-файла</span><span class="sxs-lookup"><span data-stu-id="f0743-103">Specifying a Security Descriptor From an INF File</span></span>

<span data-ttu-id="f0743-104">Можно управлять способностью процесса получать доступ к защищаемым объектам или выполнять задачи системного администрирования.</span><span class="sxs-lookup"><span data-stu-id="f0743-104">You can control the ability of a process to access securable objects or to perform system administration tasks.</span></span> <span data-ttu-id="f0743-105">Защищаемый объект — это объект, который может иметь дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="f0743-105">A securable object is an object that can have a security descriptor.</span></span> <span data-ttu-id="f0743-106">Все именованные объекты являются защищаемыми.</span><span class="sxs-lookup"><span data-stu-id="f0743-106">All named objects are securable.</span></span> <span data-ttu-id="f0743-107">Некоторые неименованные объекты, такие как процессы и объекты потоков, могут также иметь дескрипторы безопасности.</span><span class="sxs-lookup"><span data-stu-id="f0743-107">Some unnamed objects, such as process and thread objects, can have security descriptors too.</span></span> <span data-ttu-id="f0743-108">Дополнительные сведения об управлении доступом к защищаемым объектам см. в разделе [Контроль доступа](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="f0743-108">For more information about controlling access to securable objects see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="f0743-109">[Дескрипторы безопасности](/windows/desktop/SecAuthZ/security-descriptors) содержат сведения о безопасности, связанные с защищаемыми объектами.</span><span class="sxs-lookup"><span data-stu-id="f0743-109">[Security descriptors](/windows/desktop/SecAuthZ/security-descriptors) contain the security information associated with securable objects.</span></span> <span data-ttu-id="f0743-110">Для большинства защищаемых объектов можно указать дескриптор безопасности объекта в вызове функции, который создает объект.</span><span class="sxs-lookup"><span data-stu-id="f0743-110">For most securable objects, you can specify an object's security descriptor in the function call that creates the object.</span></span> <span data-ttu-id="f0743-111">Например, можно указать дескриптор безопасности в функциях [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) и [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="f0743-111">For example, you can specify a security descriptor in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) functions.</span></span>

<span data-ttu-id="f0743-112">Чтобы задать дескриптор безопасности из INF-файла, добавьте раздел безопасности, разработанный для записи INF, сразу после раздела, который устанавливает файл, раздел реестра или компонент.</span><span class="sxs-lookup"><span data-stu-id="f0743-112">To set a security descriptor from an INF file, add an INF-writer authored Security section immediately following the section that installs the file, registry key, or component.</span></span> <span data-ttu-id="f0743-113">Раздел Security должен содержать одну строку со строковым дескриптором безопасности, написанную на нем, используя формат [строк дескриптора безопасности](/windows/desktop/SecAuthZ/security-descriptor-strings).</span><span class="sxs-lookup"><span data-stu-id="f0743-113">The Security section should contain one line with the string security descriptor written on it using the format for [Security Descriptor Strings](/windows/desktop/SecAuthZ/security-descriptor-strings).</span></span> <span data-ttu-id="f0743-114">Строка также должна быть заключена в кавычки (").</span><span class="sxs-lookup"><span data-stu-id="f0743-114">The line should also be enclosed by quotation marks (").</span></span>

<span data-ttu-id="f0743-115">Например, следующий фрагмент файла INF создает раздел реестра, доступ к которому имеют только администраторы и система.</span><span class="sxs-lookup"><span data-stu-id="f0743-115">For example, the following INF file snippet would create a registry key to which only administrators and the system have access.</span></span> <span data-ttu-id="f0743-116">Обратите внимание, что для этого примера требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="f0743-116">Note that this example requires administrative privileges.</span></span>

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

<span data-ttu-id="f0743-117">В этом случае смысл строки заключается в том, что администраторы имеют полный доступ, система имеет полный контроль, а доступ наследуется ко всем подразделам.</span><span class="sxs-lookup"><span data-stu-id="f0743-117">In this case, the meaning of the string is that administrators have full control, system has full control, and access is inheritable to all subkeys.</span></span> <span data-ttu-id="f0743-118">Дополнительные сведения см. в разделе [язык определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="f0743-118">For more information see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span>

 

 
