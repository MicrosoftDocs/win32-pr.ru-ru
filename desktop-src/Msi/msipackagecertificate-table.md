---
description: В таблице Мсипаккажецертификате перечислены сертификаты цифровых подписей, используемые для проверки подлинности пакетов установки, которые делают установку Multiple-Package.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Таблица Мсипаккажецертификате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272796"
---
# <a name="msipackagecertificate-table"></a><span data-ttu-id="d78f0-103">Таблица Мсипаккажецертификате</span><span class="sxs-lookup"><span data-stu-id="d78f0-103">MsiPackageCertificate Table</span></span>

<span data-ttu-id="d78f0-104">В таблице Мсипаккажецертификате перечислены сертификаты цифровых подписей, используемые для проверки подлинности пакетов установки, которые делают [установку с несколькими пакетами](multiple-package-installations.md).</span><span class="sxs-lookup"><span data-stu-id="d78f0-104">The MsiPackageCertificate Table lists digital signature certificates used to verify the identity of the installation packages that make this [Multiple-Package Installation](multiple-package-installations.md).</span></span>

<span data-ttu-id="d78f0-105">Используйте эту таблицу для создания [многопакетной установки](multiple-package-installations.md) для продукта, содержащего несколько пакетов установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="d78f0-105">Use this table to author a [multiple-package installation](multiple-package-installations.md) for a product containing multiple Windows Installer packages.</span></span> <span data-ttu-id="d78f0-106">Если первый пакет имеет цифровую подпись и содержит таблицу Мсипаккажецертификате, указывающую цифровые сертификаты для всех оставшихся пакетов в продукте, администратор должен принять только запрос [*контроля учетных записей*](u-gly.md) (UAC), отображаемый для первого пакета.</span><span class="sxs-lookup"><span data-stu-id="d78f0-106">If the first package is digitally signed, and contains a MsiPackageCertificate Table specifying digital certificates for all the remaining packages in the product, the administrator needs only accept the [*User Account Control*](u-gly.md) (UAC) prompt displayed for the first package.</span></span> <span data-ttu-id="d78f0-107">После принятия запроса UAC для первого пакета определяемые пользователем функции в [таблице мсиембеддедчаинер](msiembeddedchainer-table.md) могут затем объединить оставшиеся пакеты с многопакетной установкой без отображения запроса UAC и необходимости ответа администратора для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="d78f0-107">After accepting the UAC's prompt for the first package, the user-defined functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) can then join the remaining packages to the multiple-package installation without displaying a UAC prompt and requiring an administrator response for each package.</span></span>

<span data-ttu-id="d78f0-108">Если одна или несколько функций в [таблице мсиембеддедчаинер](msiembeddedchainer-table.md) запрашивают неподписанный пакет, то для каждого неподписанного пакета отображается еще один запрос UAC, запрашивающий взаимодействие с администратором.</span><span class="sxs-lookup"><span data-stu-id="d78f0-108">If one or more of the functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) request an unsigned package, another UAC prompt requiring administrator interaction is displayed for each unsigned package.</span></span> <span data-ttu-id="d78f0-109">Если администратор принимает этот запрос UAC, установка нескольких пакетов продолжится.</span><span class="sxs-lookup"><span data-stu-id="d78f0-109">If the administrator accepts this UAC prompt, the multi-package installation continues.</span></span> <span data-ttu-id="d78f0-110">После того как администратор предоставил учетные данные для пакета, в ходе этой многопакетной установки запрос контроля учетных записей не будет отображаться снова для этого пакета.</span><span class="sxs-lookup"><span data-stu-id="d78f0-110">Once an administrator has provided credentials for a package, no UAC prompt will again be displayed for that package during this multi-package installation.</span></span> <span data-ttu-id="d78f0-111">Если администратор отклоняет запрос контроля учетных записей для пакета, установщик Windows выполняет откат многопакетной установки перед фиксацией установки пакетов, относящихся к продукту.</span><span class="sxs-lookup"><span data-stu-id="d78f0-111">If the administrator rejects a UAC prompt for a package, the Windows installer rolls back the multi-package installation before it commits to install any packages belonging to the product.</span></span>

