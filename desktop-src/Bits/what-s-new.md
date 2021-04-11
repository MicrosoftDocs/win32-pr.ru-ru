---
title: Новые возможности BITS
description: В следующей таблице приведены новые возможности для каждого выпуска фоновая интеллектуальная служба передачи (BITS).
ms.assetid: ef05f2e1-88be-4adb-aca7-a7b1451cfd04
keywords:
- новые биты
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b171a1d8cede9e3fd49ac81ab47ffb09f72b6200
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070937"
---
# <a name="whats-new-bits"></a>Новые возможности BITS

С момента первого выпуска в составе Windows XP фоновая интеллектуальная служба передачи (BITS) постоянно улучшился, добавляя более мощные элементы управления для разработчика и администратора для контроля и управления загрузкой. Добавлен обширный набор командлетов PowerShell; Он может подключаться к нескольким типам HTTP-серверов; Это более тщательная пропускная способность и стоимость сети пользователя, чем раньше. 

В следующей таблице приведены новые возможности для каждого выпуска фоновая интеллектуальная служба передачи (BITS).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Версия</th>
<th>Описание функций</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Версия 10,3</td>
<td>Новые функции<br/>
<ul>
<li>Добавлен <a href="/windows/win32/api/bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3"><strong>BackgroundCopyJobHttpOptions3</strong></a> , помечающий заголовки HTTP как доступные только для записи, а также для настройки обратного вызова проверки сертификата сервера.</li>
<li>Служба BITS будет хранить удостоверение службы при создании другой системной службы.</li>
<li>BITS продолжит передавать файлы в подключенном режиме ожидания, если устройство подключено к сети.</li>
</ul>
Версия BITS 10,3 включена в обновление Windows 10 Май 2019 (10,0; Сборка 18362) и более поздние версии.
</td>
</tr>
<tr class="even">
<td>Версия 10,2</td>
<td>Новые функции<br/>
<ul>
<li>Добавлен <a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2"><strong>BackgroundCopyJobHttpOptions2</strong></a> для изменения метода HTTP для загрузок HTTP.</li>
<li>Теперь служба BITS использует порядок прокси-серверов по умолчанию для более стабильной работы с остальной частью системы.</li>
<li>Программистам проще задавать конфигурацию прокси-сервера BITS для корпоративных сценариев.</li>
<li>Теперь служба BITS обеспечивает более тщательный режим работы и поддерживает [современные ждущие режимы](/windows-hardware/design/device-experiences/modern-standby).</li>
<li>Теперь службы BITS поддерживают [политики](/windows/client-management/mdm/policy-configuration-service-provider) Mobile Device Manager (MDM) в дополнение к [групповой политике](./group-policies).</li>
</ul>
Версия BITS 10,2 включена в обновление Windows 10 октября 2018 (10.0; Сборка 17763) и более поздние версии.
</td>
</tr>
<tr class="odd">
<td>Версия 10,1</td>
<td>Новые функции<br/>
<ul>
<li>Добавлены <a href="/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6"><strong>BackgroundCopyFile6</strong></a> и <a href="/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3"><strong>IBackgroundCopyCallback3</strong></a> , позволяющие выполнять сценарии произвольного доступа для загрузок HTTP.</li>
<li>В перечисление <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a> добавлены <strong>BITS_JOB_PROPERTY_ON_DEMAND_MODE</strong> и <strong>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</strong> , что позволяет настроить поведение при загрузке и уведомлении соответственно.</li>
</ul>
Версия BITS 10,1 включена в обновление Windows 10 Creator и более поздние версии.
</td>
</tr>
<tr class="even">
<td>Версия 5.0</td>
<td>Новые функции<br/>
<ul>
<li>Добавлен интерфейс <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> , который добавляет универсальные методы для получения и задания свойств задания BITS для методов, унаследованных от интерфейса <a href="/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4"><strong>IBackgroundCopyJob4</strong></a> .<br/> Сведения об использовании нового интерфейса <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> см. в разделе <a href="how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md">Управление возможностью загрузки задания BITS через дорогостоящее подключение</a> и <a href="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job.md">Получение последнего набора заголовков HTTP, полученных для каждого файла в задании загрузки BITS</a>.<br/></li>
<li>Добавлены <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_job_property_value"><strong>BITS_JOB_PROPERTY_VALUE</strong></a> объединения, <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a>и <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy"><strong>BITS_JOB_TRANSFER_POLICY</strong></a> перечисления. Примеры использования см. в приведенных выше разделах.</li>
<li>Добавлен интерфейс <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> , который добавляет методы для получения и установки универсальных свойств объектов баккграундкопифиле в методы, унаследованные от интерфейса <a href="/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4"><strong>IBackgroundCopyFile4</strong></a> . Добавление универсальных свойств позволит улучшить возможности Баккграундкопифиле в будущем, не требуя создания нового интерфейса.</li>
<li>Первое универсальное свойство, предоставляемое <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> , является свойством <strong>хттпреспонсехеадерс</strong> .</li>
<li>Добавлены <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value"><strong>BITS_FILE_PROPERTY_VALUE</strong></a> Union и перечисление <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id"><strong>BITS_FILE_PROPERTY_ID</strong></a> .</li>
</ul>
Служба BITS версии 5,0 включена в операционные системы Windows Server 2012 и Windows 8, где версия% WINDIR% \System32\QMgr.dll — &quot; 7.7. xxxx. xxxx &quot; .<br/> Следующие функции были добавлены в службу BITS в Windows 10<br/>
<ul>
<li>В Windows 10 версии 1607 можно использовать API-интерфейсы и командлеты PowerShell BITS (если они доступны) в удаленном сеансе PowerShell. Это особенно полезно при администрировании версий Windows Server 2016, которые не имеют возможности локального входа в систему. Задания BITS, запущенные через удаленные сеансы PowerShell, выполняются в контексте учетной записи пользователя сеанса и предпринимают какие-либо действия только при наличии по крайней мере одного активного локального сеанса входа в систему или удаленного сеанса PowerShell, связанных с этой учетной записью. Рассмотрите возможность использования постоянных удаленных сеансов PowerShell (см. <a href="/powershell/module/microsoft.powershell.core/new-pssession">New-PSSession</a>) для долго выполняющихся передач.</li>
<li>В Windows 10, версия 1607, теперь владелец задания BITS может задавать вспомогательные маркеры без прав администратора, если у вспомогательного токена нет возможностей администратора. Это сокращает уязвимость фоновых средств загрузки или обновления, позволяя им работать под учетной записью NetworkService с меньшими правами, а не под учетной записью с правами администратора.</li>
</ul>
Версия BITS 5,0 также включена в Windows 10, где версия% WINDIR% \System32\QMgr.dll — &quot; 7,8. xxxx &quot; . xxxx.<br/></td>
</tr>
<tr class="odd">
<td>Версия 4.0</td>
<td>Новые функции<br/>
<ul>
<li>Одноранговый кэш теперь использует Windows BranchCache. Эта новая модель однорангового кэширования заменяет модель, используемую для BITS версии 3,0. Дополнительные сведения см. в разделе <a href="peer-caching.md">одноранговое кэширование</a>.</li>
<li>Добавлена более гибкая модель доступа к ресурсам, позволяющая приложениям связать пару маркеров безопасности с заданием передачи BITS. Дополнительные сведения см. в разделе <a href="helper-tokens-for-bits-transfer-jobs.md">вспомогательные токены для заданий передачи BITS</a>.</li>
<li>Добавлен <a href="bits-compact-server.md">Облегченный сервер BITS</a>, который представляет собой изолированный файловый сервер HTTP/HTTPS, который обеспечивает возможность асинхронной передачи ограниченного числа больших файлов между компьютерами.</li>
<li>Добавлено более детализированное регулирование пропускной способности. Дополнительные сведения см. в разделе <a href="group-policies.md">групповые политики</a>.</li>
</ul>
Версия BITS 4,0 входит в операционные системы Windows Server 2008 R2 и Windows 7.<br/> Также можно загрузить BITS 4,0 для Windows Server 2008 с пакетом обновления 2 (SP2), Windows Vista с пакетом обновления 1 (SP1) и Windows Vista с пакетом обновления 2 (SP2). Сведения о скачивании BITS 4,0 см. в разделе <a href="https://support.microsoft.com/kb/968929">KB968929</a>.<br/> Версия% WINDIR% \System32\QMgr.dll — 7,5. &quot; XXXX. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Версия 3.0</td>
<td>Новые функции<br/>
<ul>
<li>Добавлено <a href="peer-caching.md">одноранговое кэширование</a> , которое позволяет скачивать содержимое с одноранговых узлов, а также передавать содержимое одноранговым узлам в сети домена.</li>
<li>Добавлено <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">уведомление</a> о том, когда файл загружается.</li>
<li>Доступ к <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">временному файлу</a> добавлен во время скачивания.</li>
<li>Добавлена возможность управления <a href="/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">перенаправлениями</a>HTTP.</li>
<li>Добавлены дополнительные <a href="group-policies.md">групповые политики</a> для управления кэшированием однорангового узла и ограничения времени загрузки.</li>
<li>В журнал системных событий добавлены события диагностики и устранения неполадок.</li>
<li>Добавлена поддержка <a href="user-account-control-and-bits.md">контроля учетных записей пользователей</a> (UAC).</li>
<li>В Windows Vista и более поздних версиях тип запуска BITS по умолчанию — отложенный автоматический запуск.</li>
</ul>
<blockquote>
[!Note]<br />
Теперь службы BITS используют групповые политики для ограничения количества заданий и файлов, которые можно создать. Это может повлиять на приложения, которые в настоящее время создают большое количество заданий или добавляют большое количество файлов в задание.
</blockquote>
<br/> <br/> Версия BITS 3,0 входит в операционные системы Windows Server 2008 и Windows Vista. <br/> Версия% WINDIR% \System32\QMgr.dll — &quot; 7.0. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Версия 2,5</td>
<td>Добавлена поддержка пользовательских заголовков HTTP, проверка подлинности клиента на основе сертификата для защищенных транспортов HTTP и IPv6. Также Добавлено использование счетчиков устройств шлюза Интернета (IGD) для более точного вычисления доступной <a href="network-bandwidth.md">пропускной способности</a>.<br/> Функции BITS 2,5 доступны в операционных системах Windows Server 2008, Windows Vista и Windows XP с пакетом обновления 3 (SP3). <br/> Также можно загрузить BITS 2,5 для Windows Server 2003 с пакетом обновления 2 (SP2), Windows Server 2003 с пакетом обновления 1 (SP1) и Windows XP с пакетом обновления 2 (SP2). Чтобы скачать BITS 2,5, перейдите в <a href="https://www.microsoft.com/download/details.aspx?id=4933">Центр загрузки Майкрософт</a> и установите KB923845.<br/> Версия% WINDIR% \System32\QMgr.dll — &quot; 6.7. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Версия 2,0</td>
<td>Добавлена поддержка выполнения параллельных загрузок переднего плана, использования путей SMB для удаленных имен, скачивания диапазонов файлов, изменения префикса или полного имени удаленного имени и ограничения использования пропускной способности клиента. Политика Жобинактивититимеаут теперь находится в разделе Конфигурация компьютера, административные шаблоны, сеть, фоновая интеллектуальная служба передачи (BITS).<br/> Версия BITS 2,0 входит в состав Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003 с пакетом обновления 1. Кроме того, можно загрузить BITS 2,0 для Windows Server 2003 и Windows XP. Чтобы скачать BITS 2,0, перейдите в <a href="https://www.microsoft.com/download/details.aspx?id=19031">Центр загрузки Майкрософт</a> и установите KB842773.<br/> Версия% WINDIR% \System32\QMgr.dll — 6,6. &quot; XXXX. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Версия 1,5</td>
<td>Добавлена возможность отправки и отправки-ответа, выполнения командной строки для событий, а затем явные учетные данные и учетные данные прокси-сервера.<br/> Начиная с BITS 1,5, пользователи с <a href="/windows/win32/secauthz/restricted-tokens">ограниченным маркером</a> не могут создавать или изменять задания.<br/> Служба BITS версии 1,5 включена в Windows Server 2003. Распространяемый пакет доступен для Windows XP в <a href="https://www.microsoft.com/download/details.aspx?id=22250">центре загрузки Майкрософт</a>.<br/> Версия% WINDIR% \System32\QMgr.dll — 6.5. &quot; XXXX. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Версия 1,2</td>
<td>Те же функциональные возможности, что и версия 1,0. Содержит внутренние обновления и улучшения.<br/> Версия BITS 1,2 входит в состав Windows XP с пакетом обновления 1 (SP1).<br/> Версия% WINDIR% \System32\QMgr.dll — 6.2. &quot; XXXX. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Версия 1.0</td>
<td>Начальный выпуск. Предоставляет приоритетные, регулируемые и асинхронные загрузки в фоновом или на переднем плане. Загружаемые файлы автоматически возобновляются после перезагрузки компьютера и отключения сети.<br/> Служба BITS версии 1,0 включена в Windows XP.<br/> Версия% WINDIR% \System32\QMgr.dll — &quot; 6.0. xxxx. xxxx &quot; .<br/></td>
</tr>
</tbody>
</table>

