---
description: Общие сведения о проблемах с частичным доверием и интерфейсе прикладного программирования (API) Стилусинпут.
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Рекомендации по частичному доверию для API Стилусинпут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceda5edfb2e4133bb0fcb3d260ff1e13f9fdb521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265682"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a><span data-ttu-id="47129-103">Рекомендации по частичному доверию для API Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="47129-103">Partial Trust Considerations for the StylusInput API</span></span>

<span data-ttu-id="47129-104">Объект [**RealTimeStylus**](realtimestylus-class.md) , принимающий параметр *Handle* , требует разрешений [UIPermissionWindow. аллвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) и [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) в дополнение к разрешениям, необходимым конструктору, принимающему параметр *аттачедконтрол* .</span><span class="sxs-lookup"><span data-stu-id="47129-104">The [**RealTimeStylus**](realtimestylus-class.md) that takes the *handle* parameter requires the [UIPermissionWindow.AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) and [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/) permissions, in addition to the permissions required by the constructor that takes the *attachedControl* parameter.</span></span>

<span data-ttu-id="47129-105">Дополнительные сведения о проблемах безопасности и доверия см. в разделе [безопасность и доверие](security-and-trust.md).</span><span class="sxs-lookup"><span data-stu-id="47129-105">For more information about security and trust issues, see [Security and Trust](security-and-trust.md).</span></span>

 

 