<span data-ttu-id="d78f0-112">**[Установщик Windows 4,0 или более ранней версии](not-supported-in-windows-installer-4-0.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d78f0-112">**[Windows Installer 4.0 or earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="d78f0-113">Эта таблица доступна начиная с установщик Windows 4,5.</span><span class="sxs-lookup"><span data-stu-id="d78f0-113">This table is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="d78f0-114">Таблица Мсипаккажецертификате содержит следующие столбцы:</span><span class="sxs-lookup"><span data-stu-id="d78f0-114">The MsiPackageCertificate Table has the following columns:</span></span>



| <span data-ttu-id="d78f0-115">Столбец</span><span class="sxs-lookup"><span data-stu-id="d78f0-115">Column</span></span>               | <span data-ttu-id="d78f0-116">Type</span><span class="sxs-lookup"><span data-stu-id="d78f0-116">Type</span></span>                         | <span data-ttu-id="d78f0-117">Ключ</span><span class="sxs-lookup"><span data-stu-id="d78f0-117">Key</span></span> | <span data-ttu-id="d78f0-118">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="d78f0-118">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="d78f0-119">паккажецертификате</span><span class="sxs-lookup"><span data-stu-id="d78f0-119">PackageCertificate</span></span>   | [<span data-ttu-id="d78f0-120">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="d78f0-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="d78f0-121">Да</span><span class="sxs-lookup"><span data-stu-id="d78f0-121">Y</span></span>   | <span data-ttu-id="d78f0-122">Нет</span><span class="sxs-lookup"><span data-stu-id="d78f0-122">N</span></span>        |
| <span data-ttu-id="d78f0-123">дигиталцертификате\_</span><span class="sxs-lookup"><span data-stu-id="d78f0-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="d78f0-124">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="d78f0-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="d78f0-125">Нет</span><span class="sxs-lookup"><span data-stu-id="d78f0-125">N</span></span>   | <span data-ttu-id="d78f0-126">Нет</span><span class="sxs-lookup"><span data-stu-id="d78f0-126">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d78f0-127">Столбцы</span><span class="sxs-lookup"><span data-stu-id="d78f0-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d78f0-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>паккажецертификате</span><span class="sxs-lookup"><span data-stu-id="d78f0-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span></span>
</dt> <dd>

<span data-ttu-id="d78f0-129">Уникальный идентификатор этой строки в таблице Мсипаккажецертификате.</span><span class="sxs-lookup"><span data-stu-id="d78f0-129">The unique identifier for this row in the MsiPackageCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="d78f0-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>дигиталцертификате</span><span class="sxs-lookup"><span data-stu-id="d78f0-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="d78f0-131">Внешний ключ в первом столбце [таблицы мсидигиталцертификате](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="d78f0-131">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="d78f0-132">Строка, указанная в таблице Мсидигиталцертификате, содержит двоичное представление сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="d78f0-132">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="d78f0-133">Проверка</span><span class="sxs-lookup"><span data-stu-id="d78f0-133">Validation</span></span>

<dl>

[<span data-ttu-id="d78f0-134">ICE39</span><span class="sxs-lookup"><span data-stu-id="d78f0-134">ICE39</span></span>](ice39.md)  
[<span data-ttu-id="d78f0-135">ICE81</span><span class="sxs-lookup"><span data-stu-id="d78f0-135">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="d78f0-136">См. также</span><span class="sxs-lookup"><span data-stu-id="d78f0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d78f0-137">мсиембеддедчаинер</span><span class="sxs-lookup"><span data-stu-id="d78f0-137">MsiEmbeddedChainer</span></span>](msiembeddedchainer-table.md)
</dt> <dt>

[<span data-ttu-id="d78f0-138">Таблица Мсидигиталцертификате</span><span class="sxs-lookup"><span data-stu-id="d78f0-138">MsiDigitalCertificate Table</span></span>](msidigitalcertificate-table.md)
</dt> </dl>

 

 



