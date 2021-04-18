---
description: В следующем списке перечислены события, поддерживаемые журналами WMI в Windows Vista и более поздних операционных системах.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: Сообщения о событиях WMI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711733"
---
# <a name="wmi-event-messages"></a>Сообщения о событиях WMI

В следующем списке перечислены события, поддерживаемые журналами WMI в Windows Vista и более поздних операционных системах.

> [!Note]  
> Следующая документация предназначена для разработчиков и ИТ-администраторов. Если вы пытаетесь разрешить сообщение об ошибке WMI в домашней системе, обратитесь к веб-сайту [Служба поддержки Майкрософт](https://support.microsoft.com/) .

 

<dl> <dt>

<span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**\_репозиторий WBEM MC не \_ \_ согласован**
</dt> <dd> <dl> <dt>

1073747424 (0x400015E0)
</dt> <dt>



Служба инструментарий управления Windows (WMI) обнаружила несогласованность с репозиторием WMI в *\\ \\ \\ репозитории каталога% WINDIR% system32* и не смог восстановить его. Репозиторий WMI теперь будет удален, и на основе механизма автоматического восстановления будет создан новый репозиторий.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**\_ \_ \_ \_ \_ Загрузка поставщика системных LocalSystem \_ для поставщика WBEM MC**
</dt> <dd> <dl> <dt>

2147483711 (0x8000003F)
</dt> <dt>



Поставщик %1 зарегистрирован в инструментарий управления Windows (WMI) пространстве имен %2 для использования учетной записи LocalSystem. Эта учетная запись является привилегированной, и поставщик может вызвать нарушение безопасности, если он неправильно олицетворяет запросы пользователей.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**\_ \_ \_ \_ \_ при \_ восстановлении не загружен MOF-файла WBEM MC**
</dt> <dd> <dl> <dt>

3221225476 (0xC0000004)
</dt> <dt>



Произошла ошибка %1 при попытке загрузить MOF %2 при восстановлении. MOF-файл, помеченный автовосстановлением.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC \_ не удается \_ активировать \_ Фильтр**
</dt> <dd> <dl> <dt>

3221225482 (0xC000000A)
</dt> <dt>



Не удалось повторно активировать фильтр событий с запросом "%2" в пространстве имен "%1" из-за ошибки %3. События не могут быть доставлены через этот фильтр, пока проблема не будет устранена.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**\_ \_ Недопустимый \_ \_ запрос поставщика \_ событий WBEM MC**
</dt> <dd> <dl> <dt>

3221225493 (0xC0000015)
</dt> <dt>



Поставщик событий %1 попытался зарегистрировать синтаксически недопустимый запрос "%2". Запрос будет проигнорирован. Запрос можно исправить, изучив репозиторий WMI в CIM Studio и обновив постоянные подписки для указанного поставщика и запроса. Если постоянная подписка создана с помощью MOF-файла, поступающего с установленным продуктом, необходимо обратиться к поставщику приложения, чтобы исправить неудачную регистрацию.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**\_ \_ Недопустимый \_ \_ \_ внутренний запрос поставщика \_ событий WBEM**
</dt> <dd> <dl> <dt>

3221225494 (0xC0000016)
</dt> <dt>



Поставщик событий %1 попытался зарегистрировать внутренний запрос события "%2" в пространстве имен "%3", для которого не удалось определить набор целевых классов объектов. Запрос будет проигнорирован.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**\_ \_ \_ \_ \_ слишком \_ широкий запрос поставщика событий WBEM MC**
</dt> <dd> <dl> <dt>

3221225495 (0xC0000017)
</dt> <dt>



Поставщик событий %1 попытался зарегистрировать запрос "%2" в пространстве имен "%3", которое слишком большое. Поставщики событий не могут предоставлять события, предоставляемые системой. Запрос будет проигнорирован. Обратитесь к поставщику приложения.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_ \_ запрос поставщика событий WBEM MC \_ \_ \_ не \_ найден**
</dt> <dd> <dl> <dt>

3221225496 (0xC0000018)
</dt> <dt>



Поставщик событий %1 попытался зарегистрировать запрос "%2", целевой класс "%3" которого в пространстве имен %4 не существует. Запрос будет проигнорирован.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**\_несобытие \_ \_ запроса поставщика \_ событий \_ WBEM \_ MC**
</dt> <dd> <dl> <dt>

3221225497 (0xC0000019)
</dt> <dt>



Поставщик событий %1 попытался зарегистрировать запрос &quot; %2 &quot; , целевой класс &quot; %3 которого &quot; не является классом событий. Запрос будет проигнорирован. Обратитесь к поставщику приложения.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**\_ \_ \_ сбой ядра WBEM MC \_**
</dt> <dd> <dl> <dt>

3221225500 (0xC000001C)
</dt> <dt>



Не удалось инициализировать ядро WMI или подсистему поставщика или подсистему событий, номер ошибки: %1. Это может быть вызвано неправильной установленной версией WMI, сбоем обновления репозитория WMI, недостатком места на диске или недостатком памяти.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**\_ \_ \_ сбой подключения ADAP MC \_ (WBEM)**
</dt> <dd> <dl> <dt>

3221225515 (0xC000002B)
</dt> <dt>



Инструментарий управления Windows (WMI) ADAP не удалось подключиться к пространству имен %1 из следующей ошибки: %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**\_сбой путкласс (WBEM MC \_ ADAP \_ PERFLIB \_ \_ )**
</dt> <dd> <dl> <dt>

3221225520 (0xC0000030)
</dt> <dt>



Инструментарий управления Windows (WMI) ADAP не удалось сохранить объект %1 в пространстве имен %2 из-за следующей ошибки %3.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ не \_ удалось \_ Добавить \_ WIN32PERF**
</dt> <dd> <dl> <dt>

3221225530 (0xC000003A)
</dt> <dt>



Инструментарий управления Windows (WMI) ADAP не удалось создать \_ базовый класс производительности Win32 в %1: result = %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ не \_ удалось \_ Добавить \_ WIN32PERFRAWDATA**
</dt> <dd> <dl> <dt>

3221225531 (0xC000003B)
</dt> <dt>



Инструментарий управления Windows (WMI) ADAP не удалось создать \_ базовый класс Win32 перфравдата %1.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**\_ \_ \_ не удалось \_ запустить репозиторий WBEM MC \_**
</dt> <dd> <dl> <dt>

3221231073 (0xC00015E1)
</dt> <dt>



Службе инструментарий управления Windows (WMI) не удалось загрузить файлы репозитория в *\\ \\ \\ репозиторий% WINDIR% system32 WBEM*. Это может быть вызвано повреждением файлов репозитория, параметрами безопасности в этом каталоге, недостатком места на диске или другими проблемами системных ресурсов, например нехваткой памяти. Если эта ошибка возникает при каждом перезапуске компьютера, администратору этого компьютера может потребоваться отключить службу WMI, проверить параметры безопасности для этой папки и файлов в этой папке и запустить служебную wmidiag для проверки работоспособности инструментарий управления Windows (WMI).


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**для WBEM \_ MC для \_ WBEM \_ требуется \_ Шифрование \_ отклонено**
</dt> <dd> <dl> <dt>

3221231077 (0xC00015E5)
</dt> <dt>



Отказано в доступе к пространству имен %1, так как оно помечено Рекуиресенкриптион, но скрипт или приложение попытались подключиться к этому пространству имен с уровнем проверки подлинности ниже " **PKT \_ Privacy**". Измените уровень проверки подлинности на **\_ общепринятое** и повторно запустите сценарий или приложение.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC для \_ WBEM \_ требуется шифрование с \_ \_ асинхронным \_ отклонением**
</dt> <dd> <dl> <dt>

3221231078 (0xC00015E6)
</dt> <dt>



Службе инструментарий управления Windows (WMI) не удалось асинхронно доставить результаты для пространства имен %1. Пространство имен помечено как Рекуиресенкриптион, но WinMgmt не удалось установить безопасное подключение к клиентскому компьютеру. Убедитесь в наличии отношений доверия между клиентскими и серверными компьютерами, чтобы клиент распознавал учетную запись компьютера сервера.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**\_узел WBEM \_ с \_ ведущим адаптером WBEM \_ уничтожен**
</dt> <dd> <dl> <dt>

3221231084 (0xC00015EC)
</dt> <dt>



Инструментарий управления Windows (WMI) остановлен WMIPRVSE.EXE, так как квота достигла значения предупреждения. Квота: %1 значение: %2, максимальное значение: %3, PID WMIPRVSE: %4.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ репфилеснотфаунд**
</dt> <dd> <dl> <dt>

3221231086 (0xC00015EE)
</dt> <dt>



Во время запуска службы службе инструментарий управления Windows (WMI) не удалось разместить файлы репозитория. Новый репозиторий будет создан на основе механизма автоматического восстановления.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ , \_ Запуск WBEM, \_ \_ успешно запущен**
</dt> <dd> <dl> <dt>

3221231087 (0xC00015EF)
</dt> <dt>



Служба инструментарий управления Windows (WMI) успешно запущена.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**\_ \_ \_ инициализация ядра WBEM, основная \_ Техническая поддержка \_ ESS \_**
</dt> <dd> <dl> <dt>

3221231089 (0xC00015F1)
</dt> <dt>



Инструментарий управления Windows (WMI)ные подсистемы службы успешно инициализированы.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**\_ \_ \_ \_ сбой инициализации службы WBEM MC \_ WBEM**
</dt> <dd> <dl> <dt>

3221225501 (0xC000001D)
</dt> <dt>



При попытке инициализации службы инструментарий управления Windows (WMI) был возвращен номер ошибки %1. Это может быть вызвано неправильной установленной версией WMI, сбоем обновления репозитория WMI, недостатком места на диске или недостатком памяти.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**\_ \_ репозиторий WBEM MC WBEM \_ \_ создан повторно**
</dt> <dd> <dl> <dt>

3221231088 (0xC00015F0)
</dt> <dt>



Репозиторий инструментарий управления Windows (WMI) успешно воссоздан повторно с помощью механизма восстановления.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События WMI](wmi-events.md)
</dt> <dt>

[Устранение неполадок WMI](wmi-troubleshooting.md).
</dt> </dl>

 

 




