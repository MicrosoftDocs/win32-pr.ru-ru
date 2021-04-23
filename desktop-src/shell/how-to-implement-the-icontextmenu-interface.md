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
# <a name="how-to-implement-the-icontextmenu-interface"></a><span data-ttu-id="df705-103">Реализация интерфейса IContextMenu</span><span class="sxs-lookup"><span data-stu-id="df705-103">How to Implement the IContextMenu Interface</span></span>

<span data-ttu-id="df705-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) является самым мощным, но также самым сложным интерфейсом для реализации.</span><span class="sxs-lookup"><span data-stu-id="df705-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated interface to implement.</span></span> <span data-ttu-id="df705-105">Настоятельно рекомендуется реализовать команду с помощью одного из статических методов глагола.</span><span class="sxs-lookup"><span data-stu-id="df705-105">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="df705-106">Дополнительные сведения см. [в разделе Выбор метода статического или динамического контекстного меню](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="df705-106">For more information, see [Choosing a Static or Dynamic Shortcut Menu Method](shortcut-choose-method.md).</span></span> <span data-ttu-id="df705-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) содержит три метода: [**жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)и [**куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), которые подробно обсуждаются.</span><span class="sxs-lookup"><span data-stu-id="df705-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand), and [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which are discussed here in detail.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="df705-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="df705-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="df705-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="df705-109">Technologies</span></span>

-   <span data-ttu-id="df705-110">C++</span><span class="sxs-lookup"><span data-stu-id="df705-110">C++</span></span>

### <a name="prerequisites"></a><span data-ttu-id="df705-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="df705-111">Prerequisites</span></span>

-   <span data-ttu-id="df705-112">Статическая команда</span><span class="sxs-lookup"><span data-stu-id="df705-112">Static Verb</span></span>
-   <span data-ttu-id="df705-113">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="df705-113">Shortcut Menu</span></span>

## <a name="instructions"></a><span data-ttu-id="df705-114">Инструкции</span><span class="sxs-lookup"><span data-stu-id="df705-114">Instructions</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="df705-115">Метод IContextMenu:: Жеткоммандстринг</span><span class="sxs-lookup"><span data-stu-id="df705-115">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="df705-116">Метод [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) обработчика используется для возврата канонического имени для команды.</span><span class="sxs-lookup"><span data-stu-id="df705-116">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="df705-117">Этот метод является необязательным.</span><span class="sxs-lookup"><span data-stu-id="df705-117">This method is optional.</span></span> <span data-ttu-id="df705-118">В Windows XP и более ранних версиях Windows, когда в проводнике Windows есть строка состояния, этот метод используется для получения текста справки, который отображается в строке состояния для пункта меню.</span><span class="sxs-lookup"><span data-stu-id="df705-118">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="df705-119">Параметр *идкмд* содержит смещение идентификатора команды, которая была определена при вызове [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="df705-119">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="df705-120">При запросе строки справки для *уфлагс* будет задано значение **GC \_ хелптекств**.</span><span class="sxs-lookup"><span data-stu-id="df705-120">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="df705-121">Скопируйте строку справки в буфер *pszName* , приведя ее к **пвстр**.</span><span class="sxs-lookup"><span data-stu-id="df705-121">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="df705-122">Строка команды запрашивается путем установки *уфлагс* в **GC \_ вербв**.</span><span class="sxs-lookup"><span data-stu-id="df705-122">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="df705-123">Скопируйте соответствующую строку в *pszName*, точно так же, как и строку справки.</span><span class="sxs-lookup"><span data-stu-id="df705-123">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="df705-124">Флаги валидатев **GC \_** и **GC \_** не используются обработчиками контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="df705-124">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="df705-125">В следующем примере показана простая реализация [**жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) , которая соответствует примеру [**куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , приведенному в разделе [метод IContextMenu:: куериконтекстмену](shortcut-menu-using-dynamic-verbs.md) этой статьи.</span><span class="sxs-lookup"><span data-stu-id="df705-125">The following example shows a simple implementation of [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](shortcut-menu-using-dynamic-verbs.md) section of this topic.</span></span> <span data-ttu-id="df705-126">Поскольку обработчик добавляет только один пункт меню, можно вернуть только один набор строк.</span><span class="sxs-lookup"><span data-stu-id="df705-126">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="df705-127">Метод проверяет, является ли *идкмд* допустимым, и, если это так, возвращает запрошенную строку.</span><span class="sxs-lookup"><span data-stu-id="df705-127">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="df705-128">Функция [**стрингкчкопи**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) используется для копирования запрашиваемой строки в *pszName* , чтобы гарантировать, что копируемая строка не превысит размер буфера, указанного в *кчнаме*.</span><span class="sxs-lookup"><span data-stu-id="df705-128">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="df705-129">Этот пример реализует поддержку только для значений Юникода *уфлагс*, поскольку только они использовались в проводнике Windows с момента выпуска Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="df705-129">This example implements support only for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


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



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="df705-130">Метод IContextMenu:: Инвокекомманд</span><span class="sxs-lookup"><span data-stu-id="df705-130">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="df705-131">Этот метод вызывается, когда пользователь щелкает элемент меню, чтобы указать обработчику выполнить связанную команду.</span><span class="sxs-lookup"><span data-stu-id="df705-131">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="df705-132">Параметр *пиЦи* указывает на структуру, содержащую сведения, необходимые для выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="df705-132">The *pici* parameter points to a structure that contains the information required to run the command.</span></span>

<span data-ttu-id="df705-133">Хотя *пиЦи* объявляется в шлобж. h как структура [**кминвокекоммандинфо**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , на практике он часто указывает на структуру [**кминвокекоммандинфоекс**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) .</span><span class="sxs-lookup"><span data-stu-id="df705-133">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="df705-134">Эта структура является расширенной версией **кминвокекоммандинфо** и содержит несколько дополнительных членов, которые позволяют передавать строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="df705-134">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="df705-135">Проверьте член **кбсизе** объекта *пиЦи* , чтобы определить, какая структура была передана.</span><span class="sxs-lookup"><span data-stu-id="df705-135">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="df705-136">Если это структура [**кминвокекоммандинфоекс**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) , а у члена **фмаск** установлен флаг **\_ \_ Юникода Mask** , приведите *пиЦи* к **кминвокекоммандинфоекс**.</span><span class="sxs-lookup"><span data-stu-id="df705-136">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="df705-137">Это позволяет приложению использовать сведения в Юникоде, содержащиеся в последних пяти элементах структуры.</span><span class="sxs-lookup"><span data-stu-id="df705-137">This enables your application to use the Unicode information that is contained in the last five members of the structure.</span></span>

<span data-ttu-id="df705-138">Элемент **лпверб** или **лпвербв** структуры используется для задания выполняемой команды.</span><span class="sxs-lookup"><span data-stu-id="df705-138">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="df705-139">Команды идентифицируются одним из следующих двух способов.</span><span class="sxs-lookup"><span data-stu-id="df705-139">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="df705-140">В строке команд команды</span><span class="sxs-lookup"><span data-stu-id="df705-140">By the command's verb string</span></span>
-   <span data-ttu-id="df705-141">По смещению идентификатора команды</span><span class="sxs-lookup"><span data-stu-id="df705-141">By the command's identifier offset</span></span>

<span data-ttu-id="df705-142">Чтобы отличить эти два варианта, проверьте, что в регистре Юникода или **лпвербв** используется слово высокого порядка **ЛПВЕРБ** для регистра ANSI.</span><span class="sxs-lookup"><span data-stu-id="df705-142">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="df705-143">Если слово с высоким порядком не равно нулю, **лпверб** или **лпвербв** содержит строку команды.</span><span class="sxs-lookup"><span data-stu-id="df705-143">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="df705-144">Если слово с высоким порядковым значением равно нулю, то смещение команды находится в слове **лпверб** нижнего порядка.</span><span class="sxs-lookup"><span data-stu-id="df705-144">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="df705-145">В следующем примере показана простая реализация [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) , которая соответствует примерам [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) и [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) , заданным до и после этого раздела.</span><span class="sxs-lookup"><span data-stu-id="df705-145">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="df705-146">Сначала метод определяет, какая структура передается.</span><span class="sxs-lookup"><span data-stu-id="df705-146">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="df705-147">Затем он определяет, определена ли команда по смещению или ее команде.</span><span class="sxs-lookup"><span data-stu-id="df705-147">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="df705-148">Если **лпверб** или **лпвербв** содержит допустимую глагол или смещение, метод отображает окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="df705-148">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


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



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="df705-149">Метод IContextMenu:: Куериконтекстмену</span><span class="sxs-lookup"><span data-stu-id="df705-149">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="df705-150">Оболочка вызывает [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , чтобы обработчик контекстного меню добавим в меню соответствующие элементы меню.</span><span class="sxs-lookup"><span data-stu-id="df705-150">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="df705-151">Он передает маркер **HMENU** в параметре *HMENU* .</span><span class="sxs-lookup"><span data-stu-id="df705-151">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="df705-152">Для параметра *индексмену* задается индекс, используемый для первого добавляемого элемента меню.</span><span class="sxs-lookup"><span data-stu-id="df705-152">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="df705-153">Все элементы меню, добавленные обработчиком, должны иметь идентификаторы, попадающие в значения параметров *идкмдфирст* и *идкмдласт* .</span><span class="sxs-lookup"><span data-stu-id="df705-153">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="df705-154">Как правило, первый идентификатор команды имеет значение *идкмдфирст*, что увеличивается на единицу (1) для каждой дополнительной команды.</span><span class="sxs-lookup"><span data-stu-id="df705-154">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="df705-155">Такой подход позволяет избежать превышения *идкмдласт* и максимально увеличить количество доступных идентификаторов в случае, если оболочка вызывает несколько обработчиков.</span><span class="sxs-lookup"><span data-stu-id="df705-155">This practice helps you to avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="df705-156">*Смещение команды* идентификатора элемента — это разница между идентификатором и значением в *идкмдфирст*.</span><span class="sxs-lookup"><span data-stu-id="df705-156">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="df705-157">Сохраните смещение каждого элемента, добавляемого обработчиком, в контекстное меню, так как оболочка может использовать смещение для указания элемента, если впоследствии вызывает [**IContextMenu:: жеткоммандстринг**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) или [**IContextMenu:: инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="df705-157">Store the offset of each item that your handler adds to the shortcut menu, because the Shell might use the offset to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="df705-158">Необходимо также назначить [команду](launch.md) для каждой добавляемой команды.</span><span class="sxs-lookup"><span data-stu-id="df705-158">You should also assign a [verb](launch.md) to each command that you add.</span></span> <span data-ttu-id="df705-159">Глагол — это строка, которую можно использовать вместо смещения для задания команды при вызове [**инвокекомманд**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="df705-159">A verb is a string that can be used instead of the offset to identify the command when [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="df705-160">Он также используется такими функциями, как [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для выполнения команд контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="df705-160">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="df705-161">Существует три флага, которые можно передать с помощью параметра *уфлагс* , относящегося к обработчикам контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="df705-161">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="df705-162">Они описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="df705-162">They are described in the following table.</span></span>



| <span data-ttu-id="df705-163">Flag</span><span class="sxs-lookup"><span data-stu-id="df705-163">Flag</span></span>             | <span data-ttu-id="df705-164">Описание</span><span class="sxs-lookup"><span data-stu-id="df705-164">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df705-165">КМФ \_ дефаултонли</span><span class="sxs-lookup"><span data-stu-id="df705-165">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="df705-166">Пользователь выбрал команду по умолчанию, обычно дважды щелкнув объект.</span><span class="sxs-lookup"><span data-stu-id="df705-166">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="df705-167">[**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) должен возвращать управление в оболочку без изменения меню.</span><span class="sxs-lookup"><span data-stu-id="df705-167">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="df705-168">КМФ \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="df705-168">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="df705-169">Ни один элемент в меню не должен быть элементом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="df705-169">No item in the menu should be the default item.</span></span> <span data-ttu-id="df705-170">Метод должен добавить в меню свои команды.</span><span class="sxs-lookup"><span data-stu-id="df705-170">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="df705-171">КМФ, \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="df705-171">CMF\_NORMAL</span></span>      | <span data-ttu-id="df705-172">Контекстное меню будет отображаться в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="df705-172">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="df705-173">Метод должен добавить в меню свои команды.</span><span class="sxs-lookup"><span data-stu-id="df705-173">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="df705-174">Чтобы добавить пункты меню в список, используйте [**инсертмену**](/windows/win32/api/winuser/nf-winuser-insertmenua) или [**инсертменуитем**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) .</span><span class="sxs-lookup"><span data-stu-id="df705-174">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="df705-175">Затем возвращается значение **HRESULT** с уровнем серьезности " \_ успешно".</span><span class="sxs-lookup"><span data-stu-id="df705-175">Then return an **HRESULT** value with the severity set to SEVERITY\_SUCCESS.</span></span> <span data-ttu-id="df705-176">В качестве значения кода задайте смещение самого крупного идентификатора команды, который был назначен, плюс один (1).</span><span class="sxs-lookup"><span data-stu-id="df705-176">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="df705-177">Например, предположим, что *идкмдфирст* имеет значение 5, и в меню добавляются три элемента с идентификаторами команд 5, 7 и 8.</span><span class="sxs-lookup"><span data-stu-id="df705-177">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="df705-178">Возвращаемое значение должно быть равно \_ HRESULT ( \_ УСПЕШНОе серьезность, 0, 8 + 1).</span><span class="sxs-lookup"><span data-stu-id="df705-178">The return value should be MAKE\_HRESULT(SEVERITY\_SUCCESS, 0, 8 + 1).</span></span>

<span data-ttu-id="df705-179">В следующем примере показана простая реализация [**куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , которая вставляет одну команду.</span><span class="sxs-lookup"><span data-stu-id="df705-179">The following example shows a simple implementation of [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="df705-180">Смещение идентификатора для команды равно \_ отображению IDM, для которого задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="df705-180">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="df705-181">Переменные **m \_ псзверб** и **m \_ пвсзверб** являются частными переменными, которые используются для хранения связанной с ними независимой от языка строки в форматах ANSI и Unicode.</span><span class="sxs-lookup"><span data-stu-id="df705-181">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables that are used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="df705-182">Примечания</span><span class="sxs-lookup"><span data-stu-id="df705-182">Remarks</span></span>

<span data-ttu-id="df705-183">Другие задачи по реализации команд см. в разделе [Создание обработчиков контекстного меню](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="df705-183">For other verb implementation tasks, see [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

 

 
