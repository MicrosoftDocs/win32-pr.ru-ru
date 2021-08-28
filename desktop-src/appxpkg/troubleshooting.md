---
title: Устранение проблем с упаковкой и развертыванием приложений для Windows, а также с обращением к ним
description: Используйте эти рекомендации для устранения неполадок, возникающих при упаковке, развертывании или выполнении запросов к пакету приложения.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: c6438f9a8d600e9df6956f61bb6317cec575c57f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480600"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a>Устранение проблем с упаковкой и развертыванием приложений для Windows, а также с обращением к ним

используйте эти рекомендации для устранения неполадок, возникающих при упаковке, развертывании или запросе пакета приложения Windows (. msix/. appx) в качестве разработчика.

> [!NOTE]
> Эта статья предназначена для разработчиков. если вы не являетесь разработчиком и ищете справку по Windows ошибке установки приложения, см. статью [поддержка Windows](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).

## <a name="get-diagnostic-information"></a>Получение диагностических сведений

При сбое API возвращается код ошибки, описывающий проблему. Если код ошибки не содержит достаточно сведений, вы найдете дополнительные диагностические сведения в подробных журналах событий.

Чтобы получить доступ к журналам событий упаковки и развертывания с помощью **Просмотр событий**, выполните следующие действия.

1. Выполните одно из следующих действий.

    * в меню Windows выберите пункт **пуск** , введите **Просмотр событий** и **нажмите клавишу ввод**.
    * Запустите **eventvwr. msc**.

2. на левой странице разверните узлы **Просмотр событий (локальные)**  >  **журналы приложений и служб**  >  **Microsoft**  >  **Windows**.
3. Проверьте наличие доступных журналов в следующих категориях:

    * **AppxPackagingOM**  >  **Microsoft-Windows-аппкспаккагинг/эксплуатация**
    * **AppXDeployment — сервер**  >  **Microsoft-Windows-AppXDeploymentServer/эксплуатация**

Начните с просмотра журналов в разделе **AppXDeployment-Server**. Если ошибка вызвана **0x80073CF0** или **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, в журналах **AppxpackagingOM** могут присутствовать дополнительные сведения.

Вы также можете использовать команду [Get-аппкслог](/powershell/module/appx/get-appxlog) в PowerShell, чтобы получить первые несколько зарегистрированных событий. В следующем примере отображаются журналы, связанные с последней операцией развертывания.

```PowerShell
Get-Appxlog
```

В следующем примере отображаются журналы, связанные с последней операцией развертывания в интерактивной таблице в отдельном окне.

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a>Коды распространенных ошибок

