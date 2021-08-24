---
title: Синтаксис String (обобщенное время)
description: Формат строки времени, определенный стандартом ASN. 1. | Синтаксис String (обобщенное время)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Схема AD синтаксиса String (обобщенное время)
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bf7d965b03b75f4186b807098a5262c402d0c19104a4c09357958b38a77a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580214"
---
# <a name="stringgeneralized-time-syntax"></a>Синтаксис String (обобщенное время)

Формат строки времени, определенный стандартом ASN. 1. Используйте этот синтаксис для хранения значений времени в Generalized-Time формате.

Формат синтаксиса Generalized-Time — "YYYYMMDDHHMMSS. 0Z". Примером допустимого значения является "20010928060000.0 Z". "Z" обозначает отсутствие разностного времени. Active Directory сохраняет дату и время как среднее время по Гринвичу (GMT). Если значение времени не указано, по умолчанию используется значение GMT.

Если время указано в часовом поясе, отличном от GMT, то разностное соединение между часовым поясом и GMT добавляется к строке вместо «Z» в формате «YYYYMMDDHHMMSS. 0 \[ +/- \] ЧЧММ». Пример допустимого значения: "20010928060000.0 + 0200". Разностное резервное копирование основано на формуле: GMT = Local + DIFFERENTIAL.

Дополнительные сведения см. в разделе ISO 8601 и X680.



| Ввод | Значение |
|--------------|----------------------------------------------------------------------------|
| Имя         | String(обобщенное_время)                                                   |
| Идентификатор синтаксиса    | 2.5.5.11                                                                   |
| ИДЕНТИФИКАТОР OM        | 24                                                                         |
| Тип MAPI    | систиме                                                                    |
| Тип ADS     | АДСТИПЕ \_ время в формате UTC \_                                                         |
| Тип варианта | \_Дата VT                                                                   |
| Тип SDS     | [System.DateTime](/dotnet/api/system.datetime) |



## <a name="see-also"></a>См. также

<dl> <dt>

[System.DateTime](/dotnet/api/system.datetime)
</dt> </dl>

 

 
