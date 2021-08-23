---
title: Типы данных IMAPI (Imapi2. h)
description: Спецификации для оптических носителей и связанных устройств определяют диапазон значений для таких элементов, как описание структуры DVD, описание сведений о диске и размер страницы компонентов.
ms.assetid: 8797a8d0-5ce5-4b16-9d41-c22fa0d67dcf
keywords:
- ULONG_IMAPI2_DVD_STRUCTURE
- ULONG_IMAPI2_ADAPTER_DESCRIPTOR
- ULONG_IMAPI2_DEVICE_DESCRIPTOR
- ULONG_IMAPI2_DISC_INFORMATION
- ULONG_IMAPI2_TRACK_INFORMATION
- ULONG_IMAPI2_FEATURE_PAGE
- ULONG_IMAPI2_MODE_PAGE
- ULONG_IMAPI2_ALL_FEATURE_PAGES
- ULONG_IMAPI2_ALL_PROFILES
- ULONG_IMAPI2_ALL_MODE_PAGES
- ULONG_IMAPI2_NONZERO
- ULONG_IMAPI2_NOT_NEGATIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f003c2e03ff3d21623111d3d43a83cddf43e31c64557cfce18b5a401cdcd5d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612014"
---
# <a name="imapi-data-types"></a>Типы данных IMAPI

Спецификации для оптических носителей и связанных устройств определяют диапазон значений для таких элементов, как описание структуры DVD, описание сведений о диске и размер страницы компонентов. IMAPI определяет следующие типы длинных целых чисел без знака (ULONG), которые обеспечивают ограничения значения диапазона. Эти типы определяются исключительно для оптимальной проверки IDL параметров, а также в качестве вспомогательной документации для вызывающих объектов, касающихся верхних ограничений для определенных операций обмена данными.


```C++
typedef ULONG ULONG_IMAPI2_DVD_STRUCTURE;
typedef ULONG ULONG_IMAPI2_ADAPTER_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DEVICE_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DISC_INFORMATION;
typedef ULONG ULONG_IMAPI2_TRACK_INFORMATION;
typedef ULONG ULONG_IMAPI2_FEATURE_PAGE;
typedef ULONG ULONG_IMAPI2_MODE_PAGE;
typedef ULONG ULONG_IMAPI2_ALL_FEATURE_PAGES;
typedef ULONG ULONG_IMAPI2_ALL_PROFILES;
typedef ULONG ULONG_IMAPI2_ALL_MODE_PAGES;
typedef ULONG ULONG_IMAPI2_NONZERO;
typedef ULONG ULONG_IMAPI2_NOT_NEGATIVE;
```





| Тип данных                                                                                                                                  | Описание                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**\_ \_ Структура DVD ulong \_ IMAPI2**                | Диапазон: 0, 65535 (0, 0x0000FFFF)<br/> Структура DVD ограничена 64 КБ из-за поля распределения, сокрывающего 2 байта.<br/>                                                                                                                                                                                     |
| <span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**\_IMAPI2ный \_ дескриптор адаптера ulong \_** | Диапазон: 0, 268435455 (0, 0x0FFFFFFF)<br/> Дескриптор адаптера не имеет неявно ограниченного размера.<br/>                                                                                                                                                                                                |
| <span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**\_ \_ Дескриптор устройства ulong \_ IMAPI2**    | Диапазон: 0, 268435455 (0, 0x0FFFFFFF)<br/> Дескриптор устройства имеет неявный ограниченный размер.<br/>                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**\_ \_ Данные о диске ulong IMAPI2 \_**       | Диапазон: 0, 65538 (0, 0x00010002)<br/> Информация о диске ограничена 64 КБ плюс 2 байта для поля размер.<br/>                                                                                                                                                                                         |
| <span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**\_ \_ Данные о дорожке IMAPI2 ulong \_**    | Диапазон: 0, 65538 (0, 0x00010002)<br/> Информация о дорожке ограничена 64 КБ плюс 2 байта для поля размера.<br/>                                                                                                                                                                                        |
| <span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**\_ \_ Страница функции ulong \_ IMAPI2**                   | Диапазон: 0256 (0, 0x00000100)<br/> Одна страница возможностей ограничена 256 байтами.<br/>                                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**\_ \_ Страница режима ulong \_ IMAPI2**                            | Диапазон: 0257 (0, 0x00000101)<br/> Страница в одном режиме ограничена 257 байтами.<br/>                                                                                                                                                                                                                    |
| <span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**ULONG \_ IMAPI2 \_ все \_ \_ страницы компонентов**   | Диапазон: 0, 65536 (0, 0x00010000)<br/> Число функций ограничено двухбайтовым полем.<br/>                                                                                                                                                                                                       |
| <span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**ULONG \_ IMAPI2 \_ все \_ Профили**                   | Диапазон: 0, 63 (0, 0x0000003F)<br/> Количество профилей для устройства — это количество профилей, которые помещаются в одном компоненте. Каждый профиль занимает четыре байта. Один компонент может содержать 252 дополнительных байт данных, достаточных для хранения максимального числа профилей 63.<br/>                                 |
| <span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**ULONG \_ IMAPI2 \_ все \_ \_ страницы режима**            | Диапазон: 0, 32763 (0, 0x00007FFB)<br/> Число страниц режима для устройства. Число в режиме Via \_ SENSE10 ограничено двухбайтовым полем.<br/> Заголовок параметра mode имеет размер 8 байт. Каждая страница имеет по крайней мере два байта. Максимальное число страниц в режиме — 32763: (65535-8)/2 округляется вниз.<br/> |
| <span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG \_ IMAPI2 \_ ненулевое значение**                                   | Диапазон: 1, 2147483647 (1, 0x7FFFFFFF)<br/> Универсальное ненулевое значение, которое можно использовать для проверки того, что значение не равно нулю.<br/>                                                                                                                                                                              |
| <span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG \_ IMAPI2 \_ Not \_ отрицателен**                   | Диапазон: 0, 2147483647 (0, 0x7FFFFFFF)<br/> 32-разрядное целое число с неотрицательным значением.<br/>                                                                                                                                                                                                              |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Imapi2. h</dt> </dl> |



 

 





