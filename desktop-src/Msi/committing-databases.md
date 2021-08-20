---
description: Изменения, вносимые в базу данных установки, не записываются в базу данных до тех пор, пока не будет вызван Мсидатабасекоммит.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Фиксация баз данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1ab5f4da5b82fb3b6b2ac7d2371bd8046ab87a23d2ef43b6473f7e36a4771a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145353"
---
# <a name="committing-databases"></a>Фиксация баз данных

Изменения, вносимые в базу данных установки, не записываются в базу данных до тех пор, пока не будет вызван [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

**Проверка завершения изменений, внесенных в базу данных**

1.  Проверьте, будет ли записана таблица при вызове [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) путем вызова [**мсидатабасеистаблеперсистент**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).
2.  Вызовите функцию [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) , чтобы завершить изменения в базе данных.

Изменения, внесенные в базу данных, накапливаются и не отражаются в реальной базе данных до тех пор, пока не будет вызван [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Временные столбцы или строки не фиксируются в базе данных. При закрытии базы данных все изменения, внесенные с момента последнего **мсидатабасекоммит** , автоматически откатываются.

 

 



