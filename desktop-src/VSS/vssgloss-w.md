---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (служба теневого копирования томов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541714"
---
# <a name="w-volume-shadow-copy-service"></a><span data-ttu-id="a70a3-103">W (служба теневого копирования томов)</span><span class="sxs-lookup"><span data-stu-id="a70a3-103">W (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="a70a3-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [р](vssgloss-h.md) [. J](vssgloss-i.md) K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="a70a3-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a70a3-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Защита файлов Windows**</span><span class="sxs-lookup"><span data-stu-id="a70a3-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="a70a3-106">Системная служба, защищающая специальные файлы операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a70a3-106">A system service that protects special operating system files.</span></span> <span data-ttu-id="a70a3-107">Если один из этих файлов удаляется или перезаписывается, защита файлов Windows заменяет файл исходным файлом из своего кэша.</span><span class="sxs-lookup"><span data-stu-id="a70a3-107">If one of these files is deleted or overwritten, Windows File Protection replaces the file with the original from its cache.</span></span>

</dd> <dt>

<span data-ttu-id="a70a3-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**средство**</span><span class="sxs-lookup"><span data-stu-id="a70a3-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**writer**</span></span>
</dt> <dd>

<span data-ttu-id="a70a3-109">Приложение, которое координирует операции ввода-вывода с теневыми копиями VSS и операциями теневого копирования (например, резервным копированием и восстановлением), чтобы данные, содержащиеся в теневом скопированном томе, находились в стабильном состоянии.</span><span class="sxs-lookup"><span data-stu-id="a70a3-109">An application that coordinates its I/O operations with VSS shadow copy and shadow copy related operations (such as backups and restores) so that their data contained on the shadow copied volume is in a consistent state.</span></span>

<span data-ttu-id="a70a3-110">Для поддержки этой координации модуль записи должен реализовать экземпляр класса, производного от абстрактного базового класса **квссвритер** для взаимодействия с инфраструктурой VSS.</span><span class="sxs-lookup"><span data-stu-id="a70a3-110">To support this coordination, a writer must implement an instance of a class derived from the abstract base class **CVssWriter** to communicate with the VSS infrastructure.</span></span> <span data-ttu-id="a70a3-111">См. также [*теневое копирование*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="a70a3-111">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70a3-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**Класс модуля записи**</span><span class="sxs-lookup"><span data-stu-id="a70a3-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**writer class**</span></span>
</dt> <dd>

<span data-ttu-id="a70a3-113">Глобальный уникальный идентификатор (GUID), предоставляемый модулем записи во время инициализации, чтобы указать, что он принадлежит данному типу модулей записи.</span><span class="sxs-lookup"><span data-stu-id="a70a3-113">A globally unique identifier (GUID) supplied by a writer during initialization to indicate that it belongs to a given type of writers.</span></span> <span data-ttu-id="a70a3-114">Например, несколько реализаций модуля записи могут совместно использовать один и тот же идентификатор класса модуля записи.</span><span class="sxs-lookup"><span data-stu-id="a70a3-114">For instance, multiple implementations of a writer could share the same writer class ID.</span></span>

<span data-ttu-id="a70a3-115">Модули записи одного и того же класса могут различаться экземплярами модуля записи.</span><span class="sxs-lookup"><span data-stu-id="a70a3-115">Writers of the same class may be distinguished by their writer instances.</span></span> <span data-ttu-id="a70a3-116">Разработчикам приложений следует указывать классы модуля записи.</span><span class="sxs-lookup"><span data-stu-id="a70a3-116">It is up to an application developer to specify writer classes.</span></span> <span data-ttu-id="a70a3-117">См. также *экземпляр модуля записи*.</span><span class="sxs-lookup"><span data-stu-id="a70a3-117">See also *writer instance*.</span></span>

</dd> <dt>

<span data-ttu-id="a70a3-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**экземпляр модуля записи**</span><span class="sxs-lookup"><span data-stu-id="a70a3-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**writer instance**</span></span>
</dt> <dd>

<span data-ttu-id="a70a3-119">Глобальный уникальный идентификатор (GUID), предоставляемый VSS для каждого процесса записи, выполняемого в системе.</span><span class="sxs-lookup"><span data-stu-id="a70a3-119">A globally unique identifier (GUID) supplied by VSS for each writer process running on a system.</span></span> <span data-ttu-id="a70a3-120">При каждом запуске модуля записи создается уникальное значение для экземпляра модуля записи.</span><span class="sxs-lookup"><span data-stu-id="a70a3-120">A unique value for the writer instance is generated each time the writer starts.</span></span>

</dd> <dt>

<span data-ttu-id="a70a3-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Документ метаданных модуля записи**</span><span class="sxs-lookup"><span data-stu-id="a70a3-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Writer Metadata Document**</span></span>
</dt> <dd>

<span data-ttu-id="a70a3-122">XML-документ, созданный модулем записи (с помощью интерфейса **ивсскреатевритерметадата** ), содержащий сведения о состоянии и компонентах модуля записи.</span><span class="sxs-lookup"><span data-stu-id="a70a3-122">An XML document created by a writer (using the **IVssCreateWriterMetadata** interface) containing information about the writer's state and components.</span></span> <span data-ttu-id="a70a3-123">Инициатор запроса может запрашивать документы метаданных модуля записи (с помощью интерфейса **ивссексаминевритерметадата** ) при выполнении операции восстановления или резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a70a3-123">A requester can query Writer Metadata Documents (using the **IVssExamineWriterMetadata** interface) when performing a restore or backup operation.</span></span>

<span data-ttu-id="a70a3-124">Документ метаданных модуля записи содержит список всех компонентов модуля записи, один из которых может участвовать в резервной копии.</span><span class="sxs-lookup"><span data-stu-id="a70a3-124">A Writer Metadata Document contains the list of all of a writer's components, any one of which might participate in a backup.</span></span> <span data-ttu-id="a70a3-125">Это отличается от документа компонента резервного копирования инициатора запроса, который содержит только те компоненты, которые явно включены в операцию резервного копирования или восстановления.</span><span class="sxs-lookup"><span data-stu-id="a70a3-125">This differs from the requester's Backup Components Document, which contains only those components explicitly included for a backup or restore operation.</span></span>

<span data-ttu-id="a70a3-126">После создания документ метаданных модуля записи должен быть просмотрен как объект только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a70a3-126">Once constructed, the Writer Metadata Document should be viewed as a read-only object.</span></span> <span data-ttu-id="a70a3-127">Его можно сохранить на диске.</span><span class="sxs-lookup"><span data-stu-id="a70a3-127">It can be saved to disk.</span></span> <span data-ttu-id="a70a3-128">См. также [*документ компоненты резервного копирования*](vssgloss-b.md), [*явное включение компонентов*](vssgloss-e.md), [*Включение неявных компонентов*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="a70a3-128">See also [*Backup Components Document*](vssgloss-b.md), [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> </dl>

 

 



