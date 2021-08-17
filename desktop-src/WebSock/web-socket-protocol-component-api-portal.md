---
title: API компонента протокола WebSocket
description: API компонента протокола WebSocket
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a712234f55b0270db9da23dc0efa1da823c85907cca92ac3428cb1225fac8a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134217"
---
# <a name="websocket-protocol-component-api"></a>API компонента протокола WebSocket

## <a name="purpose"></a>Назначение

API компонента протокола WebSocket позволяет выполнять асинхронные двунаправленные каналы связи по протоколу HTTP, которые работают через существующие сетевые посредники. С помощью API компонента протокола WebSocket клиент использует HTTP для обмена данными с сервером, а затем обе стороны переключаются на базовый протокол, на котором был разворот HTTP (например, TCP или SSL). Цель — сначала использовать HTTP для обхода сетевых посредников, а затем использовать установленный сквозной канал TCP/SSL для двунаправленного взаимодействия приложений. Протокол WebSocket \[ [вспрото](https://tools.ietf.org/html/rfc6455) \] определен в IETF, а соответствующий API JavaScript \[ [W3CAPI](https://dev.w3.org/html5/websockets/) \] определен в консорциуме W3C.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                          | Описание                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Типы данных API компонента протокола WebSocket**](web-socket-protocol-component-api-data-types.md)<br/> | Эти типы данных определяются API компонента протокола WebSocket.<br/>   |
| [Перечисления API компонента протокола WebSocket](web-socket-protocol-component-api-enumerations.md)<br/> | Эти перечисления определяются API компонента протокола WebSocket.<br/> |
| [Функции API компонента протокола WebSocket](web-socket-protocol-component-api-functions.md)<br/>       | Эти функции определяются API компонента протокола WebSocket.<br/>    |
| [Структуры API компонентов протокола WebSocket](web-socket-protocol-component-api-structures.md)<br/>     | Эти структуры определяются API компонента протокола WebSocket.<br/>   |



 

## <a name="developer-audience"></a>Аудитория разработчиков

API компонента протокола WebSocket предназначен для использования с помощью программистов C/C++. вам потребуются знакомство с HTTP и Windows сетью.

> [!Note]  
> предпочтительный способ использования протокола WebSocket на Windows — через [API Windows служб HTTP (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) или [Windows. Пространство имен Networking. Sockets](/uwp/api/Windows.Networking.Sockets).

 

## <a name="run-time-requirements"></a>Требования к среде выполнения

API компонента протокола WebSocket требует Windows 8 и более поздних версий операционной системы Windows. Интерфейсы API можно динамически связывать с помощью websocket.dll.

> [!Note]  
> websocket.dll обеспечивает поддержку HTTP-заголовков, связанных с подтверждением соответствия клиента и сервера, проверяет полученные данные подтверждения и анализирует поток данных WebSocket. Он не обрабатывает какие-либо операции HTTP (перенаправление, проверку подлинности, поддержку прокси-сервера) и не выполняет никаких операций ввода-вывода (отправка или получение байтов потока WebSocket).

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[HTTP](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[Windows Службы HTTP (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

