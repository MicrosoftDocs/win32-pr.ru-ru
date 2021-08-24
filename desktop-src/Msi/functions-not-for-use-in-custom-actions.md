---
description: Следующие функции базы данных никогда не должны вызываться из настраиваемого действия.
ms.assetid: 55fdd82b-9f34-4c2c-a837-8a09f21f568a
title: Функции, не предназначенные для использования в настраиваемых действиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaddf6edae9636a599996a4ab8208537c1c673687337b65a9fcb74d1a8fc1f58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649624"
---
# <a name="functions-not-for-use-in-custom-actions"></a>Функции, не предназначенные для использования в настраиваемых действиях

Следующие [функции базы данных](database-functions.md) никогда не должны вызываться из настраиваемого действия.

-   [**мсиконфигурепродукт**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [**мсиконфигурепродуктекс**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)
-   [**мсидатабасеапплитрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)
-   [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)
-   [**мсидатабасикспорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)
-   [**мсидатабасеженератетрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
-   [**мсидатабасеимпорт**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   [**мсидатабасемерже**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)
-   [**мсиенаблелог**](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [**мсиенаблеуипревиев**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
-   [**мсижетдатабасестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)
-   [**мсиопендатабасе**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
-   [**мсипревиевбиллбоард**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)
-   [**мсипревиевдиалог**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
-   [**мсиреинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [**мсисетекстерналуи**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [**мсисетекстерналуирекорд**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

Следующие [функции установщика](installer-function-reference.md) никогда не должны вызываться из настраиваемого действия.

-   [**мсиапплипатч**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**мсиколлектусеринфо**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
-   [**мсиконфигурефеатуре**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
-   [**мсиконфигурепродукт**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [**мсиконфигурепродуктекс**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [**мсиенаблелог**](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [**мсижетфеатуреинфо**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
-   [**мсижетпродукткоде**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)
-   [**мсижетпродуктпроперти**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)
-   [**мсиинсталлмиссингкомпонент**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)
-   [**мсиинсталлмиссингфиле**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)
-   [**мсиинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
-   [**мсиопенпаккаже**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
-   [**мсиопенпродукт**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)
-   [**мсиреинсталлфеатуре**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   [**мсиреинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [**мсисетекстерналуи**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [**мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   [**мсиусефеатуре**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
-   [**мсиусефеатурикс**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
-   [**мсиверифипаккаже**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)

Следующие [функции установщика](installer-function-reference.md) никогда не должны вызываться из настраиваемого действия, если это приведет к запуску другой установки. Они могут быть вызваны из настраиваемого действия, которое не запускает другую установку.

-   [**мсипровидекомпонент**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
-   [**мсипровидекуалифиедкомпонент**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
-   [**мсипровидекуалифиедкомпонентекс**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

пользовательское действие никогда не должно создавать новый поток, использующий функции установщик Windows для изменения состояния компонента, состояния компонента или отправки сообщений из события элемента управления. Попытка выполнить это приводит к сбою установки.

 

 



