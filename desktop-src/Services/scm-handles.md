---
description: SCM поддерживает типы Handles, чтобы разрешить доступ к следующим объектам.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Дескрипторы SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664462"
---
# <a name="scm-handles"></a><span data-ttu-id="b1ab5-103">Дескрипторы SCM</span><span class="sxs-lookup"><span data-stu-id="b1ab5-103">SCM Handles</span></span>

<span data-ttu-id="b1ab5-104">SCM поддерживает типы Handles, чтобы разрешить доступ к следующим объектам.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-104">The SCM supports handle types to allow access to the following objects.</span></span>

-   <span data-ttu-id="b1ab5-105">База данных установленных служб.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-105">The database of installed services.</span></span>
-   <span data-ttu-id="b1ab5-106">Служба.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-106">A service.</span></span>
-   <span data-ttu-id="b1ab5-107">Блокировка базы данных.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-107">The database lock.</span></span>

<span data-ttu-id="b1ab5-108">Объект SCManager представляет базу данных установленных служб.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-108">An SCManager object represents the database of installed services.</span></span> <span data-ttu-id="b1ab5-109">Это объект контейнера, который содержит объекты службы.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-109">It is a container object that holds service objects.</span></span> <span data-ttu-id="b1ab5-110">Функция [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) возвращает маркер объекта SCManager на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-110">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function returns a handle to an SCManager object on a specified computer.</span></span> <span data-ttu-id="b1ab5-111">Этот маркер используется при установке, удалении, открытии и перечислении служб, а также при блокировке базы данных служб.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-111">This handle is used when installing, deleting, opening, and enumerating services and when locking the services database.</span></span>

<span data-ttu-id="b1ab5-112">Объект службы представляет установленную службу.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-112">A service object represents an installed service.</span></span> <span data-ttu-id="b1ab5-113">Функции [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) и [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) возвращают дескрипторы для установленных служб.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-113">The [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions return handles to installed services.</span></span>

<span data-ttu-id="b1ab5-114">Функции [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)и [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) могут запрашивать различные типы доступа к SCManager и объектам службы.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-114">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea), and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions can request different types of access to SCManager and service objects.</span></span> <span data-ttu-id="b1ab5-115">Запрошенный доступ предоставляется или отклоняется в зависимости от маркера доступа вызывающего процесса и дескриптора безопасности, связанного с объектом SCManager или Service.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-115">The requested access is granted or denied depending on the access token of the calling process and the security descriptor associated with the SCManager or service object.</span></span>

<span data-ttu-id="b1ab5-116">Функция [**клосесервицехандле**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) закрывает дескрипторы SCManager и объектов службы.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-116">The [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) function closes handles to SCManager and service objects.</span></span> <span data-ttu-id="b1ab5-117">Если эти дескрипторы больше не нужны, закройте их.</span><span class="sxs-lookup"><span data-stu-id="b1ab5-117">When you no longer need these handles, be sure to close them.</span></span>

 

 