Чтобы включить в программу функции, основанные на возможностях BITS, используйте QueryInterface в (например,) объекта задания, чтобы определить, позволяет ли объект задания создавать необходимую версию. Кроме того, см. раздел [Определение версии BITS на компьютере](./determining-the-version-of-bits-on-a-computer.md) для преобразования номера версии QMgr.dll в версию BITS.

## <a name="version-103"></a>Версия 10,3

Для этой версии были добавлены следующие интерфейсы
-   [**IBackgroundCopyJobHttpOptions3**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3) 
     [ **Ибаккграундкописерверцертификатевалидатионкаллбакк**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)


## <a name="version-102"></a>Версия 10,2

Для этой версии были добавлены следующие интерфейсы
-   [**IBackgroundCopyJobHttpOptions2**](/windows/win32/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2)


## <a name="version-101"></a>Версия 10,1

Для этой версии были добавлены следующие интерфейсы
-   [**BackgroundCopyFile6**](/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6)
-   [**IBackgroundCopyCallback3**](/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3)

Следующие константы были добавлены для использования с [перечислением BITS_JOB_PROPERTY_ID](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id).

-   **\_свойство задания \_ BITS \_ в \_ \_ режиме запроса**
-   **\_ \_ \_ минимальное значение \_ \_ интервала уведомлений для свойства задания BITS \_ МС**


