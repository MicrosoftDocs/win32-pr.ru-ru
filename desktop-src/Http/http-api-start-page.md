---
title: API сервера HTTP
description: API сервера HTTP позволяет приложениям взаимодействовать по протоколу HTTP без использования Microsoft Internet Information Server (IIS).
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- API сервера HTTP
- API сервера HTTP, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133858"
---
# <a name="http-server-api"></a>API сервера HTTP

## <a name="purpose"></a>Назначение

API сервера HTTP позволяет приложениям взаимодействовать по протоколу HTTP без использования Microsoft Internet Information Server (IIS). Приложения могут регистрироваться для получения HTTP-запросов для определенных URL-адресов, получения HTTP-запросов и отправки HTTP-ответов. API сервера HTTP включает поддержку SSL, чтобы приложения могли обмениваться данными по защищенным HTTP-соединениям без служб IIS. Он также предназначен для работы с портами завершения ввода-вывода.

## <a name="developer-audience"></a>Аудитория разработчиков

Этот API предназначен для использования программистами C/C++.

## <a name="run-time-requirements"></a>Требования к среде выполнения

API сервера HTTP поддерживается в операционных системах Windows Server 2003 и Windows XP с пакетом обновления 2 (SP2). Имейте в виду, что Microsoft IIS 5, работающий в Windows XP с пакетом обновления 2 (SP2), не может использовать порт 80 совместно с другими приложениями HTTP, работающими одновременно.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                           | Описание                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Об API сервера HTTP](about-http-server-api.md)<br/>                   | Общие сведения о протоколе HTTP.<br/>                                                              |
| [Использование API сервера HTTP](using-http-server-api.md)<br/>                   | Процедурное пошаговое описание использования протокола HTTP.<br/>                                                             |
| [Справочник по API HTTP-сервера](http-server-api-reference.md)<br/>           | Документация по конкретным функциям, структурам и типам перечислений, доступным в HTTP.<br/>    |
| [Пример приложения HTTP-сервера](http-server-sample-application.md)<br/> | Пример приложения, демонстрирующий использование API сервера HTTP для выполнения задач на стороне сервера.<br/> |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Службы HTTP Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

