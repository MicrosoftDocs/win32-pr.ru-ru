---
description: Используйте эти рекомендации для полной установки установщик Windows с помощью цифровой подписи.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Создание полностью проверенной подписанной установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e76bbfb77eab8b020cb1591847d2a36d09c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662944"
---
# <a name="authoring-a-fully-verified-signed-installation"></a><span data-ttu-id="d5fda-103">Создание полностью проверенной подписанной установки</span><span class="sxs-lookup"><span data-stu-id="d5fda-103">Authoring a Fully Verified Signed Installation</span></span>

<span data-ttu-id="d5fda-104">Эти рекомендации можно использовать для полной установки установщик Windows с помощью цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="d5fda-104">You can use these guidelines to cover an entire Windows Installer installation by a digital signature.</span></span>

<span data-ttu-id="d5fda-105">Авторы установщик Windows установки должны соблюдать следующие действия, чтобы убедиться, что все части установки охватываются цифровой подписью:</span><span class="sxs-lookup"><span data-stu-id="d5fda-105">Authors of Windows Installer installations must adhere to the following to ensure that all parts of the installation are covered by a digital signature:</span></span>

-   <span data-ttu-id="d5fda-106">Используйте внутренние CAB-файлы или используйте подписанные внешние CAB-файлы и правильно создайте [таблицу мсидигиталсигнатуре](msidigitalsignature-table.md) и [таблицу мсидигиталцертификате](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="d5fda-106">Use internal cabinet files, or use signed external cabinet files and correctly author the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span>
-   <span data-ttu-id="d5fda-107">Используйте только пользовательские действия, хранящиеся в пакете или установленные вместе с пакетом.</span><span class="sxs-lookup"><span data-stu-id="d5fda-107">Use only custom actions stored within the package or installed with the package.</span></span>
-   <span data-ttu-id="d5fda-108">Подпишите пакет установки.</span><span class="sxs-lookup"><span data-stu-id="d5fda-108">Sign the installation package.</span></span>
-   <span data-ttu-id="d5fda-109">Включите в пакет [таблицу мсипатчцертификате](msipatchcertificate-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d5fda-109">Include an [MsiPatchCertificate table](msipatchcertificate-table.md) in the package.</span></span> <span data-ttu-id="d5fda-110">Чтобы включить [исправление контроля учетных записей (UAC)](user-account-control--uac--patching.md), в этой таблице должны содержаться сведения, используемые для обнаружения сертификатов, используемых для установки исправлений с цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="d5fda-110">To enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md), this table must contain information used to identify the signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="d5fda-111">Исправление контроля учетных записей позволяет автору пакета установки обнаруживать исправления с цифровой подписью, которые могут быть применены в будущем пользователями, не являющимися администраторами.</span><span class="sxs-lookup"><span data-stu-id="d5fda-111">UAC patching enables the author of the installation package to identify digitally-signed patches that can be applied in the future by non-administrator users.</span></span>

<span data-ttu-id="d5fda-112">Пример, демонстрирующий создание подписанной установки с помощью автоматизации, см. в разделе [Создание полностью проверенной установки с помощью службы автоматизации](authoring-a-fully-verified-signed-installation-using-automation.md).</span><span class="sxs-lookup"><span data-stu-id="d5fda-112">For an example showing how to author a signed installation using automation, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

 

 



