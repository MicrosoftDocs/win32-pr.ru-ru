---
description: При работе на процессоре Intel свойство Intel устанавливается установщик Windows на числовой уровень процессора.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Intel, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688994"
---
# <a name="intel-property"></a><span data-ttu-id="55f84-103">Intel, свойство</span><span class="sxs-lookup"><span data-stu-id="55f84-103">Intel property</span></span>

<span data-ttu-id="55f84-104">При работе на процессоре Intel свойство **Intel** устанавливается установщик Windows на числовой уровень процессора.</span><span class="sxs-lookup"><span data-stu-id="55f84-104">The **Intel** property is set by the Windows Installer to the numeric processor level when running on an Intel processor.</span></span> <span data-ttu-id="55f84-105">Значения совпадают с полями *впроцессорлевел* в структуре [**системных \_ сведений**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="55f84-105">The values are the same as the *wProcessorLevel* field of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span> <span data-ttu-id="55f84-106">При работе на процессоре x64 установщик Windows устанавливает свойство **Intel** в соответствии с процессором x86, который эмулируется операционной системой компьютера x64.</span><span class="sxs-lookup"><span data-stu-id="55f84-106">When running on a x64 processor, the Windows Installer sets the **Intel** property to reflect the x86 processor emulated by the x64 computer as reported by the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="55f84-107">Требования</span><span class="sxs-lookup"><span data-stu-id="55f84-107">Requirements</span></span>



| <span data-ttu-id="55f84-108">Требование</span><span class="sxs-lookup"><span data-stu-id="55f84-108">Requirement</span></span> | <span data-ttu-id="55f84-109">Значение</span><span class="sxs-lookup"><span data-stu-id="55f84-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55f84-110">Версия</span><span class="sxs-lookup"><span data-stu-id="55f84-110">Version</span></span><br/> | <span data-ttu-id="55f84-111">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="55f84-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="55f84-112">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="55f84-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="55f84-113">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="55f84-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="55f84-114">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="55f84-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55f84-115">См. также</span><span class="sxs-lookup"><span data-stu-id="55f84-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f84-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="55f84-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
