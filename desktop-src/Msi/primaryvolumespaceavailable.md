---
description: Установщик устанавливает значение свойства Примариволумеспацеаваилабле в строку, представляющую общее количество байт, доступных в единицах измерения 512, на томе, на который ссылается свойство Примариволумепас.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Примариволумеспацеаваилабле, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651873"
---
# <a name="primaryvolumespaceavailable-property"></a><span data-ttu-id="d4515-103">Примариволумеспацеаваилабле, свойство</span><span class="sxs-lookup"><span data-stu-id="d4515-103">PrimaryVolumeSpaceAvailable property</span></span>

<span data-ttu-id="d4515-104">Установщик устанавливает значение свойства **примариволумеспацеаваилабле** в строку, представляющую общее количество байт, доступных в единицах измерения 512, на томе, на который ссылается свойство [**примариволумепас**](primaryvolumepath.md) .</span><span class="sxs-lookup"><span data-stu-id="d4515-104">The installer sets the value of the **PrimaryVolumeSpaceAvailable** property to a string that represents the total number of bytes available, in units of 512, on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4515-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4515-105">Remarks</span></span>

<span data-ttu-id="d4515-106">Например, если для [**примариволумепас**](primaryvolumepath.md) задано значение "D:", а для тома D: доступно 446 134 272 байт, **примариволумеспацеаваилабле** имеет значение 871356.</span><span class="sxs-lookup"><span data-stu-id="d4515-106">For example, if [**PrimaryVolumePath**](primaryvolumepath.md) is set to "D:", and volume D: has 446,134,272 bytes free, **PrimaryVolumeSpaceAvailable** is set to 871356.</span></span>

<span data-ttu-id="d4515-107">Примечание. Если это значение должно отображаться в статическом [элементе управления "текст](text-control.md)", бит [форматсизе](formatsize-control-attribute.md) можно использовать для автоматического форматирования и пометки этого числа в килобайтах или мегабайтах соответственно.</span><span class="sxs-lookup"><span data-stu-id="d4515-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4515-108">Требования</span><span class="sxs-lookup"><span data-stu-id="d4515-108">Requirements</span></span>



| <span data-ttu-id="d4515-109">Требование</span><span class="sxs-lookup"><span data-stu-id="d4515-109">Requirement</span></span> | <span data-ttu-id="d4515-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d4515-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4515-111">Версия</span><span class="sxs-lookup"><span data-stu-id="d4515-111">Version</span></span><br/> | <span data-ttu-id="d4515-112">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d4515-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d4515-113">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d4515-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d4515-114">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d4515-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d4515-115">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d4515-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4515-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d4515-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4515-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="d4515-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




