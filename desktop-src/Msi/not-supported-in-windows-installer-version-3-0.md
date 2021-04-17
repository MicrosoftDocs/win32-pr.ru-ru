---
description: Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются установщик Windows&\# 160; 3.0 и более ранних версий.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Не поддерживается в установщик Windows 3,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673561"
---
# <a name="not-supported-in-windows-installer-30"></a><span data-ttu-id="ad5c8-103">Не поддерживается в установщик Windows 3,0</span><span class="sxs-lookup"><span data-stu-id="ad5c8-103">Not Supported in Windows Installer 3.0</span></span>

<span data-ttu-id="ad5c8-104">Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются в установщик Windows 3,0 и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="ad5c8-104">The Windows Installer functions, tables, and properties listed on this page are not supported by Windows Installer 3.0 and earlier versions.</span></span> <span data-ttu-id="ad5c8-105">Отсутствие функции из этого списка не гарантирует, что эта функция поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad5c8-105">The absence of a feature from this list does not guarantee that the feature is supported.</span></span> <span data-ttu-id="ad5c8-106">Чтобы определить, какая версия установщик Windows требуется для конкретной функции, см. основную документацию.</span><span class="sxs-lookup"><span data-stu-id="ad5c8-106">See the main documentation to determine which Windows Installer version is required for a particular feature.</span></span> <span data-ttu-id="ad5c8-107">Сведения о других установщик Windows версиях см. [в разделе новые возможности установщик Windows](what-s-new-in-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="ad5c8-107">For information about other Windows Installer versions see [What's New in Windows Installer](what-s-new-in-windows-installer.md).</span></span>

<span data-ttu-id="ad5c8-108">Установщик Windows 3,0 доступна для Windows Server 2003, Windows XP или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ad5c8-108">Windows Installer 3.0 is available for Windows Server 2003, Windows XP, or Windows 2000.</span></span> <span data-ttu-id="ad5c8-109">Список всех установщик Windows версий и распространяемых компонентов см. в разделе [выпущенные версии установщик Windows](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="ad5c8-109">For a list of all Windows Installer versions and redistributables, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

<span data-ttu-id="ad5c8-110">Следующие функции не поддерживаются в установщик Windows 3,0 и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="ad5c8-110">The following features are not supported in Windows Installer 3.0 and earlier versions.</span></span>

[<span data-ttu-id="ad5c8-111">Функции установщика</span><span class="sxs-lookup"><span data-stu-id="ad5c8-111">Installer Functions</span></span>](installer-functions.md)

-   [<span data-ttu-id="ad5c8-112">**мсисетекстерналуирекорд**</span><span class="sxs-lookup"><span data-stu-id="ad5c8-112">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="ad5c8-113">**мсинотифисидчанже**</span><span class="sxs-lookup"><span data-stu-id="ad5c8-113">**MsiNotifySidChange**</span></span>](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

<span data-ttu-id="ad5c8-114">Прототип функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="ad5c8-114">Callback Function Prototype</span></span>

-   [<span data-ttu-id="ad5c8-115">**\_запись обработчика инсталлуи \_**</span><span class="sxs-lookup"><span data-stu-id="ad5c8-115">**INSTALLUI\_HANDLER\_RECORD**</span></span>](/windows/win32/api/msi/nc-msi-installui_handler_record)

[<span data-ttu-id="ad5c8-116">Таблицы базы данных</span><span class="sxs-lookup"><span data-stu-id="ad5c8-116">Database Tables</span></span>](database-tables.md)

-   <span data-ttu-id="ad5c8-117">Столбец значение в [таблице мсипатчметадата](msipatchmetadata-table.md) принимает значения **оптимизединсталлмоде** и **минорупдатетаржетртм**.</span><span class="sxs-lookup"><span data-stu-id="ad5c8-117">The Value column of the [MsiPatchMetadata Table](msipatchmetadata-table.md) accepts **OptimizedInstallMode** and **MinorUpdateTargetRTM**.</span></span>

[<span data-ttu-id="ad5c8-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="ad5c8-118">Properties</span></span>](properties.md)

-   [<span data-ttu-id="ad5c8-119">**Msix64, свойство**</span><span class="sxs-lookup"><span data-stu-id="ad5c8-119">**Msix64 Property**</span></span>](msix64.md)

[<span data-ttu-id="ad5c8-120">Установщик Windows в 64-разрядных операционных системах</span><span class="sxs-lookup"><span data-stu-id="ad5c8-120">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)

-   <span data-ttu-id="ad5c8-121">[**Свойство "Сводка" шаблона**](template-summary.md) принимает значение x64.</span><span class="sxs-lookup"><span data-stu-id="ad5c8-121">The [**Template Summary Property**](template-summary.md) accepts the value x64.</span></span>

[<span data-ttu-id="ad5c8-122">Внутренние средства оценки согласованности — ICEs</span><span class="sxs-lookup"><span data-stu-id="ad5c8-122">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

-   [<span data-ttu-id="ad5c8-123">ICE99</span><span class="sxs-lookup"><span data-stu-id="ad5c8-123">ICE99</span></span>](ice99.md)

 

 
