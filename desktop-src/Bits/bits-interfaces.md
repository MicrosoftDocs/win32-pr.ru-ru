---
title: Интерфейсы BITS
description: Используйте следующие интерфейсы фоновая интеллектуальная служба передачи (BITS) для передачи файлов и отслеживания заданий в очереди передачи.
ms.assetid: 72668c9b-e6f3-4f3f-9d4b-50d930d1889d
ms.topic: article
ms.date: 01/08/2019
ms.openlocfilehash: fc95d4aea6d6d74ff2952cf2ef686fbaa1049732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986182"
---
# <a name="bits-interfaces"></a>Интерфейсы BITS

Используйте следующие интерфейсы фоновая интеллектуальная служба передачи (BITS) для [передачи файлов и отслеживания заданий](using-bits.md) в очереди передачи.

| Интерфейс | Описание |
|-|-|
| [**ибаккграундкопикаллбакк**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) | Клиенты реализуют интерфейс [**ибаккграундкопикаллбакк**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) , чтобы получить уведомление о завершении задания, было ли оно изменено или находится в ошибке. |
| [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) | Клиенты реализуют интерфейс [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) , чтобы получить уведомление о том, что загрузка файла завершена. |
| [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) | Клиенты реализуют интерфейс [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) , чтобы получить уведомление о завершении загрузки диапазонов файла. |
| [**ибаккграундкоперрор**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) | Извлекает сведения об ошибке задания. |
| [**ибаккграундкопифиле**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyfile) | Извлекает имена локальных и удаленных файлов для запроса на перемещение файла в задании и его ход выполнения. |
| [**IBackgroundCopyFile2**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2) | Задает новое удаленное имя для файла и получает список загружаемых диапазонов. |
| [**IBackgroundCopyFile3**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3) | Проверяет файл таким образом, чтобы одноранговые узлы могли запрашивать его содержимое и извлекать имя временного файла. |
| [**IBackgroundCopyFile4**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4) | Извлекает статистику загрузки для одноранговых и исходных серверов. |
| [**IBackgroundCopyFile5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5) | Предоставляет методы универсального свойства Get и Set для свойств Баккграундкопифиле. |
| [**IBackgroundCopyFile6**](/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6) | Возвращает или задает общие свойства передачи файлов BITS. |
| [**Использованием метода ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) | Добавляет файлы в задание, задает уровень приоритета задания, определяет состояние задания, запускает и останавливает задание. |
| [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) | Извлекает данные ответа из задания передачи, определяет ход выполнения передачи данных для ответа клиенту, запрашивает выполнение командной строки и предоставляет учетные данные для прокси-сервера и удаленной службы. |
| [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3) | Загружает диапазоны файла, изменяет префикс имени удаленного файла и сохраняет сведения о владельце и ACL в файле. |
| [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) | Включает одноранговое кэширование, ограничивает время загрузки и проверяет характеристики токена пользователя. |
| [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) | Запрашивает или задает несколько необязательных поведений задания. |
| [**ибаккграундкопижобхттпоптионс**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) | Указывает клиентские сертификаты для проверки подлинности клиента на основе сертификата и пользовательских заголовков для HTTP-запросов. |
| [**IBackgroundCopyJobHttpOptions2**](/windows/desktop/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2) | Используйте этот интерфейс для получения и (или) переопределения метода HTTP, используемого для передачи BITS. |
| [**ибаккграундкопиманажер**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) | Создает задания перемещения, извлекает объект перечислителя заданий из очереди и получает отдельные задания из очереди. |
| [**ибитспир**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeer) | Возвращает сведения о одноранговом узле в окружении. |
| [**ибитспиркачеадминистратион**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) | Управление пулом одноранговых узлов, из которого можно загрузить содержимое. |
| [**ибитспиркачерекорд**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacherecord) | Возвращает сведения о файле в кэше. |
| [**ибитстокеноптионс**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) | Связывает и управляет парой маркеров безопасности для задания передачи фоновая интеллектуальная служба передачи (BITS). |
| [**иенумбаккграундкопифилес**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) | Перечисляет файлы в задании. |
| [**иенумбаккграундкопижобс**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) | Перечисляет задания в очереди на перемещение. |
| [**иенумбитспиркачерекордс**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords) | Перечисляет записи кэша. |
| [**иенумбитспирс**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeers) | Перечисляет список одноранговых узлов, обнаруженных службой BITS. |



 

 

 




