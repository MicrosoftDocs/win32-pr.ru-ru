---
title: Структуры и объединения BITS
description: Интерфейсы фоновая интеллектуальная служба передачи (BITS) используют следующие структуры.
ms.assetid: a1b8b4a1-77d6-46ac-96d5-6a0c99cfc643
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 199d5648ba8205d0417304350a104b2e16a607e4d7f1bdce4dfe9ecec34f98dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702034"
---
# <a name="bits-structures-and-unions"></a>Структуры и объединения BITS

[Интерфейсы](bits-interfaces.md) ФОНОВАЯ интеллектуальная служба передачи (BITS) используют следующие структуры.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**BG_AUTH_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials) | Определяет целевой объект (прокси или сервер), схему проверки подлинности и учетные данные пользователя, используемые для запросов проверки подлинности пользователя. Структура передается в [метод IBackgroundCopyJob2:: сеткредентиалс](/windows/win32/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials). |
| [**BG_AUTH_CREDENTIALS_UNION**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials_union) | Определяет учетные данные, используемые для схемы проверки подлинности, указанной в [структуре BG_AUTH_CREDENTIALS](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials). |
| [**BG_BASIC_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_basic_credentials) | Определяет имя пользователя и пароль для проверки подлинности. |
| [**BG_FILE_INFO**](/windows/win32/api/bits/ns-bits-bg_file_info) | Предоставляет локальные и удаленные имена переносимого файла. |
| [**BG_FILE_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_file_progress) | Предоставляет сведения о ходе выполнения, связанные с файлами, например число переданных байтов. |
| [**BG_FILE_RANGE**](/windows/win32/api/bits2_0/ns-bits2_0-bg_file_range) | Определяет диапазон байтов для скачивания из файла. |
| [**BG_JOB_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_job_progress) | Предоставляет сведения о ходе выполнения, связанные с заданиями, такие как число переданных байтов и файлов. Для заданий отправки это состояние применяется к файлу отправки, а не к файлу ответов. Сведения о ходе выполнения файла ответов см. в разделе [структура BG_JOB_REPLY_PROGRESS](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress). |
| [**BG_JOB_REPLY_PROGRESS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress) | Предоставляет сведения о ходе выполнения задания отправки и ответа, относящиеся к части ответа. |
| [**BG_JOB_TIMES**](/windows/win32/api/bits/ns-bits-bg_job_times) | Предоставляет отметки времени, связанные с заданием. |
| [**Объединение BITS_FILE_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Предоставляет значение свойства файла BITS. |
| [**BITS_JOB_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Предоставляет значение свойства задания BITS на основе значения [перечисления BITS_JOB_PROPERTY_ID](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id). |