В этой таблице перечислены некоторые из наиболее распространенных кодов ошибок. Если вам нужна дополнительная помощь по одной из этих ошибок или если вы столкнулись с кодом ошибки, отсутствующим в этом списке, см. раздел [Дополнительные параметры справки](#get-additional-help).


| Код ошибки | Значение | Описание и возможные причины | 
|------------|-------|---------------------------------|
| <strong>E_FILENOTFOUND</strong> | 0x80070002 | Файл или путь не найден. Это может произойти во время проверки библиотеки типов COM, так как в рамках пакета MSIX путь к каталогу действительно существует.<br /> | 
| <strong>ERROR_BAD_FORMAT</strong> | 0x8007000B | Пакет имеет неправильный формат и нуждается в повторной сборке или повторной подписи.<br /> Эта ошибка может возникнуть в случае несоответствия между именем субъекта сертификата подписи и именем издателя AppxManifest.xml.<br /> См. раздел <a href="how-to-sign-a-package-using-signtool.md">как подписать пакет приложения с помощью средства SignTool</a>.<br /> | 
| <strong>E_INVALIDARG</strong> | 0x80070057 | Один или несколько аргументов недопустимы. Если проверить журнал событий AppXDeployment-Server и просмотреть следующее событие: "при установке пакета система не смогла зарегистрировать расширение Windows. Репоситорекстенсион из-за следующей ошибки: неправильный параметр". <br /> эта ошибка может возникать, если элементы манифеста DisplayName или Description содержат символы, запрещенные Windows брандмауэром. а именно  |  и все, из-за которых Windows не удалось создать профиль AppContainer для пакета. Удалите эти символы из манифеста и попробуйте установить пакет. <br /> | 
| <strong>ERROR_INSTALL_OPEN_</strong><br /><strong>PACKAGE_FAILED</strong><br /> | 0x80073CF0 | Не удалось открыть пакет.<br /> Возможные причины:<br /><ul><li>Пакет не подписан.</li><li>Имя издателя не соответствует субъекту сертификата подписи.</li><li>Отсутствует префикс file://, или не удалось найти пакет в указанном расположении.</li></ul>Дополнительные сведения см. в журнале событий <strong>AppxPackagingOM</strong> .<br /> | 
| <strong>ERROR_INSTALL_PACKAGE_</strong><br /><strong>NOT_FOUND</strong><br /> | 0x80073CF1 | Не удалось найти пакет.<br /> Эта ошибка может возникнуть при удалении пакета, который не установлен для текущего пользователя.<br /> | 
| <strong>ERROR_INSTALL_INVALID_</strong><br /><strong>ПАКЕТЫ</strong><br /> | 0x80073CF2 | Данные пакета недопустимы.<br /> | 
| <strong>ERROR_INSTALL_RESOLVE_</strong><br /><strong>DEPENDENCY_FAILED</strong><br /> | 0x80073CF3 | Пакет не прошел проверку обновлений, зависимостей или конфликтов.<br /> Возможные причины:<br /><ul><li>Входящий пакет конфликтует с установленным пакетом.</li><li>Не удается найти указанную зависимость пакета.</li><li>Пакет не поддерживает правильную архитектуру процессора.</li></ul>Дополнительные сведения см. в журнале событий <strong>AppXDeployment-Server</strong> .<br /> | 
| <strong>ERROR_INSTALL_OUT_</strong><br /><strong>OF_DISK_SPACE</strong><br /> | 0x80073CF4 | На компьютере недостаточно дискового пространства. Освободите место и повторите попытку.<br /> | 
| <strong>ERROR_INSTALL_NETWORK_</strong><br /><strong>СОСТОЯНИЕ</strong><br /> | 0x80073CF5 | Не удается скачать пакет.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>REGISTRATION_FAILURE</strong><br /> | 0x80073CF6 | Не удается зарегистрировать пакет.<br /> Дополнительные сведения см. в журнале событий <strong>AppXDeployment-Server</strong> .<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>DEREGISTRATION_EFAILURE</strong><br /> | 0x80073CF7 | Не удается отменить регистрацию пакета.<br /> Эта ошибка может возникнуть при удалении пакета.<br /> Дополнительные сведения см. в журнале событий <strong>AppXDeployment-Server</strong> .<br /> | 
| <strong>ERROR_INSTALL_CANCEL</strong> | 0x80073CF8 | Пользователь отменил запрос на установку.<br /> | 
| <strong>ERROR_INSTALL_FAILED</strong> | 0x80073CF9 | Не удалось установить пакет. Обратитесь к поставщику программного обеспечения.<br /> Дополнительные сведения см. в журнале событий <strong>AppXDeployment-Server</strong> .<br /> | 
| <strong>ERROR_REMOVE_FAILED</strong> | 0x80073CFA | Не удалось удалить пакет.<br /> Эта ошибка может возникнуть при сбоях при удалении пакета.<br /> Дополнительные сведения см. в разделе <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>ремовепаккажеасинк</strong></a>.<br /> | 
| <strong>ERROR_PACKAGE_</strong><br /><strong>ALREADY_EXISTS</strong><br /> | 0x80073CFB | Предоставленный пакет уже установлен, и переустановка пакета заблокирована. <br /> Эта ошибка может возникать при установке пакета, который не является побитовым, идентичным пакету, который уже установлен. Обратите внимание, что цифровая подпись также является частью пакета. Следовательно, если пакет перестраивается или повторно подписан, он больше не будет побитовым, идентичным ранее установленному пакету. Существует два возможных варианта исправления этой ошибки: (1) увеличение номера версии приложения, затем повторное создание и повторная подпись пакета (2) удаление старого пакета для каждого пользователя в системе перед установкой нового пакета. <br /> | 
| <strong>ERROR_NEEDS_REMEDIATION</strong> | 0x80073CFC | Не удается запустить приложение. Попробуйте переустановить приложение.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>PREREQUISITE_FAILED</strong><br /> | 0x80073CFD | Не удалось удовлетворить указанную предварительную проверку.<br /> | 
| <strong>ERROR_PACKAGE_</strong><br /><strong>REPOSITORY_CORRUPTED</strong><br /> | 0x80073CFE | Репозиторий пакетов поврежден.<br /> Эта ошибка может возникать, если папка, на которую ссылается этот раздел реестра, не существует или повреждена: <br /><strong>По адресу hklm\software\microsoft\microsoft Windows\</strong><br /><strong>куррентверсион\аппкс\паккажерепоситорирут</strong><br /> Для восстановления после этого состояния обновите компьютер.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>POLICY_FAILURE</strong><br /> | 0x80073CFF | Для установки этого приложения требуется лицензия разработчика или система, поддерживающая загрузку неопубликованных приложений. <br /> Эта ошибка может возникнуть, если пакет не соответствует одному из следующих требований:<br /><ul><li>приложение развертывается с помощью команды F5 в Visual Studio на компьютере с лицензией Windows developer.</li><li>пакет подписывается подписью майкрософт и развертывается как часть Windows или из Microsoft Store.</li><li>пакет подписывается доверенной подписью и устанавливается на компьютере с лицензией разработчика, присоединенным к домену компьютеру с включенной политикой AllowAllTrustedApps или на компьютере с лицензией на неWindowsную загрузку неопубликованных приложений с включенной политикой AllowAllTrustedApps.</li></ul> | 
| <strong>ERROR_PACKAGE_UPDATING</strong> | 0x80073D00 | Не удается запустить приложение, так как оно сейчас обновляется.<br /> | 
| <strong>ERROR_DEPLOYMENT_</strong><br /><strong>BLOCKED_BY_POLICY</strong><br /> | 0x80073D01 | Операция развертывания пакета заблокирована политикой. Обратитесь к системному администратору.<br /> Возможные причины:<br /><ul><li>Развертывание пакетов блокируется политиками управления приложениями.</li><li>Развертывание пакета блокируется политикой "разрешить операции развертывания в особых профилях".</li></ul>Одна из возможных причин — потребность в перемещаемом профиле. Сведения о настройке перемещаемых профилей пользователей в учетных записях пользователей см. в статье <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">развертывание перемещаемых профилей пользователей</a>. Если в системе нет настроенных политик и вы по-прежнему видите эту ошибку, возможно, вы выполнили вход с временным профилем. Выйдите из журнала и снова войдите в систему, а затем повторите операцию.<br /> | 
| <strong>ERROR_PACKAGES_IN_USE</strong> | 0x80073D02 | Не удалось установить пакет, так как ресурсы, которые он изменяет, сейчас используются.<br /> | 
| <strong>ERROR_RECOVERY_</strong><br /><strong>FILE_CORRUPT</strong><br /> | 0x80073D03 | Не удалось восстановить пакет, так как данные, необходимые для восстановления, повреждены.<br /> | 
| <strong>ERROR_INVALID_</strong><br /><strong>STAGED_SIGNATURE</strong><br /> | 0x80073D04 | Недопустимая подпись. Для регистрации в режиме разработчика необходимо, чтобы AppxSignature. p7x и AppxBlockMap.xml были допустимыми или не должны присутствовать.<br /> если вы разработчик, использующий клавишу F5 с Visual Studio, убедитесь, что в каталоге проекта не содержится сигнатура или файлы схемы блокировки из предыдущих версий пакета.<br /> | 
| <strong>ERROR_DELETING_EXISTING_</strong><br /><strong>APPLICATIONDATA_STORE_FAILED</strong><br /> | 0x80073D05 | Произошла ошибка при удалении ранее существующих данных приложения пакета.<br /> Эта ошибка может возникнет, если <a href="/previous-versions/hh441475(v=vs.110)">симулятор</a> работает. Закройте симулятор. Эту ошибку также можно получить, если в данных приложения открыты файлы (например, если в текстовом редакторе открыт файл журнала).<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>PACKAGE_DOWNGRADE</strong><br /> | 0x80073D06 | Не удалось установить пакет, так как уже установлена более поздняя версия этого пакета.<br /> | 
| <strong>ERROR_SYSTEM_</strong><br /><strong>NEEDS_REMEDIATION</strong><br /> | 0x80073D07 | Обнаружена ошибка в системном двоичном файле. Чтобы устранить эту проблему, попробуйте обновить компьютер. <br /> | 
| <strong>ERROR_APPX_INTEGRITY_</strong><br /><strong>FAILURE_EXTERNAL</strong><br /> | 0x80073D08 | в системе обнаружен поврежденный не Windows двоичный файл. <br /> | 
| <strong>ERROR_RESILIENCY_</strong><br /><strong>FILE_CORRUPT</strong><br /> | 0x80073D09 | Не удалось возобновить операцию, так как данные, необходимые для восстановления, повреждены. <br /> | 
| <strong>ERROR_INSTALL_FIREWALL_</strong><br /><strong>SERVICE_NOT_RUNNING</strong><br /> | 0x80073D0A | не удалось установить пакет, так как служба брандмауэра Windows не запущена. включите службу брандмауэра Windows и повторите попытку.<br /> | 
| <strong>ERROR_PACKAGE_MOVE_FAILED</strong> | 0x80073D0B | Сбой операции перемещения пакета.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>NOT_EMPTY</strong><br /> | 0x80073D0C | Не удалось выполнить операцию развертывания, так как том не пуст.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>РАБОТА</strong><br /> | 0x80073D0D | Не удалось выполнить операцию развертывания, так как том находится вне сети. Для обновления пакета том ссылается на установленный том всех версий пакета.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>ПОВРЕЖДЕН</strong><br /> | 0x80073D0E | Не удалось выполнить операцию развертывания, так как указанный том поврежден.<br /> | 
| <strong>ERROR_NEEDS_REGISTRATION</strong><br /><strong></strong><br /> | 0x80073D0F | Не удалось выполнить операцию развертывания, так как указанное приложение должно быть зарегистрировано в первую очередь.<br /> | 
| <strong>ERROR_INSTALL_WRONG_</strong><br /><strong>PROCESSOR_ARCHITECTURE</strong><br /> | 0x80073D10 | Не удалось выполнить операцию развертывания, так как пакет предназначен для неверной архитектуры процессора.<br /> | 
| <strong>ERROR_DEV_SIDELOAD_</strong><br /><strong>LIMIT_EXCEEDED</strong><br /> | 0x80073D11 | Достигнуто максимальное число пакетов загруженные неопубликованные для разработчиков, разрешенных на этом устройстве. Удалите пакет загруженные неопубликованные и повторите попытку.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_</strong><br /><strong>MAIN_PACKAGE</strong><br /> | 0x80073D12 | Для установки этого дополнительного пакета требуется основной пакет приложения. Сначала установите основной пакет и повторите попытку.<br /> | 
| <strong>ERROR_PACKAGE_NOT_</strong><br /><strong>SUPPORTED_ON_FILESYSTEM</strong><br /> | 0x80073D13 | Этот тип пакета приложения не поддерживается в этой файловой системе.<br /> | 
| <strong>ERROR_PACKAGE_MOVE_</strong><br /><strong>BLOCKED_BY_STREAMING</strong><br /> | 0x80073D14 | Операция перемещения пакета блокируется до завершения потоковой передачи приложения.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_APPLICATIONID_</strong><br /><strong>NOT_UNIQUE</strong><br /> | 0x80073D15 | Основной или другой необязательный пакет приложения имеет тот же идентификатор приложения, что и этот дополнительный пакет. Измените идентификатор приложения для дополнительного пакета, чтобы избежать конфликтов.<br /> | 
| <strong>ERROR_PACKAGE_STAGING_</strong><br /><strong>ONHOLD</strong><br /> | 0x80073D16 | Этот промежуточный сеанс удерживается, чтобы можно было задать приоритет для другой промежуточной операции.<br /> | 
| <strong>ERROR_INSTALL_INVALID_</strong><br /><strong>RELATED_SET_UPDATE</strong><br /> | 0x80073D17 | Связанный набор не может быть обновлен, так как обновленный набор является недопустимым. Все пакеты в связанном наборе должны быть обновлены одновременно.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br /> | 0x80073D18 | Необязательный пакет с точкой входа FullTrust требует, чтобы основной пакет имел возможность <strong>рунфуллтруст</strong> .<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_USER_LOG_OFF</strong><br /> | 0x80073D19 | Произошла ошибка, так как пользователь вышел из системы.<br /> | 
| <strong>ERROR_PROVISION_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_PROVISIONED</strong><br /> | 0x80073D1A | Для необязательной подготовки пакета требуется также подготовка основного пакета зависимостей.<br /> | 
| <strong>ERROR_PACKAGES_REPUTATION_</strong><br /><strong>CHECK_FAILED</strong><br /> | 0x80073D1B | Пакеты не прошли <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">проверку репутации SmartScreen</a>.<br /> | 
| <strong>ERROR_PACKAGES_REPUTATION_</strong><br /><strong>CHECK_TIMEDOUT</strong><br /> | 0x80073D1C | Истекло время ожидания операции <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">проверки репутации SmartScreen</a> .<br /> | 
| <strong>ERROR_DEPLOYMENT_OPTION_</strong><br /><strong>NOT_SUPPORTED</strong><br /> | 0x80073D1D | Текущий вариант развертывания не поддерживается.<br /> | 
| <strong>ERROR_APPINSTALLER_</strong><br /><strong>ACTIVATION_BLOCKED</strong><br /> | 0x80073D1E | Активация заблокирована из-за параметров обновления. appinstaller для этого приложения.<br /> | 
| <strong>ERROR_REGISTRATION_FROM_</strong><br /><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong><br /> | 0x80073D1F | Удаленные диски не поддерживаются. Используйте <strong> \\ server\share</strong> для регистрации удаленного пакета.<br /> | 
| <strong>ERROR_APPX_RAW_</strong><br /><strong>DATA_WRITE_FAILED</strong><br /> | 0x80073D20 | Не удалось обработать и записать Скачанные данные пакета на диск.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_VOLUME_POLICY_PACKAGE</strong><br /> | 0x80073D21 | Операция развертывания была заблокирована из-за политики семейства пакетов, запрещающей развертывания на несистемном томе. Для каждой политики это приложение должно быть установлено на системный диск, но не задано по умолчанию. в служба хранилища параметры сделайте системный диск расположением по умолчанию, чтобы сохранить новое содержимое, а затем повторите попытку установки.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_VOLUME_POLICY_MACHINE</strong><br /> | 0x80073D22 | Операция развертывания была заблокирована из-за того, что политики на уровне компьютера ограничивают развертывания на несистемном томе. Для каждой политики это приложение должно быть установлено на системный диск, но не задано по умолчанию. в служба хранилища параметры сделайте системный диск расположением по умолчанию, чтобы сохранить новое содержимое, а затем повторите попытку установки.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_PROFILE_POLICY</strong><br /> | 0x80073D23 | Операция развертывания была заблокирована, так как не разрешается использовать специальное развертывание профиля (специальные профили — это профили пользователей, в которых изменения удаляются после выхода пользователя из программы). Попробуйте войти в учетную запись, которая не является специальным профилем. Вы можете попробовать выйти из учетной записи и войти в нее снова или войти в другую учетную запись.<br /> | 
| <strong>ERROR_DEPLOYMENT_FAILED_</strong><br /><strong>CONFLICTING_MUTABLE_PACKAGE_</strong><br /><strong>КАТАЛОГИ</strong><br /> | 0x80073D24 | Не удалось выполнить операцию развертывания из-за конфликта <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">изменяемого каталога пакета</a>пакета. Чтобы установить этот пакет, удалите существующий пакет с конфликтующим изменяемым каталогом пакета.<br /> | 
| <strong>ERROR_SINGLETON_RESOURCE_</strong><br /><strong>INSTALLED_IN_ACTIVE_USER</strong><br /> | 0x80073D25 | Не удалось установить пакет, так как был указан одноэлементный ресурс, а другой пользователь с установленным пакетом вошел в систему. Убедитесь, что все активные пользователи с установленным пакетом, вышли из системы, и повторите попытку установки.<br /> | 
| ERROR_DIFFERENT_VERSION_<strong></strong><br /><strong>OF_PACKAGED_SERVICE_INSTALLED</strong><br /> | 0x80073D26 | Произошел сбой установки пакета, так как установлена другая версия службы. Попробуйте установить более новую версию пакета.<br /> | 
| <strong>ERROR_SERVICE_EXISTS_</strong><br /><strong>AS_NON_PACKAGED_SERVICE</strong><br /> | 0x80073D27 | Произошел сбой установки пакета, так как версия службы существует за пределами пакета. msix/. appx. Обратитесь к поставщику программного обеспечения.<br /> | 
| <strong>ERROR_PACKAGED_SERVICE_</strong><br /><strong>REQUIRES_ADMIN_PRIVILEGES</strong><br /> | 0x80073D28 | Не удалось установить пакет, так как требуются права администратора. Обратитесь к администратору, чтобы установить этот пакет.<br /> | 
| <strong>ERROR_REDIRECTION_TO_</strong><br /><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong><br /> | 0x80073D29 | Не удалось выполнить развертывание пакета, так как операция была перенаправлена на учетную запись по умолчанию, когда вызывающий объект не сделает этого.<br /> | 
| <strong>ERROR_PACKAGE_LACKS_</strong><br /><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong><br /> | 0x80073D2A | Не удалось выполнить развертывание пакета, так как для пакета требуется возможность, предназначенная для этого узла изначально.<br /> | 
| <strong>ERROR_UNSIGNED_PACKAGE_</strong><br /><strong>INVALID_CONTENT</strong><br /> | 0x80073D2B | Не удалось выполнить развертывание пакета, так как его содержимое недопустимо для неподписанного пакета.<br /> | 
| <strong>ERROR_UNSIGNED_PACKAGE_</strong><br /><strong>INVALID_PUBLISHER_NAMESPACE</strong><br /> | 0x80073D2C | Не удалось выполнить развертывание пакета, так как его издатель отсутствует в неподписанном пространстве имен.<br /> | 
| <strong>ERROR_SIGNED_PACKAGE_</strong><br /><strong>INVALID_PUBLISHER_NAMESPACE</strong><br /> | 0x80073D2D | Не удалось выполнить развертывание пакета, так как его издатель отсутствует в подписанном пространстве имен.<br /> | 
| <strong>ERROR_PACKAGE_EXTERNAL_</strong><br /><strong>LOCATION_NOT_ALLOWED</strong><br /> | 0x80073D2E | Не удалось выполнить развертывание пакета, так как его издатель отсутствует в подписанном пространстве имен.<br /> | 
| <strong>ERROR_INSTALL_FULLTRUST_</strong><br /><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br /> | 0x80073D2F | Зависимость среды выполнения узла, разрешающая пакет с содержимым с полным доверием, требует, чтобы основной пакет имел возможность <strong>рунфуллтруст</strong> .<br /> | 
| <strong>APPX_E_PACKAGING_INTERNAL</strong> | 0x80080200 | В API упаковки произошла внутренняя ошибка.<br /> | 
| <strong>APPX_E_INTERLEAVING_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080201 | Пакет является недопустимым, так как его содержимое чередование.<br /> | 
| <strong>APPX_E_RELATIONSHIPS_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080202 | Пакет является недопустимым, так как он содержит связи OPC.<br /> | 
| <strong>APPX_E_MISSING_</strong><br /><strong>REQUIRED_FILE</strong><br /> | 0x80080203 | Пакет является недопустимым, так как в нем отсутствует манифест или сопоставлена блокировка, или имеется файл с целостностью кода, но отсутствует файл сигнатуры.<br /> Убедитесь, что в пакете отсутствует один или несколько необходимых файлов:<br /><ul><li>\AppxManifest.xml</li><li>\AppxBlockMap.xml</li></ul>Если пакет содержит \Аппксметадата\кодеинтегрити.Кат, он также должен содержать \AppxSignature.p7x.<br /> | 
| <strong>APPX_E_INVALID_MANIFEST</strong> | 0x80080204 | Недопустимый файл AppxManifest.xml пакета.<br /> | 
| <strong>APPX_E_INVALID_BLOCKMAP</strong> | 0x80080205 | Недопустимый файл AppxBlockMap.xml пакета.<br /> | 
| <strong>APPX_E_CORRUPT_CONTENT</strong> | 0x80080206 | Не удается прочитать содержимое пакета, так как оно повреждено.<br /> | 
| <strong>APPX_E_BLOCK_</strong><br /><strong>HASH_INVALID</strong><br /> | 0x80080207 | Вычисленное хэш-значение блока не соответствует значению, хранящемуся в карте блоков.<br /> | 
| <strong>APPX_E_REQUESTED_</strong><br /><strong>RANGE_TOO_LARGE</strong><br /> | 0x80080208 | Запрошенный диапазон байтов превышает 4 ГБ при преобразовании в диапазон байтов блоков.<br /> | 
| <strong>TRUST_E_NOSIGNATURE</strong> | 0x800B0100 | В теме отсутствует подпись.<br /> Эта ошибка может возникать, если пакет не подписан или подпись недействительна. Пакет должен быть подписан для развертывания.<br /> | 
| <strong>CERT_E_UNTRUSTEDROOT</strong> | 0x800B0109 | Цепочка сертификатов обработана, но была прервана в корневом сертификате, который не является доверенным для поставщика доверия.<br /> См. раздел <a href="/previous-versions/br230260(v=vs.110)">Подписывание пакета</a>.<br /> | 
| <strong>CERT_E_CHAINING</strong> | 0x800B010A | Не удалось построить цепочку сертификатов для доверенного корневого центра сертификации.<br /> См. раздел <a href="/previous-versions/br230260(v=vs.110)">Подписывание пакета</a>.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>SIP_CLIENT_DATA</strong><br /> | 0x80080209 | Структура <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>, используемая для подписи пакета, не содержит необходимых данных<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>KEY_INFO</strong><br /> | 0x8008020A | Структура <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> , используемая для шифрования или расшифровки пакета, содержит недопустимые данные.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>контентграупмап</strong><br /> | 0x8008020B | Сопоставленная группа содержимого пакета. msix/. appx недопустима.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>APPINSTALLER</strong><br /> | 0x8008020C | Недопустимый <a href="/windows/msix/app-installer/app-installer-root">файл appinstaller</a> для пакета.<br /> | 
| <strong>APPX_E_DELTA_BASELINE_</strong><br /><strong>VERSION_MISMATCH</strong><br /> | 0x8008020D | Базовая версия пакета в разностном пакете не соответствует версии базового пакета для обновления.<br /> | 
| <strong>APPX_E_DELTA_PACKAGE_</strong><br /><strong>MISSING_FILE</strong><br /> | 0x8008020E | В разностном пакете отсутствует файл из обновленного пакета.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>DELTA_PACKAGE</strong><br /> | 0x8008020F | Недопустимый разностный пакет.<br /> | 
| <strong>APPX_E_DELTA_APPENDED_</strong><br /><strong>PACKAGE_NOT_ALLOWED</strong><br /> | 0x80080210 | Добавленный Дельта-пакет не разрешен для текущей операции.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>PACKAGING_LAYOUT</strong><br /> | 0x80080211 | Недопустимый файл макета упаковки.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>паккажесигнконфиг</strong><br /> | 0x80080212 | Недопустимый файл Паккажесигнконфиг.<br /> | 
| <strong>APPX_E_RESOURCESPRI_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080213 | Файл Resources. PRI не разрешен, если в манифесте пакета нет элементов ресурсов.<br /> | 
| <strong>APPX_E_FILE_</strong><br /><strong>COMPRESSION_MISMATCH</strong><br /> | 0x80080214 | Состояние сжатия файла в базовом плане и обновленный пакет не совпадают.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>PAYLOAD_PACKAGE_EXTENSION</strong><br /> | 0x80080215 | Расширения, отличные от. appx, не разрешены для пакетов полезных данных, предназначенных для старых платформ.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong><br /> | 0x80080216 | Недопустимый файл Енкриптионексклусионфилелист.<br /> | 


## <a name="applications-dont-start-and-their-names-are-dimmed"></a>Приложения не запускаются, и их имена недоступны

на компьютере, основанном на Windows 10, нельзя запускать некоторые приложения, и имена приложений отображаются серым цветом.

![некоторые имена приложений в меню недоступны.](./images/app-names-dimmed.png)

При попытке открыть приложение, выбрав затененное имя, может появиться одно из следующих сообщений об ошибке:

> Возникла проблема с \<*application name*> . Обратитесь к системному администратору, чтобы восстановить или переустановить его.  
> Ошибка: это приложение не может быть открыто

кроме того, следующие записи событий регистрируются в журнале «Microsoft-Windows-твинуи/эксплуатация» в разделе **applications and сервицес\микрософт\ Windows \аппс**:

> имя журнала: Microsoft-Windows-твинуи/эксплуатация  
> источник: Microsoft-Windows-иммерсивное-Shell  
> Дата: <*Дата*>  
> Идентификатор события: 5960  
> Категория задачи: (5960)  
> Уровень: ошибка  
> Ключевые слова:  
> Описание.  
> Активация приложения Microsoft.BingNews_8wekyb3d8bbwe! Аппексневс для Windows. Контракт запуска заблокирован с ошибкой 0x80073CFC, так как его пакет находится в состоянии: изменен.  

### <a name="cause"></a>Причина

Эта проблема возникает из-за изменения записи реестра для значения состояния соответствующего пакета приложения.

### <a name="resolution"></a>Решение

> [!WARNING]
> При неправильном изменении реестра с помощью редактора реестра или иного метода могут возникнуть серьезные проблемы. Эти проблемы могут потребовать переустановки операционной системы. Корпорация Майкрософт не гарантирует, что такие неполадки могут быть устранены. Ответственность за изменение реестра лежит на пользователе.

Чтобы устранить эту проблему:

1. Откройте редактор реестра и найдите подраздел **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** .
2. Чтобы создать резервную копию данных подраздела, щелкните правой кнопкой мыши **паккажелист**, выберите пункт **Экспорт**, а затем сохраните данные в виде файла реестра.
3. Для каждого из приложений, перечисленных в записях журнала Event ID 5960, выполните следующие действия.  
   1. Откройте запись **паккажестатус** .
   2. Установите значение **паккажестатус** равным нулю (**0**).
   > [!NOTE]  
   > Если в **паккажелист** нет записей для приложения, значит, у проблемы есть другая причина. В случае с примером события в этой статье полный подраздел — **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**
4. Перезагрузите компьютер.

## <a name="get-additional-help"></a>Получите дополнительную справку

если вам нужна дополнительная помощь по устранению проблемы, которая возникает при упаковке, развертывании или запросе пакета приложения Windows (. msix/. appx) в качестве разработчика, обратитесь к этим дополнительным ресурсам поддержки для разработчиков.

- [Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) предоставляет актуальные и своевременные ответы на технические проблемы от сообщества экспертов и инженеров Майкрософт.
- Для помощи в сообществе с вопросами по разработке есть наши [форумы](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)и [StackOverflow](https://stackoverflow.com/questions).
- на сайте [поддержки Windows developer](https://developer.microsoft.com/windows/support) описаны другие варианты поддержки.

## <a name="related-topics"></a>Связанные темы

- [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Подписывание пакета приложения с помощью SignTool)
- [Устранение ошибок подписи пакета приложения](how-to-troubleshoot-app-package-signature-errors.md)
