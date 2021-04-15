---
description: В КСАПО можно добавить поддержку параметров времени выполнения, реализовав интерфейс Иксапопараметерс. Поддержка параметров времени выполнения позволяет КСАПО изменять свое поведение в зависимости от параметров, передаваемых ей во время выполнения.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 'Руководство: добавление в XAPO поддержки параметра времени выполнения'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582f51b3dfbdc6d31422494906d5f945f77ccb03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497637"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a>Руководство: добавление в XAPO поддержки параметра времени выполнения

В КСАПО можно добавить поддержку параметров времени выполнения, реализовав интерфейс [**иксапопараметерс**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) . Поддержка параметров времени выполнения позволяет КСАПО изменять свое поведение в зависимости от параметров, передаваемых ей во время выполнения.

1.  Выполните действия, описанные в разделе [как создать ксапо](how-to--create-an-xapo.md).
2.  Измените КСАПО на производный от [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) и [**кксапобасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).
3.  Добавьте вызовы методов [**кксапопараметерсбасе:: бегинпроцесс**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) и [**Кксапопараметерсбасе:: Ендпроцесс**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) в реализацию [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

    > [!Note]  
    > Добавление этих методов в [иксапо::P шаблоны](how-to--build-a-basic-audio-processing-graph.md) позволяет [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) сохранит свои копии параметров Effect в поточно-ориентированном состоянии. Вызовите метод [**кксапопараметерсбасе:: бегинпроцесс**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) в начале [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process)и [**кксапопараметерсбасе:: ендпроцесс**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) в конце **иксапо::P шаблоны**.

     

4.  Добавьте дополнительный код в реализацию [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , чтобы изменить его поведение в соответствии со значениями, хранящимися в методе [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) .

    > [!Note]  
    > Добавление кода в метод [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process) для использования параметров, заданных параметром [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) , позволяет изменять поведение ксапо в течение его жизненного цикла.

     

5.  При создании экземпляра этого действия выделите буфер из трех структур, которые будут представлять параметры эффектов, и передайте его конструктору [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .

    > [!Note]  
    > Экземпляр [**кксапопараметерсбасе**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) использует этот буфер для управления параметрами эффектов, передаваемыми в него при вызове [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters). Необходимо инициализировать все блоки параметров процесса в *ппараметерблоккс* до того же значения по умолчанию до вызова любого из методов [**иксапо::P шаблоны**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**Иксапопараметерс:: Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)и **иксапопараметерс:: SetParameters** . Обычно эта инициализация обрабатывается в [**иксапо:: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) или в [**Иксапо:: локкфорпроцесс**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).

     

## <a name="related-topics"></a>См. также

<dl> <dt>

[Звуковые эффекты](audio-effects.md)
</dt> <dt>

[Обзор протокола XAPO](xapo-overview.md)
</dt> </dl>

 

 
