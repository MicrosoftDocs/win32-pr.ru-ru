---
description: В операционных системах Windows XP и более поздних версий установщик устанавливает для свойства Мсинтсуитеперсонал значение 1, если операционная система является Windows XP Home Edition.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: Мсинтсуитеперсонал, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8932cf2d2c9c5079d6955571512cbc9836e41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651826"
---
# <a name="msintsuitepersonal-property"></a><span data-ttu-id="d00ea-103">Мсинтсуитеперсонал, свойство</span><span class="sxs-lookup"><span data-stu-id="d00ea-103">MsiNTSuitePersonal property</span></span>

<span data-ttu-id="d00ea-104">В операционных системах Windows XP и более поздних версий установщик устанавливает для свойства **мсинтсуитеперсонал** значение 1, если операционная система является Windows XP Home Edition.</span><span class="sxs-lookup"><span data-stu-id="d00ea-104">On Windows XP and later operating systems, the installer sets the **MsiNTSuitePersonal** property to 1 if the operating system is Windows XP Home Edition.</span></span> <span data-ttu-id="d00ea-105">Установщик задает для этого свойства значение 1 только в том случае, если в \_ \_ структуре [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) ЗАДАН флаг Personal набора ver.</span><span class="sxs-lookup"><span data-stu-id="d00ea-105">The installer sets this property to 1 only if the VER\_SUITE\_PERSONAL flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="d00ea-106">В противном случае установщик не устанавливает это свойство.</span><span class="sxs-lookup"><span data-stu-id="d00ea-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d00ea-107">Требования</span><span class="sxs-lookup"><span data-stu-id="d00ea-107">Requirements</span></span>



| <span data-ttu-id="d00ea-108">Требование</span><span class="sxs-lookup"><span data-stu-id="d00ea-108">Requirement</span></span> | <span data-ttu-id="d00ea-109">Значение</span><span class="sxs-lookup"><span data-stu-id="d00ea-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d00ea-110">Версия</span><span class="sxs-lookup"><span data-stu-id="d00ea-110">Version</span></span><br/> | <span data-ttu-id="d00ea-111">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d00ea-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d00ea-112">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d00ea-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d00ea-113">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d00ea-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d00ea-114">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d00ea-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d00ea-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d00ea-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00ea-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="d00ea-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
