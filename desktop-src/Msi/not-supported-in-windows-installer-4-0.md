---
description: установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются установщик Windows&\# 160; 4.0 и более ранних версий.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: не поддерживается в установщик Windows 4,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444040fca716b6bd64c8598d2d2e36013fe19cc62971483507756a66f3e961bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558804"
---
# <a name="not-supported-in-windows-installer-40"></a>не поддерживается в установщик Windows 4,0

установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются в установщик Windows 4,0 и более ранних версиях. Отсутствие функции из этого списка не гарантирует, что эта функция поддерживается. чтобы определить, какая версия установщик Windows требуется для конкретной функции, см. основную документацию. сведения о других установщик Windows версиях см. [в разделе новые возможности установщик Windows](what-s-new-in-windows-installer.md).

Windows установщик 4,0 доступен для Microsoft Windows Server 2008 и Windows Vista. полный список всех установщик Windows версий и распространяемых компонентов см. в разделе [выпущенные версии установщик Windows](released-versions-of-windows-installer.md).

следующие функции не поддерживаются в установщик Windows 4,0 и более ранних версиях.

[Функции установщика](installer-functions.md)

-   [**мсибегинтрансактион**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)
-   [**мсиендтрансактион**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)
-   [**мсижоинтрансактион**](/windows/desktop/api/Msi/nf-msi-msijointransaction)

[Свойства](properties.md)

-   [**мсидисаблиеуи**](msidisableeeui.md)
-   [**мсиунинсталлсуперседедкомпонентс**](msiuninstallsupersededcomponents.md)

[Таблицы базы данных](database-tables.md)

-   [Таблица Мсиембеддедчаинер](msiembeddedchainer-table.md)
-   [Таблица Мсиембеддедуи](msiembeddedui-table.md)
-   [Таблица Мсипаккажецертификате](msipackagecertificate-table.md)
-   [Таблица компонентов](component-table.md)
- **мсидбкомпонентаттрибутесунинсталлонсуперседенце**  
    **мсидбкомпонентаттрибутесшаред**  
    
-   [CustomAction](customaction-table.md) ExtendedType, столбец  
    

[Параметр удаления исправления настраиваемого действия](custom-action-patch-uninstall-option.md)



[мситрансформвиев\<PatchGUID\>](msitransformview.md)  

**мсидбкустомактионтипепатчунинсталл**  


[Системная политика](system-policy.md)

-   [дисаблешаредкомпонент](disablesharedcomponent.md)
-   [мсидисаблимбеддедуи](msidisableembeddedui.md)

Прототипы функций обратного вызова

-   *ембеддедуихандлер*
-   *инитиализимбеддедуи*
-   *шутдовнембеддедуи*

[Внутренние средства оценки согласованности — ICEs](internal-consistency-evaluators-ices.md)

-   [ICE92](ice92.md) проверяет, что ни один компонент не имеет атрибутов **мсидбкомпонентаттрибутесперманент** и **мсидбкомпонентаттрибутесунинсталлонсуперседенце** .

## <a name="notes"></a>Примечания

Windows Установщик 4,0 не может выполнять [несколько установок пакетов](multiple-package-installations.md) с помощью [*обработки транзакций*](t-gly.md).

при использовании установщик Windows 4,0 или более ранних версий программы установки небольшие обновления и незначительные обновления могут завершиться сбоем при использовании политики [енфорцеупградекомпонентрулес](enforceupgradecomponentrules.md) или свойства [**мсиенфорцеупградекомпонентрулес**](msienforceupgradecomponentrules.md) , так как обновление удаляет компонент.

пользовательский пользовательский интерфейс не может быть внедрен в пакет установщик Windows с помощью метода, описанного в разделе [использование встроенного пользовательского интерфейса](using-an-embedded-ui.md).

 

 



