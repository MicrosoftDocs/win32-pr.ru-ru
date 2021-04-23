---
description: Совместимость со схемой CIM
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: Совместимость со схемой CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df559469ef6a8284b51951dc365bad6c302ca865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712607"
---
# <a name="cim-schema-compatibility"></a><span data-ttu-id="f0544-103">Совместимость со схемой CIM</span><span class="sxs-lookup"><span data-stu-id="f0544-103">CIM Schema Compatibility</span></span>

<span data-ttu-id="f0544-104">Ключевым компонентом инфраструктуры инструментарий управления Windows (WMI) (WMI) является объектно-ориентированная модель управляемых сущностей в системе.</span><span class="sxs-lookup"><span data-stu-id="f0544-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="f0544-105">Модель соответствует стандарту, поддерживаемому задачей «Управление рабочим столом» ([DMTF](https://www.dmtf.org/standards/wsman)) и называется модель CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="f0544-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="f0544-106">Схема CIM предоставляет единый механизм описания данных для любых данных, которые они предоставляют.</span><span class="sxs-lookup"><span data-stu-id="f0544-106">The CIM schema provides a single data description mechanism for any data that they provide.</span></span>

<span data-ttu-id="f0544-107">Начиная с Windows 7 Инструментарий WMI совместим с версией схемы CIM 2.17.1 ( [https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171) ).</span><span class="sxs-lookup"><span data-stu-id="f0544-107">Starting in Windows 7, WMI is compatible with the CIM Schema version 2.17.1 ([https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171)).</span></span> <span data-ttu-id="f0544-108">Теперь пользователи могут компилировать схему, определенную DMTF, на компьютере Windows.</span><span class="sxs-lookup"><span data-stu-id="f0544-108">Users can now compile a DMTF defined schema on a Windows computer.</span></span>

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a><span data-ttu-id="f0544-109">Преимущества совместимости схемы CIM версии 2.17.1</span><span class="sxs-lookup"><span data-stu-id="f0544-109">Benefits of CIM Schema version 2.17.1 compatibility</span></span>

-   <span data-ttu-id="f0544-110">Когда пользователь скачивает файлы схемы CIM версии 2.17.1 или DMTF MOF, они могут быть успешно скомпилированы на целевом компьютере Windows.</span><span class="sxs-lookup"><span data-stu-id="f0544-110">When a user downloads CIM Schema version 2.17.1 or DMTF MOF files, they can be successfully compiled on the target Windows computer.</span></span>
-   <span data-ttu-id="f0544-111">Версия схемы CIM 2.17.1 добавлена поддержка BIOS, принтеров, стандартных сообщений, состояния операционной системы, современных парадигм управления питанием, виртуализации и безопасности.</span><span class="sxs-lookup"><span data-stu-id="f0544-111">The CIM Schema version 2.17.1 added support for BIOS, printers, standard messages, operating system state, modern power management paradigms, virtualization and security.</span></span>
-   <span data-ttu-id="f0544-112">Версия схемы CIM 2.1.7.1 предлагает дополнительную поддержку профилей.</span><span class="sxs-lookup"><span data-stu-id="f0544-112">CIM Schema version 2.1.7.1 offers additional profile support.</span></span> <span data-ttu-id="f0544-113">Дополнительные сведения см. в разделе [перекрестное сопоставление связей между пространствами имен](cross-namespace-association-traversal.md)</span><span class="sxs-lookup"><span data-stu-id="f0544-113">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md)</span></span>

 

 



