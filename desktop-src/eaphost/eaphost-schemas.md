---
title: EAPHost и схема прежних версий
description: Описывает схему EAPHost и устаревшую схему для создания XML-кода конфигурации и XML-кода учетных данных.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dbe40f447618a9ca0da89875521349101c1191f
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104412281"
---
# <a name="eaphost-and-legacy-schema"></a>EAPHost и схема прежних версий

В этом разделе описывается схема EAPHost и схема прежних версий для создания XML-кода конфигурации и XML-кода учетных данных.

## <a name="about-eaphost-and-legacy-schema"></a>Сведения о версии EAPHost и схеме Legacy

Создание XML конфигурации начнется со схемы [еафостконфиг](eaphostconfigschema-schema.md) ; Создание XML-файла с учетными данными начинается со схемы [еафостусеркредентиалс](eaphostusercredentialsschema-schema.md) .

Несколько собственных и устаревших схем содержат общие элементы схемы. Общие элементы, используемые в конфигурации метода и учетных данных метода, абстрактны в один файл схемы, называемый «Common Schema».

Термины «конфигурация метода» и «свойства соединения» взаимозаменяемы. Аналогично, термины «учетные данные метода» и «свойства пользователя» также взаимозаменяемы.

## <a name="eaphost-schema"></a>Схема EAPHost



| схема                                                                        | Описание                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [басиапмесодконфиг](baseeapmethodconfigschema-schema.md)                   | Содержит общие элементы схемы конфигурации.     |
| [басиапмесодусеркредентиалс](baseeapmethodusercredentialsschema-schema.md) | Содержит общие элементы схемы учетных данных.        |
| [еапкоммон](eapcommonschema-schema.md)                                       | Содержит определение элемента **еапмесодтипе** . |
| [еафостконфиг](eaphostconfigschema-schema.md)                               | Содержит схему конфигурации EAPHost.             |
| [еафостусеркредентиалс](eaphostusercredentialsschema-schema.md)             | Содержит схему учетных данных EAPHost.                |



 

## <a name="legacy-schema"></a>Схема прежних версий



| схема                                                                            | Описание                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)   | Содержит общие элементы схемы конфигурации.                                               |
| [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)               | Содержит общие элементы схемы учетных данных.                                                  |
| [eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)           | Содержит общие элементы схемы конфигурации.                                               |
| [eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)                       | Содержит общие элементы схемы учетных данных.                                                  |
| [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)     | Используется с EAP-TLS для описания данных конфигурации проверки подлинности.                          |
| [eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)     | Используется с EAP-TLS для описания данных конфигурации проверки подлинности, начиная с Windows 7. |
| [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)                 | Используется с EAP-TLS для описания учетных данных проверки подлинности и учетных данных.          |
| [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) | Используется с MS-CHAPv2 для описания данных конфигурации проверки подлинности.                        |
| [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)             | Используется с MS-CHAPv2 для описания учетных данных проверки подлинности и учетных данных.        |
| [mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)     | Используется с PEAPv0 для описания данных конфигурации проверки подлинности.                           |
| [mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)     | Используется с PEAPv0 для описания данных конфигурации проверки подлинности, начиная с Windows 7.  |
| [mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)                 | Используется с PEAPv0 для описания учетных данных проверки подлинности и параметров учетных данных.           |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обзор примеров схемы EAPHost и устаревших схем](eaphost-schemas.md)
</dt> </dl>

 

 




