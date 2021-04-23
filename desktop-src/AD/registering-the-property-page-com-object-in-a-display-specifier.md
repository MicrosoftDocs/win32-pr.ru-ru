---
title: Регистрация COM-объекта страницы свойств в спецификаторе экрана
description: В этом разделе показано, как зарегистрировать библиотеку DLL расширения, содержащую страницу свойств Active Directory с реестром Windows и Active Directory.
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- Регистрация COM-объекта страницы свойств в спецификаторе экрана Active Directory
- Active Directory COM-объекта страницы свойств, регистрация в спецификаторе экрана
- Описатели экрана Active Directory, регистрация COM-объекта страницы свойств в
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5b08ac0ea6329026a6d367e71064bde917b1a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104133662"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a><span data-ttu-id="1abe8-106">Регистрация COM-объекта страницы свойств в спецификаторе экрана</span><span class="sxs-lookup"><span data-stu-id="1abe8-106">Registering the Property Page COM Object in a Display Specifier</span></span>

<span data-ttu-id="1abe8-107">При использовании COM для создания библиотеки DLL расширения для служб домен Active Directory Services необходимо также зарегистрировать расширение в реестре Windows и службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1abe8-107">When you use COM to create a property sheet extension DLL for Active Directory Domain Services, you must also register the extension with the Windows registry and Active Directory Domain Services.</span></span> <span data-ttu-id="1abe8-108">Регистрация расширения позволяет Active Directory административных оснасток MMC и оболочке Windows для распознавания расширения.</span><span class="sxs-lookup"><span data-stu-id="1abe8-108">Registering the extension enables the Active Directory administrative MMC snap-ins and the Windows shell to recognize the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="1abe8-109">Регистрация в реестре Windows</span><span class="sxs-lookup"><span data-stu-id="1abe8-109">Registering in the Windows Registry</span></span>

<span data-ttu-id="1abe8-110">Как и все серверы COM, расширение страницы свойств должно быть зарегистрировано в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="1abe8-110">Like all COM servers, a property sheet extension must be registered in the Windows registry.</span></span> <span data-ttu-id="1abe8-111">Расширение регистрируется в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="1abe8-111">The extension is registered under the following key.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

