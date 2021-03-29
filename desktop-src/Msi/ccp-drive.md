---
description: '\_Свойство Drive CCP устанавливается в корневой путь к съемному тому, для которого выполняется поиск по адресу рмккпсеарч.'
ms.assetid: 567b7d11-6d80-4ec5-810d-f32b9ebf5809
title: CCP_DRIVE, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6215881cd3a998cd63a958bfe258ad3f9872ab1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665485"
---
# <a name="ccp_drive-property"></a><span data-ttu-id="34de6-103">\_Свойство диска CCP</span><span class="sxs-lookup"><span data-stu-id="34de6-103">CCP\_DRIVE property</span></span>

<span data-ttu-id="34de6-104">Свойство **\_ Drive CCP** устанавливается в корневой путь к съемному тому, для которого выполняется поиск по адресу [рмккпсеарч](rmccpsearch-action.md).</span><span class="sxs-lookup"><span data-stu-id="34de6-104">The **CCP\_DRIVE** property is set to the root path of the removable volume that is to be searched by [RMCCPSearch](rmccpsearch-action.md).</span></span> <span data-ttu-id="34de6-105">Действие Рмккпсеарч использует подписи файлов для проверки того, что соответствующие продукты установлены в системе перед установкой обновления.</span><span class="sxs-lookup"><span data-stu-id="34de6-105">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before performing an upgrade installation.</span></span>

<span data-ttu-id="34de6-106">Это свойство обычно задается с помощью пользовательского интерфейса или настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="34de6-106">This property is typically set via the user interface or a custom action.</span></span> <span data-ttu-id="34de6-107">Это свойство должно быть задано до выполнения действия [рмккпсеарч](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="34de6-107">This property should be set before the [RMCCPSearch](rmccpsearch-action.md) action is run.</span></span>

## <a name="requirements"></a><span data-ttu-id="34de6-108">Требования</span><span class="sxs-lookup"><span data-stu-id="34de6-108">Requirements</span></span>



| <span data-ttu-id="34de6-109">Требование</span><span class="sxs-lookup"><span data-stu-id="34de6-109">Requirement</span></span> | <span data-ttu-id="34de6-110">Значение</span><span class="sxs-lookup"><span data-stu-id="34de6-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34de6-111">Версия</span><span class="sxs-lookup"><span data-stu-id="34de6-111">Version</span></span><br/> | <span data-ttu-id="34de6-112">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="34de6-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="34de6-113">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34de6-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="34de6-114">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="34de6-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="34de6-115">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="34de6-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34de6-116">См. также</span><span class="sxs-lookup"><span data-stu-id="34de6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34de6-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="34de6-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




