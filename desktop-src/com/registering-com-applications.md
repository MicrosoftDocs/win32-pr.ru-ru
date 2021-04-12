---
title: Регистрация приложений COM
description: Регистрация приложений COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331808"
---
# <a name="registering-com-applications"></a><span data-ttu-id="3d524-103">Регистрация приложений COM</span><span class="sxs-lookup"><span data-stu-id="3d524-103">Registering COM Applications</span></span>

<span data-ttu-id="3d524-104">Реестр — это системная база данных, содержащая сведения о конфигурации оборудования и программного обеспечения, а также о пользователях системы.</span><span class="sxs-lookup"><span data-stu-id="3d524-104">The registry is a system database that contains information about the configuration of system hardware and software as well as about users of the system.</span></span> <span data-ttu-id="3d524-105">Любая программа на базе Windows может добавлять сведения в реестр и считывать информацию из реестра.</span><span class="sxs-lookup"><span data-stu-id="3d524-105">Any Windows-based program can add information to the registry and read information back from the registry.</span></span> <span data-ttu-id="3d524-106">Клиенты выполняют поиск интересующих вас компонентов в реестре.</span><span class="sxs-lookup"><span data-stu-id="3d524-106">Clients search the registry for interesting components to use.</span></span>

<span data-ttu-id="3d524-107">Реестр хранит сведения обо всех COM-объектах, установленных в системе.</span><span class="sxs-lookup"><span data-stu-id="3d524-107">The registry maintains information about all the COM objects installed in the system.</span></span> <span data-ttu-id="3d524-108">Каждый раз, когда приложение создает экземпляр COM-компонента, он обращается к реестру для разрешения идентификатора CLSID или ProgID компонента в путь к файлу DLL или EXE сервера, в котором он содержится.</span><span class="sxs-lookup"><span data-stu-id="3d524-108">Whenever an application creates an instance of a COM component, the registry is consulted to resolve either the CLSID or ProgID of the component into the pathname of the server DLL or EXE that contains it.</span></span> <span data-ttu-id="3d524-109">После определения сервера компонента Windows либо загружает сервер в пространство процесса клиентского приложения (внутрипроцессный компонент), либо запускает сервер в собственном пространстве процесса (локальный и удаленный серверы).</span><span class="sxs-lookup"><span data-stu-id="3d524-109">After determining the component's server, Windows either loads the server into the process space of the client application (in-process components) or starts the server in its own process space (local and remote servers).</span></span> <span data-ttu-id="3d524-110">Сервер создает экземпляр компонента и возвращает клиенту ссылку на один из интерфейсов компонента.</span><span class="sxs-lookup"><span data-stu-id="3d524-110">The server creates an instance of the component and returns to the client a reference to one of the component's interfaces.</span></span>

<span data-ttu-id="3d524-111">Дополнительные сведения о реестре Windows см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="3d524-111">For more information about the Windows registry, see the following topics:</span></span>

-   [<span data-ttu-id="3d524-112">Иерархия реестра</span><span class="sxs-lookup"><span data-stu-id="3d524-112">Registry Hierarchy</span></span>](registry-hierarchy.md)
-   [<span data-ttu-id="3d524-113">Классы и серверы</span><span class="sxs-lookup"><span data-stu-id="3d524-113">Classes and Servers</span></span>](classes-and-servers.md)
-   [<span data-ttu-id="3d524-114">Классификация компонентов</span><span class="sxs-lookup"><span data-stu-id="3d524-114">Classifying Components</span></span>](classifying-components.md)
-   [<span data-ttu-id="3d524-115">Использование OleView</span><span class="sxs-lookup"><span data-stu-id="3d524-115">Using OleView</span></span>](using-oleview.md)
-   [<span data-ttu-id="3d524-116">Регистрация компонентов</span><span class="sxs-lookup"><span data-stu-id="3d524-116">Registering Components</span></span>](registering-components.md)
-   [<span data-ttu-id="3d524-117">Проверка регистрации</span><span class="sxs-lookup"><span data-stu-id="3d524-117">Checking Registration</span></span>](checking-registration.md)
-   [<span data-ttu-id="3d524-118">Неизвестные типы пользователей</span><span class="sxs-lookup"><span data-stu-id="3d524-118">Unknown User Types</span></span>](unknown-user-types.md)
-   [<span data-ttu-id="3d524-119">Разделы реестра COM</span><span class="sxs-lookup"><span data-stu-id="3d524-119">COM Registry Keys</span></span>](com-registry-keys.md)

 

 




