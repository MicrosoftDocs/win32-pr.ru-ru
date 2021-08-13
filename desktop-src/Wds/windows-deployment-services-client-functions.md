---
title: Windows Клиентские функции служб развертывания
description: для API клиента служб Windowsного развертывания используются следующие функции.
ms.assetid: 4cedd8a8-7f46-4229-9d96-58965b751e43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c213822323405e030ba9907f692d6fcaa370356fb395a390dfa0f1fc0818244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566389"
---
# <a name="windows-deployment-services-client-functions"></a>Windows Клиентские функции служб развертывания

для API клиента служб Windowsного развертывания используются следующие функции.



| Функция                                                                                 | Описание                                                                                                                            |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ вдскликаллбакк*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclicallback)                                          | Уведомления о ходе выполнения и сообщения об ошибках во время передачи файла или изображения.                                                              |
| [*PFN \_ вдсклитрацефунктион*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclitracefunction)                                | Получает сообщения отладки от клиента WDS.                                                                                       |
| [**вдсклиаусоризесессион**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession)                                 | Преобразует анонимный сеанс в сеанс, прошедший проверку подлинности.                                                                           |
| [**вдскликанцелтрансфер**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicanceltransfer)                                     | Отменяет операцию пересылки WDS.                                                                                                      |
| [**вдскликлосе**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliclose)                                                       | Закрывает дескриптор сеанса или образа WDS и освобождает ресурсы.                                                                      |
| [**вдскликреатесессион**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession)                                       | Запускает новый сеанс с сервером WDS.                                                                                                |
| [**вдсклифиндфирстимаже**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage)                                     | Запускает перечисление образов, хранящихся на сервере WDS, и возвращает маркер Find, который ссылается на первое изображение.                     |
| [**вдсклифинднекстимаже**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage)                                       | Перемещает ссылку на маркер Find на следующий образ, хранящийся на сервере WDS.                                                      |
| [**вдсклифристрингаррай**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifreestringarray)                                   | Освобождает массив строковых значений, которые выделены функцией [**вдсклиобтаиндриверпаккажес**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages) . |
| [**вдсклижетенумератионфлагс**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags)                           | Возвращает флаг перечисления изображений для текущего маркера изображения.                                                                       |
| [**вдсклижетимажеарчитектуре**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture)                         | Возвращает архитектуру процессора для текущего изображения.                                                                              |
| [**вдсклижетимажедескриптион**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription)                           | Возвращает описание текущего изображения.                                                                                          |
| [**вдсклижетимажеграуп**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup)                                       | Возвращает имя группы образов для текущего образа.                                                                                    |
| [**вдсклижетимажехалнаме**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname)                                   | Возвращает имя слоя абстрагирования оборудования (HAL) для текущего образа.                                                               |
| [**вдсклижетимажехандлефромфиндхандле**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromfindhandle)         | Возвращает маркер изображения для текущего изображения.                                                                                         |
| [**вдсклижетимажехандлефромтрансферхандле**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromtransferhandle) | Возвращает маркер изображения из завершенного маркера перемещения.                                                                              |
| [**вдсклижетимажеиндекс**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex)                                       | Возвращает индекс изображения для текущего изображения.                                                                                         |
| [**вдсклижетимажелангуаже**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage)                                 | Возвращает язык по умолчанию для текущего изображения.                                                                                     |
| [**вдсклижетимажелангуажес**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages)                               | Возвращает массив языков, поддерживаемых текущим изображением.                                                                          |
| [**вдсклижетимажеластмодифиедтиме**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime)                 | Возвращает время последнего изменения текущего изображения.                                                                                  |
| [**вдсклижетимаженаме**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename)                                         | Возвращает имя текущего изображения.                                                                                                 |
| [**вдсклижетимаженамеспаце**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagenamespace)                               | Возвращает имя текущего изображения.                                                                                                 |
| [**вдсклижетимажепас**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath)                                         | Возвращает путь к файлу изображения, содержащему текущий образ.                                                                    |
| [**вдсклижетимажесизе**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize)                                         | Возвращает размер текущего изображения.                                                                                                 |
| [**вдсклижетимажеверсион**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion)                                   | Возвращает версию текущего изображения.                                                                                              |
| [**вдсклижеттрансферсизе**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligettransfersize)                                   | Возвращает размер текущего перемещения.                                                                                              |
| [**вдсклиинитиализелог**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog)                                       | Инициализирует журнал для клиента.                                                                                                    |
| [**вдсклилог**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclilog)                                                           | Отправляет событие журнала на сервер WDS.                                                                                                   |
| [**вдсклиобтаиндриверпаккажес**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages)                         | Получает из образа WDS, пакетов драйверов (INF-файлов), которые могут использоваться на этом компьютере.                                           |
| [**вдсклирегистертраце**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliregistertrace)                                       | Регистрирует функцию обратного вызова, которая будет принимать сообщения отладки.                                                                    |
| [**вдсклитрансферфиле**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferfile)                                         | Передает файл с WDS-сервера в клиент WDS с помощью протокола многоадресной передачи.                                              |
| [**вдсклитрансферимаже**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferimage)                                       | Передает образ с WDS-сервера.                                                                                                  |
| [**вдскливаитфортрансфер**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliwaitfortransfer)                                   | Ожидает завершения перемещения.                                                                                                      |



 



| Функция                                                             | Описание                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**вдсклижетдриверкуериксмл**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetdriverqueryxml)           | Создает XML-строку, которую можно использовать для запроса пакетов драйверов на сервере WDS. доступно, начиная с Windows 8 и Windows Server 2012.               |
| [**вдсклиобтаиндриверпаккажесекс**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackagesex) | Получает пакеты драйверов (INF-файлы), применимые к указанному XML-файлу запроса драйвера WDS. доступно, начиная с Windows 8 и Windows Server 2012. |



 

 

 




