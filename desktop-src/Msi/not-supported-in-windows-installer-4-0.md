---
description: Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются установщик Windows&\# 160; 4.0 и более ранних версий.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: Не поддерживается в установщик Windows 4,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4307422c71976057948759078dc321e38dc543b7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105674575"
---
# <a name="not-supported-in-windows-installer-40"></a>Не поддерживается в установщик Windows 4,0

Установщик Windows функции, таблицы и свойства, перечисленные на этой странице, не поддерживаются в установщик Windows 4,0 и более ранних версиях. Отсутствие функции из этого списка не гарантирует, что эта функция поддерживается. Чтобы определить, какая версия установщик Windows требуется для конкретной функции, см. основную документацию. Сведения о других установщик Windows версиях см. [в разделе новые возможности установщик Windows](what-s-new-in-windows-installer.md).

Установщик Windows 4,0 доступна для Microsoft Windows Server 2008 и Windows Vista. Полный список всех установщик Windows версий и распространяемых компонентов см. в разделе [выпущенные версии установщик Windows](released-versions-of-windows-installer.md).

Следующие функции не поддерживаются в установщик Windows 4,0 и более ранних версиях.

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

Установщик Windows 4,0 не может выполнять [несколько установок пакетов](multiple-package-installations.md) с помощью [*обработки транзакций*](t-gly.md).

При использовании установщик Windows 4,0 или более ранних версий программы установки небольшие обновления и незначительные обновления могут завершиться сбоем при использовании политики [енфорцеупградекомпонентрулес](enforceupgradecomponentrules.md) или свойства [**мсиенфорцеупградекомпонентрулес**](msienforceupgradecomponentrules.md) , так как обновление удаляет компонент.

Пользовательский пользовательский интерфейс не может быть внедрен в пакет установщик Windows с помощью метода, описанного в разделе [Использование встроенного пользовательского интерфейса](using-an-embedded-ui.md).

 

 



