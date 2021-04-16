---
description: Установщик задает для свойства Мситаблетпк ненулевое значение, если текущей операционной системой является Windows XP Tablet PC Edition.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Мситаблетпк, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679612"
---
# <a name="msitabletpc-property"></a><span data-ttu-id="ed2c8-103">Мситаблетпк, свойство</span><span class="sxs-lookup"><span data-stu-id="ed2c8-103">MsiTabletPC property</span></span>

<span data-ttu-id="ed2c8-104">Установщик задает для свойства **мситаблетпк** ненулевое значение, если текущей операционной системой является Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="ed2c8-104">The installer sets the **MsiTabletPC** property to a nonzero value if the current operating system is Windows XP Tablet PC Edition.</span></span> <span data-ttu-id="ed2c8-105">Установщик использует функцию [**жетсистемметрикс**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) с **SM \_ TABLETPC**, а свойство получает ненулевое значение, возвращаемое этой функцией.</span><span class="sxs-lookup"><span data-stu-id="ed2c8-105">The installer uses the [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function with **SM\_TABLETPC**, and the property receives the nonzero value returned by this function.</span></span> <span data-ttu-id="ed2c8-106">Если текущая система не является Windows XP Tablet PC Edition, функция **жетсистемметрикс** возвращает нуль, а установщик не устанавливает это свойство.</span><span class="sxs-lookup"><span data-stu-id="ed2c8-106">If the current system is not Windows XP Tablet PC Edition, the **GetSystemMetrics** function returns zero and the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed2c8-107">Требования</span><span class="sxs-lookup"><span data-stu-id="ed2c8-107">Requirements</span></span>



| <span data-ttu-id="ed2c8-108">Требование</span><span class="sxs-lookup"><span data-stu-id="ed2c8-108">Requirement</span></span> | <span data-ttu-id="ed2c8-109">Значение</span><span class="sxs-lookup"><span data-stu-id="ed2c8-109">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed2c8-110">Версия</span><span class="sxs-lookup"><span data-stu-id="ed2c8-110">Version</span></span><br/> | <span data-ttu-id="ed2c8-111">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ed2c8-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ed2c8-112">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed2c8-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ed2c8-113">Установщик Windows 4,5 в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed2c8-113">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ed2c8-114">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ed2c8-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed2c8-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ed2c8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed2c8-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed2c8-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ed2c8-117">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="ed2c8-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
