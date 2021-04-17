---
description: Свойство UpgradeCode представляет собой идентификатор GUID, представляющий связанный набор продуктов. Значение UpgradeCode используется в таблице Upgrade для поиска связанных версий уже установленных продуктов. Это свойство используется действием Регистерпродукт.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: UpgradeCode, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651903"
---
# <a name="upgradecode-property"></a><span data-ttu-id="c01e3-104">UpgradeCode, свойство</span><span class="sxs-lookup"><span data-stu-id="c01e3-104">UpgradeCode property</span></span>

<span data-ttu-id="c01e3-105">Свойство **UpgradeCode** представляет собой идентификатор GUID, представляющий связанный набор продуктов.</span><span class="sxs-lookup"><span data-stu-id="c01e3-105">The **UpgradeCode** property is a GUID representing a related set of products.</span></span> <span data-ttu-id="c01e3-106">Значение **UpgradeCode** используется в [таблице Upgrade](upgrade-table.md) для поиска связанных версий уже установленных продуктов.</span><span class="sxs-lookup"><span data-stu-id="c01e3-106">The **UpgradeCode** is used in the [Upgrade Table](upgrade-table.md) to search for related versions of the product that are already installed.</span></span>

<span data-ttu-id="c01e3-107">Это свойство используется [действием регистерпродукт](registerproduct-action.md).</span><span class="sxs-lookup"><span data-stu-id="c01e3-107">This property is used by the [RegisterProduct action](registerproduct-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c01e3-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c01e3-108">Remarks</span></span>

<span data-ttu-id="c01e3-109">Настоятельно рекомендуется, чтобы авторы установочных пакетов указали **UpgradeCode** для своего приложения.</span><span class="sxs-lookup"><span data-stu-id="c01e3-109">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span>

## <a name="requirements"></a><span data-ttu-id="c01e3-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c01e3-110">Requirements</span></span>



| <span data-ttu-id="c01e3-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c01e3-111">Requirement</span></span> | <span data-ttu-id="c01e3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c01e3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c01e3-113">Версия</span><span class="sxs-lookup"><span data-stu-id="c01e3-113">Version</span></span><br/> | <span data-ttu-id="c01e3-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c01e3-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c01e3-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c01e3-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c01e3-116">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c01e3-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c01e3-117">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c01e3-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c01e3-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c01e3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c01e3-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="c01e3-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c01e3-120">Установка исправлений и обновления</span><span class="sxs-lookup"><span data-stu-id="c01e3-120">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="c01e3-121">Подготовка приложения к будущим основным обновлениям</span><span class="sxs-lookup"><span data-stu-id="c01e3-121">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




