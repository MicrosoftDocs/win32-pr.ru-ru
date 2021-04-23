---
description: Установщик Windows могут использовать цифровые подписи в качестве средства для обнаружения поврежденных ресурсов.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4df800bbcfa9ed2fb0d016794b3ebcf1535be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272798"
---
# <a name="msicertexe"></a><span data-ttu-id="1876b-103">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="1876b-103">Msicert.exe</span></span>

<span data-ttu-id="1876b-104">Установщик Windows могут использовать цифровые подписи в качестве средства для обнаружения поврежденных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1876b-104">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="1876b-105">Сертификат подписавший может сравниваться с сертификатом подписи внешнего ресурса, устанавливаемого пакетом.</span><span class="sxs-lookup"><span data-stu-id="1876b-105">A signer certificate may be compared to the signer certificate of an external resource to be installed by the package.</span></span> <span data-ttu-id="1876b-106">Дополнительные сведения см. в статье [цифровые подписи и установщик Windows](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="1876b-106">For more information, see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="1876b-107">MsiCert.exe — это служебная программа командной строки, которую можно использовать для заполнения [таблицы мсидигиталсигнатуре](msidigitalsignature-table.md) и [таблицы мсидигиталцертификате](msidigitalcertificate-table.md) сведениями о цифровой подписи внешнего CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="1876b-107">MsiCert.exe is a command line utility that can be used to populate the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md) with the digital signature information of an external cabinet file.</span></span> <span data-ttu-id="1876b-108">CAB-файл должен быть подписан цифровой подписью и перечислен в [таблице Media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="1876b-108">The cabinet file must by digitally signed and listed in the [Media table](media-table.md).</span></span> <span data-ttu-id="1876b-109">MsiCert.exe использует сведения о сертификате подписавшего из CAB-файла с цифровой подписью и создаст и добавит таблицы Мсидигиталсигнатуре и Мсидигиталцертификате в базу данных, если они еще не существуют.</span><span class="sxs-lookup"><span data-stu-id="1876b-109">MsiCert.exe uses the signer certificate information from the digitally signed cabinet and will create and add the MsiDigitalSignature and MsiDigitalCertificate tables to the database if they do not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="1876b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1876b-110">Syntax</span></span>

<span data-ttu-id="1876b-111">**мсицерт-d** *{база данных}* **-m** *{запись носителя}* **-c** *{Cabinet}* **\[ - \] h**</span><span class="sxs-lookup"><span data-stu-id="1876b-111">**msicert -d** *{database}* **-m** *{media entry}* **-c** *{cabinet}* **\[-h\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="1876b-112">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="1876b-112">Command Line Options</span></span>

<span data-ttu-id="1876b-113">Параметры командной строки не учитывают регистр, а знаки косой черты могут использоваться вместо тире.</span><span class="sxs-lookup"><span data-stu-id="1876b-113">The command line options are case-insensitive and slash delimiters may be used instead of a dash.</span></span>



| <span data-ttu-id="1876b-114">Параметр</span><span class="sxs-lookup"><span data-stu-id="1876b-114">Option</span></span> | <span data-ttu-id="1876b-115">Параметр</span><span class="sxs-lookup"><span data-stu-id="1876b-115">Parameter</span></span>        | <span data-ttu-id="1876b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1876b-116">Description</span></span>                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1876b-117">-d</span><span class="sxs-lookup"><span data-stu-id="1876b-117">-d</span></span>     | <database> | <span data-ttu-id="1876b-118">Обновляемая база данных (MSI-файл).</span><span class="sxs-lookup"><span data-stu-id="1876b-118">The database (.msi file) that is being updated.</span></span>                                                         |
| <span data-ttu-id="1876b-119">-M</span><span class="sxs-lookup"><span data-stu-id="1876b-119">-m</span></span>     | <media Id> | <span data-ttu-id="1876b-120">Запись в поле DiskId [таблицы Media](media-table.md) в записи для CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="1876b-120">The entry in the DiskId field of the [Media table](media-table.md) in the record for the cabinet file.</span></span> |
| <span data-ttu-id="1876b-121">-c</span><span class="sxs-lookup"><span data-stu-id="1876b-121">-c</span></span>     | <cabinet>  | <span data-ttu-id="1876b-122">Путь к CAB-файлу с цифровой подписью.</span><span class="sxs-lookup"><span data-stu-id="1876b-122">The path to the digitally signed cabinet file.</span></span>                                                          |
| <span data-ttu-id="1876b-123">-H</span><span class="sxs-lookup"><span data-stu-id="1876b-123">-h</span></span>     |                  | <span data-ttu-id="1876b-124">Включить хэш цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="1876b-124">Include the hash of the digital signature.</span></span> <span data-ttu-id="1876b-125">Это необязательно.</span><span class="sxs-lookup"><span data-stu-id="1876b-125">This is optional.</span></span>                                            |



 

<span data-ttu-id="1876b-126">Это средство доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="1876b-126">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1876b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="1876b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1876b-128">Средства разработки установщик Windows</span><span class="sxs-lookup"><span data-stu-id="1876b-128">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="1876b-129">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="1876b-129">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



