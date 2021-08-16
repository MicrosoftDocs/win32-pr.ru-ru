---
description: Службы обычно пишутся как консольные приложения.
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: Точка входа службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a8f44322048351161bb8f3b8afdd619129d18b5effb5dc850d8909afbb3673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888976"
---
# <a name="service-entry-point"></a>Точка входа службы

Службы обычно пишутся как консольные приложения. Точкой входа консольного приложения является его **Основная** функция. Функция **Main** получает аргументы из значения **ImagePath** из раздела реестра для службы. Дополнительные сведения см. в разделе "Примечания" функции [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) .

Когда SCM запускает программу службы, она ожидает вызова функции [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) . Используйте следующие рекомендации.

-   Служба типа " \_ \_ собственный процесс Win32" \_ должна вызывать [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) немедленно, из своего основного потока. Инициализацию можно выполнить после запуска службы, как описано в разделе [Service ServiceMain Function](service-servicemain-function.md).
-   Если типом службы является \_ \_ Общий \_ процесс Win32 и существует общая инициализация всех служб в программе, можно выполнить инициализацию в основном потоке перед вызовом [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera), если он занимает менее 30 секунд. В противном случае необходимо создать другой поток для выполнения общей инициализации, в то время как главный поток вызывает **сбой StartServiceCtrlDispatcher**. При запуске службы все равно следует выполнять инициализацию, зависящую от службы.

Функция [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) принимает структуру [**\_ \_ записи таблицы службы**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) для каждой службы, содержащейся в процессе. Каждая структура задает имя службы и точку входа для службы. Пример см. в разделе [написание функции Main служебной программы](writing-a-service-program-s-main-function.md).

Если [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) завершается успешно, вызывающий поток не возвращает значение, пока все выполняющиеся службы в процессе не перешли в \_ состояние остановлена. SCM отправляет управляющие запросы в этот поток через именованный канал. Поток выступает в качестве диспетчера управления, выполняя следующие задачи:

-   Создание нового потока для вызова соответствующей точки входа при запуске новой службы.
-   Вызовите соответствующую [функцию обработчика](service-control-handler-function.md) для обработки запросов управления службами.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Написание основной функции служебной программы](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



