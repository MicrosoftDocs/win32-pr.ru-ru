---
description: Состояние установки вспомогательного файла зависит не от его собственных сведений о версиях файлов, но и от управления версиями его сопутствующего родителя.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Сопутствующие файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999029"
---
# <a name="companion-files"></a><span data-ttu-id="6f966-103">Сопутствующие файлы</span><span class="sxs-lookup"><span data-stu-id="6f966-103">Companion Files</span></span>

<span data-ttu-id="6f966-104">Состояние установки вспомогательного файла зависит не от его собственных сведений о версиях файлов, но и от управления версиями его сопутствующего родителя.</span><span class="sxs-lookup"><span data-stu-id="6f966-104">The installation state of a companion file depends not on its own file versioning information, but on the versioning of its companion parent.</span></span> <span data-ttu-id="6f966-105">См. [правила управления версиями файлов](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="6f966-105">See the [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="6f966-106">Чтобы указать сопутствующий файл, первичный ключ вспомогательного родителя в [таблице File](file-table.md) должен быть создан в столбце Version записи для сопровождающего.</span><span class="sxs-lookup"><span data-stu-id="6f966-106">To specify a companion file, the primary key of the companion parent in the [File table](file-table.md) must be authored into the Version column of the record for the companion.</span></span>

<span data-ttu-id="6f966-107">В следующем примере файл a является сопутствующим родителем, а Филеб — сопутствующий файл.</span><span class="sxs-lookup"><span data-stu-id="6f966-107">In the following example, FileA is the companion parent and FileB is the companion file.</span></span>

<span data-ttu-id="6f966-108">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="6f966-108">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="6f966-109">Файл</span><span class="sxs-lookup"><span data-stu-id="6f966-109">File</span></span>  | <span data-ttu-id="6f966-110">Версия</span><span class="sxs-lookup"><span data-stu-id="6f966-110">Version</span></span> |
|-------|---------|
| <span data-ttu-id="6f966-111">Файл а</span><span class="sxs-lookup"><span data-stu-id="6f966-111">FileA</span></span> | <span data-ttu-id="6f966-112">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="6f966-112">1.0.0.0</span></span> |
| <span data-ttu-id="6f966-113">филеб</span><span class="sxs-lookup"><span data-stu-id="6f966-113">FileB</span></span> | <span data-ttu-id="6f966-114">Файл а</span><span class="sxs-lookup"><span data-stu-id="6f966-114">FileA</span></span>   |



 

<span data-ttu-id="6f966-115">В этом примере состояние установки Филеб зависит от [правил управления версиями файлов](file-versioning-rules.md) и сведений об управлении версиями файла.</span><span class="sxs-lookup"><span data-stu-id="6f966-115">In this example, the installation state of FileB depends on the [File Versioning Rules](file-versioning-rules.md) and the versioning information for FileA.</span></span> <span data-ttu-id="6f966-116">Если установщик определяет, что версия файла a в пакете должна быть установлена поверх более старой версии файла, которая уже существует на компьютере пользователя, она также установит Филеб из пакета независимо от версии установленных Филеб.</span><span class="sxs-lookup"><span data-stu-id="6f966-116">If the installer determines that the version of FileA in the package should be installed over an older version of FileA that already exists on the user's computer, it will also install FileB from the package regardless of the version of any installed FileB.</span></span>

<span data-ttu-id="6f966-117">Обратите внимание, что файл, который является путем к ключу для своего компонента, не должен быть сопутствующим файлом.</span><span class="sxs-lookup"><span data-stu-id="6f966-117">Note that a file that is the key path for its component must not be a companion file.</span></span> <span data-ttu-id="6f966-118">Это приведет к тому, что логика управления версиями файла пути к ключу определяется сопутствующим родительским файлом.</span><span class="sxs-lookup"><span data-stu-id="6f966-118">This would result in the versioning logic of the key path file being determined by the companion parent file.</span></span>

 

 



