---
title: Методы (IInertiaProcessor)
description: В этом разделе содержатся методы для интерфейса IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Touch, интерфейс IInertiaProcessor
- Касание Windows, методы интерфейса
- инерция, интерфейс IInertiaProcessor
- Интерфейс IInertiaProcessor, методы
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710435"
---
# <a name="methods-iinertiaprocessor"></a>Методы (IInertiaProcessor)

В этом разделе содержатся методы для интерфейса [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .



| Метод                                                 | Описание                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Перезапуск**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | Инициализирует процессор с начальной меткой времени и перезапускает инерцию.                                                                                                                                                    |
| [**Процесс**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | Выполняет вычисления для текущего такта и может вызвать событие **Дельта** или **Completed** в зависимости от того, завершено ли экстраполяция. Если экстраполяция завершается в предыдущем такте, метод является оператором No-Op. |
| [**процесстиме**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | Выполняет вычисления для заданного такта и может вызвать событие **Дельта** или **Completed** в зависимости от того, завершено ли экстраполяция.                                                                        |
| [**Завершить**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | Завершает текущую манипуляцию и останавливает инерцию в обработчике инерции.                                                                                                                                              |
| [**комплететиме**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | Завершает текущую обработку в заданном такте, останавливает инерцию в обработчике инерции и создает событие ManipulationCompleted.                                                                                   |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




