---
description: установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются установщик Windows&\# 160; 3.0 и более ранних версий.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: не поддерживается в установщик Windows 3,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398b4211433762c68ed39af012d895d65aeee8fdc5a17f1e6142df76fcbe056c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926304"
---
# <a name="not-supported-in-windows-installer-30"></a>не поддерживается в установщик Windows 3,0

установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются в установщик Windows 3,0 и более ранних версиях. Отсутствие функции из этого списка не гарантирует, что эта функция поддерживается. чтобы определить, какая версия установщик Windows требуется для конкретной функции, см. основную документацию. сведения о других установщик Windows версиях см. [в разделе новые возможности установщик Windows](what-s-new-in-windows-installer.md).

Windows установщик 3,0 доступен для Windows Server 2003, Windows XP или Windows 2000. список всех установщик Windows версий и распространяемых компонентов см. в разделе [выпущенные версии установщик Windows](released-versions-of-windows-installer.md).

следующие функции не поддерживаются в установщик Windows 3,0 и более ранних версиях.

[Функции установщика](installer-functions.md)

-   [**мсисетекстерналуирекорд**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**мсинотифисидчанже**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

Прототип функции обратного вызова

-   [**\_запись обработчика инсталлуи \_**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[Таблицы базы данных](database-tables.md)

-   Столбец значение в [таблице мсипатчметадата](msipatchmetadata-table.md) принимает значения **оптимизединсталлмоде** и **минорупдатетаржетртм**.

[Свойства](properties.md)

-   [**Msix64, свойство**](msix64.md)

[Windows Установщик на 64-разрядных операционных системах](windows-installer-on-64-bit-operating-systems.md)

-   [**Свойство "Сводка" шаблона**](template-summary.md) принимает значение x64.

[Внутренние средства оценки согласованности — ICEs](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
