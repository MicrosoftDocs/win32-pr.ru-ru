---
description: Следующие структуры поддерживают функции API таблиц распределенной маршрутизации (DRT).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Структуры таблиц распределенной маршрутизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663349"
---
# <a name="distributed-routing-table-structures"></a>Структуры таблиц распределенной маршрутизации

Следующие структуры поддерживают функции API таблиц распределенной маршрутизации (DRT).



| Структура                                                  | Описание                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_данные DRT**](/windows/desktop/api/drt/ns-drt-drt_data)                              | Содержит большой двоичный объект данных. Эта структура используется несколькими функциями DRT.                                                                                                                   |
| [**\_Регистрация DRT**](/windows/desktop/api/drt/ns-drt-drt_registration)              | Содержит регистрацию ключа. Это член структуры [**\_ \_ результатов поиска DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) , который является аргументом, передаваемым в [**дртрегистеркэй**](/windows/desktop/api/drt/nf-drt-drtregisterkey). |
| [**\_адрес DRT**](/windows/desktop/api/drt/ns-drt-drt_address)                        | Содержит сведения о конечной точке для узла DRT, который принимал участие в поиске. Эти сведения предназначены для использования при отладке проблем с подключением.                                   |
| [**\_список адресов \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_address_list)             | Содержит набор структур [**\_ адресов DRT**](/windows/desktop/api/drt/ns-drt-drt_address) , представляющих узлы, к которым осуществляется обращение во время поиска ключа.                                                             |
| [**\_поставщик безопасности \_ DRT**](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | Определяет интерфейс, который должен быть реализован поставщиком безопасности.                                                                                                                   |
| [**\_поставщик начальной загрузки DRT \_**](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | Определяет интерфейс, который должен быть реализован поставщиком начальной загрузки.                                                                                                                  |
| [**\_Параметры DRT**](/windows/desktop/api/drt/ns-drt-drt_settings)                      | Определяет параметры DRT при инициализации. Эта структура передается в качестве аргумента в [**дртопен**](/windows/desktop/api/drt/nf-drt-drtopen).                                                                           |
| [**\_сведения о поиске в DRT \_**](/windows/desktop/api/drt/ns-drt-drt_search_info)               | Определяет поисковый запрос. Эта структура передается в качестве аргумента в [**дртстартсеарч**](/windows/desktop/api/drt/nf-drt-drtstartsearch).                                                                             |
| [**\_Результат поиска \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result)           | Содержит результат поиска. Эта структура возвращается функцией [**дртжетсеарчресулт**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).                                                                                |
| [**\_данные событий \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | Содержит данные события, возвращаемые вызовом [**дртжетевентдата**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) после того, как приложение получит сигнал события.                                                    |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Перечисление таблиц распределенной маршрутизации](distributed-routing-table-enumerations.md)
</dt> <dt>

[Функции таблиц распределенной маршрутизации](distributed-routing-table-functions.md)
</dt> <dt>

[Справочник по распределенной маршрутизации API таблиц](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



