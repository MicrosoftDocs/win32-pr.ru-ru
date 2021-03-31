---
description: Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются установщик Windows&\# 160; 2.0 и более ранних версий.
ms.assetid: 850b598a-338e-4f84-8336-01e962256a08
title: Не поддерживается в установщик Windows 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ee09133af9ef611a93c2511d7b130b2175561b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913259"
---
# <a name="not-supported-in-windows-installer-20"></a>Не поддерживается в установщик Windows 2,0

Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются в установщик Windows 2,0 и более ранних версиях. Отсутствие функции из этого списка не гарантирует, что эта функция поддерживается. Чтобы определить, какая версия установщик Windows требуется для конкретной функции, см. основную документацию. Сведения о других установщик Windows версиях см. [в разделе новые возможности установщик Windows](what-s-new-in-windows-installer.md).

Установщик Windows 2,0 может работать на Microsoft Windows 2000, Microsoft Windows XP или Windows Server 2003. Список всех установщик Windows версий см. в разделе [выпущенные версии установщик Windows](released-versions-of-windows-installer.md).

Следующие функции не поддерживаются в установщик Windows 2,0 и более ранних версиях.

[Функции установщика](installer-functions.md)

-   [**мсиремовепатчес**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
-   [**мсидетерминепатчсекуенце**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
-   [**мсиапплимултиплепатчес**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
-   [**мсиенумпатчесекс**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
-   [**мсижетпатчинфоекс**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
-   [**мсиенумпродуктсекс**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
-   [**мсижетпродуктинфоекс**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
-   [**мсикуерифеатурестатикс**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
-   [**мсикуерикомпонентстате**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
-   [**мсиекстрактпатчксмлдата**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
-   [**мсидетерминеаппликаблепатчес**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
-   [**мсисаурцелистенумсаурцес**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
-   [**мсисаурцелистаддсаурцеекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
-   [**мсисаурцелистклеарсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
-   [**мсисаурцелистклеараллекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
-   [**мсисаурцелистфорцересолутионекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa)
-   [**мсисаурцелистжетинфо**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
-   [**мсисаурцелистсетинфо**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
-   [**мсисаурцелистенуммедиадискс**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
-   [**мсисаурцелистаддмедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
-   [**мсисаурцелистклеармедиадиск**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)

[Структуры установщик Windows](installer-structures.md)

-   [**мсипатчсекуенцеинфо**](/windows/win32/api/msi/ns-msi-msipatchsequenceinfoa)

[Таблицы базы данных](database-tables.md)

-   [мсипатчцертификате](msipatchcertificate-table.md)
-   [мсипатчсекуенце](msipatchsequence-table.md)
-   [мсипатчметадата](msipatchmetadata-table.md)

[Свойства](properties.md)

-   [**мсидисаблелуапатчинг**](msidisableluapatching.md)
-   [**мсиенфорцеупградекомпонентрулес**](msienforceupgradecomponentrules.md)
-   [**мсипатчремове**](msipatchremove.md)
-   [**MsiPatchRemovalList**](msipatchremovallist.md)
-   [**мсиуисаурцересонли**](msiuisourceresonly.md)
-   [**мсиуихидеканцел**](msiuihidecancel.md)
-   [**мсиуипрогрессонли**](msiuiprogressonly.md)

[Системная политика](system-policy.md)

-   [дисаблелуапатчинг](disableluapatching.md)
-   [дисаблепатчунинсталл](disablepatchuninstall.md)
-   [дисаблефливеигхтпатчинг](disableflyweightpatching.md)
-   [енфорцеупградекомпонентрулес](enforceupgradecomponentrules.md)
-   [макспатчкачесизе](maxpatchcachesize.md)

[Код ошибки](error-codes.md)

-   \_Удаление исправления \_ ошибки \_ не поддерживается
-   Ошибка \_ неизвестного \_ исправления
-   \_исправление ошибки \_ без \_ последовательности
-   \_Удаление исправления \_ ошибки \_ запрещено
-   Ошибка \_ недопустимого \_ \_ XML-файла исправления
-   Ошибка при \_ исправлении \_ управляемого \_ объявленного \_ продукта

Режимы ведения журнала

-   [**ИНСТАЛЛЛОГМОДЕ \_ логонлйонеррор**](/windows/desktop/api/Msi/nf-msi-msienableloga)

[Интерфейс автоматизации](automation-interface.md)

-   Свойства [ **объекта Product**](product-object.md)

    -   [**Product. ведение**](product-usersid.md)
    -   [**Product. sources**](product-sources.md)
    -   [**Product. Медиадискс**](product-mediadisks.md)
    -   [**Product. Феатурестате**](product-featurestate.md)
    -   [**Продукт. контекст**](product-context.md)
    -   [**Product. Инсталлпроперти**](product-installproperty.md)
    -   [**Product. ProductCode**](product-productcode.md)
    -   [**Product. Компонентстате**](product-componentstate.md)
    -   [**Product. штат**](product-state.md)
    -   [**Product. Саурцелистинфо**](product-sourcelistinfo.md)

-   Методы [ **объекта Product**](product-object.md)

    -   [**Product. Саурцелистфорцересолутион**](product-sourcelistforceresolution.md)
    -   [**Product. Саурцелистклеармедиадиск**](product-sourcelistclearmediadisk.md)
    -   [**Product. Саурцелистклеаралл**](product-sourcelistclearall.md)
    -   [**Product. Саурцелистклеарсаурце**](product-sourcelistclearsource.md)
    -   [**Product. Саурцелистаддсаурце**](product-sourcelistaddsource.md)
    -   [**Product. Саурцелистаддмедиадиск**](product-sourcelistaddmediadisk.md)

-   Свойства [ **объекта Patch**](patch-object.md)

    -   [**Обновление.**](patch-usersid.md)
    -   [**Исправление. состояние**](patch-state.md)
    -   [**Исправление. источники**](patch-sources.md)
    -   [**Patch. Саурцелистинфо**](patch-sourcelistinfo.md)
    -   [**Patch. ProductCode**](patch-productcode.md)
    -   [**Patch. Патчпроперти**](patch-patchproperty.md)
    -   [**Patch. Патчкоде**](patch-patchcode.md)
    -   [**Patch. Медиадискс**](patch-mediadisks.md)
    -   [**Исправление. контекст**](patch-context.md)

-   Методы [ **объекта Patch**](patch-object.md)

    -   [**Patch. Саурцелистфорцересолутион**](patch-sourcelistforceresolution.md)
    -   [**Patch. Саурцелистклеаралл**](patch-sourcelistclearall.md)
    -   [**Patch. Саурцелистклеарсаурце**](patch-sourcelistclearsource.md)
    -   [**Patch. Саурцелистклеармедиадиск**](patch-sourcelistclearmediadisk.md)
    -   [**Patch. Саурцелистаддсаурце**](patch-sourcelistaddsource.md)
    -   [**Patch. Саурцелистаддмедиадиск**](patch-sourcelistaddmediadisk.md)

-   Свойства [ **объекта установщика**](installer-object.md)

    -   [**Установщик. Продуктсекс**](installer-productsex.md)
    -   [**Установщик. ProductInfo**](installer-productinfo.md)
    -   [**Установщик. Патчесекс**](installer-patchesex.md)

-   Методы [ **объекта установщика**](installer-object.md)

    -   [**Установщик. Апплимултиплепатчес**](installer-applymultiplepatches.md)
    -   [**Установщик. Апплипатч**](installer-applypatch.md)
    -   [**Установщик. Ремовепатчес**](installer-removepatches.md)
    -   [**Установщик. Екстрактпатчксмлдата**](installer-extractpatchxmldata.md)

Следующие функции также не поддерживаются в установщик Windows версии 2.0.2600. Установщик Windows версии 2.0.2600 была выпущена в Windows XP и Windows 2000 Server. Эти функции доступны начиная с версии установщик Windows 2.0.3790, выпущенной в Windows Server 2003. Список всех установщик Windows версий см. в разделе [выпущенные версии установщик Windows](released-versions-of-windows-installer.md).

[Функции установщика](installer-functions.md)

-   [**мсиадвертисепродуктекс**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
    -   \_экземпляр мсиадвертисеоптионс
-   [**мсиапплипатч**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**мсижетпродуктинфо**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

[Интерфейс автоматизации](automation-interface.md)

-   Методы [ **объекта установщика**](installer-object.md)

    -   [**Установщик. Апплипатч**](installer-applypatch.md)
    -   [**Установщик. ProductInfo**](installer-productinfo.md)

[Свойства](properties.md)

-   [**мсиневинстанце**](msinewinstance.md)
-   [**мсиинстанцегуид**](msiinstanceguid.md)
-   [**мсинтсуитевебсервер**](msintsuitewebserver.md)

[Параметры выполнения In-Script настраиваемого действия](custom-action-in-script-execution-options.md)

-   [**мсидбкустомактионтипетсаваре**](custom-action-in-script-execution-options.md)

[Код ошибки](error-codes.md)

-   [Ошибка при \_ установке \_ удаленного \_ запрещенного](error-codes.md)

[Политики компьютера](machine-policies.md)

-   [дисаблемси](disablemsi.md)
-   [Политика Трансформссекуре](transformssecure-policy.md)

[Параметры командной строки](command-line-options.md)

-   [/c](command-line-options.md)
-   [параметра](command-line-options.md)
-   [/лкс](command-line-options.md)

[Атрибуты элемента управления](control-attributes.md)

-   **Имажехандле** был удален

## <a name="notes"></a>Примечания

[Стандартные параметры Command-Line установщика](standard-installer-command-line-options.md) не поддерживаются установщик Windows 2,0. Вместо этого используйте [Параметры командной строки](command-line-options.md)установщик Windows.

Когда установщик Windows 2,0 устанавливает пакет исправлений, он игнорирует данные в таблицах [мсипатчсекуенце](msipatchsequence-table.md) или [мсипатчметадата](msipatchmetadata-table.md) . Более поздние версии установщик Windows могут использовать сведения в этих таблицах для улучшения последовательности, удаления и оптимизации исправлений. Дополнительные сведения о улучшении функций исправления в установщик Windows см. в разделе [Установка исправлений](patching.md).

Установщик Windows 2,0 не поддерживает удаляемые [исправления](uninstallable-patches.md) , и единственным методом удаления отдельных исправлений из приложения является удаление всего исправленного приложения и последующая повторная установка без повторного применения удаляемых исправлений.

Установщик Windows 2,0 не поддерживает последовательность исправлений и устанавливает исправления в том порядке, в котором они были предоставлены системе при [установке нескольких исправлений](installing-multiple-patches.md).

Установщик Windows 2,0 не поддерживает использование [исправлений контроля учетных записей (UAC)](user-account-control--uac--patching.md) для включения исправлений с цифровой подписью, которые могут применяться пользователями, не являющимися администраторами.

Установщик Windows 2,0 не поддерживает [оптимизацию исправлений](patch-optimization.md). Установка исправлений может занять значительно больше времени, чем в более поздних версиях установщик Windows, которые обновляют только файлы, затронутые исправлением.

Установщик Windows 2,0 не поддерживает [использование установщик Windows для инвентаризации продуктов и исправлений](inventory-products-and-patches-.md).

Установщик Windows 2,0 не поддерживает получение и изменение сведений о списке источников для установщик Windows приложений и исправлений, установленных в системе для всех пользователей. Более поздние версии установщик Windows позволяют администраторам управлять списками источников и свойствами исходного списка для сети, URL-адресов и источников мультимедиа. Более поздние версии позволяют администраторам управлять исходными списками из внешнего процесса. Дополнительные сведения см. в разделе [Управление источниками установки](managing-installation-sources.md).

Установщик Windows 2,0 не поддерживает установку нескольких экземпляров продуктов или исправлений без отдельного пакета установки для каждого экземпляра. Более поздние версии установщик Windows могут устанавливать несколько экземпляров продукта с помощью преобразований кода продукта и одного пакета MSI или одного исправления. Дополнительные сведения см. в разделе [Установка нескольких экземпляров продуктов и исправлений](installing-multiple-instances-of-products-and-patches.md).

Начиная с Windows XP с пакетом обновления 2 (SP2), установщик Windows может использовать протоколы HTTP, HTTPS и FILE. Установщик не поддерживает протоколы FTP и GOPHER.

 

 



