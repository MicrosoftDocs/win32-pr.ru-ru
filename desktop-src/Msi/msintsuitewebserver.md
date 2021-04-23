---
description: В операционных системах Windows 2000 и более поздних версий установщик устанавливает для свойства Мсинтсуитевебсервер значение 1, если установщик работает в выпуске Windows Server 2003 на веб-сайте.
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: Мсинтсуитевебсервер, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082e3ae7f107bf3499f5a48473d53ebb530138a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665461"
---
# <a name="msintsuitewebserver-property"></a><span data-ttu-id="e5f79-103">Мсинтсуитевебсервер, свойство</span><span class="sxs-lookup"><span data-stu-id="e5f79-103">MsiNTSuiteWebServer property</span></span>

<span data-ttu-id="e5f79-104">В операционных системах Windows 2000 и более поздних версий установщик устанавливает для свойства **мсинтсуитевебсервер** значение 1, если установщик работает в выпуске windows Server 2003 на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="e5f79-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteWebServer** property to 1 if the installer is running on a web edition of the Windows Server 2003.</span></span> <span data-ttu-id="e5f79-105">Установщик задает для этого свойства значение 1, только если в \_ \_ структуре [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) установлен флаг колонки ver Suite.</span><span class="sxs-lookup"><span data-stu-id="e5f79-105">The installer sets this property to 1 only if the VER\_SUITE\_BLADE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="e5f79-106">В противном случае установщик не устанавливает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e5f79-106">Otherwise the installer does not set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5f79-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5f79-107">Remarks</span></span>

<span data-ttu-id="e5f79-108">Это свойство доступно только в выпуске установщика Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e5f79-108">This property is available only with the Windows Server 2003 release of the installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5f79-109">Требования</span><span class="sxs-lookup"><span data-stu-id="e5f79-109">Requirements</span></span>



| <span data-ttu-id="e5f79-110">Требование</span><span class="sxs-lookup"><span data-stu-id="e5f79-110">Requirement</span></span> | <span data-ttu-id="e5f79-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e5f79-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5f79-112">Версия</span><span class="sxs-lookup"><span data-stu-id="e5f79-112">Version</span></span><br/> | <span data-ttu-id="e5f79-113">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e5f79-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e5f79-114">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e5f79-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e5f79-115">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e5f79-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e5f79-116">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e5f79-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5f79-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e5f79-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5f79-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5f79-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="e5f79-119">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="e5f79-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 
