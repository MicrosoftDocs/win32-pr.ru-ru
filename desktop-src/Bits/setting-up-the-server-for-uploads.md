---
title: Настройка сервера для отправки
description: Чтобы передать файлы на сервер с помощью службы BITS, на сервере должны быть установлены службы IIS и серверное расширение BITS ISAPI. Требования к службам IIS см. в разделе требования IIS к отправке BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e075478f6e0335c6bf601a9289d93d4d3fac2aefd9e4f1ef820e938a1bfc0ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004724"
---
# <a name="setting-up-the-server-for-uploads"></a>Настройка сервера для отправки

Чтобы передать файлы на сервер с помощью службы BITS, на сервере должны быть установлены службы IIS и серверное расширение BITS ISAPI. Требования к службам IIS см. в разделе [требования IIS к отправке BITS](iis-requirements-for-bits-uploads.md).

Сведения о настройке виртуального каталога IIS, используемого BITS для отправки, см. в следующих разделах.

-   [Настройка разрешений для виртуальных каталогов](setting-permissions-on-virtual-directories.md)
-   [Написание сценария для настройки виртуального каталога](writing-a-script-to-configure-the-virtual-directory.md)
-   [Использование пользовательского интерфейса IIS для настройки виртуального каталога](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [Предотвращение нескольких отправок](preventing-multiple-uploads.md)
-   [Upload Рекомендации](upload-best-practices.md)

> [!Note]  
> Некоторые установки IIS включают компонент фильтрации UrlScan. Если средство UrlScan включено, администратор должен добавить команду "POST BITS \_ " в список разрешенных HTTP-команд URLScan. В противном случае отправка клиента BITS завершится ошибкой. Дополнительные сведения о включении команд в UrlScan см. в документации по UrlScan.

 

 

 




