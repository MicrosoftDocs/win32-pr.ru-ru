---
title: Использование ADSI с Exchange
description: для Exchange 2000 сведения об использовании ADSI с Exchange содержатся в пакете SDK Exchange 2000. Дополнительные сведения см. в разделе задачи управления для ADSI.
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- adsi для Exchange adsi
- adsi для Exchange adsi, почтовые ящики
- adsi для Exchange adsi, почтовые ящики, создание
- adsi для Exchange adsi, почтовые ящики, удаление
- adsi для Exchange adsi, почтовых ящиков, установка дескриптора безопасности на
- adsi для Exchange adsi, почтовых ящиков, поиска домашнего сервера для
- adsi для Exchange adsi, получение и изменение сообщений
- adsi для Exchange adsi, дескрипторы безопасности
- adsi для Exchange adsi, дескрипторы безопасности, манипуляции
- adsi для Exchange adsi, дескрипторов безопасности, настройка
- adsi для Exchange adsi, контейнер получателей
- adsi для Exchange adsi, просмотр свойств объекта Exchange
- adsi для Exchange adsi, контейнеров получателей, настраиваемых
- adsi для Exchange adsi, Exchange Server
- adsi для Exchange adsi, Exchange Server, просмотра и изменения схемы
- adsi для Exchange adsi, Exchange Server, листинг версии сервера
- adsi для Exchange adsi, Exchange Server, организации и имени сайта
- adsi для Exchange adsi, Exchange Server, поиск домашнего сервера почтовых ящиков
- adsi для Exchange adsi, адреса электронной почты, получение
- adsi для Exchange adsi, списки рассылки, создание
- adsi для Exchange adsi, скрытых или удаленных записей
- adsi для Exchange adsi, извлечение изменений службы каталогов
- adsi для Exchange adsi, размер сообщения
- adsi для Exchange adsi, устранение неполадок
- почтовые ящики ADSI
- почтовые ящики ADSI, создание
- почтовые ящики ADSI, удаление
- почтовые ящики ADSI, Установка дескриптора безопасности на
- почтовые ящики ADSI, поиск домашнего сервера для
- сообщения ADSI, получение и изменение
- Exchange ADSI
- Exchange ADSI, почтовые ящики
- Exchange ADSI, почтовые ящики, создание
- Exchange ADSI, почтовые ящики, удаление
- Exchange ADSI, почтовые ящики, Установка дескриптора безопасности
- Exchange ADSI, почтовые ящики, поиск домашнего сервера для
- Exchange ADSI, получение и изменение сообщений
- Exchange ADSI, дескрипторы безопасности
- Exchange ADSI, дескрипторы безопасности, манипуляции
- Exchange ADSI, дескрипторы безопасности, Настройка
- Exchange ADSI, контейнер получателей
- Exchange ADSI, просмотр свойств объекта Exchange
- Exchange ADSI, контейнер получателей, Пользовательский
- Exchange ADSI, Exchange Server
- Exchange ADSI, Exchange Server, просмотр и изменение схемы
- Exchange ADSI, Exchange Server, вывод версии сервера
- Exchange ADSI, Exchange Server, организация и имя сайта
- Exchange ADSI, Exchange Server, поиск домашнего сервера почтовых ящиков
- Exchange ADSI, адреса электронной почты, получение
- Exchange ADSI, списки рассылки, создание
- Exchange Элементы ADSI, скрытые или удаленные записи
- Exchange ADSI, извлечение изменений службы каталогов
- Exchange ADSI, размер сообщения
- Exchange ADSI, устранение неполадок
- дескрипторы безопасности ADSI, для объектов Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f48a1015674ea8bf413cb9edbf55f0f64f6211b85bb876baeb6ab47868482ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690133"
---
# <a name="using-adsi-with-exchange"></a>Использование ADSI с Exchange

для Exchange 2000 сведения об использовании ADSI с Exchange содержатся в пакете SDK Exchange 2000. Дополнительные сведения см. в разделе [задачи управления для ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).

В этом разделе можно найти следующие задачи:

-   Создание URL-адреса пользователя
-   Создание путей Active Directory
-   перечисление серверов Exchange 2000 с помощью ADSI
-   Управление атрибутами расширения с помощью ADSI
-   Добавление и удаление объекта Manager с помощью ADSI
-   перечисление свойств объекта Exchange с помощью ADSI/ADO
-   получение Exchange различающегося имени в формате ADSI
-   поиск Exchange имени организации с помощью ADSI
-   поиск Exchange списков адресов с помощью ADSI
-   Создание списка рассылки с помощью КДОЕКСМ и ADSI
-   Настройка ограничения для сообщений на виртуальном SMTP-сервере с помощью ADSI

сведения о Exchange 5,5 см. в справочнике по adsi, а также в руководстве по [Exchange adsi](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) .

В этом разделе можно найти следующие задачи:

-   просмотр и изменение схемы Exchange Server
-   просмотр необработанных свойств объекта Exchange
-   создание Exchange почтового ящика
-   настройка дескриптора безопасности в почтовом ящике Exchange
-   Управление дескрипторами безопасности и идентификаторами SID
-   Удаление объекта почтового ящика
-   Создание пользовательского получателя
-   Создание контейнера получателей
-   Получение имени Организации и сайта с сервера
-   перечисление версии сервера Exchange для всех серверов в организации
-   Поиск домашнего сервера почтового ящика
-   Получение адресов электронной почты
-   Доступ к скрытым или удаленным записям
-   Получение изменений, внесенных в службу каталогов
-   Создание списка рассылки на основе результатов запроса
-   Получение или изменение размера сообщения
-   Использование кодов ошибок LDAP для устранения неполадок

 

 