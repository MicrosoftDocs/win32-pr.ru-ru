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
# <a name="packaging-deployment-and-query-glossary"></a><span data-ttu-id="b35c1-103">Глоссарий упаковки, развертывания и запросов</span><span class="sxs-lookup"><span data-stu-id="b35c1-103">Packaging, deployment, and query glossary</span></span>

<dl> <dt>

<span data-ttu-id="b35c1-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**Идентификатор модели пользователя приложения**</span><span class="sxs-lookup"><span data-stu-id="b35c1-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**application user model ID**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-105">Идентификатор модели пользователя приложения уникальным образом определяет приложение в операционной системе, чтобы операционная система могла отправлять уведомления и т. д. в приложение.</span><span class="sxs-lookup"><span data-stu-id="b35c1-105">The application user model ID uniquely identifies an app on the operating system so the operating system can send notifications and so on to the app.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**Блочная схема**</span><span class="sxs-lookup"><span data-stu-id="b35c1-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**block map**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-107">Определяет индексы и криптографические хэши для блоков исполняемого кода и данных, хранящихся в файлах пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="b35c1-107">Defines the indices and cryptographic hashes for blocks of executable code and data that are stored in the files of an app package.</span></span> <span data-ttu-id="b35c1-108">Для каждого пакета приложения требуется BlockMap.xml файл.</span><span class="sxs-lookup"><span data-stu-id="b35c1-108">A BlockMap.xml file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**пакет зависимостей**</span><span class="sxs-lookup"><span data-stu-id="b35c1-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**dependency package**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-110">Пакет, от которого зависит другой пакет.</span><span class="sxs-lookup"><span data-stu-id="b35c1-110">A package on which another package depends.</span></span> <span data-ttu-id="b35c1-111">Зависимость объявляется в манифесте зависимого пакета, а не в манифесте пакета зависимостей.</span><span class="sxs-lookup"><span data-stu-id="b35c1-111">The dependency is declared in the dependent package's manifest and not in the dependency package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**зависимый пакет**</span><span class="sxs-lookup"><span data-stu-id="b35c1-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**dependent package**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-113">Пакет, который принимает зависимость от другого пакета.</span><span class="sxs-lookup"><span data-stu-id="b35c1-113">A package that takes a dependency on another package.</span></span> <span data-ttu-id="b35c1-114">Зависимость объявляется в манифесте зависимого пакета.</span><span class="sxs-lookup"><span data-stu-id="b35c1-114">The dependency is declared in the dependent package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**файлы с объемом**</span><span class="sxs-lookup"><span data-stu-id="b35c1-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**footprint files**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-116">Файлы в пакете приложения, которые не являются частью развертываемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b35c1-116">Files within an app package that are not part of the app to be deployed.</span></span> <span data-ttu-id="b35c1-117">Эти файлы содержат метаданные, относящиеся к пакету.</span><span class="sxs-lookup"><span data-stu-id="b35c1-117">These files provide metadata pertaining to the package.</span></span> <span data-ttu-id="b35c1-118">К стандартным файлам с размерами относятся манифест, блочная схема, схема потока и цифровая подпись.</span><span class="sxs-lookup"><span data-stu-id="b35c1-118">Standard footprint files include the manifest, block map, stream map, and digital signature.</span></span> <span data-ttu-id="b35c1-119">Создаваемые файлы создаются как часть процесса сборки пакета.</span><span class="sxs-lookup"><span data-stu-id="b35c1-119">Footprint files are created as part of the package build process.</span></span> <span data-ttu-id="b35c1-120">Кроме спецификации OPC, \[ \_ типы содержимого \] . XML и файлы, имена которых соответствуют \* \\ \_ \\ \* шаблону "RELS. rels", являются файлами с размерами.</span><span class="sxs-lookup"><span data-stu-id="b35c1-120">In addition per the OPC specification, \[Content\_Types\].xml and files whose names match the "\*\\\_rels\\\*.rels" pattern are footprint files.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**явление**</span><span class="sxs-lookup"><span data-stu-id="b35c1-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifest**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-122">XML-файл, описывающий содержимое и метаданные, связанные с пакетом, включая идентификатор пакета.</span><span class="sxs-lookup"><span data-stu-id="b35c1-122">An XML file that describes the contents and metadata associated with a package including the package ID.</span></span> <span data-ttu-id="b35c1-123">XML-файл манифеста необходим для каждого пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="b35c1-123">A manifest XML file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**СООТВЕТСТВИЕ**</span><span class="sxs-lookup"><span data-stu-id="b35c1-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-125">Соглашение Open Packaging Conventions (OPC) описывает технологию файлового контейнера, описанную в стандартах ISO/IEC 29500 и ECMA 376.</span><span class="sxs-lookup"><span data-stu-id="b35c1-125">Open Packaging Conventions (OPC) describes a container-file technology that is documented in the ISO/IEC 29500 and ECMA 376 standards.</span></span> <span data-ttu-id="b35c1-126">Пакеты приложений соответствуют требованиям OPC.</span><span class="sxs-lookup"><span data-stu-id="b35c1-126">App packages are OPC-compliant.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**пакеты**</span><span class="sxs-lookup"><span data-stu-id="b35c1-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-128">Единица измерения для развертывания, управления и обслуживания, связанная с моделью упаковки приложений.</span><span class="sxs-lookup"><span data-stu-id="b35c1-128">The unit of deployment, management, and servicing software associated with the app packaging model.</span></span> <span data-ttu-id="b35c1-129">Пакет содержит файлы, составляющие приложение, а также файл манифеста, описывающий программное обеспечение для Windows.</span><span class="sxs-lookup"><span data-stu-id="b35c1-129">A package contains the files that constitute the app, along with a manifest file that describes the software to Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**имя семейства пакетов**</span><span class="sxs-lookup"><span data-stu-id="b35c1-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**package family name**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-131">Сериализованная форма идентификатора пакета, который уникальным образом представляет семейство пакетов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b35c1-131">A serialized form of the package ID that uniquely represents the package family on the computer.</span></span> <span data-ttu-id="b35c1-132">Он подходит для именования объектов, таких как файлы и папки.</span><span class="sxs-lookup"><span data-stu-id="b35c1-132">It is suitable for naming objects such as files and folders.</span></span> <span data-ttu-id="b35c1-133">Имя семейства пакетов похоже на полное имя пакета, но включает только имя и издателя.</span><span class="sxs-lookup"><span data-stu-id="b35c1-133">The package family name is similar to the package full name, but includes only the name and publisher.</span></span> <span data-ttu-id="b35c1-134">Так как она исключает информацию, которая изменяется при обслуживании (версия, архитектура и сведения о ресурсах), она полезна для независимых от версии ссылок на пакет.</span><span class="sxs-lookup"><span data-stu-id="b35c1-134">Because it excludes info that changes with servicing (version, architecture, and resource info), it is useful for version-independent references to the package.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**полное имя пакета**</span><span class="sxs-lookup"><span data-stu-id="b35c1-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**package full name**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-136">Сериализованная форма идентификатора пакета, который уникальным образом представляет данную версию пакета на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b35c1-136">A serialized form of the package ID that uniquely represents this version of the package on the computer.</span></span> <span data-ttu-id="b35c1-137">Он подходит для именования объектов, таких как файлы и папки.</span><span class="sxs-lookup"><span data-stu-id="b35c1-137">It is suitable for naming objects such as files and folders.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**Идентификатор пакета**</span><span class="sxs-lookup"><span data-stu-id="b35c1-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**package ID**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-139">Глобальный уникальный идентификатор пакета.</span><span class="sxs-lookup"><span data-stu-id="b35c1-139">A globally unique identifier for a package.</span></span> <span data-ttu-id="b35c1-140">Он состоит из кортежа атрибутов для пакета, включая имя, издателя, поддерживаемую архитектуру, сведения о ресурсе и версию.</span><span class="sxs-lookup"><span data-stu-id="b35c1-140">It is composed of a tuple of attributes for the package including name, publisher, supported architecture, resource info, and version.</span></span> <span data-ttu-id="b35c1-141">См. раздел полное имя пакета и имя семейства пакетов для сериализованных форм идентификатора пакета.</span><span class="sxs-lookup"><span data-stu-id="b35c1-141">See package full name and package family name for serialized forms of the package ID.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**Идентификатор приложения относительно пакета**</span><span class="sxs-lookup"><span data-stu-id="b35c1-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**package relative application ID**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-143">Атрибут **ID** элемента [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) в манифесте пакета, который также называется праид.</span><span class="sxs-lookup"><span data-stu-id="b35c1-143">The **Id** attribute on the [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) element within the package manifest, which is also known as PRAID.</span></span> <span data-ttu-id="b35c1-144">Эта строка уникально идентифицирует приложение в пакете.</span><span class="sxs-lookup"><span data-stu-id="b35c1-144">This string uniquely identifies an app within a package.</span></span> <span data-ttu-id="b35c1-145">Этот атрибут является обязательным для элемента **Application** .</span><span class="sxs-lookup"><span data-stu-id="b35c1-145">This attribute is required for the **Application** element.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**файлы полезных данных**</span><span class="sxs-lookup"><span data-stu-id="b35c1-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**payload files**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-147">Файлы в пакете приложения, которые являются частью развертываемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b35c1-147">The files within an app package that are part of the app to be deployed.</span></span> <span data-ttu-id="b35c1-148">Эти файлы извлекаются и помещаются в папку установки пользователя.</span><span class="sxs-lookup"><span data-stu-id="b35c1-148">These files are extracted and placed in the user's installation folder.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**Идентификатор ресурса**</span><span class="sxs-lookup"><span data-stu-id="b35c1-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**resource ID**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-150">Необязательная часть идентификатора пакета, используемая для различения ресурсов в пакете.</span><span class="sxs-lookup"><span data-stu-id="b35c1-150">An optional part of a package ID that is used to differentiate the resources in the package.</span></span> <span data-ttu-id="b35c1-151">Например, идентификатор ресурса можно использовать для указания языка или языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="b35c1-151">For example, a resource ID can be used to specify the language or locale.</span></span>

</dd> <dt>

<span data-ttu-id="b35c1-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Главный каталог ZIP**</span><span class="sxs-lookup"><span data-stu-id="b35c1-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**ZIP central directory**</span></span>
</dt> <dd>

<span data-ttu-id="b35c1-153">Последовательности байтов в ZIP-файле, где хранятся метаданные о ZIP-архиве и его содержимом, включая имя, размер, параметры сжатия и расположение в архиве.</span><span class="sxs-lookup"><span data-stu-id="b35c1-153">The byte sequences in a ZIP file that store metadata about the ZIP archive and its contents including name, size, compression settings, and location within the archive.</span></span>

</dd> </dl>

 

 