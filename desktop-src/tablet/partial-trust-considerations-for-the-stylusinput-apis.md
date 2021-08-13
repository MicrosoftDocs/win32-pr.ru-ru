---
description: Общие сведения о проблемах с частичным доверием и интерфейсе прикладного программирования (API) Стилусинпут.
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Рекомендации по частичному доверию для API Стилусинпут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 596e8b50692ae09e9fbaf73f9254afbec8f29d6481a2dc3e27727beb27546441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449354"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>Рекомендации по частичному доверию для API Стилусинпут

Объект [**RealTimeStylus**](realtimestylus-class.md) , принимающий параметр *Handle* , требует разрешений [UIPermissionWindow. аллвиндовс](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) и [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) в дополнение к разрешениям, необходимым конструктору, принимающему параметр *аттачедконтрол* .

Дополнительные сведения о проблемах безопасности и доверия см. в разделе [безопасность и доверие](security-and-trust.md).

 

 
