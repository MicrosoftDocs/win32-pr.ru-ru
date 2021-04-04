---
description: 'В файловой системе NTFS поддерживаются два типа ссылок: жесткие связи и соединения.'
ms.assetid: 548acfe5-c9e1-4227-ba20-674e071f121f
title: Связывание файлов и каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70bcb905b73f7635ba5bdc4afcc44280023c7a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999412"
---
# <a name="file-and-directory-linking"></a><span data-ttu-id="566a0-103">Связывание файлов и каталогов</span><span class="sxs-lookup"><span data-stu-id="566a0-103">File and Directory Linking</span></span>

<span data-ttu-id="566a0-104">Файловая система NTFS предоставляет возможность создания системного представления файла или каталога в расположении в структуре каталогов, отличной от объекта файла или каталога, с которым выполняется связь.</span><span class="sxs-lookup"><span data-stu-id="566a0-104">The NTFS file system provides the ability to create a system representation of a file or directory in a location in the directory structure that is different from the file or directory object that is being linked to.</span></span> <span data-ttu-id="566a0-105">Этот процесс называется компоновкой.</span><span class="sxs-lookup"><span data-stu-id="566a0-105">This process is called linking.</span></span> <span data-ttu-id="566a0-106">В файловой системе NTFS поддерживаются два типа ссылок: [жесткие связи и соединения](hard-links-and-junctions.md).</span><span class="sxs-lookup"><span data-stu-id="566a0-106">There are two types of links supported in the NTFS file system: [hard links and junctions](hard-links-and-junctions.md).</span></span>

<span data-ttu-id="566a0-107">Файловая система NTFS также предоставляет [службу отслеживания распределенных каналов](distributed-link-tracking-and-object-identifiers.md), которая автоматически отслеживает ссылки при их перемещении.</span><span class="sxs-lookup"><span data-stu-id="566a0-107">The NTFS file system also provides the [distributed link tracking service](distributed-link-tracking-and-object-identifiers.md), which automatically tracks links as they are moved.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="566a0-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="566a0-108">In this section</span></span>



| <span data-ttu-id="566a0-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="566a0-109">Topic</span></span>                                                                                                               | <span data-ttu-id="566a0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="566a0-110">Description</span></span>                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="566a0-111">Жесткие связи и соединения</span><span class="sxs-lookup"><span data-stu-id="566a0-111">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)<br/>                                                 | <span data-ttu-id="566a0-112">Описывает жесткие связи и соединения.</span><span class="sxs-lookup"><span data-stu-id="566a0-112">Describes hard links and junctions.</span></span><br/>                                                                          |
| [<span data-ttu-id="566a0-113">Отслеживание распределенных ссылок и идентификаторы объектов</span><span class="sxs-lookup"><span data-stu-id="566a0-113">Distributed Link Tracking and Object Identifiers</span></span>](distributed-link-tracking-and-object-identifiers.md)<br/> | <span data-ttu-id="566a0-114">**Служба отслеживания распределенных каналов** позволяет клиентским приложениям отслеживать перемещенные источники связей.</span><span class="sxs-lookup"><span data-stu-id="566a0-114">The **distributed link tracking service** enables client applications to track link sources that have moved.</span></span><br/> |



 

 

 




