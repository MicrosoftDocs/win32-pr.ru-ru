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
# <a name="eaphost-and-legacy-schema"></a><span data-ttu-id="049c1-103">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="049c1-103">EAPHost and Legacy Schema</span></span>

<span data-ttu-id="049c1-104">В этом разделе описывается схема EAPHost и схема прежних версий для создания XML-кода конфигурации и XML-кода учетных данных.</span><span class="sxs-lookup"><span data-stu-id="049c1-104">This topic describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span>

## <a name="about-eaphost-and-legacy-schema"></a><span data-ttu-id="049c1-105">Сведения о версии EAPHost и схеме Legacy</span><span class="sxs-lookup"><span data-stu-id="049c1-105">About EAPHost and Legacy Schema</span></span>

<span data-ttu-id="049c1-106">Создание XML конфигурации начнется со схемы [еафостконфиг](eaphostconfigschema-schema.md) ; Создание XML-файла с учетными данными начинается со схемы [еафостусеркредентиалс](eaphostusercredentialsschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="049c1-106">Creating configuration XML commences with the [eaphostconfig](eaphostconfigschema-schema.md) schema; creating credential XML commences with the [eaphostusercredentials](eaphostusercredentialsschema-schema.md) schema.</span></span>

<span data-ttu-id="049c1-107">Несколько собственных и устаревших схем содержат общие элементы схемы.</span><span class="sxs-lookup"><span data-stu-id="049c1-107">Several of the native and legacy schema contain common schema elements.</span></span> <span data-ttu-id="049c1-108">Общие элементы, используемые в конфигурации метода и учетных данных метода, абстрактны в один файл схемы, называемый «Common Schema».</span><span class="sxs-lookup"><span data-stu-id="049c1-108">Common elements used in method configuration and method credentials are abstracted into a single schema file, referred to as the "common schema".</span></span>

<span data-ttu-id="049c1-109">Термины «конфигурация метода» и «свойства соединения» взаимозаменяемы.</span><span class="sxs-lookup"><span data-stu-id="049c1-109">The terms "method configuration" and "connection properties" are used interchangeably.</span></span> <span data-ttu-id="049c1-110">Аналогично, термины «учетные данные метода» и «свойства пользователя» также взаимозаменяемы.</span><span class="sxs-lookup"><span data-stu-id="049c1-110">Likewise, the terms "method credentials" and "user properties" are also used interchangeably.</span></span>

## <a name="eaphost-schema"></a><span data-ttu-id="049c1-111">Схема EAPHost</span><span class="sxs-lookup"><span data-stu-id="049c1-111">EAPHost Schema</span></span>



| <span data-ttu-id="049c1-112">схема</span><span class="sxs-lookup"><span data-stu-id="049c1-112">Schema</span></span>                                                                        | <span data-ttu-id="049c1-113">Описание</span><span class="sxs-lookup"><span data-stu-id="049c1-113">Description</span></span>                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="049c1-114">басиапмесодконфиг</span><span class="sxs-lookup"><span data-stu-id="049c1-114">baseeapmethodconfig</span></span>](baseeapmethodconfigschema-schema.md)                   | <span data-ttu-id="049c1-115">Содержит общие элементы схемы конфигурации.</span><span class="sxs-lookup"><span data-stu-id="049c1-115">Contains common configuration schema elements.</span></span>     |
| [<span data-ttu-id="049c1-116">басиапмесодусеркредентиалс</span><span class="sxs-lookup"><span data-stu-id="049c1-116">baseeapmethodusercredentials</span></span>](baseeapmethodusercredentialsschema-schema.md) | <span data-ttu-id="049c1-117">Содержит общие элементы схемы учетных данных.</span><span class="sxs-lookup"><span data-stu-id="049c1-117">Contains common credential schema elements.</span></span>        |
| [<span data-ttu-id="049c1-118">еапкоммон</span><span class="sxs-lookup"><span data-stu-id="049c1-118">eapcommon</span></span>](eapcommonschema-schema.md)                                       | <span data-ttu-id="049c1-119">Содержит определение элемента **еапмесодтипе** .</span><span class="sxs-lookup"><span data-stu-id="049c1-119">Contains the **EapMethodType** element definition.</span></span> |
| [<span data-ttu-id="049c1-120">еафостконфиг</span><span class="sxs-lookup"><span data-stu-id="049c1-120">eaphostconfig</span></span>](eaphostconfigschema-schema.md)                               | <span data-ttu-id="049c1-121">Содержит схему конфигурации EAPHost.</span><span class="sxs-lookup"><span data-stu-id="049c1-121">Contains EAPHost configuration schema.</span></span>             |
| [<span data-ttu-id="049c1-122">еафостусеркредентиалс</span><span class="sxs-lookup"><span data-stu-id="049c1-122">eaphostusercredentials</span></span>](eaphostusercredentialsschema-schema.md)             | <span data-ttu-id="049c1-123">Содержит схему учетных данных EAPHost.</span><span class="sxs-lookup"><span data-stu-id="049c1-123">Contains EAPHost credential schema.</span></span>                |



 