<span data-ttu-id="1abe8-112">*<clsid>* Строковое представление идентификатора CLSID, созданное функцией [**стрингфромклсид**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="1abe8-112">*<clsid>* is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="1abe8-113">В *<clsid>* ключе имеется ключ **InprocServer32** , который идентифицирует объект как 32-разрядный сервер in-proc.</span><span class="sxs-lookup"><span data-stu-id="1abe8-113">Under the *<clsid>* key, there is an **InProcServer32** key that identifies the object as a 32-bit in-proc server.</span></span> <span data-ttu-id="1abe8-114">В ключе **InprocServer32** расположение библиотеки DLL указывается в значении по умолчанию, а модель потоков указывается в значении **ThreadingModel** .</span><span class="sxs-lookup"><span data-stu-id="1abe8-114">Under the **InProcServer32** key, the location of the DLL is specified in the default value and the threading model is specified in the **ThreadingModel** value.</span></span> <span data-ttu-id="1abe8-115">Все расширения страниц свойств должны использовать модель потоков "апартамента".</span><span class="sxs-lookup"><span data-stu-id="1abe8-115">All property sheet extensions must use the "Apartment" threading model.</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="1abe8-116">Регистрация в домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="1abe8-116">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="1abe8-117">Регистрация расширения страницы свойств относится только к одному языку.</span><span class="sxs-lookup"><span data-stu-id="1abe8-117">Property sheet extension registration is specific to one locale.</span></span> <span data-ttu-id="1abe8-118">Если расширение страницы свойств применяется ко всем языкам, оно должно быть зарегистрировано в объекте [**дисплайспеЦифиер**](/windows/desktop/ADSchema/c-displayspecifier) класса объекта во всех вложенных компонентах языкового стандарта в контейнере описатели вывода.</span><span class="sxs-lookup"><span data-stu-id="1abe8-118">If the property sheet extension applies to all locales, it must be registered in the object class [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) object in all of the locale subcontainers in the Display Specifiers container.</span></span> <span data-ttu-id="1abe8-119">Если расширение страницы свойств локализовано для определенного языкового стандарта, зарегистрируйте его в объекте **дисплайспеЦифиер** в этом вложенном элементе locale.</span><span class="sxs-lookup"><span data-stu-id="1abe8-119">If the property sheet extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale subcontainer.</span></span> <span data-ttu-id="1abe8-120">Дополнительные сведения о контейнерах и языковых стандартах для описателей вывода см. в разделе [описатели](display-specifiers.md) и [контейнеры дисплайспеЦифиерс](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="1abe8-120">For more information about the Display Specifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="1abe8-121">Существует три атрибута спецификаторов вывода, которые может зарегистрировать расширение страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="1abe8-121">There are three display specifier attributes that a property sheet extension can be registered under.</span></span> <span data-ttu-id="1abe8-122">Это [**админпропертипажес**](/windows/desktop/ADSchema/a-adminpropertypages), [**шеллпропертипажес**](/windows/desktop/ADSchema/a-shellpropertypages)и [**админмултиселектпропертипажес**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).</span><span class="sxs-lookup"><span data-stu-id="1abe8-122">These are [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages), and [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).</span></span>

<span data-ttu-id="1abe8-123">Атрибут [**админпропертипажес**](/windows/desktop/ADSchema/a-adminpropertypages) определяет страницы административных свойств, отображаемые в Active Directory административных оснастках. Страница свойств отображается, когда пользователь просматривает свойства объектов соответствующего класса в одной из оснасток Active Directory администрирования MMC.</span><span class="sxs-lookup"><span data-stu-id="1abe8-123">The [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) attribute identifies administrative property pages to display in Active Directory administrative snap-ins. The property page appears when the user views properties for objects of the appropriate class in one of the Active Directory administrative MMC snap-ins.</span></span>

<span data-ttu-id="1abe8-124">Атрибут [**шеллпропертипажес**](/windows/desktop/ADSchema/a-shellpropertypages) определяет страницы свойств конечного пользователя, отображаемые в оболочке Windows.</span><span class="sxs-lookup"><span data-stu-id="1abe8-124">The [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) attribute identifies end-user property pages to display in the Windows shell.</span></span> <span data-ttu-id="1abe8-125">Страница свойств отображается, когда пользователь просматривает свойства объектов соответствующего класса в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="1abe8-125">The property page appears when the user views the properties for objects of the appropriate class in the Windows Explorer.</span></span> <span data-ttu-id="1abe8-126">Начиная с операционных систем Windows Server 2003, оболочка Windows больше не отображает объекты служб домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1abe8-126">Beginning with the Windows Server 2003 operating systems, the Windows shell no longer displays objects from Active Directory Domain Services.</span></span>

<span data-ttu-id="1abe8-127">[**Админмултиселектпропертипажес**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) доступен только в операционных системах Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1abe8-127">The [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) is only available on the Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1abe8-128">Страница свойств отображается, когда пользователь просматривает свойства более чем одного объекта соответствующего класса в одной из оснасток Active Directory администрирования MMC.</span><span class="sxs-lookup"><span data-stu-id="1abe8-128">The property page appears when the user views properties for more than one object of the appropriate class in one of the Active Directory administrative MMC snap-ins.</span></span>

<span data-ttu-id="1abe8-129">Все эти атрибуты являются многозначными.</span><span class="sxs-lookup"><span data-stu-id="1abe8-129">All of these attributes are multi-valued.</span></span>

<span data-ttu-id="1abe8-130">Значения для атрибутов [**админпропертипажес**](/windows/desktop/ADSchema/a-adminpropertypages) и [**шеллпропертипажес**](/windows/desktop/ADSchema/a-shellpropertypages) должны иметь следующий формат.</span><span class="sxs-lookup"><span data-stu-id="1abe8-130">The values for the [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) and [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) attributes require the following format.</span></span>


```C++
<order number>,<clsid>,<optional data>
```



<span data-ttu-id="1abe8-131">Значения для атрибута [**админмултиселектпропертипажес**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) должны иметь следующий формат.</span><span class="sxs-lookup"><span data-stu-id="1abe8-131">The values for the [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attribute require the following format.</span></span>


```C++
<order number>,<clsid>
```



<span data-ttu-id="1abe8-132">&lt;Порядковый номер &gt; — это число без знака, представляющее расположение страницы на листе.</span><span class="sxs-lookup"><span data-stu-id="1abe8-132">The "&lt;order number&gt;" is an unsigned number that represents the page position in the sheet.</span></span> <span data-ttu-id="1abe8-133">При отображении страницы свойств значения сортируются с помощью сравнения "номер заказа" каждого значения &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="1abe8-133">When a property sheet is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="1abe8-134">Если несколько значений имеют одинаковый &lt; порядковый номер, то &gt; эти COM-объекты страницы свойств загружаются в том порядке, в котором они считываются с Active Directory сервера.</span><span class="sxs-lookup"><span data-stu-id="1abe8-134">If more than one value has the same "&lt;order number&gt;", those property page COM objects are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="1abe8-135">По возможности следует использовать несуществующий " &lt; номер заказа &gt; ", то есть один, который не используется другими значениями в свойстве.</span><span class="sxs-lookup"><span data-stu-id="1abe8-135">If possible, you should use a non-existing "&lt;order number&gt;"; that is, one not used by other values in the property.</span></span> <span data-ttu-id="1abe8-136">Нет предписанной начальной должности, и в &lt; последовательности "номер заказа" могут пропуски &gt; .</span><span class="sxs-lookup"><span data-stu-id="1abe8-136">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="1abe8-137">" &lt; CLSID &gt; " — это строковое представление идентификатора CLSID, созданное функцией [**стрингфромклсид**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="1abe8-137">The "&lt;clsid&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="1abe8-138">" &lt; Необязательные данные &gt; " — это строковое значение, которое не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1abe8-138">The "&lt;optional data&gt;" is a string value that is not required.</span></span> <span data-ttu-id="1abe8-139">Это значение может быть извлечено COM-объектом страницы свойств с помощью указателя [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) , переданного в метод [**Ишеллекстинит:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) .</span><span class="sxs-lookup"><span data-stu-id="1abe8-139">This value can be retrieved by the property page COM object using the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to its [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method.</span></span> <span data-ttu-id="1abe8-140">COM-объект страницы свойств получает эти данные путем вызова интерфейса [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) с форматом буфера обмена [**кфстр \_ дспропертипажеинфо**](cfstr-dspropertypageinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="1abe8-140">The property page COM object obtains this data by calling [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) with the [**CFSTR\_DSPROPERTYPAGEINFO**](cfstr-dspropertypageinfo.md) clipboard format.</span></span> <span data-ttu-id="1abe8-141">Это обеспечивает **хглобал** , который содержит структуру [**Дспропертипажеинфо**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) , структура **дспропертипажеинфо** содержит строку в Юникоде, содержащую " &lt; необязательные данные &gt; ".</span><span class="sxs-lookup"><span data-stu-id="1abe8-141">This provides an **HGLOBAL** that contains a [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) structure The **DSPROPERTYPAGEINFO** structure contains a Unicode string that contains the "&lt;optional data&gt;".</span></span> <span data-ttu-id="1abe8-142">&lt;Использование необязательных данных &gt; с атрибутом [**админмултиселектпропертипажес**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) не допускается.</span><span class="sxs-lookup"><span data-stu-id="1abe8-142">The "&lt;optional data&gt;" is not allowed with the [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attribute.</span></span> <span data-ttu-id="1abe8-143">В следующем примере кода C/C++ показано, как получить " &lt; необязательные данные &gt; ".</span><span class="sxs-lookup"><span data-stu-id="1abe8-143">The following C/C++ code example shows how to retrieve the "&lt;optional data&gt;".</span></span>


```C++
fe.cfFormat = RegisterClipboardFormat(CFSTR_DSPROPERTYPAGEINFO);
fe.ptd = NULL;
fe.dwAspect = DVASPECT_CONTENT;
fe.lindex = -1;
fe.tymed = TYMED_HGLOBAL;
hr = pDataObj->GetData(&fe, &stm);
if(SUCCEEDED(hr))
{
    DSPROPERTYPAGEINFO *pPageInfo;
    
    pPageInfo = (DSPROPERTYPAGEINFO*)GlobalLock(stm.hGlobal);
    if(pPageInfo)
    {
        LPWSTR  pwszData;

        pwszData = (LPWSTR)((LPBYTE)pPageInfo + pPageInfo->offsetString);
        pwszData = NULL;
        
        GlobalUnlock(stm.hGlobal);
    }

    ReleaseStgMedium(&stm);
}
```



<span data-ttu-id="1abe8-144">Расширение страницы свойств может реализовывать несколько страниц свойств. одним из возможных способов использования " &lt; необязательных данных &gt; " является имя отображаемых страниц.</span><span class="sxs-lookup"><span data-stu-id="1abe8-144">A property sheet extension can implement more than one property page; one possible use of the "&lt;optional data&gt;" is to name the pages to display.</span></span> <span data-ttu-id="1abe8-145">Это обеспечивает гибкость при выборе реализации нескольких COM-объектов, по одному для каждой страницы или на один COM-объект для работы с несколькими страницами.</span><span class="sxs-lookup"><span data-stu-id="1abe8-145">This provides the flexibility of choosing to implement multiple COM objects, one for each page, or a single COM object to handle multiple pages.</span></span>

<span data-ttu-id="1abe8-146">В следующем примере кода приведен пример значения, которое можно использовать для атрибутов [**админпропертипажес**](/windows/desktop/ADSchema/a-adminpropertypages), [**шеллпропертипажес**](/windows/desktop/ADSchema/a-shellpropertypages)или [**админмултиселектпропертипажес**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .</span><span class="sxs-lookup"><span data-stu-id="1abe8-146">The following code example is an example value that can be used for the [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages), or [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attributes.</span></span>


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> <span data-ttu-id="1abe8-147">Для оболочки Windows данные описателя экрана извлекаются при входе пользователя в систему и кэшируются для сеанса пользователя.</span><span class="sxs-lookup"><span data-stu-id="1abe8-147">For the Windows shell, display specifier data is retrieved at user logon, and cached for the user session.</span></span> <span data-ttu-id="1abe8-148">Для административных оснасток данные описателя просмотра извлекаются при загрузке оснастки и кэшируются на время существования процесса.</span><span class="sxs-lookup"><span data-stu-id="1abe8-148">For administrative snap-ins, the display specifier data is retrieved when the snap-in is loaded, and is cached for the lifetime of the process.</span></span> <span data-ttu-id="1abe8-149">Для оболочки Windows это означает, что изменения описателей вывода вступают в силу после выхода пользователя из системы и последующего входа в систему.</span><span class="sxs-lookup"><span data-stu-id="1abe8-149">For the Windows shell, this indicates that changes to display specifiers take effect after a user logs off and then logs on again.</span></span> <span data-ttu-id="1abe8-150">Для административных оснасток изменения вступают в силу при загрузке оснастки или файла консоли.</span><span class="sxs-lookup"><span data-stu-id="1abe8-150">For the administrative snap-ins, changes take effect when the snap-in or console file is loaded.</span></span>

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a><span data-ttu-id="1abe8-151">Добавление значения в атрибуты расширения на странице свойств</span><span class="sxs-lookup"><span data-stu-id="1abe8-151">Adding a Value to the Property Sheet Extension Attributes</span></span>

<span data-ttu-id="1abe8-152">Следующая процедура описывает, как зарегистрировать расширение таблицы свойств в одном из атрибутов расширения на странице свойств.</span><span class="sxs-lookup"><span data-stu-id="1abe8-152">The following procedure describes how to register a property sheet extension under one of the property sheet extension attributes.</span></span>

<span data-ttu-id="1abe8-153">**Регистрация расширения таблицы свойств в одном из атрибутов расширения на странице свойств**</span><span class="sxs-lookup"><span data-stu-id="1abe8-153">**Registering a property sheet extension under one of the property sheet extension attributes**</span></span>

1.  <span data-ttu-id="1abe8-154">Убедитесь, что расширение еще не существует в значениях атрибута.</span><span class="sxs-lookup"><span data-stu-id="1abe8-154">Ensure that the extension does not already exist in the attribute values.</span></span>
2.  <span data-ttu-id="1abe8-155">Добавьте новое значение в конец списка упорядочения страниц свойств.</span><span class="sxs-lookup"><span data-stu-id="1abe8-155">Add the new value at the end of the property page ordering list.</span></span> <span data-ttu-id="1abe8-156">Задается часть " &lt; номер заказа &gt; " в значении атрибута для следующего значения после самого высокого номера заказа.</span><span class="sxs-lookup"><span data-stu-id="1abe8-156">That is set the "&lt;order number&gt;" portion of the attribute value to the next value after the highest existing order number.</span></span>
3.  <span data-ttu-id="1abe8-157">Метод [**iAds::P утекс**](/windows/desktop/api/iads/nf-iads-iads-putex) используется для добавления нового значения к атрибуту.</span><span class="sxs-lookup"><span data-stu-id="1abe8-157">The [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method is used to add the new value to the attribute.</span></span> <span data-ttu-id="1abe8-158">Параметр *лнконтролкоде* должен быть установлен в **объявление \_ Свойства ADS \_ ,** чтобы новое значение добавлялось к существующим значениям и не перезаписывать существующие значения.</span><span class="sxs-lookup"><span data-stu-id="1abe8-158">The *lnControlCode* parameter must be set to **ADS\_PROPERTY\_APPEND** so that the new value is appended to the existing values and does not, therefore, overwrite the existing values.</span></span> <span data-ttu-id="1abe8-159">Метод [**iAds:: сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) должен вызываться впоследствии для фиксации изменений в каталоге.</span><span class="sxs-lookup"><span data-stu-id="1abe8-159">The [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method must be called afterward to commit the change to the directory.</span></span>

<span data-ttu-id="1abe8-160">Имейте в виду, что одно и то же расширение вкладки свойств можно зарегистрировать для нескольких классов объектов.</span><span class="sxs-lookup"><span data-stu-id="1abe8-160">Be aware that the same property sheet extension can be registered for more than one object class.</span></span>

<span data-ttu-id="1abe8-161">Метод [**iAds::P утекс**](/windows/desktop/api/iads/nf-iads-iads-putex) используется для добавления нового значения к атрибуту.</span><span class="sxs-lookup"><span data-stu-id="1abe8-161">The [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method is used to add the new value to the attribute.</span></span> <span data-ttu-id="1abe8-162">Параметр *лнконтролкоде* должен быть установлен в значение **\_ \_ append свойства**, чтобы новое значение применялись к существующим значениям и не было, таким образом, перезаписать существующие значения.</span><span class="sxs-lookup"><span data-stu-id="1abe8-162">The *lnControlCode* parameter must be set to **ADS\_PROPERTY\_APPEND**, so that the new value is appended to the existing values and does not, therefore, overwrite the existing values.</span></span> <span data-ttu-id="1abe8-163">Метод [**iAds:: сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) должен быть вызван после фиксации изменения в каталоге.</span><span class="sxs-lookup"><span data-stu-id="1abe8-163">The [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method must be called after to commit the change to the directory.</span></span>

<span data-ttu-id="1abe8-164">В следующем примере кода расширение страницы свойств добавляется в класс Group в языковой стандарт компьютера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1abe8-164">The following code example adds a property sheet extension to the group class in the computer's default locale.</span></span> <span data-ttu-id="1abe8-165">Имейте в виду, что функция **аддпропертипажетодисплайспеЦифиер** проверяет CLSID расширения страницы свойств в существующих значениях, получает наибольший порядковый номер и добавляет значение для страницы свойств с помощью метода [**iAds::P утекс**](/windows/desktop/api/iads/nf-iads-iads-putex) с **\_ \_ добавлением в свойство ADS** кода элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1abe8-165">Be aware that the **AddPropertyPageToDisplaySpecifier** function verifies the property sheet extension CLSID in the existing values, gets the highest order number, and adds the value for the property page using [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) with the **ADS\_PROPERTY\_APPEND** control code.</span></span>


```C++
//  Add msvcrt.dll to the project.
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include "atlbase.h"

HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of the class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         );

HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                 );

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject);

//  Entry point for the application.
void wmain(int argc, wchar_t *argv[ ])
{

    wprintf(L"This program adds a sample property page to the display specifier for group class in the local computer's default locale.\n");

    // Initialize COM.
    CoInitialize(NULL);
    HRESULT hr = S_OK;

    //  Class ID for the sample property page.
    LPOLESTR szCLSID = L"{D9FCE809-8A10-11d2-A7E7-00C04F79DC0F}";
    LPOLESTR szClass = L"group";
    CLSID clsid;
    //  Convert to GUID.
    hr = CLSIDFromString(
        szCLSID,  //  Pointer to the string representation of the CLSID.
        &clsid    //  Pointer to the CLSID.
        );

    hr = AddPropertyPageToDisplaySpecifier(szClass, //  ldapDisplayName of the class.
                                           &clsid //  CLSID of property page COM object.
                                          );
    if (S_OK == hr)
        wprintf(L"Property page registered successfully\n");
    else if (S_FALSE == hr)
        wprintf(L"Property page was not added because it was already registered.\n");
    else
        wprintf(L"Property page was not added. HR: %x.\n");

    //  Uninitialize COM.
    CoUninitialize();
    return;
}

//  Adds a property page to Active Directory admin snap-ins.
HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         )
{
    HRESULT hr = E_FAIL;
    IADsContainer *pContainer = NULL;
    LPOLESTR szDispSpec = new OLECHAR[MAX_PATH];
    IADs *pObject = NULL;
    VARIANT var;
    CComBSTR sbstrProperty = L"adminPropertyPages";
    LCID locale = NULL;
    //  Get the display specifier container using default system locale.
    //  When adding a property page COM object, specify the locale
    //  because the registration is locale-specific.
    //  This means if you created a property page
    //  for German, explicitly add it to the 407 container,
    //  so that it will be used when a computer is running with locale
    //  set to German and not the locale set on the
    //  computer where this application is running.
    hr = BindToDisplaySpecifiersContainerByLocale(&locale,
                                                  &pContainer
                                                 );
    //  Handle fail case where dispspec object
    //  is not found and give option to create one.

    if (SUCCEEDED(hr))
    {
        //  Bind to display specifier object for the specified class.
        //  Build the display specifier name.
#ifdef _MBCS
        wcscpy_s(szDispSpec, szClassName);
        wcscat_s(szDispSpec, L"-Display");
        hr = GetDisplaySpecifier(pContainer, szDispSpec, &pObject);
#endif _MBCS#endif _MBCS
        if (SUCCEEDED(hr))
        {
            //  Convert GUID to string.
            LPOLESTR szDSGUID = new WCHAR [39];
            ::StringFromGUID2(*pPropPageCLSID, szDSGUID, 39); 

            //  Get the adminPropertyPages property.
            hr = pObject->GetEx(sbstrProperty, &var);
            if (SUCCEEDED(hr))
            {
                LONG lstart, lend;
                SAFEARRAY *sa = V_ARRAY(&var);
                VARIANT varItem;
                //  Get the lower and upper bound.
                hr = SafeArrayGetLBound(sa, 1, &lstart);
                if (SUCCEEDED(hr))
                {
                    hr = SafeArrayGetUBound(sa, 1, &lend);
                }
                if (SUCCEEDED(hr))
                {
                    //  Iterate the values to verify if the prop page CLSID
                    //  is already registered.
                    VariantInit(&varItem);
                    BOOL bExists = FALSE;
                    UINT uiLastItem = 0;
                    UINT uiTemp = 0;
                    INT iOffset = 0;
                    LPOLESTR szMainStr = new OLECHAR[MAX_PATH];
                    LPOLESTR szItem = new OLECHAR[MAX_PATH];
                    LPOLESTR szStr = NULL;
                    for (long idx=lstart; idx <= lend; idx++)
                    {
                        hr = SafeArrayGetElement(sa, &idx, &varItem);
                        if (SUCCEEDED(hr))
                        {
#ifdef _MBCS
                            //  Verify that the specified CLSID is already registered.
                            wcscpy_s(szMainStr,varItem.bstrVal);
                            if (wcsstr(szMainStr,szDSGUID))
                                bExists = TRUE;
                            //  Get the index which is the number before the first comma.
                            szStr = wcschr(szMainStr, ',');
                            iOffset = (int)(szStr - szMainStr);
                            wcsncpy_s(szItem, szMainStr, iOffset);
                            szItem[iOffset]=0L;
                            uiTemp = _wtoi(szItem);
                            if (uiTemp > uiLastItem)
                                uiLastItem = uiTemp;
                            VariantClear(&varItem);
#endif _MBCS
                        }
                    }
                    //  If the CLSID is not registered, add it.
                    if (!bExists)
                    {
                        //  Build the value to add.
                        LPOLESTR szValue = new OLECHAR[MAX_PATH];
                        //  Next index to add at end of list.
#ifdef _MBCS
                        uiLastItem++;
                        _itow_s(uiLastItem, szValue, 10);   
                        wcscat_s(szValue,L",");
                        //  Add the class ID for the property page.
                        wcscat_s(szValue,szDSGUID);
                        wprintf(L"Value to add: %s\n", szValue);
#endif _MBCS

                        VARIANT varAdd;
                        //  Only one value to add
                        LPOLESTR pszAddStr[1];
                        pszAddStr[0]=szValue;
                        ADsBuildVarArrayStr(pszAddStr, 1, &varAdd);

                        hr = pObject->PutEx(ADS_PROPERTY_APPEND, sbstrProperty, varAdd);
                        if (SUCCEEDED(hr))
                        {
                            //  Commit the change.
                            hr = pObject->SetInfo();
                        }
                    }
                    else
                        hr = S_FALSE;
                }
            }
            VariantClear(&var);
        }
        if (pObject)
            pObject->Release();
    }

    return hr;
}

//  This function returns a pointer to the display specifier container 
//  for the specified locale.
//  If locale is NULL, use the default system locale and then return the locale in the locale param.
HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                )
{
    HRESULT hr = E_FAIL;

    if ((!ppDispSpecCont)||(!locale))
        return E_POINTER;

    //  If no locale is specified, use the default system locale.
    if (!(*locale))
    {
        *locale = GetSystemDefaultLCID();
        if (!(*locale))
            return E_FAIL;
    }

    //  Verify that it is a valid locale.
    if (!IsValidLocale(*locale, LCID_SUPPORTED))
        return E_INVALIDARG;

    LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
    IADs *pObj = NULL;
    VARIANT var;

    hr = ADsOpenObject(L"LDAP://rootDSE",
                       NULL,
                       NULL,
                       ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                       IID_IADs,
                       (void**)&pObj);

    if (SUCCEEDED(hr))
    {
        //  Get the DN to the config container.
        hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
        if (SUCCEEDED(hr))
        {
#ifdef _MBCS
            //  Build the string to bind to the DisplaySpecifiers container.
            swprintf_s(szPath,L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", *locale, var.bstrVal);
            //  Bind to the DisplaySpecifiers container.
            *ppDispSpecCont = NULL;
            hr = ADsOpenObject(szPath,
                               NULL,
                               NULL,
                               ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                               IID_IADsContainer,
                               (void**)ppDispSpecCont);
#endif _MBCS

            if(FAILED(hr))
            {
                if (*ppDispSpecCont)
                {
                    (*ppDispSpecCont)->Release();
                    (*ppDispSpecCont) = NULL;
                }
            }
        }
    }
    //   Cleanup.
    VariantClear(&var);
    if (pObj)
        pObj->Release();

    return hr;
}

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject)
{
    HRESULT hr = E_FAIL;
    CComBSTR sbstrDSPath;
    IDispatch *pDisp = NULL;

    if (!pContainer)
    {
        hr = E_POINTER;
        return hr;
    }

    //  Verify other pointers.
    //  Initialize the output pointer.
    (*ppObject) = NULL;

    //  Build relative path to the display specifier object.
    sbstrDSPath = "CN=";
    sbstrDSPath += szDispSpec;

    //  Use child object binding with IADsContainer::GetObject.
    hr = pContainer->GetObject(CComBSTR("displaySpecifier"),
        sbstrDSPath,
        &pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(IID_IADs, (void**)ppObject);
        if (FAILED(hr))
        {
            //  Clean up.
            if (*ppObject)
                (*ppObject)->Release();
        }
    }

    if (pDisp)
        pDisp->Release();

    return hr;

}
```



 

 