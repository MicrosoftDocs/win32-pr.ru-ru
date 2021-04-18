---
description: В этом разделе описаны новые функции, добавленные в счетчики производительности для каждого выпуска.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Новые возможности (счетчики производительности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0c1189a185351eabae438a01c6f111952f164e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663171"
---
# <a name="whats-new-with-performance-counters"></a>Новые возможности счетчиков производительности

В этом разделе описаны новые функции, добавленные в счетчики производительности для каждого выпуска.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 и Windows Server 2008 R2

Средство [КТРПП](ctrpp.md) было изменено для улучшения и упрощения создания кода. Теперь средство создает только заголовок и файл ресурсов. Если требуется старое поведение при создании кода (не рекомендуется), можно использовать новый `-legacy` аргумент.

- Теперь необходимо указать новые `-o` `-rc` аргументы и, задающих имя и расположение заголовка и файла ресурсов соответственно.
- Можно использовать необязательный `-prefix` аргумент New для указания строки, добавляемой в начало глобальных переменных и функций, определенных в создаваемом файле заголовка.
- Если необходимо обновить манифест счетчиков, использование нового создания кода исключает необходимость слияния предыдущей реализации обратного вызова с новым созданным кодом, так как обратные вызовы больше не включаются в созданный код.

`symbol`Для следующих элементов манифеста доступен новый атрибут:

- [поставщики](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [подписан](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

`symbol`Атрибут является обязательным для [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) и [CounterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)и является необязательным для [счетчика](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element). Атрибут позволяет указать символическое имя, которое можно использовать для ссылки на каждый элемент при вызове функций поставщика (например, можно использовать символьное имя набора счетчиков при вызове [перфкреатеинстанце](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).

## <a name="windows-vista"></a>Windows Vista

Архитектура счетчиков производительности для предоставления данных счетчиков была полностью изменена в этом выпуске.

Ранее вы использовали INI-файл для определения данных счетчика и реализовали библиотеку DLL производительности, которая выполнялась в процессе потребителя для предоставления данных по запросу потребителя. Эта архитектура устарела и не рекомендуется для нового кода из-за серьезных проблем с производительностью и надежностью.

Новая архитектура использует манифест для определения данных счетчика и выполняет код в процессе поставщика для предоставления данных, когда потребитель запрашивает их. Дополнительные сведения см. в разделе [предоставление данных счетчика с помощью версии 2,0](providing-counter-data-using-version-2-0.md).

Для этого выпуска были добавлены следующие функции:

- [контролкаллбакк](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [перфкреатеинстанце](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [перфделетеинстанце](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [перфкуеринстанце](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [перфсеткаунтерсетинфо](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [перфсетулонгкаунтервалуе](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [перфсетулонглонгкаунтервалуе](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [перфсеткаунтеррефвалуе](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [перфстартпровидер](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [перфстоппровидер](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

Для этого выпуска были добавлены следующие структуры:

- [\_удостоверение счетчика производительности \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [\_сведения о счетчике производительности \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [\_сведения о наборе счетчиков производительности \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [\_экземпляр COUNTERSET производительности \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

Список XML-элементов, используемых в манифесте для определения счетчиков, см. в разделе [схема счетчиков производительности](performance-counters-schema.md).

Сведения о средстве предварительного процессора КТРПП, который анализирует манифест и создает код, используемый в качестве отправной точки для поставщика, см. в разделе [КТРПП](ctrpp.md).
