---
description: Свойство ПАТЧНЕВСУММАРИКОММЕНТС обновляет свойство сводки комментариев административной установки при установке исправлений.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: ПАТЧНЕВСУММАРИКОММЕНТС, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe2bff9613fa5d39ae300e15c3ee816c5c6fce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651686"
---
# <a name="patchnewsummarycomments-property"></a><span data-ttu-id="55c3e-103">ПАТЧНЕВСУММАРИКОММЕНТС, свойство</span><span class="sxs-lookup"><span data-stu-id="55c3e-103">PATCHNEWSUMMARYCOMMENTS property</span></span>

<span data-ttu-id="55c3e-104">Свойство **патчневсуммарикомментс** обновляет свойство [**сводки комментариев**](comments-summary.md) административной установки при установке исправлений.</span><span class="sxs-lookup"><span data-stu-id="55c3e-104">The **PATCHNEWSUMMARYCOMMENTS** property updates the [**Comments Summary**](comments-summary.md) property of an administrative installation during patching.</span></span> <span data-ttu-id="55c3e-105">Это свойство задается только при преобразовании в MSP-файле.</span><span class="sxs-lookup"><span data-stu-id="55c3e-105">This property is only set by a transform in a .msp file.</span></span> <span data-ttu-id="55c3e-106">MSP-файл должен включать преобразование, которое добавляет это свойство в [таблицу свойств](property-table.md) и задает его значение.</span><span class="sxs-lookup"><span data-stu-id="55c3e-106">The .msp file must include a transform that adds this property to the [Property table](property-table.md) and sets its value.</span></span> <span data-ttu-id="55c3e-107">Затем программа установки записывает значение **патчневсуммарикомментс** в свойство [**сводки номера редакции**](revision-number-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="55c3e-107">The installer then writes the value of **PATCHNEWSUMMARYCOMMENTS** to the [**Revision Number Summary**](revision-number-summary.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="55c3e-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55c3e-108">Remarks</span></span>

<span data-ttu-id="55c3e-109">Свойства [**патчневпаккажекоде**](patchnewpackagecode.md), **патчневсуммарикомментс** и [**патчневсуммарисубжект**](patchnewsummarysubject.md) используются для обновления сводных данных при установке исправления в административный образ.</span><span class="sxs-lookup"><span data-stu-id="55c3e-109">The [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS**, and [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) properties are used to update the summary information when a patch is installed to an administrative image.</span></span>

## <a name="requirements"></a><span data-ttu-id="55c3e-110">Требования</span><span class="sxs-lookup"><span data-stu-id="55c3e-110">Requirements</span></span>



| <span data-ttu-id="55c3e-111">Требование</span><span class="sxs-lookup"><span data-stu-id="55c3e-111">Requirement</span></span> | <span data-ttu-id="55c3e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="55c3e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55c3e-113">Версия</span><span class="sxs-lookup"><span data-stu-id="55c3e-113">Version</span></span><br/> | <span data-ttu-id="55c3e-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="55c3e-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="55c3e-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="55c3e-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="55c3e-116">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="55c3e-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="55c3e-117">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="55c3e-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55c3e-118">См. также</span><span class="sxs-lookup"><span data-stu-id="55c3e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c3e-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="55c3e-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




