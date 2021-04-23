---
description: Компоненты указывают типы данных, которые они представляют через тип.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Типы компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693696"
---
# <a name="component-types"></a><span data-ttu-id="8d26b-103">Типы компонентов</span><span class="sxs-lookup"><span data-stu-id="8d26b-103">Component Types</span></span>

<span data-ttu-id="8d26b-104">Компоненты указывают типы данных, которые они представляют через тип.</span><span class="sxs-lookup"><span data-stu-id="8d26b-104">Components indicate the sort of data they represent through a type.</span></span>

<span data-ttu-id="8d26b-105">В настоящее время типы компонентов (см. раздел [**\_ \_ тип компонента VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) имеют следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="8d26b-105">Currently, component types (see [**VSS\_COMPONENT\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) are limited to the following:</span></span>

-   <span data-ttu-id="8d26b-106">Компоненты базы данных</span><span class="sxs-lookup"><span data-stu-id="8d26b-106">Database components</span></span>
-   <span data-ttu-id="8d26b-107">Группы файлов</span><span class="sxs-lookup"><span data-stu-id="8d26b-107">File groups</span></span>

<span data-ttu-id="8d26b-108">Сведения о реализации типов компонентов см. в разделе [Определение компонентов по модулям записи](definition-of-components-by-writers.md).</span><span class="sxs-lookup"><span data-stu-id="8d26b-108">For implementation information about setting component types, see [Definition of Components by Writers](definition-of-components-by-writers.md).</span></span>

<span data-ttu-id="8d26b-109">Модули записи имеют тип данных, указывающий их использование (см. сведения о [**\_ \_ типе источника VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)). это может быть следующее:</span><span class="sxs-lookup"><span data-stu-id="8d26b-109">Writers have a data typing that indicates their usage (see [**VSS\_SOURCE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), which can be the following:</span></span>

-   <span data-ttu-id="8d26b-110">Транзакционная база данных (например, SQL Server);</span><span class="sxs-lookup"><span data-stu-id="8d26b-110">A transactional database (such as an SQL server)</span></span>
-   <span data-ttu-id="8d26b-111">Нетранзакционная база данных (например, клиент электронной таблицы)</span><span class="sxs-lookup"><span data-stu-id="8d26b-111">A nontransactional database (such as a spreadsheet client)</span></span>
-   <span data-ttu-id="8d26b-112">Файловая группа (другая)</span><span class="sxs-lookup"><span data-stu-id="8d26b-112">File group (other)</span></span>

<span data-ttu-id="8d26b-113">Указание типа компонента в качестве базы данных позволяет упростить идентификацию содержимого, позволяет отдельно обрабатывать файлы журналов и данных (Дополнительные сведения см. в разделе [**ивсскреатевритерметадата**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) и [**ивссексаминевритерметадата**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) ) и обеспечивает более высокий строгий выбор файлов, не разрешая рекурсивного выбора файлов или использования [*альтернативного пути*](vssgloss-a.md) (см. раздел [**ивсскреатевритерметадата:: адддатабасефилес**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) и [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).</span><span class="sxs-lookup"><span data-stu-id="8d26b-113">Specifying a component type as database allows for easier identification of its content, allows for separate handling of log and data files (see [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) and [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) for details), and enforces greater rigor in file selection by not allowing either recursive file selection or using an [*alternate path*](vssgloss-a.md) (see [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) and [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).</span></span>

<span data-ttu-id="8d26b-114">С другой стороны, с помощью компонента файловой группы, по цене не зная, какие данные он содержит, вы можете получить большую свободу при вставке файлов, так как можно использовать рекурсивную спецификацию и альтернативные пути.</span><span class="sxs-lookup"><span data-stu-id="8d26b-114">With a file group component, on the other hand, at the price of not knowing what data it contains, you have greater freedom about how files are inserted, because you can use recursive specification and alternate paths.</span></span>

<span data-ttu-id="8d26b-115">Дополнительные типы компонентов могут быть добавлены в будущем.</span><span class="sxs-lookup"><span data-stu-id="8d26b-115">Additional component types may be added in the future.</span></span>

 

 



