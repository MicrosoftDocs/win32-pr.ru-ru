---
description: Установщик задает свойство Редиректеддллсуппорт, если системная платформа, выполняющая установку, поддерживает изолированные компоненты.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Редиректеддллсуппорт, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed308eaf022ada5c6c8697ba47f55605f1fecbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668633"
---
# <a name="redirecteddllsupport-property"></a><span data-ttu-id="1cf02-103">Редиректеддллсуппорт, свойство</span><span class="sxs-lookup"><span data-stu-id="1cf02-103">RedirectedDLLSupport property</span></span>

<span data-ttu-id="1cf02-104">Установщик задает свойство **редиректеддллсуппорт** , если системная платформа, выполняющая установку, поддерживает [изолированные компоненты](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="1cf02-104">The installer sets the **RedirectedDLLSupport** property if the system platform performing the installation supports [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="1cf02-105">Установщик задает для свойства **редиректеддллсуппорт** значение 1, если система, в которой выполняется установка, поддерживает [изолированные компоненты](isolated-components.md) на основе. ЛОКАЛЬНЫЕ файлы.</span><span class="sxs-lookup"><span data-stu-id="1cf02-105">The installer sets the **RedirectedDLLSupport** property to a value of 1 if the system performing the installation supports [Isolated Components](isolated-components.md) based on .LOCAL files.</span></span> <span data-ttu-id="1cf02-106">Установщик задает для свойства **редиректеддллсуппорт** значение 2, если система, выполняющая установку, поддерживает изоляцию с помощью любой из них. ЛОКАЛЬНЫЕ файлы или параллельные сборки Win32.</span><span class="sxs-lookup"><span data-stu-id="1cf02-106">The installer sets the **RedirectedDLLSupport** property to a value of 2 if the system that performs the installation supports isolation using either .LOCAL files or Win32 side-by-side assemblies.</span></span>

<span data-ttu-id="1cf02-107">Свойство **редиректеддллсуппорт** можно использовать для условия [действия Исолатекомпонентс](isolatecomponents-action.md) в таблице [инсталлуисекуенце](installuisequence-table.md) или [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1cf02-107">The **RedirectedDLLSupport** property can be used to condition the [IsolateComponents action](isolatecomponents-action.md) in the [InstallUISequence table](installuisequence-table.md) or [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cf02-108">Требования</span><span class="sxs-lookup"><span data-stu-id="1cf02-108">Requirements</span></span>



| <span data-ttu-id="1cf02-109">Требование</span><span class="sxs-lookup"><span data-stu-id="1cf02-109">Requirement</span></span> | <span data-ttu-id="1cf02-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1cf02-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf02-111">Версия</span><span class="sxs-lookup"><span data-stu-id="1cf02-111">Version</span></span><br/> | <span data-ttu-id="1cf02-112">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1cf02-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1cf02-113">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1cf02-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1cf02-114">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1cf02-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1cf02-115">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="1cf02-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1cf02-116">См. также</span><span class="sxs-lookup"><span data-stu-id="1cf02-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf02-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="1cf02-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




