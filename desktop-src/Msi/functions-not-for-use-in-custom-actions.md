---
description: Следующие функции базы данных никогда не должны вызываться из настраиваемого действия.
ms.assetid: 55fdd82b-9f34-4c2c-a837-8a09f21f568a
title: Функции, не предназначенные для использования в настраиваемых действиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c77c4714ca65614200cf77d6b207b6eebcaf179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663696"
---
# <a name="functions-not-for-use-in-custom-actions"></a><span data-ttu-id="b0896-103">Функции, не предназначенные для использования в настраиваемых действиях</span><span class="sxs-lookup"><span data-stu-id="b0896-103">Functions Not for Use in Custom Actions</span></span>

<span data-ttu-id="b0896-104">Следующие [функции базы данных](database-functions.md) никогда не должны вызываться из настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="b0896-104">The following [Database Functions](database-functions.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="b0896-105">**мсиконфигурепродукт**</span><span class="sxs-lookup"><span data-stu-id="b0896-105">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="b0896-106">**мсиконфигурепродуктекс**</span><span class="sxs-lookup"><span data-stu-id="b0896-106">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="b0896-107">**мсикреатетрансформсуммаринфо**</span><span class="sxs-lookup"><span data-stu-id="b0896-107">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)
-   [<span data-ttu-id="b0896-108">**мсидатабасеапплитрансформ**</span><span class="sxs-lookup"><span data-stu-id="b0896-108">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)
-   [<span data-ttu-id="b0896-109">**мсидатабасекоммит**</span><span class="sxs-lookup"><span data-stu-id="b0896-109">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)
-   [<span data-ttu-id="b0896-110">**мсидатабасикспорт**</span><span class="sxs-lookup"><span data-stu-id="b0896-110">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)
-   [<span data-ttu-id="b0896-111">**мсидатабасеженератетрансформ**</span><span class="sxs-lookup"><span data-stu-id="b0896-111">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
-   [<span data-ttu-id="b0896-112">**мсидатабасеимпорт**</span><span class="sxs-lookup"><span data-stu-id="b0896-112">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   [<span data-ttu-id="b0896-113">**мсидатабасемерже**</span><span class="sxs-lookup"><span data-stu-id="b0896-113">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)
-   [<span data-ttu-id="b0896-114">**мсиенаблелог**</span><span class="sxs-lookup"><span data-stu-id="b0896-114">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="b0896-115">**мсиенаблеуипревиев**</span><span class="sxs-lookup"><span data-stu-id="b0896-115">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
-   [<span data-ttu-id="b0896-116">**мсижетдатабасестате**</span><span class="sxs-lookup"><span data-stu-id="b0896-116">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)
-   [<span data-ttu-id="b0896-117">**мсиопендатабасе**</span><span class="sxs-lookup"><span data-stu-id="b0896-117">**MsiOpenDatabase**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
-   [<span data-ttu-id="b0896-118">**мсипревиевбиллбоард**</span><span class="sxs-lookup"><span data-stu-id="b0896-118">**MsiPreviewBillboard**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)
-   [<span data-ttu-id="b0896-119">**мсипревиевдиалог**</span><span class="sxs-lookup"><span data-stu-id="b0896-119">**MsiPreviewDialog**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
-   [<span data-ttu-id="b0896-120">**мсиреинсталлпродукт**</span><span class="sxs-lookup"><span data-stu-id="b0896-120">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="b0896-121">**мсисетекстерналуи**</span><span class="sxs-lookup"><span data-stu-id="b0896-121">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="b0896-122">**мсисетекстерналуирекорд**</span><span class="sxs-lookup"><span data-stu-id="b0896-122">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="b0896-123">**мсисетинтерналуи**</span><span class="sxs-lookup"><span data-stu-id="b0896-123">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

<span data-ttu-id="b0896-124">Следующие [функции установщика](installer-function-reference.md) никогда не должны вызываться из настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="b0896-124">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="b0896-125">**мсиапплипатч**</span><span class="sxs-lookup"><span data-stu-id="b0896-125">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [<span data-ttu-id="b0896-126">**мсиколлектусеринфо**</span><span class="sxs-lookup"><span data-stu-id="b0896-126">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
-   [<span data-ttu-id="b0896-127">**мсиконфигурефеатуре**</span><span class="sxs-lookup"><span data-stu-id="b0896-127">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
-   [<span data-ttu-id="b0896-128">**мсиконфигурепродукт**</span><span class="sxs-lookup"><span data-stu-id="b0896-128">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="b0896-129">**мсиконфигурепродуктекс**</span><span class="sxs-lookup"><span data-stu-id="b0896-129">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="b0896-130">**мсиенаблелог**</span><span class="sxs-lookup"><span data-stu-id="b0896-130">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="b0896-131">**мсижетфеатуреинфо**</span><span class="sxs-lookup"><span data-stu-id="b0896-131">**MsiGetFeatureInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
-   [<span data-ttu-id="b0896-132">**мсижетпродукткоде**</span><span class="sxs-lookup"><span data-stu-id="b0896-132">**MsiGetProductCode**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)
-   [<span data-ttu-id="b0896-133">**мсижетпродуктпроперти**</span><span class="sxs-lookup"><span data-stu-id="b0896-133">**MsiGetProductProperty**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)
-   [<span data-ttu-id="b0896-134">**мсиинсталлмиссингкомпонент**</span><span class="sxs-lookup"><span data-stu-id="b0896-134">**MsiInstallMissingComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)
-   [<span data-ttu-id="b0896-135">**мсиинсталлмиссингфиле**</span><span class="sxs-lookup"><span data-stu-id="b0896-135">**MsiInstallMissingFile**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)
-   [<span data-ttu-id="b0896-136">**мсиинсталлпродукт**</span><span class="sxs-lookup"><span data-stu-id="b0896-136">**MsiInstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
-   [<span data-ttu-id="b0896-137">**мсиопенпаккаже**</span><span class="sxs-lookup"><span data-stu-id="b0896-137">**MsiOpenPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
-   [<span data-ttu-id="b0896-138">**мсиопенпродукт**</span><span class="sxs-lookup"><span data-stu-id="b0896-138">**MsiOpenProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenproducta)
-   [<span data-ttu-id="b0896-139">**мсиреинсталлфеатуре**</span><span class="sxs-lookup"><span data-stu-id="b0896-139">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   [<span data-ttu-id="b0896-140">**мсиреинсталлпродукт**</span><span class="sxs-lookup"><span data-stu-id="b0896-140">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="b0896-141">**мсисетекстерналуи**</span><span class="sxs-lookup"><span data-stu-id="b0896-141">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="b0896-142">**мсисетинтерналуи**</span><span class="sxs-lookup"><span data-stu-id="b0896-142">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   [<span data-ttu-id="b0896-143">**мсиусефеатуре**</span><span class="sxs-lookup"><span data-stu-id="b0896-143">**MsiUseFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
-   [<span data-ttu-id="b0896-144">**мсиусефеатурикс**</span><span class="sxs-lookup"><span data-stu-id="b0896-144">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
-   [<span data-ttu-id="b0896-145">**мсиверифипаккаже**</span><span class="sxs-lookup"><span data-stu-id="b0896-145">**MsiVerifyPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)

<span data-ttu-id="b0896-146">Следующие [функции установщика](installer-function-reference.md) никогда не должны вызываться из настраиваемого действия, если это приведет к запуску другой установки.</span><span class="sxs-lookup"><span data-stu-id="b0896-146">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action if doing so starts another installation.</span></span> <span data-ttu-id="b0896-147">Они могут быть вызваны из настраиваемого действия, которое не запускает другую установку.</span><span class="sxs-lookup"><span data-stu-id="b0896-147">They may be called from a custom action that does not start another installation.</span></span>

-   [<span data-ttu-id="b0896-148">**мсипровидекомпонент**</span><span class="sxs-lookup"><span data-stu-id="b0896-148">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
-   [<span data-ttu-id="b0896-149">**мсипровидекуалифиедкомпонент**</span><span class="sxs-lookup"><span data-stu-id="b0896-149">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
-   [<span data-ttu-id="b0896-150">**мсипровидекуалифиедкомпонентекс**</span><span class="sxs-lookup"><span data-stu-id="b0896-150">**MsiProvideQualifiedComponentEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

<span data-ttu-id="b0896-151">Пользовательское действие никогда не должно создавать новый поток, использующий функции установщик Windows для изменения состояния компонента, состояния компонента или отправки сообщений из события элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b0896-151">A custom action should never spawn a new thread that uses Windows Installer functions to change the feature state, component state, or to send messages from a Control Event.</span></span> <span data-ttu-id="b0896-152">Попытка выполнить это приводит к сбою установки.</span><span class="sxs-lookup"><span data-stu-id="b0896-152">Attempting to do this causes the installation to fail.</span></span>

 

 



