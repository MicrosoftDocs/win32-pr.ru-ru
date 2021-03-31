---
title: Перечисления ADSI
description: Интерфейсы служб Active Directory (ADSI) определяют и используют перечисления, перечисленные в следующей таблице.
ms.assetid: f0ad5ce5-742d-40dc-ac5a-31d779e40bfd
ms.tgt_platform: multiple
keywords:
- Интерфейсы ADSI ADSI, ссылка, перечисления
- Перечисления ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459aa59bc0f7907f59a4cd5a7e5fcb4f1b2630d8
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/27/2020
ms.locfileid: "104069651"
---
# <a name="adsi-enumerations"></a>Перечисления ADSI

Интерфейсы служб Active Directory (ADSI) определяют и используют перечисления, перечисленные в следующей таблице.



| Перечисление                                                           | Описание                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_перечисление АЦЕФЛАГ ADS \_**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum)                        | Указывает способ распространения безопасности для наследуемых записей управления доступом (ACE) и типов аудита для системного ACE.                                                                                                                                             |
| [**\_перечисление ACETYPE ADS \_**](/windows/win32/api/iads/ne-iads-ads_acetype_enum)                        | Указывает тип ACE.                                                                                                                                                                                                                                           |
| [**\_перечисление проверки подлинности ADS \_**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)          | Указывает уровень безопасности, используемый при проверке подлинности клиента.                                                                                                                                                                                                     |
| [**ОБЪЯВЛЕНИЯ \_ о \_ \_ перечислении ссылок**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)       | Указывает поведение при отслеживании ссылок.                                                                                                                                                                                                                       |
| [**ADS \_ дерефенум**](/windows/win32/api/iads/ne-iads-ads_derefenum)                               | Задает поведение разыменования псевдонима.                                                                                                                                                                                                                    |
| [**\_перечисление отображаемых объявлений \_**](/windows/win32/api/iads/ne-iads-ads_display_enum)                        | Указывает способ отображения пути.                                                                                                                                                                                                                                |
| [**\_ \_ перечислимый режим ЭКРАНИРОВАНия ADS \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)               | Указывает, являются ли специальные символы экранированными, неэкранированными или несенсорными.                                                                                                                                                                                        |
| [**\_перечисление ФЛАГТИПЕ ADS \_**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum)                      | Указывает наличие полей **ObjectType** или **инхеритедобжекттипе** в элементе управления доступом.                                                                                                                                                                         |
| [**\_перечисление в формате ADS \_**](/windows/win32/api/iads/ne-iads-ads_format_enum)                          | Задает тип значений в объекте PathName.                                                                                                                                                                                                                |
| [**\_ \_ Перечисление типов групп баннеров \_**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)                 | Задает тип группы элемента.                                                                                                                                                                                                                           |
| [**ADS \_ имя \_ иниттипе \_ перечисление**](/windows/win32/api/iads/ne-iads-ads_name_inittype_enum)           | Указывает тип инициализации, которую необходимо выполнить с объектом преобразования имени.                                                                                                                                                                                  |
| [**\_ \_ Перечисление типов имен баннеров \_**](/windows/win32/api/iads/ne-iads-ads_name_type_enum)                   | Указывает формат, используемый для представления различающихся имен.                                                                                                                                                                                                       |
| [**\_перечисление параметров ADS \_**](/windows/win32/api/iads/ne-iads-ads_option_enum)                          | Указывает доступные параметры, которые интерфейс [**иадсобжектоптионс**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) использует для манипуляций с объектами каталога.                                                                                                                        |
| [**\_ \_ перечисление кодировки паролей ADS \_**](/windows/win32/api/iads/ne-iads-ads_password_encoding_enum)   | Используется для задания типа кодировки паролей, используемой с параметром **метода ADS в \_ параметре \_ password \_** , в методах [**иадсобжектоптионс::**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) иадсобжектоптионс и [**:: SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) . |
| [**\_перечисление ПАСТИПЕ ADS \_**](/windows/win32/api/iads/ne-iads-ads_pathtype_enum)                      | Указывает тип объекта, для которого изменяется дескриптор безопасности.                                                                                                                                                                                        |
| [**\_перечисление предпочтений ADS \_**](/windows/win32/api/iads/ne-iads-ads_preferences_enum)                | Указывает параметры запроса OLE DB для ADSI.                                                                                                                                                                                                           |
| [**\_ \_ перечисление операций свойства ADS \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) | Указывает способы обновления значений свойств в кэше свойств.                                                                                                                                                                                               |
| [**\_перечисление прав ADS \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum)                          | Указывает права доступа к объекту службы каталогов.                                                                                                                                                                                                        |
| [**ADS \_ скопинум**](/windows/win32/api/iads/ne-iads-ads_scopeenum)                               | Задает область поиска в каталоге.                                                                                                                                                                                                                        |
| [**\_ \_ перечислимый элемент управления SD ADS \_**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)                 | Указывает, что список управления доступом (ACL) должен быть защищен при рекурсивном применении новых разрешений к дереву каталогов.                                                                                                                                  |
| [**\_ \_ перечисление формата SD ADS \_**](/windows/win32/api/iads/ne-iads-ads_sd_format_enum)                   | Задает формат для преобразования дескриптора безопасности.                                                                                                                                                                                                      |
| [**\_ \_ перечисление редакций SD ADS \_**](/windows/win32/api/iads/ne-iads-ads_sd_revision_enum)               | Указывает номер редакции элемента управления доступом или ACL.                                                                                                                                                                                                                   |
| [**\_перечисление СЕАРЧПРЕФ ADS \_**](/windows/win32/api/iads/ne-iads-ads_searchpref_enum)                  | Задает параметры поиска.                                                                                                                                                                                                                              |
| [**\_ \_ Перечисление сведений о безопасности ADS \_**](/windows/win32/api/iads/ne-iads-ads_security_info_enum)           | Задает параметры для проверки данных безопасности.                                                                                                                                                                                                                |
| [**\_перечисление СЕТТИПЕ ADS \_**](/windows/win32/api/iads/ne-iads-ads_settype_enum)                        | Указывает формат пути в [**иадспаснаме:: Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set).                                                                                                                                                                                       |
| [**ADS \_ статусенум**](/windows/win32/api/iads/ne-iads-ads_statusenum)                             | Указывает состояние параметров поиска.                                                                                                                                                                                                                       |
| [**\_перечисление СИСТЕМФЛАГ ADS \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)                  | Задает типы атрибутов, представленные объектом **attributeSchema** .                                                                                                                                                                                   |
| [**\_ \_ Перечисление флагов пользователей ADS \_**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)                   | Задает флаги, используемые для управления свойствами пользователя.                                                                                                                                                                                                            |
| [**\_перечисление диалектов ADSI \_**](/windows/win32/api/iads/ne-iads-adsi_dialect_enum)                      | Указывает доступные диалекты запросов ADSI.                                                                                                                                                                                                                          |
| [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum)                                    | Указывает типы данных, используемые для интерпретации расширенной строки синтаксиса ADSI.                                                                                                                                                                                            |



 

## <a name="remarks"></a>Комментарии

Поскольку приложения Visual Basic сценариев выпуска не могут считывать данные из библиотеки типов, приложения VBScript не могут распознать символьные константы, как определено в этих перечислениях. Вместо этого следует использовать числовые константы для установки соответствующих флагов в приложениях VBScript. Чтобы использовать символьные константы в качестве хорошей практики программирования, напишите явные объявления таких констант, как это сделано здесь, в приложениях VBScript.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
</dt> <dt>

[**Иадспаснаме:: Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)
</dt> </dl>

 

 




