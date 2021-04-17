---
description: 'Для определения установщик Windows версии можно использовать следующие методы:'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: Определение версии установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a48434fe415084a93158fb3445a36906d8b8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663711"
---
# <a name="determining-the-windows-installer-version"></a>Определение версии установщик Windows

Для определения установщик Windows версии можно использовать следующие методы:

-   Вызовите функцию [**мсижетфилеверсион**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) с параметром *сзфилепас* , для которого задан путь к файлу Msi.dll.

    Вы можете вызвать функцию [**шжеткновнфолдерпас**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) с **\_ системной** константой CSid, чтобы получить путь к Msi.dll. Начиная с Windows Vista, приложения должны использовать функцию [**шжетфолдерпас**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) и **рефкновнфолдерид** "System". Существующие приложения, использующие функцию **шжетфолдерпас** и тип **CSid** , продолжат работать.

-   Значение свойства [**установщика. Version**](installer-version.md) [**объекта установщика**](installer-object.md) эквивалентно строкам из четырех полей, перечисленным в [выпущенных версиях установщик Windows](released-versions-of-windows-installer.md) разделе.
-   Приложения могут получить версию установщик Windows с помощью [**дллжетверсион**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).
-   Установщик задает для свойства [**версионмси**](versionmsi.md) версию установщик Windows, которая выполняется во время установки.

Дополнительные сведения см. в статье [Released Versions of установщик Windows](released-versions-of-windows-installer.md).

 

 
