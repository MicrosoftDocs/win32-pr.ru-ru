---
description: Когда пользователь запускает Просмотр событий для просмотра записей журнала событий, он вызывает функцию Реадевентлог для получения структур EVENTLOGRECORD.
ms.assetid: 1d5b62cb-cf5b-4f4c-8521-1c783ae3afc7
title: Просмотр журнала событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c566fef29cfb110883741ddc0e6c298d6a1255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264048"
---
# <a name="viewing-the-event-log"></a>Просмотр журнала событий

Когда пользователь запускает Просмотр событий для просмотра записей журнала событий, он вызывает функцию [**реадевентлог**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) для получения структур [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) . Просмотр событий использует источник события и идентификатор события для получения текста сообщения для каждого события из зарегистрированного файла сообщения (указывается значением реестра **евентмессажефиле** для источника). Просмотр событий использует функцию [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) для загрузки файла сообщения. Затем Просмотр событий использует функцию [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) для получения базовой строки описания из загруженного модуля. Наконец, Просмотр событий заменяет параметры вставки в базовой строке описания для получения окончательной строки сообщения.

 

 
