---
description: Типы счетчиков алгоритма таймера точности получают более точные показания, чем системные таймеры.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Типы счетчиков для алгоритма таймера точности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818049"
---
# <a name="precision-timer-algorithm-counter-types"></a><span data-ttu-id="2805b-103">Типы счетчиков для алгоритма таймера точности</span><span class="sxs-lookup"><span data-stu-id="2805b-103">Precision Timer Algorithm Counter Types</span></span>

<span data-ttu-id="2805b-104">Типы счетчиков алгоритма таймера точности получают более точные показания, чем системные таймеры.</span><span class="sxs-lookup"><span data-stu-id="2805b-104">The precision timer algorithm counter types obtain more accurate readings than system timers.</span></span> <span data-ttu-id="2805b-105">Служба, предоставляющая данные, также предоставляет метку времени, которая устраняет ошибки, которые могут возникать из-за небольшого и переменного времени между записью системной метки времени и сбором данных из библиотеки DLL производительности.</span><span class="sxs-lookup"><span data-stu-id="2805b-105">The service that provides the data also provides a timestamp, which eliminates the errors that can occur because of the small and variable time that elapses between capture of the system timestamp and collection of the data from the performance DLL.</span></span> <span data-ttu-id="2805b-106">Этот базовый штамп времени для таймеров точности — это \_ \_ свойство метки времени точности производительности, которое должно следовать за \_ \_ свойством таймера точности производительности.</span><span class="sxs-lookup"><span data-stu-id="2805b-106">This base timestamp for precision timers is a PERF\_PRECISION\_TIMESTAMP property, which must immediately follow the PERF\_PRECISION\_TIMER property.</span></span>



| <span data-ttu-id="2805b-107">Константа CounterType</span><span class="sxs-lookup"><span data-stu-id="2805b-107">CounterType Constant</span></span>                                                                                         | <span data-ttu-id="2805b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2805b-108">Description</span></span>                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2805b-109">[Производительность \_ Десятичный \_ \_ таймер системы точности](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))541525248</span><span class="sxs-lookup"><span data-stu-id="2805b-109">[PERF\_PRECISION\_SYSTEM\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248</span></span><br/> | <span data-ttu-id="2805b-110">Аналогично \_ таймеру счетчика производительности \_ , за исключением того, что он использует определенное счетчиком базовое значение, а не системную метку времени.</span><span class="sxs-lookup"><span data-stu-id="2805b-110">Similar to PERF\_COUNTER\_TIMER except that it uses a counter defined time base instead of the system timestamp.</span></span>             |
| <span data-ttu-id="2805b-111">[Производительность \_ Десятичный \_ \_ таймер 100 с точностью](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))542573824</span><span class="sxs-lookup"><span data-stu-id="2805b-111">[PERF\_PRECISION\_100NS\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 542573824</span></span><br/>  | <span data-ttu-id="2805b-112">Аналогично \_ \_ таймеру производительности 100NSEC, за исключением того, что в нем используется счетчик 100 нс, а не метка времени в системе.</span><span class="sxs-lookup"><span data-stu-id="2805b-112">Similar to PERF\_100NSEC\_TIMER except that it uses a 100ns counter defined time base instead of the system 100ns timestamp.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2805b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="2805b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2805b-114">Типы счетчиков производительности WMI</span><span class="sxs-lookup"><span data-stu-id="2805b-114">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

