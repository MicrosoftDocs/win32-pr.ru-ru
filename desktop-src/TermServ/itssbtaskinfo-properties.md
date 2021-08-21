---
title: Свойства Итссбтаскинфо
description: Интерфейс Итссбтаскинфо предоставляет следующие свойства.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d91b24b95b6b19cb439350c0c6823306c66a8fab5fe47f0f9e9fb739df64e3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128072"
---
# <a name="itssbtaskinfo-properties"></a>Свойства Итссбтаскинфо

Интерфейс [**итссбтаскинфо**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) предоставляет следующие свойства.

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[**Свойство Context**](itssbtaskinfo-context.md)
</dt> <dd>

Извлекает байты контекста, связанные с задачей.

</dd> <dt>

[**Свойство крайний срок**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

Возвращает время, в которое должна быть инициирована задача. Используется для определения приоритетов исправлений. Сначала будет инициировано исправление с самым ранним сроком.

</dd> <dt>

[**EndTime, свойство**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

Возвращает последнее время, в течение которого агент задачи может запустить задачу.

</dd> <dt>

[**Свойство идентификатора**](itssbtaskinfo-identifier.md)
</dt> <dd>

Извлекает идентификатор GUID, используемый агентом задачи в качестве уникального идентификатора.

</dd> <dt>

[**Свойство Label**](itssbtaskinfo-label.md)
</dt> <dd>

Извлекает метку, которая описывает назначение задачи.

</dd> <dt>

[**Свойство подключаемого модуля**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

Возвращает отображаемое имя агента задачи.

</dd> <dt>

[**StartTime, свойство**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

Возвращает самое раннее время, в течение которого агент задачи может запустить задачу.

</dd> <dt>

[**Свойство Status**](itssbtaskinfo-status.md)
</dt> <dd>

Извлекает значение [**перечисления \_ \_ состояния задачи RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) , представляющее состояние задачи.

</dd> <dt>

[**TargetId, свойство**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

Извлекает идентификатор целевого объекта.

</dd> </dl>

 

 




