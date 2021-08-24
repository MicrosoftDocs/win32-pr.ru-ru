---
description: 'для определения установщик Windows версии можно использовать следующие методы:'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: определение версии установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e13907790585356fa4a5bc8376fe87f30793e0e3af71e1b0c113f30cf04b8f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764224"
---
# <a name="determining-the-windows-installer-version"></a>определение версии установщик Windows

для определения установщик Windows версии можно использовать следующие методы:

-   Вызовите функцию [**мсижетфилеверсион**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) с параметром *сзфилепас* , для которого задан путь к файлу Msi.dll.

    Вы можете вызвать функцию [**шжеткновнфолдерпас**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) с **\_ системной** константой CSid, чтобы получить путь к Msi.dll. начиная с Windows Vista, приложения должны использовать функцию [**шжетфолдерпас**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) и **рефкновнфолдерид** "System". Существующие приложения, использующие функцию **шжетфолдерпас** и тип **CSid** , продолжат работать.

-   значение свойства [**установщика. Version**](installer-version.md) [**объекта установщика**](installer-object.md) эквивалентно строкам из четырех полей, перечисленным в [выпущенных версиях установщик Windows](released-versions-of-windows-installer.md) разделе.
-   приложения могут получить версию установщик Windows с помощью [**дллжетверсион**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).
-   установщик задает для свойства [**версионмси**](versionmsi.md) версию установщик Windows, которая выполняется во время установки.

дополнительные сведения см. в статье [released versions of установщик Windows](released-versions-of-windows-installer.md).

 

 