## <a name="version-50"></a>Версия 5.0

Для этой версии были добавлены следующие интерфейсы:

-   [**IBackgroundCopyJob5**](/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)

## <a name="version-40"></a>Версия 4.0

Для этой версии были добавлены следующие интерфейсы:

-   [**ибитстокен**](/windows/win32/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
-   [**IBackgroundCopyFile4**](/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4)

## <a name="version-30"></a>Версия 3.0

Для этой версии были добавлены следующие интерфейсы:

-   [**IBackgroundCopyCallback2**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2)
-   [**IBackgroundCopyFile3**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3)
-   [**IBackgroundCopyJob4**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)
-   [**ибитспир**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeer)
-   [**ибитспиркачеадминистратион**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration)
-   [**ибитспиркачерекорд**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacherecord)
-   [**иенумбитспиркачерекордс**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords)
-   [**иенумбитспирс**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeers)

Следующие константы были добавлены для использования с методом [**ибаккграундкопижобхттпоптионс:: сетсекуритифлагс**](/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) :

-   **\_ \_ политика перенаправления HTTP BG \_ \_ разрешает \_ Автоматическое выполнение**
-   **\_ \_ \_ \_ отчет разрешения политики перенаправления HTTP BG \_**
-   **\_ \_ запретить политику перенаправления HTTP BG \_ \_**
-   **\_ \_ Маска политики перенаправления HTTP-запроса BG \_ \_**
-   **\_ \_ политика перенаправления HTTP BG \_ разрешает протокол \_ \_ HTTPS \_ для \_ http**

## <a name="version-25"></a>Версия 2,5

Следующий интерфейс и перечисление были добавлены для версии 2,5:

-   [**ибаккграундкопижобхттпоптионс**](/windows/win32/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions)
-   [**\_ \_ расположение хранилища сертификатов \_ BG**](/windows/win32/api/Bits2_5/ne-bits2_5-bg_cert_store_location)

## <a name="version-20"></a>Версия 2,0

Следующие интерфейсы, структура и разделы были добавлены для версии 2,0:

-   [**IBackgroundCopyJob3**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)
-   [**IBackgroundCopyFile2**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2)
-   [**\_диапазон файлов \_ BG**](/windows/win32/api/Bits2_0/ns-bits2_0-bg_file_range)
-   [Групповые политики](group-policies.md)

Сведения о параллельных загрузках переднего плана см. в разделе "Примечания" для [**\_ \_ приоритета задания BG**](/windows/win32/api/Bits/ne-bits-bg_job_priority).

Сведения об использовании протокола SMB см. в разделе [**\_ \_ сведения о файле BG**](/windows/win32/api/Bits/ns-bits-bg_file_info).

## <a name="version-15"></a>Версия 1,5

Следующие интерфейсы и разделы были добавлены для версии 1,5:

-   [**IBackgroundCopyJob2**](/windows/win32/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
-   [Получение ответа из задания Upload-Reply](retrieving-the-reply-from-an-upload-reply-job.md)
-   [Регистрация для выполнения программы](registering-to-execute-a-program.md)
-   [Параметры сервера BITS для заданий отправки](bits-server-settings-for-upload-jobs.md)
-   [Настройка сервера для отправки](setting-up-the-server-for-uploads.md)
-   [Использование заголовков запросов и ответов BITS](using-bits-notification-request-response-headers.md)

 
## <a name="updating-bits-versions"></a>Обновление версий BITS
 
Вы можете загрузить BITS 4,0 для Windows Server 2008 с пакетом обновления 2 (SP2), Windows Vista с пакетом обновления 1 (SP1) и Windows Vista с пакетом обновления 2 (SP2). Сведения о скачивании BITS 4,0 см. в разделе [KB968929](https://support.microsoft.com/kb/968929).
