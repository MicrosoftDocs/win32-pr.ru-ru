---
description: Модули записи и запрашивающие объекты сохраняют сведения, необходимые для операции резервного копирования или восстановления в собственных документах метаданных.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: Метаданные VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e718d3fb0290f8610944180c079e4d615124eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692369"
---
# <a name="vss-metadata"></a><span data-ttu-id="9d10b-103">Метаданные VSS</span><span class="sxs-lookup"><span data-stu-id="9d10b-103">VSS Metadata</span></span>

<span data-ttu-id="9d10b-104">Модули записи и запрашивающие объекты сохраняют сведения, необходимые для операции резервного копирования или восстановления в собственных документах метаданных.</span><span class="sxs-lookup"><span data-stu-id="9d10b-104">Both writers and requesters maintain information necessary to a backup or restore operation in their own metadata documents.</span></span>

<span data-ttu-id="9d10b-105">Эти документы, [*документ метаданных модуля записи*](vssgloss-w.md) и [*документ с компонентами резервного копирования*](vssgloss-b.md), соответственно, используются в качестве базиса для модуля записи и взаимодействия с инициатором и координации во время действий резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="9d10b-105">These documents, the [*Writer Metadata Document*](vssgloss-w.md) and the [*Backup Components Document*](vssgloss-b.md), respectively, are used as the basis for writer and requester communication and coordination during backup and restore activities.</span></span>

<span data-ttu-id="9d10b-106">Метаданные представлены в формате XML с помощью собственной схемы.</span><span class="sxs-lookup"><span data-stu-id="9d10b-106">The metadata is represented in XML format using a proprietary schema.</span></span> <span data-ttu-id="9d10b-107">Метаданные можно копировать на диск, на ленту или на любое другое запоминающее устройство.</span><span class="sxs-lookup"><span data-stu-id="9d10b-107">Metadata can be copied to disk, tape, or any other mass storage device.</span></span> <span data-ttu-id="9d10b-108">Он всегда должен быть сохранен на носителе резервных копий во время операции резервного копирования и должен быть получен с этого носителя в ходе операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="9d10b-108">It should always be saved to the backup media during a backup operation, and will need to be retrieved from that media in the course of a restore operation.</span></span>

<span data-ttu-id="9d10b-109">**Внимание!** Конкретные сведения о формате и схеме предназначены только для системного использования.</span><span class="sxs-lookup"><span data-stu-id="9d10b-109">**Caution:** The specific details of the format and schema are for system use only.</span></span> <span data-ttu-id="9d10b-110">Разработчики не должны пытаться изменить или напрямую использовать XML-представление метаданных.</span><span class="sxs-lookup"><span data-stu-id="9d10b-110">Developers should not attempt to modify or directly use the XML representation of the metadata.</span></span>

<span data-ttu-id="9d10b-111">Модули записи и инициаторы поставляются с различными методами запросов и Set для доступа и изменения компонентов резервного копирования и документов метаданных модуля записи:</span><span class="sxs-lookup"><span data-stu-id="9d10b-111">Writers and requesters are provided with a variety of query and set methods to access and modify the Backup Components and Writer Metadata documents:</span></span>

-   [<span data-ttu-id="9d10b-112">Работа с документом метаданных модуля записи</span><span class="sxs-lookup"><span data-stu-id="9d10b-112">Working with the Writer Metadata Document</span></span>](working-with-the-writer-metadata-document.md)
-   [<span data-ttu-id="9d10b-113">Работа с документом компонентов резервного копирования</span><span class="sxs-lookup"><span data-stu-id="9d10b-113">Working with the Backup Components Document</span></span>](working-with-the-backup-components-document.md)
-   [<span data-ttu-id="9d10b-114">Компоненты метаданных VSS</span><span class="sxs-lookup"><span data-stu-id="9d10b-114">VSS Metadata Components</span></span>](vss-metadata-components.md)

 

 



