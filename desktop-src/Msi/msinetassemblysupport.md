---
description: Свойство Мсинетассемблисуппорт указывает, поддерживает ли компьютер общеязыковые сборки времени выполнения.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: Мсинетассемблисуппорт, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651777"
---
# <a name="msinetassemblysupport-property"></a><span data-ttu-id="bb220-103">Мсинетассемблисуппорт, свойство</span><span class="sxs-lookup"><span data-stu-id="bb220-103">MsiNetAssemblySupport property</span></span>

<span data-ttu-id="bb220-104">Свойство **мсинетассемблисуппорт** указывает, поддерживает ли компьютер общеязыковые сборки времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="bb220-104">The **MsiNetAssemblySupport** property indicates whether the computer supports common language run-time assemblies.</span></span> <span data-ttu-id="bb220-105">В системах, поддерживающих общеязыковые сборки времени выполнения, установщик устанавливает значение **мсинетассемблисуппорт** в качестве версии файла Fusion.dll.</span><span class="sxs-lookup"><span data-stu-id="bb220-105">On systems that support common language run-time assemblies, the installer sets the value of **MsiNetAssemblySupport** to the file version of Fusion.dll.</span></span> <span data-ttu-id="bb220-106">Установщик не устанавливает это свойство, если операционная система не поддерживает общеязыковые сборки времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="bb220-106">The installer does not set this property if the operating system does not support common language run-time assemblies.</span></span> <span data-ttu-id="bb220-107">Если несколько версий Fusion.dll установлены параллельно на компьютере пользователя, это свойство устанавливается в последнюю версию файла Fusion.dll.</span><span class="sxs-lookup"><span data-stu-id="bb220-107">When multiple versions of Fusion.dll are installed side-by-side on the user's computer, this property is set to the latest version of the Fusion.dll file.</span></span> <span data-ttu-id="bb220-108">Например, если платформа .NET Framework версии 1.0.3705 (Fusion.dll версии 1.0.3705.15) и платформа .NET Framework версии 1.1.4322 (Fusion.dll версии 1.1.4322.314) устанавливаются параллельно, свойство **мсинетассемблисуппорт** имеет значение 1.1.4322.314.</span><span class="sxs-lookup"><span data-stu-id="bb220-108">For example, if .NET Framework version 1.0.3705 (Fusion.dll version 1.0.3705.15)and .NET Framework version 1.1.4322 (Fusion.dll version 1.1.4322.314) are installed side-by-side, the **MsiNetAssemblySupport** property is set to 1.1.4322.314.</span></span> <span data-ttu-id="bb220-109">Дополнительные сведения см. в разделе [сборки](assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="bb220-109">For more information, see [Assemblies](assemblies.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb220-110">Требования</span><span class="sxs-lookup"><span data-stu-id="bb220-110">Requirements</span></span>



| <span data-ttu-id="bb220-111">Требование</span><span class="sxs-lookup"><span data-stu-id="bb220-111">Requirement</span></span> | <span data-ttu-id="bb220-112">Значение</span><span class="sxs-lookup"><span data-stu-id="bb220-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb220-113">Версия</span><span class="sxs-lookup"><span data-stu-id="bb220-113">Version</span></span><br/> | <span data-ttu-id="bb220-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bb220-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bb220-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bb220-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bb220-116">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb220-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bb220-117">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="bb220-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb220-118">См. также</span><span class="sxs-lookup"><span data-stu-id="bb220-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb220-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb220-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




