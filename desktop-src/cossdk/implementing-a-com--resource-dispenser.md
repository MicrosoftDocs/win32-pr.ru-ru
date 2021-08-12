---
description: Реализация распределителя ресурсов COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Реализация распределителя ресурсов COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9c37de2a4910af908bdc3f2e38f1c1b55699b133a59a818b8a09236f8c0a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547896"
---
# <a name="implementing-a-com-resource-dispenser"></a>Реализация распределителя ресурсов COM+

Следующие шаги описывают общую процедуру реализации распределителя ресурсов COM+:

1.  Определите формат **рестипид** , который определяет, как ресурсы отличаются друг от друга.

2.  Используйте файл заголовка Мтксдм. h и библиотеку Мтксдм. lib соответственно.

3.  Создайте библиотеку DLL, которая реализует интерфейс [**идиспенсердривер**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) и API, которые требуется предоставить приложениям.

4.  Во время запуска ([*DllMain*](/windows/desktop/Dlls/dllmain) или первый вызов API-интерфейса распределителя) вызовите функцию [**жетдиспенсерманажер**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) . Он возвращает указатель на интерфейс [**идиспенсерманажер**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) диспетчера распределителя.

5.  Вызовите метод [**идиспенсерманажер:: регистердиспенсер**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), передав ему указатель на реализацию [**идиспенсердривер**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver). В результате диспетчер распределителя создает держатель (диспетчер пула) для распределителя ресурсов, а затем возвращает указатель на интерфейс [**ихолдер**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) .

6.  Сохраните этот указатель, чтобы можно было вызывать [**ихолдер:: аллокресаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) и [**Ихолдер:: фриресаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).

7.  Теперь можно (в ответ на вызовы API) выполнять вызовы [**аллокресаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) и [**фриресаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource). **Аллокресаурце** изначально реагирует на обратный вызов метода [**креатересаурце**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) , но последующие вызовы **аллокресаурце** обслуживаются из растущего пула ресурсов.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Основные понятия распределителя ресурсов COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Интерфейсы распределителя ресурсов COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
