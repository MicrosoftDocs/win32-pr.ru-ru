---
title: Общие файлы хранилища и Common-Store SIS
description: Все резервные файлы, поддерживаемые резервным копированием хранилища единственных копий, называются файлами общего хранилища.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Резервное копирование общих хранилищ
- Резервное копирование хранилища единственных экземпляров (SIS), общие хранилища
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890888"
---
# <a name="the-sis-common-store-and-common-store-files"></a><span data-ttu-id="b1bda-105">Общие файлы хранилища и Common-Store SIS</span><span class="sxs-lookup"><span data-stu-id="b1bda-105">The SIS Common Store and Common-Store Files</span></span>

<span data-ttu-id="b1bda-106">Все резервные файлы, поддерживаемые резервным копированием хранилища единственных копий, называются *файлами общего хранилища*.</span><span class="sxs-lookup"><span data-stu-id="b1bda-106">All backing files maintained by single-instance store (SIS) backup are called *common-store files*.</span></span> <span data-ttu-id="b1bda-107">На каждом томе, поддерживаемом SIS, существует одно *Общее хранилище* , которое содержит все файлы общего хранилища, существующие на этом томе.</span><span class="sxs-lookup"><span data-stu-id="b1bda-107">One *common store* exists on each SIS-maintained volume and contains all of the common-store files that exist on that volume.</span></span> <span data-ttu-id="b1bda-108">Этот каталог находится в корневом каталоге тома и имеет имя " \\ Общее хранилище SIS".</span><span class="sxs-lookup"><span data-stu-id="b1bda-108">This directory is located in the root directory of the volume and is named "\\SIS Common Store".</span></span> <span data-ttu-id="b1bda-109">Общее хранилище реализуется как каталог, защищенный от обычного доступа пользователей, так как доступ к файлам общего хранилища предназначен только для функций API резервного копирования SIS, а не для резервного копирования и восстановления приложений.</span><span class="sxs-lookup"><span data-stu-id="b1bda-109">The common store is implemented as a directory that is protected against normal user access, because common-store files are intended to be accessed directly only by SIS backup API functions and not backup and restore applications.</span></span>

<span data-ttu-id="b1bda-110">Ниже перечислены свойства файла общего хранилища.</span><span class="sxs-lookup"><span data-stu-id="b1bda-110">The properties of a common-store file are the following:</span></span>

-   <span data-ttu-id="b1bda-111">Файл общего хранилища может иметь одну или несколько ссылок, указывающих на него.</span><span class="sxs-lookup"><span data-stu-id="b1bda-111">A common-store file may have one or more links pointing to it.</span></span>
-   <span data-ttu-id="b1bda-112">После создания содержимое файла общего хранилища никогда не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b1bda-112">After it is created, the contents of a common-store file never change.</span></span>
-   <span data-ttu-id="b1bda-113">Имена файлов общего хранилища являются глобально уникальными, то есть являются уникальными для всех томов во всех системах мира, а привязка между именем файла общего хранилища и его данными является глобально статичной.</span><span class="sxs-lookup"><span data-stu-id="b1bda-113">The names of common-store files are globally unique—that is, they are unique across all volumes across all systems in the world, and the binding between a common-store file name and its data is globally static.</span></span>

<span data-ttu-id="b1bda-114">При включении SIS на томе в общее хранилище создается одна копия повторяющихся файлов, а все дублирующиеся файлы заменяются [ссылками на SIS](sis-links-and-reparse-points.md) , указывающими на файл общего хранилища.</span><span class="sxs-lookup"><span data-stu-id="b1bda-114">When SIS is enabled on a volume, one copy of the duplicate files is then created to the common store, and all of the duplicate files are replaced with [SIS links](sis-links-and-reparse-points.md) pointing to the common-store file.</span></span> <span data-ttu-id="b1bda-115">Дополнительные сведения см. в статье [Включение или отключение хранилища единственных копий на томе](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) в документации TechNet.</span><span class="sxs-lookup"><span data-stu-id="b1bda-115">For more information, see [Enabling or Disabling SIS on a Volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) in the TechNet documentation.</span></span>

<span data-ttu-id="b1bda-116">Когда для операции записи осуществляется доступ к одной из ссылок SIS, фильтр SIS сначала восстанавливает исходное содержимое файла ссылки SIS из файла общего хранилища, а точка повторного анализа, связывающая файл ссылки SIS с общим хранилищем, удаляется, а затем операция записи выполняется для исходного файла назначения.</span><span class="sxs-lookup"><span data-stu-id="b1bda-116">When one of the SIS links is accessed for a write operation, the SIS filter first restores the original contents of the SIS link file from the common-store file, the reparse point linking the SIS link file to the common store is removed, and then the write operation is performed on the original destination file.</span></span>

<span data-ttu-id="b1bda-117">Файл общего хранилища удаляется только в том случае, если последняя ссылка на SIS указывает на нее.</span><span class="sxs-lookup"><span data-stu-id="b1bda-117">The common-store file is removed only when the last SIS link pointing to it is deleted.</span></span>

 

 