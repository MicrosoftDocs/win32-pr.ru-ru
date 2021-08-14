---
title: Реализация COM-объекта страницы свойств
description: Расширение страницы свойств — это COM-объект, реализованный как внутрипроцессный сервер.
ms.assetid: 77a71086-1949-4828-801e-073ea5a6838b
ms.tgt_platform: multiple
keywords:
- Реализация COM-объекта страницы свойств
- COM-объект страницы свойств, реализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504c27bcf4703bb49a3e8620c287c30ae9017ab6e65345d003f2acb6c9b544e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187615"
---
# <a name="implementing-the-property-page-com-object"></a>Реализация COM-объекта страницы свойств

Расширение страницы свойств — это COM-объект, реализованный как внутрипроцессный сервер. Расширение страницы свойств должно реализовывать интерфейсы [**ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) и [**ишеллпропшитекст**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . При отображении страницы свойств для объекта класса, для которого было зарегистрировано расширение страницы свойств, в спецификаторе отображения класса создается экземпляр расширения страницы свойств.

-   [Реализация Ишеллекстинит](#implementing-ishellextinit)
-   [Реализация Ишеллпропшитекст](#implementing-ishellpropsheetext)
-   [Передача объекта расширения на страницу свойств](#passing-the-extension-object-to-the-property-page)
-   [Работа с объектом уведомления](#working-with-the-notification-object)
-   [Прочее](#miscellaneous)
-   [Вкладки свойств с множественным выбором](#multiple-selection-property-sheets)
-   [новые с Windows Server 2003](#new-with-windows-server-2003)
-   [Связанные темы](#related-topics)

## <a name="implementing-ishellextinit"></a>Реализация Ишеллекстинит

После создания экземпляра COM-объекта расширения страницы свойств вызывается метод [**ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . **Ишеллекстинит:: Initialize** предоставляет расширение страницы свойств с объектом [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) , который содержит данные, относящиеся к объекту каталога, к которому применяется страница свойств.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) содержит данные в формате [**кфстр \_ дсобжектнамес**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) . Формат данных **кфстр \_ дсобжектнамес** — это **Хглобал** , содержащий структуру [**дсобжектнамес**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) . Структура **дсобжектнамес** содержит данные объектов каталога, к которым применяется расширение страницы свойств.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) также содержит данные в формате [**\_ \_ \_ \_ параметров отображаемой спецификации кфстр DS**](cfstr-ds-display-spec-options.md) . Формат **данных \_ \_ \_ \_ параметров отображаемой спецификации кфстр DS** — это **хглобал** , содержащий структуру [**дсдисплайспекоптионс**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) . **Дсдисплайспекоптионс** содержит данные конфигурации для использования расширением.

Если в [**ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)возвращается любое значение, отличное от **S \_ OK** , страница свойств не отображается.

Параметры *пидлфолдер* и *хкэйпрогид* метода [**ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) не используются.

Указатель [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) может быть сохранен расширением путем увеличения счетчика ссылок **IDataObject**. Этот интерфейс должен быть освобожден, если он больше не требуется.

## <a name="implementing-ishellpropsheetext"></a>Реализация Ишеллпропшитекст

После возврата [**ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) вызывается метод [**Ишеллпропшитекст:: аддпажес**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) . Расширение страницы свойств должно добавить страницу или страницы во время этого метода. Страница свойств создается путем заполнения структуры [**пропшитпаже**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) и последующей передачи этой структуры в функцию [**креатепропертишитпаже**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . Затем страница свойств добавляется на вкладку свойств путем вызова функции обратного вызова, передаваемой в **ишеллпропшитекст:: аддпажес** в параметре *лпфнаддпаже* .

Если в [**ишеллпропшитекст:: аддпажес**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)возвращается любое значение, отличное от **S \_ OK** , страница свойств не отображается.

Если расширение таблицы свойств не требуется для добавления каких-либо страниц на страницу свойств, оно не должно вызывать функцию обратного вызова, переданную в [**ишеллпропшитекст:: аддпажес**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) в параметре *лпфнаддпаже* .

Метод [**ишеллпропшитекст:: реплацепаже**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) не используется.

## <a name="passing-the-extension-object-to-the-property-page"></a>Передача объекта расширения на страницу свойств

Объект расширения страницы свойств независим от страницы свойств. Во многих случаях желательно иметь возможность использовать объект расширения или какой-либо другой объект на странице свойств. Для этого задайте для члена **lParam** структуры [**пропшитпаже**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) указатель на объект. После этого страница свойств может получить это значение при обработке сообщения [**WM \_ инитдиалог**](../dlgbox/wm-initdialog.md) . Для страницы свойств параметр *lParam* сообщения **WM \_ инитдиалог** является указателем на структуру **пропшитпаже** . Получите указатель объекта путем приведения *lParam* сообщения **WM \_ Инитдиалог** к указателю **Пропшитпаже** , а затем извлечения члена **lParam** структуры **пропшитпаже** .

В следующем примере кода C++ показано, как передать объект на страницу свойств.


```C++
case WM_INITDIALOG:
    {
        LPPROPSHEETPAGE pPage = (LPPROPSHEETPAGE)lParam;

        if(NULL != pPage)
        {
            CPropSheetExt *pPropSheetExt;
            pPropSheetExt = (CPropSheetExt*)pPage->lParam;

            if(pPropSheetExt)
            {
                return pPropSheetExt>OnInitDialog(wParam, lParam);
            }
        }
    }
    break;
```



Имейте в виду, что после вызова [**ишеллпропшитекст:: аддпажес**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) страница свойств освободит объект расширения страницы свойств и никогда не будет использовать его повторно. Это означает, что объект расширения будет удален до отображения страницы свойств. Когда страница пытается получить доступ к указателю объекта, память будет освобождена и указатель будет недопустимым. Чтобы исправить это, увеличьте счетчик ссылок для объекта расширения при добавлении страницы и отпустите объект при уничтожении диалогового окна страницы свойств. Это создает еще одну ошибку, поскольку диалоговое окно страницы свойств не создается до тех пор, пока страница не будет отображена в первый раз. Если пользователь никогда не выбирает страницу расширения, страница никогда не создается и уничтожается. В результате объект расширения никогда не будет освобожден, поэтому происходит утечка памяти. Чтобы избежать этого, реализуйте функцию обратного вызова страницы свойств. Для этого добавьте флаг **PSP \_ усекаллбакк** в элемент **dwFlags** структуры [**Пропшитпаже**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) и присвойте элементу **пфнкаллбакк** структуры **пропшитпаже** адрес реализованной функции [**пропшитпажепрок**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) . Когда функция **пропшитпажепрок** получает уведомление о **\_ выпуске пспкб** , параметр *ППСП* объекта **пропшитпажепрок** содержит указатель на структуру **пропшитпаже** . Член **lParam** структуры **пропшитпаже** содержит указатель расширения, который можно использовать для освобождения объекта.

В следующем примере кода C++ показано, как освободить объект расширения.


```C++
UINT CALLBACK CPropSheetExt::PageCallbackProc(  HWND hWnd,
                                                UINT uMsg,
                                                LPPROPSHEETPAGE ppsp)
{
    switch(uMsg)
    {
    case PSPCB_CREATE:
        // Must return TRUE to enable the page to be created.
        return TRUE;

    case PSPCB_RELEASE:
        {
            /*
            Release the object. This is called even if the page dialog box was 
            never actually created.
            */
            CPropSheetExt *pPropSheetExt = (CPropSheetExt*)ppsp->lParam;

            if(pPropSheetExt)
            {
                pPropSheetExt->Release();
            }
        }
        break;
    }

    return FALSE;
}
```



## <a name="working-with-the-notification-object"></a>Работа с объектом уведомления

Так как страницы расширения таблицы свойств отображаются на странице свойств, созданной компонентом, неизвестным для расширения, необходимо использовать "Manager" для обработки обмена данными между страницами расширения и страницей свойств. Этот диспетчер называется объектом уведомления. Объект уведомления функционирует как ведущий между отдельными страницами и страницей свойств.

Когда инициализируется объект расширения страницы свойств, расширение должно создать объект уведомления путем вызова [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)и передачи [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) , полученного из [**ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) , и имени объекта каталога. Нет необходимости увеличивать значение счетчика ссылок интерфейса **IDataObject** , поскольку это будет сделано объектом уведомления, созданным функцией **адспропкреатенотифйобж** . Обработчик объекта уведомления, предоставленный **адспропкреатенотифйобж** , должен быть сохранен для последующего использования. **Адспропкреатенотифйобж** можно вызывать во время **Ишеллекстинит:: Initialize** или [**ишеллпропшитекст:: аддпажес**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Когда расширение страницы свойств завершит работу, оно должно отправить в объект уведомления [**сообщение \_ \_ о \_ выходе адспроп**](wm-adsprop-notify-exit.md) . Это приводит к уничтожению объекта уведомления. Это лучше выполнить, когда функция [**пропшитпажепрок**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) получает уведомление о **\_ выпуске пспкб** .

Расширение страницы свойств может получать данные в дополнение к, которое предоставляется в формате буфера обмена [**кфстр \_ дсобжектнамес**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) путем вызова [**адспропжетинитинфо**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo). Одним из преимуществ использования **адспропжетинитинфо** является то, что он предоставляет объект [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) , используемый для программной работы с объектом каталога.

> [!Note]  
> В отличие от большинства методов и функций COM, [**адспропжетинитинфо**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) не увеличивает счетчик ссылок для объекта [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) . **Идиректорйобжект** не должно освобождаться, пока число ссылок не будет увеличиваться вручную.

 

При первом создании страницы свойств расширение должно зарегистрировать страницу с объектом уведомления, вызвав [**адспропсесвнд**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) с маркером окна страницы.

[**Адспропчеккифвритабле**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcheckifwritable) — это служебная функция, которую расширение страницы свойств может использовать для определения возможности написания свойства.

## <a name="miscellaneous"></a>Разное

Маркер страницы свойств передается в процедуру диалогового окна страницы. Страница свойств является прямым родителем страницы свойств, поэтому ее можно получить, вызвав функцию- [**родитель**](/windows/win32/api/winuser/nf-winuser-getparent) с помощью маркера страницы свойств.

При изменении содержимого страницы расширения расширение должно использовать макрос [**пропшит \_ Changed**](/windows/win32/api/prsht/nf-prsht-propsheet_changed) для уведомления страницы свойств об изменениях. После этого на странице свойств будет включена кнопка Применить.

## <a name="multiple-selection-property-sheets"></a>Страницы свойств Multiple-Selection

в операционных системах Windows Server 2003 и более поздних версий оснастки MMC Active Directory администрирования поддерживают расширения страниц свойств для нескольких объектов каталога. Эти страницы свойств отображаются, когда свойства просматриваются более чем по одному элементу за раз. Основное различие между расширением таблицы свойств с одним выбором и расширением таблицы свойств с множественным выбором заключается в том, что структура [**дсобжектнамес**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) , предоставляемая форматом буфера обмена [**Кфстр \_ дсобжектнамес**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) в [**ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) , будет содержать более одной структуры [**дсобжект**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

При создании объекта уведомления расширение таблицы свойств с множественным выбором должно передавать уникальное имя, предоставленное оснасткой, а не имя, созданное расширением. Чтобы получить уникальное имя, запросите формат буфера обмена [**кфстр \_ DS \_ мултиселектпроппаже**](cfstr-ds-multiselectproppage.md) из [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) , полученного из [**ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Эти данные являются **хглобал** , содержащим строку в Юникоде, завершающуюся нулем, которая является уникальным именем. Это уникальное имя затем передается функции [**адспропкреатенотифйобж**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) для создания объекта уведомления. Пример функции **креатеадснотификатионобжект** в [примере кода для реализации com-объекта страницы свойств](example-code-for-implementation-of-the-property-sheet-com-object.md) демонстрирует, как это сделать правильно, а также обеспечить совместимость с более ранними версиями оснастки, которые не поддерживают вкладки свойств с множественным выбором.

Для страниц свойств с множественным выбором система привязывается только к первому объекту в массиве [**дсобжект**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) . Из-за этого [**адспропжетинитинфо**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) предоставляет только атрибуты [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) и Write для первого объекта в массиве. Другие объекты в массиве не привязаны к.

Расширение вкладки свойств с множественным выбором регистрируется в атрибуте [**админмултиселектпропертипажес**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .

## <a name="new-with-windows-server-2003"></a>новые с Windows Server 2003

ниже перечислены новые возможности Windows Server 2003.

Если на странице свойств обнаружена ошибка, [**адспропсендеррормессаже**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) можно вызвать с соответствующими данными об ошибке. **Адспропсендеррормессаже** будет хранить все сообщения об ошибках в очереди. Эти сообщения будут отображаться при следующем вызове [**адспропшоверрордиалог**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) . Когда **адспропшоверрордиалог** возвращает, сообщения в очереди удаляются.

Windows В сервере 2003 введена функция [**адспропсесвндвиститле**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwndwithtitle) . Эта функция похожа на [**адспропсесвнд**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd), но включает заголовок страницы. Это позволяет диалоговое окно ошибки, отображаемое [**адспропшоверрордиалог**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) , позволяет пользователю получить более полезные данные. Если расширение страницы свойств использует функцию **адспропшоверрордиалог** , то расширение должно использовать **адспропсесвндвиститле** , а не **адспропсесвнд**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Пример кода для реализации COM-объекта страницы свойств](example-code-for-implementation-of-the-property-sheet-com-object.md)
</dt> </dl>

 

 