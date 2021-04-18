---
description: Установка бита done
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Установка бита done
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701264"
---
# <a name="setting-the-done-bit"></a>Установка бита done

COM+ будет деактивировать активируемый JIT-компилятором объект на основе состояния свойства контекста, установленного бита, следующим образом:

-   Если для установленного бита задано значение true, COM+ деактивирует объект при возврате текущего вызова метода.
-   Если для установленного бита задано значение false, то объект остается активным при возврате текущего вызова метода.

По умолчанию в качестве бита завершения задано значение false при создании объекта и инициализации его контекста. (Любой JIT-активируемый объект создается в собственном контексте, поэтому для него задается собственный бит done.) Однако этот параметр по умолчанию можно изменить отдельно для каждого метода с помощью свойства Автозаполнение. Установить бит завершения можно следующими способами.

-   Использование [ **иконтекстстате**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)
-   Использование [ **иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)
-   Использование свойства автоматического завершения

## <a name="using-icontextstate"></a>Использование Иконтекстстате

Можно использовать [**иконтекстстате:: сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) , чтобы задать для бита done значение true или false.

Вы можете использовать [**иконтекстстате:: жетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) для получения текущего состояния завершенного бита из контекста объекта.

## <a name="using-iobjectcontext"></a>Использование Иобжектконтекст

Вы можете использовать следующие методы в [**иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) для установки установленного бита при одновременной установке одинакового бита, используемого для голосования в транзакциях:

-   [**Сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) сигнализирует, что вы сделали, и проголосуем за фиксацию текущей транзакции. Он устанавливает для битов и последовательный бит значение true.
-   [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) сигнализирует о завершении и думс текущую транзакцию. Он устанавливает для аргумента Done значение true, а для бита — значение false.
-   [**Енаблекоммит**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) сигнализирует о том, что вы не сделали, но проголосуем за фиксацию транзакции. Он устанавливает для аргумента Done значение false, а для бита — значение true.
-   [**Дисаблекоммит**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) сигнализирует о том, что вы не сделали, и вы не зафиксировали транзакцию в данный момент, обычно потому, что состояние не согласуется. Он устанавливает как бит завершения, так и последовательный бит в значение false.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Основные понятия JIT-активации COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Включение JIT-активации для компонента](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Объединение объектов в пул и JIT-активация COM+](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Транзакции и JIT-активация COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



