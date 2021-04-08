---
title: API запросов пакетов
description: Сведения о API запросов пакетов, который можно использовать для получения сведений о пакетах приложений, установленных в системе. Каждый пакет приложения содержит файлы, составляющие приложение Windows, и файл манифеста, описывающий программное обеспечение для Windows.
ms.assetid: EDDFC8B1-E224-4921-BED6-FC81711BA5BF
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 5632edf661b4ea82177473bbb35f2674674500c6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069829"
---
# <a name="package-query-api"></a>API запросов пакетов

Сведения о API запросов пакетов, который можно использовать для получения сведений о пакетах приложений, установленных в системе. Каждый пакет приложения содержит файлы, составляющие приложение Windows, и файл манифеста, описывающий программное обеспечение для Windows.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                 | Описание                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**клосепаккажеинфо**](/windows/desktop/api/AppModel/nf-appmodel-closepackageinfo)<br/>                                               | Закрывает ссылку на указанные сведения о пакете.<br/>                                                                                              |
| [**финдпаккажесбипаккажефамили**](/windows/desktop/api/AppModel/nf-appmodel-findpackagesbypackagefamily)<br/>                         | Находит пакеты с указанным именем семейства для текущего пользователя. <br/>                                                                              |
| [**форматаппликатионусермоделид**](/windows/desktop/api/AppModel/nf-appmodel-formatapplicationusermodelid)<br/>                       | Конструирует [идентификатор модели пользователя приложения](appx-packaging-glossary.md) из имени семейства пакетов и идентификатора приложения, относительный от пакета (праид). <br/> |
| [**жетаппликатионусермоделид**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelid)<br/>                             | Возвращает [идентификатор модели пользователя приложения](appx-packaging-glossary.md) для указанного процесса.<br/>                                                          |
| [**жетаппликатионусермоделидфромтокен**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelidfromtoken)<br/>           | Возвращает [идентификатор пользовательской модели приложения](appx-packaging-glossary.md) для указанного токена.<br/>                                                            |
| [**жеткуррентаппликатионусермоделид**](/windows/desktop/api/Appmodel/nf-appmodel-getcurrentapplicationusermodelid)<br/>               | Возвращает [идентификатор модели пользователя приложения](appx-packaging-glossary.md) для текущего процесса.<br/>                                                            |
| [**жеткуррентпаккажефамилинаме**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefamilyname)<br/>                         | Возвращает имя семейства пакетов для вызывающего процесса.<br/>                                                                                                 |
| [**жеткуррентпаккажефуллнаме**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefullname)<br/>                             | Возвращает полное имя пакета для вызывающего процесса.<br/>                                                                                                   |
| [**жеткуррентпаккажеид**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageid)<br/>                                         | Возвращает идентификатор пакета для вызывающего процесса.<br/>                                                                                             |
| [**жеткуррентпаккажеинфо**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)<br/>                                     | Возвращает сведения о пакете для вызывающего процесса.<br/>                                                                                                 |
| [**GetCurrentPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo2)<br/>                                     | Возвращает сведения о пакете для вызывающего процесса с параметром для указания типа папки пакета.<br/>                                                                                               |
| [**жеткуррентпаккажепас**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath)<br/>                                     | Возвращает путь к пакету для вызывающего процесса.<br/>                                                                                                        |
| [**GetCurrentPackagePath2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath2)<br/>                                     | Возвращает путь к пакету для вызывающего процесса с параметром для указания типа папки пакета.<br/>                                                                                                        |
| [**жетпаккажеаппликатионидс**](/windows/desktop/api/AppModel/nf-appmodel-getpackageapplicationids)<br/>                               | Возвращает идентификаторы приложений в указанном пакете.<br/>                                                                                                        |
| [**жетпаккажефамилинаме**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilyname)<br/>                                       | Возвращает имя семейства пакетов для указанного процесса.<br/>                                                                                               |
| [**жетпаккажефамилинамефромтокен**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilynamefromtoken)<br/>                     | Возвращает имя семейства пакетов для указанного токена.<br/>                                                                                                 |
| [**жетпаккажефуллнаме**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullname)<br/>                                           | Возвращает полное имя пакета для указанного процесса.<br/>                                                                                                 |
| [**жетпаккажефуллнамефромтокен**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullnamefromtoken)<br/>                         | Возвращает полное имя пакета для указанного токена.<br/>                                                                                                   |
| [**жетпаккажеид**](/windows/desktop/api/AppModel/nf-appmodel-getpackageid)<br/>                                                       | Возвращает идентификатор пакета (ID) для указанного процесса.<br/>                                                                                           |
| [**жетпаккажеинфо**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)<br/>                                                   | Возвращает сведения о пакете для указанного пакета.<br/>                                                                                               |
| [**GetPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo2)<br/>                                                   | Возвращает сведения о пакете для указанного пакета с параметром для указания типа папки пакета.<br/>                                                                                               |
| [**GetPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepath)<br/>                                                   | Возвращает путь для указанного пакета.<br/>                                                                                                              |
| [**жетпаккажепасбифуллнаме**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname)<br/>                               | Возвращает путь к указанному пакету.<br/>                                                                                                               |
| [**GetPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname2)<br/>                               | Возвращает путь к указанному пакету с параметром для указания типа папки пакета.<br/>                                                                                                               |
| [**жетпаккажесбипаккажефамили**](/windows/desktop/api/AppModel/nf-appmodel-getpackagesbypackagefamily)<br/>                           | Возвращает пакеты с указанным именем семейства для текущего пользователя. <br/>                                                                               |
| [**жетстажедпаккажеоригин**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackageorigin)<br/>                                   | Возвращает источник указанного пакета.<br/>                                                                                                             |
| [**жетстажедпаккажепасбифуллнаме**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname)<br/>                   | Возвращает путь к указанному промежуточному пакету.<br/>                                                                                                        |
| [**GetStagedPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname2)<br/>                   | Возвращает путь к указанному промежуточному пакету с параметром для указания типа папки пакета.<br/>                                                                                                        |
| [**опенпаккажеинфобифуллнаме**](/windows/desktop/api/AppModel/nf-appmodel-openpackageinfobyfullname)<br/>                             | Открывает сведения о пакете указанного пакета.<br/>                                                                                               |
| [**паккажефамилинамефромфуллнаме**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromfullname)<br/>                     | Возвращает имя семейства пакетов для указанного полного имени пакета.<br/>                                                                                     |
| [**паккажефамилинамефромид**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromid)<br/>                                 | Возвращает имя семейства пакетов для указанного идентификатора пакета.<br/>                                                                                    |
| [**паккажефуллнамефромид**](/windows/desktop/api/AppModel/nf-appmodel-packagefullnamefromid)<br/>                                     | Возвращает полное имя пакета для указанного идентификатора пакета (ID).<br/>                                                                                 |
| [**паккажеидфромфуллнаме**](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)<br/>                                     | Возвращает идентификатор пакета (ID) для указанного полного имени пакета.<br/>                                                                                 |
| [**паккаженамеандпублишеридфромфамилинаме**](/windows/desktop/api/AppModel/nf-appmodel-packagenameandpublisheridfromfamilyname)<br/> | Возвращает имя пакета и идентификатор издателя (идентификатор) для указанного имени семейства пакетов.<br/>                                                            |
| [**парсеаппликатионусермоделид**](/windows/desktop/api/AppModel/nf-appmodel-parseapplicationusermodelid)<br/>                         | Разстраивает [идентификатор модели пользователя приложения](appx-packaging-glossary.md) в соответствии с именем семейства пакетов и идентификатором приложения, относительным для пакета (праид).<br/>      |
| [**паккажеоригин**](/windows/desktop/api/AppModel/ne-appmodel-packageorigin)<br/>                                                     | Указывает источник пакета. <br/>                                                                                                                   |
| [**Константы удостоверений**](identity-constants.md)<br/>                                           | Задает длину строк для полей идентификаторов пакета.<br/>                                                                                |
| [**Константы пакета**](package-constants.md)<br/>                                             | Указывает, как должны обрабатываться пакеты.<br/>                                                                                                           |
| [**\_идентификатор пакета**](/windows/desktop/api/AppModel/ns-appmodel-package_id)<br/>                                                          | Представляет идентификационные данные пакета, такие как имя, версия и издатель.<br/>                                                                  |
| [**\_сведения о пакете**](/windows/desktop/api/AppModel/ns-appmodel-package_info)<br/>                                                      | Представляет идентификационную информацию пакета, включающую идентификатор пакета, полное имя и расположение установки.<br/>                                  |
| [**\_версия пакета**](/windows/desktop/api/AppModel/ns-appmodel-package_version)<br/>                                                | Представляет сведения о версии пакета.<br/>                                                                                                           |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

**Основные понятия**
</dt> <dt>

[Пакеты и развертывание приложений](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

[Словарь терминов](appx-packaging-glossary.md)
</dt> <dt>

**Ссылки**
</dt> <dt>

[Схема манифеста пакета приложений](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[API для упаковки](interfaces.md)
</dt> <dt>

[APIP для развертывание пакета](package-deployment-api.md)
</dt> </dl>

 

