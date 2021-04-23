---
description: Если задать свойство ДИСАБЛЕМЕДИА, установщик не сможет зарегистрировать какой-либо источник мультимедиа, например компакт-диск, в качестве допустимого источника для продукта. Тем не менее, если обзор включен, пользователь может перейти к источнику мультимедиа.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: ДИСАБЛЕМЕДИА, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665546"
---
# <a name="disablemedia-property"></a><span data-ttu-id="b6b96-104">ДИСАБЛЕМЕДИА, свойство</span><span class="sxs-lookup"><span data-stu-id="b6b96-104">DISABLEMEDIA property</span></span>

<span data-ttu-id="b6b96-105">Если задать свойство [**дисаблемедиа**](disablemedia.md) , установщик не сможет зарегистрировать какой-либо источник мультимедиа, например компакт-диск, в качестве допустимого источника для продукта.</span><span class="sxs-lookup"><span data-stu-id="b6b96-105">Setting the [**DISABLEMEDIA**](disablemedia.md) property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="b6b96-106">Тем не менее, если обзор включен, пользователь может перейти к источнику мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b6b96-106">If browsing is enabled, however, a user may still browse to a media source.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6b96-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6b96-107">Remarks</span></span>

<span data-ttu-id="b6b96-108">Обратите внимание, что свойство [**дисаблемедиа**](disablemedia.md) отличается от результата задания политики дисаблемедиа.</span><span class="sxs-lookup"><span data-stu-id="b6b96-108">Note that the [**DISABLEMEDIA**](disablemedia.md) property has a different effect than setting the DisableMedia policy.</span></span> <span data-ttu-id="b6b96-109">Параметр **дисаблемедиа** предотвращает регистрацию источника мультимедиа, и это также предотвращает установку приложения в первый раз из источников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b6b96-109">Setting **DISABLEMEDIA** prevents the registration of any media source, and this also prevents the first time installation of an application from a media sources.</span></span>

<span data-ttu-id="b6b96-110">Дополнительные сведения о защите источников мультимедиа [*управляемого приложения*](m-gly.md) от пользователей, не являющихся администраторами, см. в разделе [устойчивость источника](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="b6b96-110">For details about securing the media sources of [*managed application*](m-gly.md) against browsing and installation by non-administrative users, see [Source Resiliency](source-resiliency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6b96-111">Требования</span><span class="sxs-lookup"><span data-stu-id="b6b96-111">Requirements</span></span>



| <span data-ttu-id="b6b96-112">Требование</span><span class="sxs-lookup"><span data-stu-id="b6b96-112">Requirement</span></span> | <span data-ttu-id="b6b96-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b6b96-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b96-114">Версия</span><span class="sxs-lookup"><span data-stu-id="b6b96-114">Version</span></span><br/> | <span data-ttu-id="b6b96-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b6b96-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b6b96-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b6b96-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b6b96-117">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b6b96-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b6b96-118">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b6b96-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6b96-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b6b96-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b96-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="b6b96-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




