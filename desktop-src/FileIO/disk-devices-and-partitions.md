---
description: Описывает жесткий диск, разделы и основную загрузочную запись.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Дисковые устройства и разделы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570780"
---
# <a name="disk-devices-and-partitions"></a><span data-ttu-id="a264f-103">Дисковые устройства и разделы</span><span class="sxs-lookup"><span data-stu-id="a264f-103">Disk Devices and Partitions</span></span>

<span data-ttu-id="a264f-104">Жесткий диск состоит из набора вращающиеся с накоплением, каждый из которых содержит электромагнитные данные, которые хранятся в концентрических кругах или в *дорожках*.</span><span class="sxs-lookup"><span data-stu-id="a264f-104">A hard disk consists of a set of stacked platters, each of which has data stored electromagnetically in concentric circles, or *tracks*.</span></span> <span data-ttu-id="a264f-105">Каждый Негнущийся имеет две головки — по одной на каждой стороне негнущийся, которая считывает или записывает данные по мере прокрутки диска.</span><span class="sxs-lookup"><span data-stu-id="a264f-105">Each platter has two heads, one on each side of the platter, that reads or writes data as the disk spins.</span></span> <span data-ttu-id="a264f-106">*Жесткий* диск управляет размещением, чтением и записью жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="a264f-106">A *hard disk drive* controls the positioning, reading, and writing of the hard disk.</span></span> <span data-ttu-id="a264f-107">Обратите внимание, что заголовки всех вращающиеся размещаются как единое целое.</span><span class="sxs-lookup"><span data-stu-id="a264f-107">Note that the heads of all platters are positioned as a unit.</span></span>

<span data-ttu-id="a264f-108">Наименьшая адресная единица записи — это *сектор*.</span><span class="sxs-lookup"><span data-stu-id="a264f-108">The smallest addressable unit of a track is a *sector*.</span></span> <span data-ttu-id="a264f-109">*Цилиндр* определяется как набор дорожек, которые отображаются в одном расположении на каждом Негнущийся.</span><span class="sxs-lookup"><span data-stu-id="a264f-109">A *cylinder* is defined as the set of tracks that appear in the same location on each platter.</span></span> <span data-ttu-id="a264f-110">Например, на следующей диаграмме показан жесткий диск с четырьмя вращающиеся.</span><span class="sxs-lookup"><span data-stu-id="a264f-110">For example, the following diagram shows a hard disk with four platters.</span></span> <span data-ttu-id="a264f-111">Цилиндр X состоит из восьми дорожек (следом X от каждой стороны каждого Негнущийся).</span><span class="sxs-lookup"><span data-stu-id="a264f-111">Cylinder X consists of eight tracks (track X from each side of each platter).</span></span>

![жесткий диск, включая дорожки, секторы и вращающиеся](images/diskdevice.png)

<span data-ttu-id="a264f-113">Жесткий диск может содержать один или несколько логических регионов, называемых *разделами*.</span><span class="sxs-lookup"><span data-stu-id="a264f-113">A hard disk can contain one or more logical regions called *partitions*.</span></span> <span data-ttu-id="a264f-114">Разделы создаются, когда пользователь форматирует жесткий диск в качестве *базового диска*.</span><span class="sxs-lookup"><span data-stu-id="a264f-114">Partitions are created when the user formats a hard disk as a *basic disk*.</span></span> <span data-ttu-id="a264f-115">Windows также поддерживает *динамические диски*, которые не рассматриваются в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="a264f-115">Windows also supports *dynamic disks*, which are not discussed in this topic.</span></span> <span data-ttu-id="a264f-116">Дополнительные сведения о базовых дисках и динамических дисках см. в разделе [базовые и динамические](basic-and-dynamic-disks.md)диски.</span><span class="sxs-lookup"><span data-stu-id="a264f-116">For more information about basic disks and dynamic disks, see [Basic and Dynamic Disks](basic-and-dynamic-disks.md).</span></span>

<span data-ttu-id="a264f-117">Создание нескольких разделов на диске обеспечивает внешний вид отдельных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="a264f-117">The creation of multiple partitions on a disk allows the appearance of having separate hard drives.</span></span> <span data-ttu-id="a264f-118">Например, система с одним жестким диском с одним разделом содержит один том, обозначенный системой как диск C. Система с жестким диском с двумя разделами обычно содержит диски C и D. Наличие нескольких разделов на жестком диске может упростить управление системой, например, организацию файлов или поддержку нескольких пользователей.</span><span class="sxs-lookup"><span data-stu-id="a264f-118">For example, a system with one hard disk that has one partition contains a single volume, designated by the system as drive C. A system with a hard disk with two partitions typically contains drives C and D. Having multiple partitions on a hard disk can make it easier to manage the system, for example to organize files or to support multiple users.</span></span>

<span data-ttu-id="a264f-119">Первый физический сектор на базовом диске содержит структуру данных, известную как основная загрузочная запись (MBR).</span><span class="sxs-lookup"><span data-stu-id="a264f-119">The first physical sector on a basic disk contains a data structure known as the Master Boot Record (MBR).</span></span> <span data-ttu-id="a264f-120">MBR содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="a264f-120">The MBR contains the following:</span></span>

-   <span data-ttu-id="a264f-121">Программа загрузки (размер до 442 байт)</span><span class="sxs-lookup"><span data-stu-id="a264f-121">A boot program (up to 442 bytes in size)</span></span>
-   <span data-ttu-id="a264f-122">Подпись диска (уникальное 4-байтовое число)</span><span class="sxs-lookup"><span data-stu-id="a264f-122">A disk signature (a unique 4-byte number)</span></span>
-   <span data-ttu-id="a264f-123">Таблица разделов (до четырех записей)</span><span class="sxs-lookup"><span data-stu-id="a264f-123">A partition table (up to four entries)</span></span>
-   <span data-ttu-id="a264f-124">Маркер конца MBR (всегда 0x55AA)</span><span class="sxs-lookup"><span data-stu-id="a264f-124">An end-of-MBR marker (always 0x55AA)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a264f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a264f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a264f-126">Об управлении томами</span><span class="sxs-lookup"><span data-stu-id="a264f-126">About Volume Management</span></span>](about-volume-management.md)
</dt> <dt>

[<span data-ttu-id="a264f-127">Базовые и динамические диски</span><span class="sxs-lookup"><span data-stu-id="a264f-127">Basic and Dynamic Disks</span></span>](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



