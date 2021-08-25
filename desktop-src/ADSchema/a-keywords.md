---
title: Атрибут keywords
description: Список ключевых слов, которые можно использовать для нахождение определенной точки соединения.
ms.assetid: 24297ebf-8d32-4b22-9dd9-b26bce675118
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута keywords
- Схема AD атрибута keywords
topic_type:
- apiref
api_name:
- Keywords
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2efa6f3b24aae32cdd0501a5474133981f2c9e582997663480814c6d1167e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924824"
---
# <a name="keywords-attribute"></a>Атрибут keywords

Список ключевых слов, которые можно использовать для нахождение определенной точки соединения.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | Keywords                                    |
| LDAP-отображаемое имя | keywords                                    |
| Размер              | \-                                          |
| Привилегия обновления  | \-                                          |
| Частота обновления  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.48                       |
| System-ID — GUID    | bf967993-0de6-11d0-a285-00aa003049e2        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|----------------------------------------------------------|
| Идентификатор ссылки                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | Неверно                                                    |
| Является однозначным       | Неверно                                                    |
| Индексируется             | Верно                                                     |
| В глобальном каталоге      | Верно                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 256                                                      |
| Search-Flags           | 0x00000001                                               |
| System-Flags           | 0x00000010                                               |
| Классы, используемые в        | [**Точка соединения**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Неверно                                                                                                                                                                                                                                                                                   |
| Является однозначным       | Неверно                                                                                                                                                                                                                                                                                   |
| Индексируется             | Верно                                                                                                                                                                                                                                                                                    |
| В глобальном каталоге      | Верно                                                                                                                                                                                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Классы, используемые в        | [**Версия приложения**](c-applicationversion.md)<br/> [**Точка соединения**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**MS-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**MS-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                       |
| MAPI-Id                | \-                                                                                                                       |
| System-Only            | Неверно                                                                                                                    |
| Является однозначным       | Неверно                                                                                                                    |
| Индексируется             | Верно                                                                                                                     |
| В глобальном каталоге      | Верно                                                                                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                             |
| Range-Lower            | 1                                                                                                                        |
| Range-Upper            | 256                                                                                                                      |
| Search-Flags           | 0x00000001                                                                                                               |
| System-Flags           | 0x00000010                                                                                                               |
| Классы, используемые в        | [**MS-DS-Service-Connection-Point-publication-Service**](c-msds-serviceconnectionpointpublicationservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Неверно                                                                                                                                                                                                                                                                                   |
| Является однозначным       | Неверно                                                                                                                                                                                                                                                                                   |
| Индексируется             | Верно                                                                                                                                                                                                                                                                                    |
| В глобальном каталоге      | Верно                                                                                                                                                                                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Классы, используемые в        | [**Версия приложения**](c-applicationversion.md)<br/> [**Точка соединения**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**MS-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**MS-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Неверно                                                                                                                                                                                                                                                                                   |
| Является однозначным       | Неверно                                                                                                                                                                                                                                                                                   |
| Индексируется             | Верно                                                                                                                                                                                                                                                                                    |
| В глобальном каталоге      | Верно                                                                                                                                                                                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Классы, используемые в        | [**Версия приложения**](c-applicationversion.md)<br/> [**Точка соединения**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**MS-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**MS-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Неверно                                                                                                                                                                                                                                                                                   |
| Является однозначным       | Неверно                                                                                                                                                                                                                                                                                   |
| Индексируется             | Верно                                                                                                                                                                                                                                                                                    |
| В глобальном каталоге      | Верно                                                                                                                                                                                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Классы, используемые в        | [**Версия приложения**](c-applicationversion.md)<br/> [**Точка соединения**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**MS-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**MS-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Неверно                                                                                                                                                                                                                                                                                   |
| Является однозначным       | Неверно                                                                                                                                                                                                                                                                                   |
| Индексируется             | Верно                                                                                                                                                                                                                                                                                    |
| В глобальном каталоге      | Верно                                                                                                                                                                                                                                                                                    |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Классы, используемые в        | [**Версия приложения**](c-applicationversion.md)<br/> [**Точка соединения**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**MS-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**MS-DS-App-Data**](c-msds-appdata.md)<br/> |



 

 





