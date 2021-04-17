---
description: Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются установщик Windows&\# 160; 3.0 и более ранних версий.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Не поддерживается в установщик Windows 3,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673561"
---
# <a name="not-supported-in-windows-installer-30"></a>Не поддерживается в установщик Windows 3,0

Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются в установщик Windows 3,0 и более ранних версиях. Отсутствие функции из этого списка не гарантирует, что эта функция поддерживается. Чтобы определить, какая версия установщик Windows требуется для конкретной функции, см. основную документацию. Сведения о других установщик Windows версиях см. [в разделе новые возможности установщик Windows](what-s-new-in-windows-installer.md).

Установщик Windows 3,0 доступна для Windows Server 2003, Windows XP или Windows 2000. Список всех установщик Windows версий и распространяемых компонентов см. в разделе [выпущенные версии установщик Windows](released-versions-of-windows-installer.md).

Следующие функции не поддерживаются в установщик Windows 3,0 и более ранних версиях.

[Функции установщика](installer-functions.md)

-   [**мсисетекстерналуирекорд**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**мсинотифисидчанже**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

Прототип функции обратного вызова

-   [**\_запись обработчика инсталлуи \_**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[Таблицы базы данных](database-tables.md)

-   Столбец значение в [таблице мсипатчметадата](msipatchmetadata-table.md) принимает значения **оптимизединсталлмоде** и **минорупдатетаржетртм**.

[Свойства](properties.md)

-   [**Msix64, свойство**](msix64.md)

[Установщик Windows в 64-разрядных операционных системах](windows-installer-on-64-bit-operating-systems.md)

-   [**Свойство "Сводка" шаблона**](template-summary.md) принимает значение x64.

[Внутренние средства оценки согласованности — ICEs](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
