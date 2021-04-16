---
description: В операционных системах Windows 2000 и более поздних версий установщик устанавливает для свойства Мсинтсуитебаккоффице значение 1, если установлены компоненты Microsoft BackOffice.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: Мсинтсуитебаккоффице, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2d9f2f1d95446c32b4f2addf520f3d5b4dadc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652188"
---
# <a name="msintsuitebackoffice-property"></a><span data-ttu-id="a2951-103">Мсинтсуитебаккоффице, свойство</span><span class="sxs-lookup"><span data-stu-id="a2951-103">MsiNTSuiteBackOffice property</span></span>

<span data-ttu-id="a2951-104">В операционных системах Windows 2000 и более поздних версий установщик устанавливает для свойства **мсинтсуитебаккоффице** значение 1, если установлены компоненты Microsoft BackOffice.</span><span class="sxs-lookup"><span data-stu-id="a2951-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteBackOffice** property to 1 if Microsoft BackOffice components are installed.</span></span> <span data-ttu-id="a2951-105">Установщик задает для этого свойства значение 1, только если в \_ \_ структуре [**ОСВЕРСИОНИНФОЕКС**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) задан флаг BackOffice Suite.</span><span class="sxs-lookup"><span data-stu-id="a2951-105">The installer sets this property to 1 only if the VER\_SUITE\_BACKOFFICE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="a2951-106">В противном случае установщик не устанавливает это свойство.</span><span class="sxs-lookup"><span data-stu-id="a2951-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2951-107">Требования</span><span class="sxs-lookup"><span data-stu-id="a2951-107">Requirements</span></span>



| <span data-ttu-id="a2951-108">Требование</span><span class="sxs-lookup"><span data-stu-id="a2951-108">Requirement</span></span> | <span data-ttu-id="a2951-109">Значение</span><span class="sxs-lookup"><span data-stu-id="a2951-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2951-110">Версия</span><span class="sxs-lookup"><span data-stu-id="a2951-110">Version</span></span><br/> | <span data-ttu-id="a2951-111">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a2951-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a2951-112">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a2951-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a2951-113">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a2951-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a2951-114">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a2951-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2951-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a2951-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2951-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="a2951-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
