---
description: 'Если установочный пакет, поставляемый с приложением, не находится в корне компакт-диска, который клиенты получают, свойство МЕДИАПАККАЖЕПАС должно быть установлено в командной строке относительно пути к приложению на компакт-диске. Например, если путь к пакету на носителе равен E: \\ MyPath \\My.msi, используйте медиапаккажепас =&\# 0034; \\ MyPath \\ & \# 0034;. Администраторы могут создавать CD-ROMs из точки административной установки. Если расположение корня установки изменено на новых компакт-дисках, свойству МЕДИАПАККАЖЕПАС необходимо присвоить новый путь для установки с этого носителя. Источник с расположением на компакт-диске, отличающимся от указанного в пакете, непригоден для использования. Однако нет необходимости использовать это свойство при создании точки административной установки из носителя для доставки.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: МЕДИАПАККАЖЕПАС, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675803"
---
# <a name="mediapackagepath-property"></a><span data-ttu-id="b6023-106">МЕДИАПАККАЖЕПАС, свойство</span><span class="sxs-lookup"><span data-stu-id="b6023-106">MEDIAPACKAGEPATH property</span></span>

<span data-ttu-id="b6023-107">Если установочный пакет, поставляемый с приложением, не находится в корне компакт-диска, который клиенты получают, свойство **медиапаккажепас** должно быть установлено в командной строке относительно пути к приложению на компакт-диске.</span><span class="sxs-lookup"><span data-stu-id="b6023-107">If the installation package shipping with an application is not at the root of the CD-ROM that customers receive, the **MEDIAPACKAGEPATH** property must be set on the command line to the relative path of the application on the CD-ROM.</span></span>

<span data-ttu-id="b6023-108">Например, если путь к пакету на носителе равен E: \\ MyPath \\My.msi, используйте медиапаккажепас = " \\ MyPath \\ ".</span><span class="sxs-lookup"><span data-stu-id="b6023-108">For example, if the path to the package on the media is E:\\MyPath\\My.msi, then use MEDIAPACKAGEPATH="\\MyPath\\".</span></span>

<span data-ttu-id="b6023-109">Администраторы могут создавать CD-ROMs из точки административной установки.</span><span class="sxs-lookup"><span data-stu-id="b6023-109">Administrators may create CD-ROMs from an administrative installation point.</span></span> <span data-ttu-id="b6023-110">Если расположение корня установки изменено на новых компакт-дисках, свойству **медиапаккажепас** необходимо присвоить новый путь для установки с этого носителя.</span><span class="sxs-lookup"><span data-stu-id="b6023-110">If the location of the root of the installation is changed on the new CD-ROMs, the **MEDIAPACKAGEPATH** property must be set to the new path to install from this media.</span></span> <span data-ttu-id="b6023-111">Источник с расположением на компакт-диске, отличающимся от указанного в пакете, непригоден для использования.</span><span class="sxs-lookup"><span data-stu-id="b6023-111">A source with a location on the CD-ROM different than what is specified in the package is unusable.</span></span> <span data-ttu-id="b6023-112">Однако нет необходимости использовать это свойство при создании точки административной установки из носителя для доставки.</span><span class="sxs-lookup"><span data-stu-id="b6023-112">It is not necessary, however, to use this property when creating an administrative installation point from shipping media.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6023-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b6023-113">Requirements</span></span>



| <span data-ttu-id="b6023-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b6023-114">Requirement</span></span> | <span data-ttu-id="b6023-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b6023-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6023-116">Версия</span><span class="sxs-lookup"><span data-stu-id="b6023-116">Version</span></span><br/> | <span data-ttu-id="b6023-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b6023-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b6023-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b6023-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b6023-119">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b6023-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b6023-120">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b6023-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6023-121">См. также</span><span class="sxs-lookup"><span data-stu-id="b6023-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6023-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="b6023-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




