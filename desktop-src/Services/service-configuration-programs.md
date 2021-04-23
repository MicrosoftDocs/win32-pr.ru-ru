---
description: Программисты и системные администраторы используют программы настройки служб для изменения или запроса базы данных установленных служб.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Программы настройки служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144623"
---
# <a name="service-configuration-programs"></a><span data-ttu-id="b5d7b-103">Программы настройки служб</span><span class="sxs-lookup"><span data-stu-id="b5d7b-103">Service Configuration Programs</span></span>

<span data-ttu-id="b5d7b-104">Программисты и системные администраторы используют программы настройки служб для изменения или запроса базы данных установленных служб.</span><span class="sxs-lookup"><span data-stu-id="b5d7b-104">Programmers and system administrators use service configuration programs to modify or query the database of installed services.</span></span> <span data-ttu-id="b5d7b-105">Доступ к базе данных также можно получить с помощью функций реестра.</span><span class="sxs-lookup"><span data-stu-id="b5d7b-105">The database can also be accessed by using the registry functions.</span></span> <span data-ttu-id="b5d7b-106">Однако следует использовать только функции конфигурации SCM, которые гарантируют правильную установку и настройку службы.</span><span class="sxs-lookup"><span data-stu-id="b5d7b-106">However, you should only use the SCM configuration functions, which ensure that the service is properly installed and configured.</span></span>

<span data-ttu-id="b5d7b-107">Функции конфигурации SCM должны быть либо обработчиком объекта SCManager, либо маркером для объекта службы.</span><span class="sxs-lookup"><span data-stu-id="b5d7b-107">The SCM configuration functions require either a handle to an SCManager object or a handle to a service object.</span></span> <span data-ttu-id="b5d7b-108">Для получения этих дескрипторов программа настройки службы должна:</span><span class="sxs-lookup"><span data-stu-id="b5d7b-108">To obtain these handles, the service configuration program must:</span></span>

1.  <span data-ttu-id="b5d7b-109">Используйте функцию [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) для получения маркера базы данных SCM на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="b5d7b-109">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="b5d7b-110">Используйте функцию [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) или [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) для получения маркера объекта службы.</span><span class="sxs-lookup"><span data-stu-id="b5d7b-110">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="b5d7b-111">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="b5d7b-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b5d7b-112">Установка, удаление и перечисление служб</span><span class="sxs-lookup"><span data-stu-id="b5d7b-112">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
-   [<span data-ttu-id="b5d7b-113">Конфигурация службы</span><span class="sxs-lookup"><span data-stu-id="b5d7b-113">Service Configuration</span></span>](service-configuration.md)
-   [<span data-ttu-id="b5d7b-114">Настройка службы с помощью SC</span><span class="sxs-lookup"><span data-stu-id="b5d7b-114">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)

 

 



