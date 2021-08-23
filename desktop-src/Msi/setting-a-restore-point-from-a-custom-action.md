---
description: настраиваемые действия не должны вызывать функцию срсетресторепоинт, так как это может привести к тому, что точка входа восстановления записывается в середину установщик Windows установки.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Настройка точки восстановления из настраиваемого действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b30dad9f8f250c0ae82286425d092538ad8324715e632e2c5074e428454f76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628584"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>Настройка точки восстановления из настраиваемого действия

настраиваемые действия не должны вызывать функцию [**срсетресторепоинт**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) , так как это может привести к тому, что точка входа восстановления записывается в середину установщик Windows установки.

дополнительные сведения см. [в разделе точки восстановления системы и установщик Windows](system-restore-points-and-the-windows-installer.md).

 

 
