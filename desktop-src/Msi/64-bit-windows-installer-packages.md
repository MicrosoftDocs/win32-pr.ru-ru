---
description: 64-разрядный пакет содержит частично или полностью 64-разрядные установщик Windows компонентов.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: 64-разрядные пакеты установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909159"
---
# <a name="64-bit-windows-installer-packages"></a><span data-ttu-id="78b17-103">64-разрядные пакеты установщик Windows</span><span class="sxs-lookup"><span data-stu-id="78b17-103">64-bit Windows Installer Packages</span></span>

<span data-ttu-id="78b17-104">64-разрядный пакет содержит частично или полностью 64-разрядные [установщик Windows](windows-installer-components.md) компонентов.</span><span class="sxs-lookup"><span data-stu-id="78b17-104">A 64-bit package consists partially or entirely of 64-bit [Windows Installer](windows-installer-components.md) components.</span></span> <span data-ttu-id="78b17-105">В следующем списке перечислены требования для каждого 64-разрядного пакета установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="78b17-105">The following list identifies the requirements for every 64-bit Windows Installer package:</span></span>

-   <span data-ttu-id="78b17-106">Значение "Intel64" необходимо указать в поле "платформа" Свойства " [**Сводка" шаблона**](template-summary.md) , только если пакет выполняется на процессоре Intel64 (Itanium).</span><span class="sxs-lookup"><span data-stu-id="78b17-106">The value "Intel64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Intel64 (Itanium) processor.</span></span>
-   <span data-ttu-id="78b17-107">Значение "x64" необходимо указать в поле "платформа" Свойства " [**Сводка" шаблона**](template-summary.md) , только если пакет выполняется на процессоре x64.</span><span class="sxs-lookup"><span data-stu-id="78b17-107">The value "x64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an x64 processor.</span></span>
-   <span data-ttu-id="78b17-108">Значение "Arm64" необходимо указать в поле "платформа" Свойства " [**Сводка" шаблона**](template-summary.md) , только если пакет выполняется в процессоре Arm64.</span><span class="sxs-lookup"><span data-stu-id="78b17-108">The value "Arm64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Arm64 processor.</span></span>
-   <span data-ttu-id="78b17-109">Для свойства " [**Сводка количества страниц**](page-count-summary.md) " должно быть задано целое число 200 или больше, поскольку установщик Windows 2,0 — это минимальная версия, способная устанавливать 64-разрядные компоненты.</span><span class="sxs-lookup"><span data-stu-id="78b17-109">The [**Page Count Summary**](page-count-summary.md) property must be set to the integer 200 or greater, because Windows Installer 2.0 is the minimum version that is capable of installing 64-bit components.</span></span> <span data-ttu-id="78b17-110">Пакеты для платформы Arm64 должны иметь значение 500 или выше.</span><span class="sxs-lookup"><span data-stu-id="78b17-110">Packages for the Arm64 platform require a value of 500 or greater.</span></span>
-   <span data-ttu-id="78b17-111">Каждый 64-разрядный компонент установщик Windows в пакете должен включать бит **msidbComponentAttributes64bit** в столбец Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="78b17-111">Each 64-bit Windows Installer component in the package must include the **msidbComponentAttributes64bit** bit in the Attributes column of the [Component Table](component-table.md).</span></span>

<span data-ttu-id="78b17-112">Дополнительные сведения см. [в разделе установщик Windows на 64-разрядных операционных системах](windows-installer-on-64-bit-operating-systems.md) и [32-разрядных установщик Windows пакетах](32-bit-windows-installer-packages.md).</span><span class="sxs-lookup"><span data-stu-id="78b17-112">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md) and [32-bit Windows Installer Packages](32-bit-windows-installer-packages.md).</span></span>

 

 



