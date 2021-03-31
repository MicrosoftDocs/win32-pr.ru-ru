---
description: Изменения, вносимые в базу данных установки, не записываются в базу данных до тех пор, пока не будет вызван Мсидатабасекоммит.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Фиксация баз данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1336b094703e61b14966e7a73a6e67f73762024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911343"
---
# <a name="committing-databases"></a>Фиксация баз данных

Изменения, вносимые в базу данных установки, не записываются в базу данных до тех пор, пока не будет вызван [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

**Проверка завершения изменений, внесенных в базу данных**

1.  Проверьте, будет ли записана таблица при вызове [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) путем вызова [**мсидатабасеистаблеперсистент**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).
2.  Вызовите функцию [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) , чтобы завершить изменения в базе данных.

Изменения, внесенные в базу данных, накапливаются и не отражаются в реальной базе данных до тех пор, пока не будет вызван [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Временные столбцы или строки не фиксируются в базе данных. При закрытии базы данных все изменения, внесенные с момента последнего **мсидатабасекоммит** , автоматически откатываются.

 

 



