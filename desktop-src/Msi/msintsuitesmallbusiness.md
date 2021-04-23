---
description: В операционных системах Windows 2000 и более поздних версий установщик устанавливает для свойства Мсинтсуитесмаллбусинесс значение 1, если установлен Microsoft Small Business Server.
ms.assetid: 9ac578b9-316f-413c-aae0-4f414109583b
title: Мсинтсуитесмаллбусинесс, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8b1e523ff038e4639cb0f92762c3914bbf5f6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665462"
---
# <a name="msintsuitesmallbusiness-property"></a><span data-ttu-id="29b5d-103">Мсинтсуитесмаллбусинесс, свойство</span><span class="sxs-lookup"><span data-stu-id="29b5d-103">MsiNTSuiteSmallBusiness property</span></span>

<span data-ttu-id="29b5d-104">В операционных системах Windows 2000 и более поздних версий установщик устанавливает для свойства **мсинтсуитесмаллбусинесс** значение 1, если установлен Microsoft Small Business Server.</span><span class="sxs-lookup"><span data-stu-id="29b5d-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteSmallBusiness** property to 1 if Microsoft Small Business Server is installed.</span></span> <span data-ttu-id="29b5d-105">Установщик задает для этого свойства значение 1, только если в \_ \_ структуре [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) установлен флаг смаллбусинесс набора ver Suite.</span><span class="sxs-lookup"><span data-stu-id="29b5d-105">The installer sets this property to 1 only if the VER\_SUITE\_SMALLBUSINESS flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="29b5d-106">В противном случае установщик не устанавливает это свойство.</span><span class="sxs-lookup"><span data-stu-id="29b5d-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="29b5d-107">Требования</span><span class="sxs-lookup"><span data-stu-id="29b5d-107">Requirements</span></span>



| <span data-ttu-id="29b5d-108">Требование</span><span class="sxs-lookup"><span data-stu-id="29b5d-108">Requirement</span></span> | <span data-ttu-id="29b5d-109">Значение</span><span class="sxs-lookup"><span data-stu-id="29b5d-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29b5d-110">Версия</span><span class="sxs-lookup"><span data-stu-id="29b5d-110">Version</span></span><br/> | <span data-ttu-id="29b5d-111">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="29b5d-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="29b5d-112">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="29b5d-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="29b5d-113">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29b5d-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="29b5d-114">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="29b5d-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29b5d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="29b5d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29b5d-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="29b5d-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
