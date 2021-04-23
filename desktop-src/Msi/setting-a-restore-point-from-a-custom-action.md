---
description: Настраиваемые действия не должны вызывать функцию Срсетресторепоинт, так как это может привести к тому, что точка входа восстановления записывается в середину установщик Windows установки.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Настройка точки восстановления из настраиваемого действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8539c436dbdb960c813b6125557639161dd4a329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156787"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a><span data-ttu-id="7e564-103">Настройка точки восстановления из настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="7e564-103">Setting a Restore Point from a Custom Action</span></span>

<span data-ttu-id="7e564-104">Настраиваемые действия не должны вызывать функцию [**срсетресторепоинт**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) , так как это может привести к тому, что точка входа восстановления записывается в середину установщик Windows установки.</span><span class="sxs-lookup"><span data-stu-id="7e564-104">Custom actions must not call the [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) function because this may result in a restore entry point being written into the middle of a Windows Installer installation.</span></span>

<span data-ttu-id="7e564-105">Дополнительные сведения см. [в разделе точки восстановления системы и установщик Windows](system-restore-points-and-the-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="7e564-105">For more information, see [System Restore Points and the Windows Installer](system-restore-points-and-the-windows-installer.md).</span></span>

 

 
