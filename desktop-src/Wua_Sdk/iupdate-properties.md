---
description: Интерфейс Иупдате определяет следующие свойства.
ms.assetid: d87544f1-a107-440f-8ce0-77d9f2d90578
title: Свойства Иупдате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93db8e7d8d6786e3f3f827d9eb2e9f97c43aae4781edf0a05fcf6d03e8fb1f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859864"
---
# <a name="iupdate-properties"></a>Свойства Иупдате

Интерфейс [**иупдате**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) определяет следующие свойства.



| Свойство                                                                           | Описание                                                                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аутоселектонвебситес**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_autoselectonwebsites)                       | возвращает логическое значение, указывающее, отмечено ли обновление автоматически выбранным Центр обновления Windows.                                                                   |
| [**бундледупдатес**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_bundledupdates)                                   | Возвращает интерфейс, содержащий сведения о упорядоченном списке пакетов обновлений для обновления.                                                                           |
| [**канрекуиресаурце**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_canrequiresource)                               | Возвращает логическое значение, указывающее, требуется ли исходный носитель обновления для установки или удаления.                                                          |
| [**Категории**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_categories)                                           | Возвращает интерфейс, содержащий коллекцию категорий, к которым относится обновление.                                                                                             |
| [**Крайний срок**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deadline)                                               | Возвращает дату, на которую должно быть установлено обновление.                                                                                                                                |
| [**делтакомпресседконтентаваилабле**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentavailable) | Возвращает логическое значение, указывающее, доступно ли на сервере разностное сжатое содержимое для обновления.                                                                       |
| [**делтакомпресседконтентпреферред**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentpreferred) | Возвращает логическое значение, указывающее, следует ли предпочитать сжатое содержимое при скачивании и установке или удалении обновления, если доступно содержимое с разностной сжатием. |
| [**деплойментактион**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deploymentaction)                               | Возвращает действие, для которого развернуто обновление.                                                                                                                                   |
| [**Описание**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_description)                                         | Возвращает локализованное описание обновления.                                                                                                                                       |
| [**довнлоадконтентс**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadcontents)                               | Возвращает сведения о файле для скачивания содержимого обновления.                                                                                                                    |
| [**довнлоадприорити**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadpriority)                               | Возвращает предлагаемый приоритет загрузки обновления.                                                                                                                                 |
| [**еулаакцептед**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulaaccepted)                                       | Возвращает логическое значение, указывающее, принимаются ли на компьютере условия лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, связанные с обновлением.                                 |
| [**еулатекст**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulatext)                                               | Возвращает полный локализованный текст условий лицензионного соглашения на использование программного обеспечения корпорации Майкрософт, связанных с обновлением.                                                                           |
| [**хандлерид**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_handlerid)                                             | Возвращает обработчик установки обновления.                                                                                                                                             |
| [**Идентификация**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_identity)                                               | Возвращает интерфейс, содержащий уникальный идентификатор обновления.                                                                                                                |
| [**Изображение**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_image)                                                     | Возвращает интерфейс, содержащий сведения об изображении, связанном с обновлением.                                                                                      |
| [**инсталлатионбехавиор**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_installationbehavior)                       | Возвращает интерфейс, содержащий параметры установки обновления.                                                                                                             |
| [**Бета-версия**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isbeta)                                                   | Возвращает логическое значение, указывающее, является ли обновление бета-версией.                                                                                                           |
| [**Загружено**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isdownloaded)                                       | Возвращает логическое значение, указывающее, кэшируется ли все содержимое обновления на компьютере.                                                                                       |
| [**IsHidden**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)                                               | Возвращает логическое значение, указывающее, скрыто ли обновление пользователем.                                                                                                          |
| [**IsInstalled**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isinstalled)                                         | Возвращает логическое значение, указывающее, установлено ли обновление на компьютере при выполнении поиска.                                                                     |
| [**Обязательный**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ismandatory)                                         | Возвращает логическое значение, указывающее, является ли установка обновления обязательной.                                                                                            |
| [**Удалить**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isuninstallable)                                 | Возвращает логическое значение, указывающее, может ли пользователь удалить обновление с компьютера.                                                                                        |
| [**кбартиклеидс**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_kbarticleids)                                       | Возвращает коллекцию идентификаторов статей базы знаний Майкрософт, связанных с обновлением.                                                                                      |
| [**Языки**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_languages)                                              | Возвращает интерфейс, содержащий языки, поддерживаемые обновлением.                                                                                                     |
| [**ластдеплойментчанжетиме**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_lastdeploymentchangetime)               | Возвращает дату последнего опубликования обновления в формате времени (UTC) на сервере, который развертывает обновление.                                               |
| [**максдовнлоадсизе**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_maxdownloadsize)                                 | Возвращает максимальный размер загружаемого обновления.                                                                                                                                       |
| [**миндовнлоадсизе**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_mindownloadsize)                                 | Возвращает минимальный размер скачивания обновления.                                                                                                                                       |
| [**мореинфаурлс**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_moreinfourls)                                       | Возвращает коллекцию строк, зависящих от языка, которые указывают гиперссылки на дополнительные сведения об обновлении.                                                                    |
| [**мсрксеверити**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_msrcseverity)                                       | Возвращает оценочную степень серьезности обновления в центре Microsoft Security Response.                                                                                                          |
| [**рекоммендедкпуспид**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed)                         | Возвращает рекомендуемую скорость ЦП, используемую для установки обновления, в мегагерцах (МГц).                                                                                                      |
| [**рекоммендедхарддискспаце**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace)               | Возвращает рекомендуемый объем свободного места, который должен быть доступен на жестком диске перед установкой обновления. Свободное место указывается в мегабайтах (МБ).                             |
| [**рекоммендедмемори**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedmemory)                             | Возвращает рекомендуемый объем физической памяти, который должен быть доступен на компьютере перед установкой обновления. Объем физической памяти указывается в мегабайтах (МБ).         |
| [**ReleaseNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_releasenotes)                                       | Получает заметки о локализованном выпуске для обновления.                                                                                                                                    |
| [**секуритибуллетинидс**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_securitybulletinids)                         | Возвращает коллекцию строковых значений, содержащих идентификаторы бюллетеней безопасности, связанные с обновлением.                                                                      |
| [**суперседедупдатеидс**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supersededupdateids)                         | Возвращает коллекцию идентификаторов обновления. Эта коллекция идентификаторов указывает обновления, заменяемые обновлением.                                                    |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supporturl)                                           | Возвращает гиперссылку на сведения о поддержке для конкретного языка обновления.                                                                                                       |
| [**Название**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)                                                     | Возвращает локализованное название обновления.                                                                                                                                             |
| [**Тип**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_type)                                                       | Возвращает тип обновления.                                                                                                                                                        |
| [**унинсталлатионбехавиор**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationbehavior)                   | Возвращает интерфейс, содержащий параметры удаления для обновления.                                                                                                          |
| [**унинсталлатионнотес**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationnotes)                         | Возвращает заметки об удалении для обновления.                                                                                                                                       |
| [**унинсталлатионстепс**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationsteps)                         | Возвращает интерфейс, содержащий шаги по удалению для обновления.                                                                                                            |



 

 

 



