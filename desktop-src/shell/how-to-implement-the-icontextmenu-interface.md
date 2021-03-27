---
description: IContextMenu является самым мощным, но также самым сложным интерфейсом для реализации.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Реализация интерфейса IContextMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f251b9a64c3f401239eeb7c88286c016f399cc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998451"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a>Реализация интерфейса IContextMenu

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) является самым мощным, но также самым сложным интерфейсом для реализации. Настоятельно рекомендуется реализовать команду с помощью одного из статических методов глагола. Дополнительные сведения см. [в разделе Выбор метода статического или динамического контекстного меню](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) содержит три метода: [**жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)и [**куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), которые подробно обсуждаются.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   C++

### <a name="prerequisites"></a>Предварительные условия

-   Статическая команда
-   Контекстное меню

## <a name="instructions"></a>Инструкции

### <a name="icontextmenugetcommandstring-method"></a>Метод IContextMenu:: Жеткоммандстринг

Метод [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) обработчика используется для возврата канонического имени для команды. Этот метод является необязательным. В Windows XP и более ранних версиях Windows, когда в проводнике Windows есть строка состояния, этот метод используется для получения текста справки, который отображается в строке состояния для пункта меню.

Параметр *идкмд* содержит смещение идентификатора команды, которая была определена при вызове [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) . При запросе строки справки для *уфлагс* будет задано значение **GC \_ хелптекств**. Скопируйте строку справки в буфер *pszName* , приведя ее к **пвстр**. Строка команды запрашивается путем установки *уфлагс* в **GC \_ вербв**. Скопируйте соответствующую строку в *pszName*, точно так же, как и строку справки. Флаги валидатев **GC \_** и **GC \_** не используются обработчиками контекстного меню.

В следующем примере показана простая реализация [**жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) , которая соответствует примеру [**куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , приведенному в разделе [метод IContextMenu:: куериконтекстмену](shortcut-menu-using-dynamic-verbs.md) этой статьи. Поскольку обработчик добавляет только один пункт меню, можно вернуть только один набор строк. Метод проверяет, является ли *идкмд* допустимым, и, если это так, возвращает запрошенную строку.

Функция [**стрингкчкопи**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) используется для копирования запрашиваемой строки в *pszName* , чтобы гарантировать, что копируемая строка не превысит размер буфера, указанного в *кчнаме*. Этот пример реализует поддержку только для значений Юникода *уфлагс*, поскольку только они использовались в проводнике Windows с момента выпуска Windows 2000.


```
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb that is passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a>Метод IContextMenu:: Инвокекомманд

Этот метод вызывается, когда пользователь щелкает элемент меню, чтобы указать обработчику выполнить связанную команду. Параметр *пиЦи* указывает на структуру, содержащую сведения, необходимые для выполнения команды.

Хотя *пиЦи* объявляется в шлобж. h как структура [**кминвокекоммандинфо**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , на практике он часто указывает на структуру [**кминвокекоммандинфоекс**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) . Эта структура является расширенной версией **кминвокекоммандинфо** и содержит несколько дополнительных членов, которые позволяют передавать строки в Юникоде.

Проверьте член **кбсизе** объекта *пиЦи* , чтобы определить, какая структура была передана. Если это структура [**кминвокекоммандинфоекс**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) , а у члена **фмаск** установлен флаг **\_ \_ Юникода Mask** , приведите *пиЦи* к **кминвокекоммандинфоекс**. Это позволяет приложению использовать сведения в Юникоде, содержащиеся в последних пяти элементах структуры.

Элемент **лпверб** или **лпвербв** структуры используется для задания выполняемой команды. Команды идентифицируются одним из следующих двух способов.

-   В строке команд команды
-   По смещению идентификатора команды

Чтобы отличить эти два варианта, проверьте, что в регистре Юникода или **лпвербв** используется слово высокого порядка **ЛПВЕРБ** для регистра ANSI. Если слово с высоким порядком не равно нулю, **лпверб** или **лпвербв** содержит строку команды. Если слово с высоким порядковым значением равно нулю, то смещение команды находится в слове **лпверб** нижнего порядка.

В следующем примере показана простая реализация [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) , которая соответствует примерам [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) и [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) , заданным до и после этого раздела. Сначала метод определяет, какая структура передается. Затем он определяет, определена ли команда по смещению или ее команде. Если **лпверб** или **лпвербв** содержит допустимую глагол или смещение, метод отображает окно сообщения.


```
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a>Метод IContextMenu:: Куериконтекстмену

Оболочка вызывает [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , чтобы обработчик контекстного меню добавим в меню соответствующие элементы меню. Он передает маркер **HMENU** в параметре *HMENU* . Для параметра *индексмену* задается индекс, используемый для первого добавляемого элемента меню.

Все элементы меню, добавленные обработчиком, должны иметь идентификаторы, попадающие в значения параметров *идкмдфирст* и *идкмдласт* . Как правило, первый идентификатор команды имеет значение *идкмдфирст*, что увеличивается на единицу (1) для каждой дополнительной команды. Такой подход позволяет избежать превышения *идкмдласт* и максимально увеличить количество доступных идентификаторов в случае, если оболочка вызывает несколько обработчиков.

*Смещение команды* идентификатора элемента — это разница между идентификатором и значением в *идкмдфирст*. Сохраните смещение каждого элемента, добавляемого обработчиком, в контекстное меню, так как оболочка может использовать смещение для указания элемента, если впоследствии вызывает [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) или [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

Необходимо также назначить [команду](launch.md) для каждой добавляемой команды. Глагол — это строка, которую можно использовать вместо смещения для задания команды при вызове [**инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) . Он также используется такими функциями, как [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для выполнения команд контекстного меню.

Существует три флага, которые можно передать с помощью параметра *уфлагс* , относящегося к обработчикам контекстного меню. Они описаны в следующей таблице.



| Flag             | Описание                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| КМФ \_ дефаултонли | Пользователь выбрал команду по умолчанию, обычно дважды щелкнув объект. [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) должен возвращать управление в оболочку без изменения меню. |
| КМФ \_ по умолчанию   | Ни один элемент в меню не должен быть элементом по умолчанию. Метод должен добавить в меню свои команды.                                                                                                                          |
| КМФ, \_ Обычная      | Контекстное меню будет отображаться в обычном режиме. Метод должен добавить в меню свои команды.                                                                                                                            |



 

Чтобы добавить пункты меню в список, используйте [**инсертмену**](/windows/win32/api/winuser/nf-winuser-insertmenua) или [**инсертменуитем**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) . Затем возвращается значение **HRESULT** с уровнем серьезности " \_ успешно". В качестве значения кода задайте смещение самого крупного идентификатора команды, который был назначен, плюс один (1). Например, предположим, что *идкмдфирст* имеет значение 5, и в меню добавляются три элемента с идентификаторами команд 5, 7 и 8. Возвращаемое значение должно быть равно \_ HRESULT ( \_ УСПЕШНОе серьезность, 0, 8 + 1).

В следующем примере показана простая реализация [**куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , которая вставляет одну команду. Смещение идентификатора для команды равно \_ отображению IDM, для которого задано значение 0. Переменные **m \_ псзверб** и **m \_ пвсзверб** являются частными переменными, которые используются для хранения связанной с ними независимой от языка строки в форматах ANSI и Unicode.


```
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a>Примечания

Другие задачи по реализации команд см. в разделе [Создание обработчиков контекстного меню](context-menu-handlers.md).

 

 
