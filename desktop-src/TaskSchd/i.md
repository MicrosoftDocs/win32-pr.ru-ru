---
title: I (планировщик задач)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14bec8dd745aee798ebb6aa9cb296d7a0990b85b44562fb94ea844d2d5d3397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072644"
---
# <a name="i-task-scheduler"></a>I (планировщик задач)

A B C D [E](e.md) F G р. J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**условия простоя**
</dt> <dd>

Период времени, в течение которого на компьютере нет вводимых пользователем данных. Условия простоя связаны с запланированным временем начала задачи.

Эти условия задаются путем вызова [**исчедуледворкитем:: сетфлагс**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).

</dd> <dt>

<span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**триггеры бездействия**
</dt> <dd>

Триггер на основе события, который срабатывает, когда компьютер переходит в состояние бездействия в течение определенного промежутка времени.

Триггеры простоя создаются путем задания \_ для элемента типа триггера задачи в \_ структуре [**\_ триггера**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) задания \_ \_ триггера события \_ во \_ время бездействия.

</dd> <dt>

<span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**время ожидания простоя**
</dt> <dd>

Интервал времени (в минутах), используемый триггером простоя или условием простоя. Триггеры бездействия — это триггеры на основе событий, которые не связаны с запланированным временем. Условия простоя связаны с запланированным временем начала задачи.

Время простоя задается вызовом [**исчедуледворкитем:: сетидлеваит**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).

</dd> </dl>

 

 




