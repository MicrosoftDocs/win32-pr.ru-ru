---
title: EC_WMT_INDEX_EVENT (пакет SDK для формата Windows Media 11)
description: '\_ \_ событие индекса EC \_ ВМТ'
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- Пакет SDK Windows Media Format, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- Расширенный формат систем (ASF), EC_WMT_INDEX_EVENT
- ASF (Расширенный системный формат), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070951"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a>EC_WMT_INDEX_EVENT (пакет SDK для формата Windows Media 11)

Отправляется пакетом SDK Windows Media Format, когда приложение использует модуль записи ASF для индексирования видеофайлов Windows Media.

Параметры

*lParam1*

Может быть одним из следующих сообщений **\_ о состоянии ВМТ** .



| Сообщение              | Описание                                     |
|----------------------|-------------------------------------------------|
| ВМТ \_ запущен         | Индексирование начато. *lParam2* имеет нулевое значение.          |
| ВМТ \_ закрыт          | Индексирование завершено. *lParam2* имеет нулевое значение. |
| \_ \_ ход выполнения индекса ВМТ | Выполняется индексирование.                        |



 

*lParam2*

Если *LPARAM1* ВМТ \_ Closed или ВМТ \_ Started, то *lParam2* равен нулю. Если *lParam1* является ВМТ \_ \_ ходом выполнения индекса, то *lParam2* представляет собой **DWORD** , который выражает объем работ в процентах от общего размера загрузки.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Справочник по КАСФ DirectShow**](directshow-qasf-reference.md)
</dt> </dl>

 

 




