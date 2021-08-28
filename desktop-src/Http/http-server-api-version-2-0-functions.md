---
title: Функции API сервера HTTP версии 2,0
description: API сервера HTTP версии 2,0 предоставляет следующие функции.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- Функции API сервера HTTP версии 2,0
- Функции HTTP, API HTTP-сервера версии 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b832a3f8fb1a97c48c49809d3e2f1975965becdc4c7bbf3942601d577d4702d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981364"
---
# <a name="http-server-api-version-20-functions"></a>Функции API сервера HTTP версии 2,0

API сервера HTTP версии 2,0 предоставляет следующие функции.

| Функция | Описание |
|-|-|
| [**хттпделегатерекуестекс**](/windows/win32/api/http/nf-http-httpdelegaterequestex) | Делегирует запрос от исходной очереди запросов к целевой очереди запросов. |
| [**хттпфиндурлграупид**](/windows/win32/api/http/nf-http-httpfindurlgroupid) | Извлекает идентификатор группы URL-адресов и очередь запросов. |
| [**хттписфеатуресуппортед**](/windows/win32/api/http/nf-http-httpisfeaturesupported) | Проверяет, поддерживается ли определенный компонент. |

## <a name="server-session"></a>Сеанс сервера

| Функция | Описание |
|-|-|
| [**хттпклосесерверсессион**](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [**хттпкреатесерверсессион**](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [**хттпкуерисерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [**хттпсетсерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a>Группы URL-адресов

| Функция | Описание |
|-|-|
| [**хттпаддурлтаурлграуп**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [**хттпкреатеурлграуп**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [**хттпклосеурлграуп**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [**хттпкуерюрлграуппроперти**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [**хттпремовеурлфромурлграуп**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [**хттпсетурлграуппроперти**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a>Очередь запросов

| Функция | Описание |
|-|-|
| [**хттпклосерекуесткуеуе**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [**хттпкреатерекуесткуеуе**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [**хттпкуерирекуесткуеуепроперти**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [**хттпсетрекуесткуеуепроперти**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [**хттпшутдовнрекуесткуеуе**](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [**хттпваитфордемандстарт**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a>Связанные темы

[Структуры API HTTP-сервера версии 2,0](http-server-api-version-2-0-structures.md)
