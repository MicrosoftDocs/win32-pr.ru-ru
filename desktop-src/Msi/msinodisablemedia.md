---
description: Установите свойство МСИНОДИСАБЛЕМЕДИА, чтобы программа установки не заблокировала значение свойства ДИСАБЛЕМЕДИА. Если задать свойство ДИСАБЛЕМЕДИА, установщик не сможет зарегистрировать какой-либо источник мультимедиа, например компакт-диск, в качестве допустимого источника для продукта.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: МСИНОДИСАБЛЕМЕДИА, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652056"
---
# <a name="msinodisablemedia-property"></a><span data-ttu-id="3258d-104">МСИНОДИСАБЛЕМЕДИА, свойство</span><span class="sxs-lookup"><span data-stu-id="3258d-104">MSINODISABLEMEDIA property</span></span>

<span data-ttu-id="3258d-105">Установите свойство **мсинодисаблемедиа** , чтобы программа установки не заблокировала значение свойства [**дисаблемедиа**](-disablemedia.md) .</span><span class="sxs-lookup"><span data-stu-id="3258d-105">Set the **MSINODISABLEMEDIA** property to prevent the installer from setting the [**DISABLEMEDIA**](-disablemedia.md) property.</span></span> <span data-ttu-id="3258d-106">Если задать свойство **дисаблемедиа** , установщик не сможет зарегистрировать какой-либо источник мультимедиа, например компакт-диск, в качестве допустимого источника для продукта.</span><span class="sxs-lookup"><span data-stu-id="3258d-106">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span>

<span data-ttu-id="3258d-107">Если **мсинодисаблемедиа** не задан, установщик может добавить [**дисаблемедиа**](-disablemedia.md) в поток свойств администрирования при выполнении [административной установки](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="3258d-107">When **MSINODISABLEMEDIA** is not set, the installer might add [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream when performing an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="3258d-108">Это предотвращает установку пользователями из административного образа с носителя, например с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="3258d-108">This prevents users who install from the administrative image from ever installing from media, such as a CD-ROM.</span></span>

-   <span data-ttu-id="3258d-109">При выполнении административной установки установщик добавляет [**дисаблемедиа**](-disablemedia.md) в поток свойств администрирования только в том случае, если свойство [**сводки количества страниц**](page-count-summary.md) меньше 150.</span><span class="sxs-lookup"><span data-stu-id="3258d-109">When performing an administrative installation, the installer only adds [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream if the [**Page Count Summary**](page-count-summary.md) Property is less than 150.</span></span>

<span data-ttu-id="3258d-110">Если [**дисаблемедиа**](-disablemedia.md) указан в свойстве [**Админпропертиес**](adminproperties.md) , установка **мсинодисаблемедиа** предотвращает установку **дисаблемедиа** во время административной установки.</span><span class="sxs-lookup"><span data-stu-id="3258d-110">If [**DISABLEMEDIA**](-disablemedia.md) is listed in the [**AdminProperties**](adminproperties.md) property, setting **MSINODISABLEMEDIA** prevents **DISABLEMEDIA** from being set during an administrative installation.</span></span> <span data-ttu-id="3258d-111">В этом случае установщик может зарегистрировать источник мультимедиа, и пользователь может выполнить переустановку из источника носителя, если исходный образ административной установки стал недоступным позже.</span><span class="sxs-lookup"><span data-stu-id="3258d-111">In this case, the installer may register a media source and a user could then have the option to reinstall from the media source if the original administrative installation image became unavailable later.</span></span>

## <a name="requirements"></a><span data-ttu-id="3258d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3258d-112">Requirements</span></span>



| <span data-ttu-id="3258d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="3258d-113">Requirement</span></span> | <span data-ttu-id="3258d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3258d-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3258d-115">Версия</span><span class="sxs-lookup"><span data-stu-id="3258d-115">Version</span></span><br/> | <span data-ttu-id="3258d-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3258d-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3258d-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3258d-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3258d-118">Установщик Windows в Windows Server 2003, Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3258d-118">Windows Installer on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="3258d-119">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3258d-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3258d-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3258d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3258d-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="3258d-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




