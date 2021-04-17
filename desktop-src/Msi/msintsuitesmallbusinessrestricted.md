---
description: В операционных системах Windows 2000 и более поздних версий установщик устанавливает для свойства Мсинтсуитесмаллбусинессрестриктед значение 1, если Microsoft Small Business Server устанавливается с ограниченным клиентской лицензией принудительно.
ms.assetid: a7100df4-6fe4-4159-ba94-9b5bd1803107
title: Мсинтсуитесмаллбусинессрестриктед, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d85fa7fe83c0c8c7cd40788453d1078e7a6b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651824"
---
# <a name="msintsuitesmallbusinessrestricted-property"></a><span data-ttu-id="ed342-103">Мсинтсуитесмаллбусинессрестриктед, свойство</span><span class="sxs-lookup"><span data-stu-id="ed342-103">MsiNTSuiteSmallBusinessRestricted property</span></span>

<span data-ttu-id="ed342-104">В операционных системах Windows 2000 и более поздних версий установщик устанавливает для свойства **мсинтсуитесмаллбусинессрестриктед** значение 1, если Microsoft Small Business Server устанавливается с ограниченным клиентской лицензией принудительно.</span><span class="sxs-lookup"><span data-stu-id="ed342-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteSmallBusinessRestricted** property to 1 if Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="ed342-105">Установщик задает для этого свойства значение 1, только если в \_ \_ \_ структуре [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) установлен флаг смаллбусинесс Suite Restricted.</span><span class="sxs-lookup"><span data-stu-id="ed342-105">The installer sets this property to 1 only if the VER\_SUITE\_SMALLBUSINESS\_RESTRICTED flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="ed342-106">В противном случае установщик не устанавливает это свойство.</span><span class="sxs-lookup"><span data-stu-id="ed342-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed342-107">Требования</span><span class="sxs-lookup"><span data-stu-id="ed342-107">Requirements</span></span>



| <span data-ttu-id="ed342-108">Требование</span><span class="sxs-lookup"><span data-stu-id="ed342-108">Requirement</span></span> | <span data-ttu-id="ed342-109">Значение</span><span class="sxs-lookup"><span data-stu-id="ed342-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed342-110">Версия</span><span class="sxs-lookup"><span data-stu-id="ed342-110">Version</span></span><br/> | <span data-ttu-id="ed342-111">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ed342-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ed342-112">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed342-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ed342-113">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed342-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ed342-114">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ed342-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed342-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ed342-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed342-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed342-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