## <a name="legacy-schema"></a><span data-ttu-id="049c1-124">Схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="049c1-124">Legacy Schema</span></span>



| <span data-ttu-id="049c1-125">схема</span><span class="sxs-lookup"><span data-stu-id="049c1-125">Schema</span></span>                                                                            | <span data-ttu-id="049c1-126">Описание</span><span class="sxs-lookup"><span data-stu-id="049c1-126">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="049c1-127">baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="049c1-127">baseeapconnectionpropertiesv1</span></span>](baseeapconnectionpropertiesv1schema-schema.md)   | <span data-ttu-id="049c1-128">Содержит общие элементы схемы конфигурации.</span><span class="sxs-lookup"><span data-stu-id="049c1-128">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="049c1-129">baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="049c1-129">baseeapuserpropertiesv1</span></span>](baseeapuserpropertiesv1schema-schema.md)               | <span data-ttu-id="049c1-130">Содержит общие элементы схемы учетных данных.</span><span class="sxs-lookup"><span data-stu-id="049c1-130">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="049c1-131">eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="049c1-131">eapconnectionpropertiesv1</span></span>](eapconnectionpropertiesv1schema-schema.md)           | <span data-ttu-id="049c1-132">Содержит общие элементы схемы конфигурации.</span><span class="sxs-lookup"><span data-stu-id="049c1-132">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="049c1-133">eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="049c1-133">eapuserpropertiesv1</span></span>](eapuserpropertiesv1schema-schema.md)                       | <span data-ttu-id="049c1-134">Содержит общие элементы схемы учетных данных.</span><span class="sxs-lookup"><span data-stu-id="049c1-134">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="049c1-135">eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="049c1-135">eaptlsconnectionpropertiesv1</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="049c1-136">Используется с EAP-TLS для описания данных конфигурации проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="049c1-136">Is used with EAP-TLS to describe authentication configuration data.</span></span>                          |
| [<span data-ttu-id="049c1-137">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="049c1-137">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="049c1-138">Используется с EAP-TLS для описания данных конфигурации проверки подлинности, начиная с Windows 7.</span><span class="sxs-lookup"><span data-stu-id="049c1-138">Is used with EAP-TLS to describe authentication configuration data beginning with Windows 7.</span></span> |
| [<span data-ttu-id="049c1-139">eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="049c1-139">eaptlsuserpropertiesv1</span></span>](eaptlsuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="049c1-140">Используется с EAP-TLS для описания учетных данных проверки подлинности и учетных данных.</span><span class="sxs-lookup"><span data-stu-id="049c1-140">Is used with EAP-TLS to describe authentication credentials and credential options.</span></span>          |
| [<span data-ttu-id="049c1-141">mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="049c1-141">mschapv2connectionpropertiesv1</span></span>](mschapv2connectionpropertiesv1schema-schema.md) | <span data-ttu-id="049c1-142">Используется с MS-CHAPv2 для описания данных конфигурации проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="049c1-142">Is used with MS-CHAPv2 to describe authentication configuration data.</span></span>                        |
| [<span data-ttu-id="049c1-143">mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="049c1-143">mschapv2userpropertiesv1</span></span>](mschapv2userpropertiesv1schema-schema.md)             | <span data-ttu-id="049c1-144">Используется с MS-CHAPv2 для описания учетных данных проверки подлинности и учетных данных.</span><span class="sxs-lookup"><span data-stu-id="049c1-144">Is used with MS-CHAPv2 to describe authentication credentials and credential options.</span></span>        |
| [<span data-ttu-id="049c1-145">mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="049c1-145">mspeapconnectionpropertiesv1</span></span>](mspeapconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="049c1-146">Используется с PEAPv0 для описания данных конфигурации проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="049c1-146">Is used with PEAPv0 to describe authentication configuration data.</span></span>                           |
| [<span data-ttu-id="049c1-147">mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="049c1-147">mspeapconnectionpropertiesv2</span></span>](mspeapconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="049c1-148">Используется с PEAPv0 для описания данных конфигурации проверки подлинности, начиная с Windows 7.</span><span class="sxs-lookup"><span data-stu-id="049c1-148">Is used with PEAPv0 to describe authentication configuration data beginning with Windows 7.</span></span>  |
| [<span data-ttu-id="049c1-149">mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="049c1-149">mspeapuserpropertiesv1</span></span>](mspeapuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="049c1-150">Используется с PEAPv0 для описания учетных данных проверки подлинности и параметров учетных данных.</span><span class="sxs-lookup"><span data-stu-id="049c1-150">Is used with PEAPv0 to describe authentication credentials and credential options.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="049c1-151">См. также</span><span class="sxs-lookup"><span data-stu-id="049c1-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="049c1-152">Обзор примеров схемы EAPHost и устаревших схем</span><span class="sxs-lookup"><span data-stu-id="049c1-152">Reviewing EAPHost and Legacy Schema Samples</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




