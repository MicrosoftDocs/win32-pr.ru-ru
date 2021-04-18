---
description: Сборки среды CLR, установленные в глобальный кэш сборок, должны иметь одинаковые файлы во всех экземплярах сборки.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Режимы переустановки сборок среды CLR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663055"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a><span data-ttu-id="62b11-103">Режимы переустановки сборок среды CLR</span><span class="sxs-lookup"><span data-stu-id="62b11-103">Reinstallation Modes of Common Language Runtime Assemblies</span></span>

<span data-ttu-id="62b11-104">Сборки среды CLR, установленные в глобальный кэш сборок, должны иметь одинаковые файлы во всех экземплярах сборки.</span><span class="sxs-lookup"><span data-stu-id="62b11-104">Common language runtime assemblies that are installed to the global assembly cache must have identical files in all occurrences of the assembly.</span></span> <span data-ttu-id="62b11-105">Это означает, что режимы переустановки, используемые [**мсиреинсталлфеатуре**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) и [**мсиреинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) , должны иметь разные значения для обычных компонентов и сборок среды CLR.</span><span class="sxs-lookup"><span data-stu-id="62b11-105">This means that the reinstallation modes used by [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) and [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) must have different meanings for regular components and common language runtime assemblies.</span></span> <span data-ttu-id="62b11-106">Следующие определения режимов переустановки применяются к сборкам среды CLR.</span><span class="sxs-lookup"><span data-stu-id="62b11-106">The following definitions of reinstall modes apply to common language runtime assemblies.</span></span>



| <span data-ttu-id="62b11-107">Режим переустановки</span><span class="sxs-lookup"><span data-stu-id="62b11-107">Reinstall mode</span></span>                  | <span data-ttu-id="62b11-108">Значение для компонентов Microsoft .NET</span><span class="sxs-lookup"><span data-stu-id="62b11-108">Meaning for Microsoft .NET Components</span></span>                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b11-109">REINSTALLMODE \_ филемиссинг</span><span class="sxs-lookup"><span data-stu-id="62b11-109">REINSTALLMODE\_FILEMISSING</span></span>      | <span data-ttu-id="62b11-110">Установите или переустановите компонент среды CLR, если он отсутствует или неполон.</span><span class="sxs-lookup"><span data-stu-id="62b11-110">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="62b11-111">REINSTALLMODE \_ филеолдерверсион</span><span class="sxs-lookup"><span data-stu-id="62b11-111">REINSTALLMODE\_FILEOLDERVERSION</span></span> | <span data-ttu-id="62b11-112">Установите или переустановите компонент среды CLR, если он отсутствует или неполон.</span><span class="sxs-lookup"><span data-stu-id="62b11-112">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="62b11-113">REINSTALLMODE \_ филикуалверсион</span><span class="sxs-lookup"><span data-stu-id="62b11-113">REINSTALLMODE\_FILEEQUALVERSION</span></span> | <span data-ttu-id="62b11-114">Установите или переустановите компонент среды CLR, если он отсутствует или неполон.</span><span class="sxs-lookup"><span data-stu-id="62b11-114">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="62b11-115">REINSTALLMODE \_ филиксакт</span><span class="sxs-lookup"><span data-stu-id="62b11-115">REINSTALLMODE\_FILEEXACT</span></span>        | <span data-ttu-id="62b11-116">Установите или переустановите компонент среды CLR, если он отсутствует или неполон.</span><span class="sxs-lookup"><span data-stu-id="62b11-116">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="62b11-117">REINSTALLMODE \_ филеверифи</span><span class="sxs-lookup"><span data-stu-id="62b11-117">REINSTALLMODE\_FILEVERIFY</span></span>       | <span data-ttu-id="62b11-118">Установите или переустановите компонент среды CLR, если он отсутствует или если существующий компонент неполон или поврежден.</span><span class="sxs-lookup"><span data-stu-id="62b11-118">Install or reinstall the common language runtime component if it is missing or if the existing component is incomplete or corrupt.</span></span> |
| <span data-ttu-id="62b11-119">REINSTALLMODE \_ филереплаце</span><span class="sxs-lookup"><span data-stu-id="62b11-119">REINSTALLMODE\_FILEREPLACE</span></span>      | <span data-ttu-id="62b11-120">Всегда устанавливайте или переустановите компонент среды CLR.</span><span class="sxs-lookup"><span data-stu-id="62b11-120">Always install or reinstall the common language runtime component.</span></span>                                                                 |



 

 

 



