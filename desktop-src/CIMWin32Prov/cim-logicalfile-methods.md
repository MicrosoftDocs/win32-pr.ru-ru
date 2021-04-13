---
description: Класс CIM \_ LogicalFile предоставляет следующие методы.
ms.assetid: 0ACA0C89-BFA6-4B1F-98F1-FB6ACEE65905
ms.tgt_platform: multiple
title: Методы CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2227511388a2e1edf93f8c12bde6506a8cfce4b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538501"
---
# <a name="cim_logicalfile-methods"></a><span data-ttu-id="0b4f5-103">\_Методы LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="0b4f5-103">CIM\_LogicalFile Methods</span></span>

<span data-ttu-id="0b4f5-104">Класс [**CIM \_ LogicalFile**](cim-logicalfile.md) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0b4f5-104">The [**CIM\_LogicalFile**](cim-logicalfile.md) class exposes the following methods.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b4f5-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0b4f5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0b4f5-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0b4f5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="0b4f5-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="0b4f5-107">In this section</span></span>

-   [<span data-ttu-id="0b4f5-108">**Метод Чанжесекуритипермиссионс**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-108">**ChangeSecurityPermissions method**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-109">**Метод Чанжесекуритипермиссионсекс**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-109">**ChangeSecurityPermissionsEx method**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-110">**Метод сжатия**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-110">**Compress method**</span></span>](compress-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-111">**Метод Компрессекс**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-111">**CompressEx method**</span></span>](compressex-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-112">**Метод Copy**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-112">**Copy method**</span></span>](copy-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-113">**Метод Копекс**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-113">**CopyEx method**</span></span>](copyex-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-114">**Метод Delete**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-114">**Delete method**</span></span>](delete-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-115">**Метод Делетикс**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-115">**DeleteEx method**</span></span>](deleteex-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-116">**Метод Жетеффективепермиссион**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-116">**GetEffectivePermission method**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-117">**Переименование метода**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-117">**Rename method**</span></span>](rename-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-118">**Метод Такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-118">**TakeOwnerShip method**</span></span>](takeownership-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-119">**Метод Такеовнершипекс**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-119">**TakeOwnerShipEx method**</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-120">**Распаковать метод**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-120">**Uncompress method**</span></span>](uncompress-method-in-class-cim-logicalfile.md)
-   [<span data-ttu-id="0b4f5-121">**Метод Ункомпрессекс**</span><span class="sxs-lookup"><span data-stu-id="0b4f5-121">**UncompressEx method**</span></span>](uncompressex-method-in-class-cim-logicalfile.md)

 

 



