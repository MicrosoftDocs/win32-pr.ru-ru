---
title: Клиентские функции транспорта WDS
description: Этот модуль определяет структуры и функции, которые составляют интерфейс между получателем содержимого и транспортным клиентом.
ms.assetid: 20c3116b-3a0d-4048-b6f2-81c03e0a80ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f228370aa0973e124b1877dcf8a458d1356170fbb872a05a1867ac0489c00a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680404"
---
# <a name="wds-transport-client-functions"></a>Клиентские функции транспорта WDS

Этот модуль определяет структуры и функции, которые составляют интерфейс между получателем содержимого и транспортным клиентом.



| Функция                                                                              | Описание                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ вдстранспортклиентрецеивеконтентс*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivecontents) | Указывает, что блок данных готов к использованию.                                                                                                                         |
| [*PFN \_ вдстранспортклиентрецеивеметадата*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivemetadata) | Получает метаданные о файле.                                                                                                                                 |
| [*PFN \_ вдстранспортклиентсессионкомплете*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessioncomplete) | Указывает, что сеанс успешно завершен или произошла ошибка.                                                                                                  |
| [*PFN \_ вдстранспортклиентсессионстарт*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstart)       | Указывает размер файла и другие сведения о стороне сервера для файла потребителю.                                                                                   |
| [*PFN \_ вдстранспортклиентсессионстартекс*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex)   | Указывает размер файла и другие сведения о стороне сервера для файла потребителю.                                                                                   |
| [**вдстранспортклиентаддрефбуффер**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientaddrefbuffer)              | Увеличивает счетчик ссылок на буфер, принадлежащий клиенту многоадресной рассылки.                                                                                                   |
| [**вдстранспортклиентканцелсессион**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcancelsession)            | Освобождает ресурсы, связанные с сеансом в клиенте.                                                                                                             |
| [**вдстранспортклиентклосесессион**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientclosesession)              | Освобождает ресурсы, связанные с сеансом в клиенте.                                                                                                             |
| [**вдстранспортклиенткомплетерецеиве**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcompletereceive)        | Указывает, что вся обработка блока данных завершена, и клиент многоадресной рассылки может удалить этот блок данных из кэша, чтобы освободить место для последующего получения. |
| [**вдстранспортклиентинитиализе**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitialize)                  | Инициализирует клиент многоадресной рассылки.                                                                                                                                           |
| [**вдстранспортклиентинитиализесессион**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitializesession)    | Инициирует передачу файлов многоадресной рассылки.                                                                                                                                        |
| [**вдстранспортклиенткуеристатус**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientquerystatus)                | Извлекает текущее состояние текущей или полной многоадресной передачи из клиента многоадресной рассылки.                                                                    |
| [**вдстранспортклиентрегистеркаллбакк**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientregistercallback)      | Регистрирует обратный вызов для многоадресного клиента.                                                                                                                             |
| [**вдстранспортклиентрелеасебуффер**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientreleasebuffer)            | Уменьшает значение счетчика ссылок на буфер, принадлежащий клиенту многоадресной рассылки.                                                                                                   |
| [**вдстранспортклиентшутдовн**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientshutdown)                      | Завершает работу клиента многоадресной рассылки.                                                                                                                                            |
| [**вдстранспортклиентстартсессион**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession)              | Инициирует передачу файлов многоадресной рассылки.                                                                                                                                        |
| [**вдстранспортклиентваитфоркомплетион**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientwaitforcompletion)    | Блокируется до тех пор, пока не завершится сеанс многоадресной рассылки или не будет достигнуто указанное время ожидания.                                                                                  |



 

 

 




