---
title: Глоссарий упаковки, развертывания и запросов
description: Содержит определения терминов, связанных с упаковкой, развертыванием и запросом для приложений Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a2112b593e2d2a5aaf4f06525160e2d799bad1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104412780"
---
# <a name="packaging-deployment-and-query-glossary"></a>Глоссарий упаковки, развертывания и запросов

<dl> <dt>

<span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**Идентификатор модели пользователя приложения**
</dt> <dd>

Идентификатор модели пользователя приложения уникальным образом определяет приложение в операционной системе, чтобы операционная система могла отправлять уведомления и т. д. в приложение.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**Блочная схема**
</dt> <dd>

Определяет индексы и криптографические хэши для блоков исполняемого кода и данных, хранящихся в файлах пакета приложения. Для каждого пакета приложения требуется BlockMap.xml файл.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**пакет зависимостей**
</dt> <dd>

Пакет, от которого зависит другой пакет. Зависимость объявляется в манифесте зависимого пакета, а не в манифесте пакета зависимостей.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**зависимый пакет**
</dt> <dd>

Пакет, который принимает зависимость от другого пакета. Зависимость объявляется в манифесте зависимого пакета.

</dd> <dt>

<span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**файлы с объемом**
</dt> <dd>

Файлы в пакете приложения, которые не являются частью развертываемого приложения. Эти файлы содержат метаданные, относящиеся к пакету. К стандартным файлам с размерами относятся манифест, блочная схема, схема потока и цифровая подпись. Создаваемые файлы создаются как часть процесса сборки пакета. Кроме спецификации OPC, \[ \_ типы содержимого \] . XML и файлы, имена которых соответствуют \* \\ \_ \\ \* шаблону "RELS. rels", являются файлами с размерами.

</dd> <dt>

<span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**явление**
</dt> <dd>

XML-файл, описывающий содержимое и метаданные, связанные с пакетом, включая идентификатор пакета. XML-файл манифеста необходим для каждого пакета приложения.

</dd> <dt>

<span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**СООТВЕТСТВИЕ**
</dt> <dd>

Соглашение Open Packaging Conventions (OPC) описывает технологию файлового контейнера, описанную в стандартах ISO/IEC 29500 и ECMA 376. Пакеты приложений соответствуют требованиям OPC.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**пакеты**
</dt> <dd>

Единица измерения для развертывания, управления и обслуживания, связанная с моделью упаковки приложений. Пакет содержит файлы, составляющие приложение, а также файл манифеста, описывающий программное обеспечение для Windows.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**имя семейства пакетов**
</dt> <dd>

Сериализованная форма идентификатора пакета, который уникальным образом представляет семейство пакетов на компьютере. Он подходит для именования объектов, таких как файлы и папки. Имя семейства пакетов похоже на полное имя пакета, но включает только имя и издателя. Так как она исключает информацию, которая изменяется при обслуживании (версия, архитектура и сведения о ресурсах), она полезна для независимых от версии ссылок на пакет.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**полное имя пакета**
</dt> <dd>

Сериализованная форма идентификатора пакета, который уникальным образом представляет данную версию пакета на компьютере. Он подходит для именования объектов, таких как файлы и папки.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**Идентификатор пакета**
</dt> <dd>

Глобальный уникальный идентификатор пакета. Он состоит из кортежа атрибутов для пакета, включая имя, издателя, поддерживаемую архитектуру, сведения о ресурсе и версию. См. раздел полное имя пакета и имя семейства пакетов для сериализованных форм идентификатора пакета.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**Идентификатор приложения относительно пакета**
</dt> <dd>

Атрибут **ID** элемента [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) в манифесте пакета, который также называется праид. Эта строка уникально идентифицирует приложение в пакете. Этот атрибут является обязательным для элемента **Application** .

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**файлы полезных данных**
</dt> <dd>

Файлы в пакете приложения, которые являются частью развертываемого приложения. Эти файлы извлекаются и помещаются в папку установки пользователя.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**Идентификатор ресурса**
</dt> <dd>

Необязательная часть идентификатора пакета, используемая для различения ресурсов в пакете. Например, идентификатор ресурса можно использовать для указания языка или языкового стандарта.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Главный каталог ZIP**
</dt> <dd>

Последовательности байтов в ZIP-файле, где хранятся метаданные о ZIP-архиве и его содержимом, включая имя, размер, параметры сжатия и расположение в архиве.

</dd> </dl>

 

 