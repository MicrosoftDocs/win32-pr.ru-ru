---
description: Придерживайтесь этих рекомендаций при создании 64-разрядного модуля слияния.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Использование 64-разрядных модулей слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815432"
---
# <a name="using-64-bit-merge-modules"></a><span data-ttu-id="e5b6b-103">Использование 64-разрядных модулей слияния</span><span class="sxs-lookup"><span data-stu-id="e5b6b-103">Using 64-bit Merge Modules</span></span>

<span data-ttu-id="e5b6b-104">64-разрядный модуль слияния имеет любую из характеристик, указанных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="e5b6b-104">A 64-bit merge module has any of the characteristics identified in this this topic.</span></span>

-   <span data-ttu-id="e5b6b-105">Модуль слияния содержит по крайней мере один компонент, скомпилированный для 64-разрядных операционных систем.</span><span class="sxs-lookup"><span data-stu-id="e5b6b-105">The merge module contains at least one component that has been compiled for 64-bit operating systems.</span></span>
-   <span data-ttu-id="e5b6b-106">Модуль слияния не содержит 64-разрядных компонентов, но предназначен для использования только с [64-разрядными установщик Windows](64-bit-windows-installer-packages.md) пакетами.</span><span class="sxs-lookup"><span data-stu-id="e5b6b-106">The merge module contains no 64-bit components, but is intended for use only with [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>

<span data-ttu-id="e5b6b-107">Модули слияния можно использовать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e5b6b-107">Merge modules can be used as follows:</span></span>

-   <span data-ttu-id="e5b6b-108">64-разрядный модуль слияния можно объединить в [64-разрядный пакет установщик Windows](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b6b-108">A 64-bit merge module can be merged into a [64-bit Windows Installer](64-bit-windows-installer-packages.md) package.</span></span> <span data-ttu-id="e5b6b-109">Для свойств [**сводки шаблона**](template-summary.md) в модуле слияния и в пакете установщик Windows должен быть задан один и тот же тип 64-разрядного процессора.</span><span class="sxs-lookup"><span data-stu-id="e5b6b-109">The [**Template Summary**](template-summary.md) properties in the merge module and in the Windows Installer package must be set to the same type of 64-bit processor.</span></span> <span data-ttu-id="e5b6b-110">Модуль слияния x64 можно объединить только в пакеты x64, а модуль Intel64 MERGE можно объединить только в пакеты Intel64.</span><span class="sxs-lookup"><span data-stu-id="e5b6b-110">A x64 merge module can be merged only into x64 packages and an Intel64 merge module can be merged only into Intel64 packages.</span></span>
-   <span data-ttu-id="e5b6b-111">32-разрядный модуль слияния можно объединить в пакеты 32 или [64-bit установщик Windows](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b6b-111">A 32-bit merge module can be merged into 32-bit or [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>
-   <span data-ttu-id="e5b6b-112">64-разрядный модуль слияния можно объединить в 64-разрядный пакет в 32-разрядной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="e5b6b-112">A 64-bit merge module can be merged into a 64-bit package on a 32-bit operating system.</span></span>

<span data-ttu-id="e5b6b-113">При создании 64-разрядного модуля слияния придерживайтесь следующих действий:</span><span class="sxs-lookup"><span data-stu-id="e5b6b-113">Adhere to the following when authoring a 64-bit merge module:</span></span>

-   <span data-ttu-id="e5b6b-114">Используйте ту же общую процедуру, что и при создании 32-разрядных модулей слияния.</span><span class="sxs-lookup"><span data-stu-id="e5b6b-114">Use the same general procedure as when authoring 32-bit merge modules.</span></span> <span data-ttu-id="e5b6b-115">Дополнительные сведения см. в разделе [о модулях слияния](about-merge-modules.md) и [разработке модулей слияния](authoring-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="e5b6b-115">For information, see [About Merge Modules](about-merge-modules.md) and [Authoring Merge Modules](authoring-merge-modules.md).</span></span>
-   <span data-ttu-id="e5b6b-116">При запуске системы Intel64 необходимо задать свойство [**сводки шаблона**](template-summary.md) со значением Intel64.</span><span class="sxs-lookup"><span data-stu-id="e5b6b-116">You must set the [**Template Summary**](template-summary.md) property with the Intel64 value if running an Intel64 system.</span></span> <span data-ttu-id="e5b6b-117">При запуске системы x64 необходимо задать для свойства " **Сводка" шаблона** значение x64.</span><span class="sxs-lookup"><span data-stu-id="e5b6b-117">You must set the **Template Summary** property with the x64 value if running an x64 system.</span></span> <span data-ttu-id="e5b6b-118">Дополнительные сведения см. в статье [Справочник по сводному потоку для модуля слияния](merge-module-summary-information-stream-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e5b6b-118">For information see [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md).</span></span>
-   <span data-ttu-id="e5b6b-119">Если для одного и того же компонента существует как 32-разрядный, так и 64-битный модуль слияния, рекомендуется, чтобы модули имели разные сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="e5b6b-119">When both 32-bit and 64-bit merge modules exist for the same component, it is recommended that the modules have different signatures.</span></span> <span data-ttu-id="e5b6b-120">Это позволит пакету содержать обе версии компонента.</span><span class="sxs-lookup"><span data-stu-id="e5b6b-120">This will enable a package to contain both versions of the component.</span></span>

<span data-ttu-id="e5b6b-121">Дополнительные сведения см. [в разделе установщик Windows в 64-разрядных операционных системах](windows-installer-on-64-bit-operating-systems.md).</span><span class="sxs-lookup"><span data-stu-id="e5b6b-121">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md).</span></span>

 

 



