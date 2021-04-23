---
title: Интерфейсы ADSI
description: В этом разделе описываются категории, используемые для интерфейсов ADSI.
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- Интерфейсы ADSI ADSI
- Интерфейс ADSI ADSI, Справочник, интерфейсы
- интерфейсы ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2930292defa99301fb74f37c933a9af24b73f1fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410613"
---
# <a name="adsi-interfaces"></a><span data-ttu-id="c5132-106">Интерфейсы ADSI</span><span class="sxs-lookup"><span data-stu-id="c5132-106">ADSI Interfaces</span></span>

<span data-ttu-id="c5132-107">Интерфейсы служб Active Directory (ADSI) поддерживают широкий набор интерфейсов, которые можно классифицировать в соответствии со следующими категориями.</span><span class="sxs-lookup"><span data-stu-id="c5132-107">Active Directory Service Interfaces (ADSI) supports a rich set of interfaces that can be classified according to the following categories:</span></span>

-   <span data-ttu-id="c5132-108">[Ядро](core-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c5132-108">[Core](core-interfaces.md).</span></span> <span data-ttu-id="c5132-109">Эти интерфейсы предоставляют основные функции управления объектами ADSI.</span><span class="sxs-lookup"><span data-stu-id="c5132-109">These interfaces provide the basic object management functions of ADSI objects.</span></span> <span data-ttu-id="c5132-110">К основным функциям относятся предоставление точки входа в хранилище каталога, Загрузка свойств в кэш свойств и фиксация изменений в базовом каталоге.</span><span class="sxs-lookup"><span data-stu-id="c5132-110">The core functions include providing an entry point into a directory store, loading properties into the property cache, and committing changes to the underlying directory.</span></span>
-   <span data-ttu-id="c5132-111">[Схема](schema-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c5132-111">[Schema](schema-interfaces.md).</span></span> <span data-ttu-id="c5132-112">Эти интерфейсы предоставляют методы для управления и расширения схемы каталога.</span><span class="sxs-lookup"><span data-stu-id="c5132-112">These interfaces provide methods for managing and extending the directory schema.</span></span>
-   <span data-ttu-id="c5132-113">[Кэш свойств](property-cache-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c5132-113">[Property Cache](property-cache-interfaces.md).</span></span> <span data-ttu-id="c5132-114">Эти интерфейсы определяют методы для управления свойствами в кэше свойств.</span><span class="sxs-lookup"><span data-stu-id="c5132-114">These interfaces define methods for manipulating properties in the property cache.</span></span>
-   <span data-ttu-id="c5132-115">[Постоянный объект](persistent-object-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c5132-115">[Persistent Object](persistent-object-interfaces.md).</span></span> <span data-ttu-id="c5132-116">Эти интерфейсы управляют постоянными данными в пространстве имен базовой службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="c5132-116">These interfaces manipulate persistent data in the namespace of the underlying directory service.</span></span> <span data-ttu-id="c5132-117">Объекты ADSI реализуют эти типы интерфейсов для предоставления доступа к их постоянным данным, включая учетные записи пользователей, общие файловые ресурсы, организационные иерархии и списки заданий в очереди печати.</span><span class="sxs-lookup"><span data-stu-id="c5132-117">ADSI objects implement these types of interfaces to provide access to their persistent data, including user accounts, file shares, organizational hierarchies, and job listings in a print queue.</span></span>
-   <span data-ttu-id="c5132-118">[Динамический объект](dynamic-object-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c5132-118">[Dynamic Object](dynamic-object-interfaces.md).</span></span> <span data-ttu-id="c5132-119">Эти интерфейсы работают с динамическими данными в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="c5132-119">These interfaces work with dynamic data in a directory service.</span></span> <span data-ttu-id="c5132-120">Объекты каталога, не представленные в базовой службе каталогов, реализуют такие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="c5132-120">Directory objects not represented in the underlying directory service implement such interfaces.</span></span> <span data-ttu-id="c5132-121">Примеры динамических данных включают команды, выданные по сети.</span><span class="sxs-lookup"><span data-stu-id="c5132-121">Examples of dynamic data include commands issued over a network.</span></span>
-   <span data-ttu-id="c5132-122">[Безопасность](security-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c5132-122">[Security](security-interfaces.md).</span></span> <span data-ttu-id="c5132-123">Эти интерфейсы позволяют клиенту ADSI устанавливать свои учетные данные на сервер и использовать функции безопасности, поддерживаемые службой каталогов, такие как список управления доступом или дескрипторы безопасности.</span><span class="sxs-lookup"><span data-stu-id="c5132-123">These interfaces enable an ADSI client to establish its credentials to a server and use security features that the directory service supports, such as the access control list or security descriptors.</span></span>
-   <span data-ttu-id="c5132-124">[Не Автоматизация](non-automation-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c5132-124">[Non-Automation](non-automation-interfaces.md).</span></span> <span data-ttu-id="c5132-125">Эти интерфейсы позволяют клиентам без автоматизации (например, приложениям C/C++) доступ к объектам каталога с низкими издержками, предоставляя доступ vtable к методам для управления и поиска объектов службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="c5132-125">These interfaces allow non-Automation clients (for example, C/C++ applications) low-overhead access to directory objects by providing Vtable access to methods for managing and searching directory service objects.</span></span>
-   <span data-ttu-id="c5132-126">[Расширение](extension-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c5132-126">[Extension](extension-interfaces.md).</span></span> <span data-ttu-id="c5132-127">Эти интерфейсы позволяют клиентам ADSI расширять возможности существующих классов ADSI для предоставления настраиваемых решений службам каталогов.</span><span class="sxs-lookup"><span data-stu-id="c5132-127">These interfaces allow ADSI clients to extend the features of existing ADSI classes to offer customized solutions to directory services.</span></span>
-   <span data-ttu-id="c5132-128">[Служебная программа](utility-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c5132-128">[Utility](utility-interfaces.md).</span></span> <span data-ttu-id="c5132-129">Эти интерфейсы предоставляют расширенные вспомогательные функции для управления объектами ADSI.</span><span class="sxs-lookup"><span data-stu-id="c5132-129">These interfaces provide advanced helper functions for managing ADSI objects.</span></span>
-   <span data-ttu-id="c5132-130">[Тип данных](data-type-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c5132-130">[Data Type](data-type-interfaces.md).</span></span> <span data-ttu-id="c5132-131">Эти интерфейсы предоставляют методы для доступа к типам данных ADSI.</span><span class="sxs-lookup"><span data-stu-id="c5132-131">These interfaces provide methods to access ADSI data types.</span></span>

 

 




