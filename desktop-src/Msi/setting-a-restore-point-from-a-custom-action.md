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
# <a name="setting-a-restore-point-from-a-custom-action"></a>Настройка точки восстановления из настраиваемого действия

Настраиваемые действия не должны вызывать функцию [**срсетресторепоинт**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) , так как это может привести к тому, что точка входа восстановления записывается в середину установщик Windows установки.

Дополнительные сведения см. [в разделе точки восстановления системы и установщик Windows](system-restore-points-and-the-windows-installer.md).

 

 
