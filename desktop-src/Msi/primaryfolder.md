---
description: ПРИМАРИФОЛДЕР — это глобальное свойство, позволяющее автору назначить первичную папку для установки.
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: ПРИМАРИФОЛДЕР, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651735"
---
# <a name="primaryfolder-property"></a><span data-ttu-id="79257-103">ПРИМАРИФОЛДЕР, свойство</span><span class="sxs-lookup"><span data-stu-id="79257-103">PRIMARYFOLDER property</span></span>

<span data-ttu-id="79257-104">**Примарифолдер** — это глобальное свойство, позволяющее автору назначить первичную папку для установки.</span><span class="sxs-lookup"><span data-stu-id="79257-104">The **PRIMARYFOLDER** is a global property that allows the author to designate a primary folder for the installation.</span></span> <span data-ttu-id="79257-105">Значение этого свойства должно быть именем ключа каталога, который существует в [таблице Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="79257-105">The value for this property must be the key name of a directory that exists in the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="79257-106">Установщик использует разрешенный путь к первичной папке, чтобы определить, какой том следует использовать при задании значений свойства [**примариволумепас**](primaryvolumepath.md) , свойства [**Примариволумеспацеаваилабле**](primaryvolumespaceavailable.md) , свойства [**примариволумеспацерекуиред**](primaryvolumespacerequired.md) и свойства [**примариволумеспацеремаининг**](primaryvolumespaceremaining.md) .</span><span class="sxs-lookup"><span data-stu-id="79257-106">The installer uses the resolved path of the primary folder to determine which volume to use when setting the values of the [**PrimaryVolumePath**](primaryvolumepath.md) property, [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) property, and [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) property.</span></span> <span data-ttu-id="79257-107">Установщик предоставляет значения этих свойств для пользователей в пользовательском интерфейсе, помогая им управлять дисковым пространством.</span><span class="sxs-lookup"><span data-stu-id="79257-107">The installer provides the values of these latter properties to users in the user interface to help them manage disk space.</span></span> <span data-ttu-id="79257-108">Обычно Авторы пакетов могут выбрать самую крупную папку в качестве основной папки.</span><span class="sxs-lookup"><span data-stu-id="79257-108">Commonly package authors can select the largest folder as the primary folder.</span></span>

<span data-ttu-id="79257-109">Значение этого свойства должно быть именем ключа записи каталога, найденной в [таблице Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="79257-109">The value for this property must be the key name of a directory record found in the [Directory table](directory-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79257-110">Требования</span><span class="sxs-lookup"><span data-stu-id="79257-110">Requirements</span></span>



| <span data-ttu-id="79257-111">Требование</span><span class="sxs-lookup"><span data-stu-id="79257-111">Requirement</span></span> | <span data-ttu-id="79257-112">Значение</span><span class="sxs-lookup"><span data-stu-id="79257-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79257-113">Версия</span><span class="sxs-lookup"><span data-stu-id="79257-113">Version</span></span><br/> | <span data-ttu-id="79257-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="79257-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="79257-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="79257-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="79257-116">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="79257-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="79257-117">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="79257-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79257-118">См. также</span><span class="sxs-lookup"><span data-stu-id="79257-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79257-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="79257-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




