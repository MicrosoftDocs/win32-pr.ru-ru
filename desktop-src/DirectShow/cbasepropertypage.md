---
description: Класс Кбасепропертипаже является абстрактным классом для реализации страницы свойств. Этот класс используется при написании фильтра (или другого объекта), поддерживающего страницы свойств.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: Класс Кбасепропертипаже (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168b2d450ec8efc30851286120d47ba6247fe6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668926"
---
# <a name="cbasepropertypage-class"></a><span data-ttu-id="5984c-104">Класс Кбасепропертипаже</span><span class="sxs-lookup"><span data-stu-id="5984c-104">CBasePropertyPage class</span></span>

![Иерархия классов кбасепропертипаже](images/cprop01.png)

<span data-ttu-id="5984c-106">`CBasePropertyPage`Класс является абстрактным классом для реализации страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-106">The `CBasePropertyPage` class is an abstract class for implementing a property page.</span></span> <span data-ttu-id="5984c-107">Этот класс используется при написании фильтра (или другого объекта), поддерживающего страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-107">Use this class if you are writing a filter (or other object) that supports property pages.</span></span>



| <span data-ttu-id="5984c-108">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="5984c-108">Protected Member Variables</span></span>                                             | <span data-ttu-id="5984c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5984c-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5984c-110">**m \_ бдирти**</span><span class="sxs-lookup"><span data-stu-id="5984c-110">**m\_bDirty**</span></span>](cbasepropertypage-m-bdirty.md)                        | <span data-ttu-id="5984c-111">Указывает, изменились ли какие бы то ни было свойства.</span><span class="sxs-lookup"><span data-stu-id="5984c-111">Indicates whether any of the properties have changed.</span></span>                                                                             |
| [<span data-ttu-id="5984c-112">**m \_ диалогид**</span><span class="sxs-lookup"><span data-stu-id="5984c-112">**m\_DialogId**</span></span>](cbasepropertypage-m-dialogid.md)                    | <span data-ttu-id="5984c-113">Идентификатор ресурса для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5984c-113">Resource identifier for the dialog.</span></span>                                                                                               |
| [<span data-ttu-id="5984c-114">**m \_ DLG**</span><span class="sxs-lookup"><span data-stu-id="5984c-114">**m\_Dlg**</span></span>](cbasepropertypage-m-dlg.md)                              | <span data-ttu-id="5984c-115">Обработчик для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5984c-115">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="5984c-116">**m \_ HWND**</span><span class="sxs-lookup"><span data-stu-id="5984c-116">**m\_hwnd**</span></span>](cbasepropertypage-m-hwnd.md)                            | <span data-ttu-id="5984c-117">Обработчик для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5984c-117">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="5984c-118">**m \_ ппажесите**</span><span class="sxs-lookup"><span data-stu-id="5984c-118">**m\_pPageSite**</span></span>](cbasepropertypage-m-ppagesite.md)                  | <span data-ttu-id="5984c-119">Указатель на интерфейс **ипропертипажесите** сайта страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-119">Pointer to the **IPropertyPageSite** interface of the property page site.</span></span>                                                         |
| [<span data-ttu-id="5984c-120">**m \_ титлеид**</span><span class="sxs-lookup"><span data-stu-id="5984c-120">**m\_TitleId**</span></span>](cbasepropertypage-m-titleid.md)                      | <span data-ttu-id="5984c-121">Идентификатор ресурса для строки, содержащей заголовок диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5984c-121">Resource identifier for a string that contains the dialog title.</span></span>                                                                  |
| <span data-ttu-id="5984c-122">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="5984c-122">Public Methods</span></span>                                                         | <span data-ttu-id="5984c-123">Описание</span><span class="sxs-lookup"><span data-stu-id="5984c-123">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="5984c-124">**кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="5984c-124">**CBasePropertyPage**</span></span>](cbasepropertypage-cbasepropertypage.md)       | <span data-ttu-id="5984c-125">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="5984c-125">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="5984c-126">**~ Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="5984c-126">**~CBasePropertyPage**</span></span>](cbasepropertypage--cbasepropertypage.md)     | <span data-ttu-id="5984c-127">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="5984c-127">Destructor method.</span></span> <span data-ttu-id="5984c-128">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="5984c-128">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="5984c-129">**Активировать**</span><span class="sxs-lookup"><span data-stu-id="5984c-129">**OnActivate**</span></span>](cbasepropertypage-onactivate.md)                     | <span data-ttu-id="5984c-130">Вызывается при активации страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-130">Called when the property page is activated.</span></span> <span data-ttu-id="5984c-131">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="5984c-131">Virtual.</span></span>                                                                              |
| [<span data-ttu-id="5984c-132">**онаппличанжес**</span><span class="sxs-lookup"><span data-stu-id="5984c-132">**OnApplyChanges**</span></span>](cbasepropertypage-onapplychanges.md)             | <span data-ttu-id="5984c-133">Вызывается, когда пользователь применяет изменения к странице свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-133">Called when the user applies changes to the property page.</span></span> <span data-ttu-id="5984c-134">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="5984c-134">Virtual.</span></span>                                                               |
| [<span data-ttu-id="5984c-135">**Подключение OnConnect**</span><span class="sxs-lookup"><span data-stu-id="5984c-135">**OnConnect**</span></span>](cbasepropertypage-onconnect.md)                       | <span data-ttu-id="5984c-136">Предоставляет указатель **IUnknown** на объект, связанный со страницей свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-136">Provides an **IUnknown** pointer to the object associated with the property page.</span></span> <span data-ttu-id="5984c-137">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="5984c-137">Virtual.</span></span>                                        |
| [<span data-ttu-id="5984c-138">**OnDeactivate**</span><span class="sxs-lookup"><span data-stu-id="5984c-138">**OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)                 | <span data-ttu-id="5984c-139">Вызывается при уничтожении окна диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5984c-139">Called when the dialog box window is destroyed.</span></span> <span data-ttu-id="5984c-140">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="5984c-140">Virtual.</span></span>                                                                          |
| [<span data-ttu-id="5984c-141">**Ondisconnectие**</span><span class="sxs-lookup"><span data-stu-id="5984c-141">**OnDisconnect**</span></span>](cbasepropertypage-ondisconnect.md)                 | <span data-ttu-id="5984c-142">Вызывается, когда страница свойств должна освободить связанный объект.</span><span class="sxs-lookup"><span data-stu-id="5984c-142">Called when the property page should release the associated object.</span></span> <span data-ttu-id="5984c-143">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="5984c-143">Virtual.</span></span>                                                      |
| [<span data-ttu-id="5984c-144">**онрецеивемессаже**</span><span class="sxs-lookup"><span data-stu-id="5984c-144">**OnReceiveMessage**</span></span>](cbasepropertypage-onreceivemessage.md)         | <span data-ttu-id="5984c-145">Вызывается, когда диалоговое окно получает сообщение.</span><span class="sxs-lookup"><span data-stu-id="5984c-145">Called when the dialog box receives a message.</span></span> <span data-ttu-id="5984c-146">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="5984c-146">Virtual.</span></span>                                                                           |
| <span data-ttu-id="5984c-147">Методы Ипропертипаже</span><span class="sxs-lookup"><span data-stu-id="5984c-147">IPropertyPage Methods</span></span>                                                  | <span data-ttu-id="5984c-148">Описание</span><span class="sxs-lookup"><span data-stu-id="5984c-148">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="5984c-149">**Вызова**</span><span class="sxs-lookup"><span data-stu-id="5984c-149">**Activate**</span></span>](cbasepropertypage-activate.md)                         | <span data-ttu-id="5984c-150">Создает окно диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5984c-150">Creates the dialog box window.</span></span>                                                                                                    |
| [<span data-ttu-id="5984c-151">**Применить**</span><span class="sxs-lookup"><span data-stu-id="5984c-151">**Apply**</span></span>](cbasepropertypage-apply.md)                               | <span data-ttu-id="5984c-152">Применяет текущие значения страницы свойств к объекту, связанному со страницей свойств</span><span class="sxs-lookup"><span data-stu-id="5984c-152">Applies the current property page values to the object associated with the property page</span></span>                                          |
| [<span data-ttu-id="5984c-153">**Отключение**</span><span class="sxs-lookup"><span data-stu-id="5984c-153">**Deactivate**</span></span>](cbasepropertypage-deactivate.md)                     | <span data-ttu-id="5984c-154">Уничтожает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5984c-154">Destroys the dialog window.</span></span>                                                                                                       |
| [<span data-ttu-id="5984c-155">**жетпажеинфо**</span><span class="sxs-lookup"><span data-stu-id="5984c-155">**GetPageInfo**</span></span>](cbasepropertypage-getpageinfo.md)                   | <span data-ttu-id="5984c-156">Извлекает сведения о странице свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-156">Retrieves information about the property page.</span></span>                                                                                    |
| [<span data-ttu-id="5984c-157">**Справка**</span><span class="sxs-lookup"><span data-stu-id="5984c-157">**Help**</span></span>](cbasepropertypage-help.md)                                 | <span data-ttu-id="5984c-158">Вызывает справку страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-158">Invokes the property page help.</span></span>                                                                                                   |
| [<span data-ttu-id="5984c-159">**испажедирти**</span><span class="sxs-lookup"><span data-stu-id="5984c-159">**IsPageDirty**</span></span>](cbasepropertypage-ispagedirty.md)                   | <span data-ttu-id="5984c-160">Указывает, изменилась ли страница свойств с момента ее активации или последнего вызова метода **ипропертипаже:: Apply**.</span><span class="sxs-lookup"><span data-stu-id="5984c-160">Indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> |
| [<span data-ttu-id="5984c-161">**Переместить**</span><span class="sxs-lookup"><span data-stu-id="5984c-161">**Move**</span></span>](cbasepropertypage-move.md)                                 | <span data-ttu-id="5984c-162">Определяет положение и изменяет размер диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5984c-162">Positions and resizes the dialog box.</span></span>                                                                                             |
| [<span data-ttu-id="5984c-163">**сетобжектс**</span><span class="sxs-lookup"><span data-stu-id="5984c-163">**SetObjects**</span></span>](cbasepropertypage-setobjects.md)                     | <span data-ttu-id="5984c-164">Предоставляет указатели **IUnknown** для объектов, связанных со страницей свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-164">Provides **IUnknown** pointers for the objects associated with the property page.</span></span>                                                 |
| [<span data-ttu-id="5984c-165">**сетпажесите**</span><span class="sxs-lookup"><span data-stu-id="5984c-165">**SetPageSite**</span></span>](cbasepropertypage-setpagesite.md)                   | <span data-ttu-id="5984c-166">Инициализирует страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-166">Initializes the property page.</span></span>                                                                                                    |
| [<span data-ttu-id="5984c-167">**Казывающи**</span><span class="sxs-lookup"><span data-stu-id="5984c-167">**Show**</span></span>](cbasepropertypage-show.md)                                 | <span data-ttu-id="5984c-168">Показывает или скрывает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5984c-168">Shows or hides the dialog box.</span></span>                                                                                                    |
| [<span data-ttu-id="5984c-169">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="5984c-169">**TranslateAccelerator**</span></span>](cbasepropertypage-translateaccelerator.md) | <span data-ttu-id="5984c-170">Указывает странице свойств обработать нажатие клавиши.</span><span class="sxs-lookup"><span data-stu-id="5984c-170">Instructs the property page to process a keystroke.</span></span>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="5984c-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5984c-171">Remarks</span></span>

<span data-ttu-id="5984c-172">Страница свойств является COM-объектом, поэтому необходимо создать идентификатор GUID для идентификатора класса (CLSID) и предоставить запись в массиве [**кфакторитемплате**](cfactorytemplate.md) .</span><span class="sxs-lookup"><span data-stu-id="5984c-172">A property page is a COM object, so you must generate a GUID for the class identifier (CLSID) and provide an entry in the [**CFactoryTemplate**](cfactorytemplate.md) array.</span></span> <span data-ttu-id="5984c-173">Дополнительные сведения см. в разделе [DirectShow и com](directshow-and-com.md).</span><span class="sxs-lookup"><span data-stu-id="5984c-173">For more information, see [DirectShow and COM](directshow-and-com.md).</span></span> <span data-ttu-id="5984c-174">В следующем примере показана типичная запись фабрики класса:</span><span class="sxs-lookup"><span data-stu-id="5984c-174">The following example shows a typical class factory entry:</span></span>


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



<span data-ttu-id="5984c-175">Фильтр должен предоставлять интерфейс **испеЦифипропертипажес** .</span><span class="sxs-lookup"><span data-stu-id="5984c-175">Your filter must expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="5984c-176">Этот интерфейс содержит один метод, а **-страницы**, который возвращает идентификатор CLSID страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-176">This interface contains a single method, **GetPages**, which returns the CLSID of the property page.</span></span> <span data-ttu-id="5984c-177">В следующем примере показано, как реализовать этот метод:</span><span class="sxs-lookup"><span data-stu-id="5984c-177">The following example shows how to implement this method:</span></span>


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



<span data-ttu-id="5984c-178">Не забывайте также переопределять метод **нонделегатингкуеринтерфаце** для фильтра.</span><span class="sxs-lookup"><span data-stu-id="5984c-178">Remember to override the filter's **NonDelegatingQueryInterface** method as well.</span></span> <span data-ttu-id="5984c-179">Дополнительные сведения см. в статье [DirectShow и com](directshow-and-com.md) и [**инонделегатингункновн**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="5984c-179">For more information, see [DirectShow and COM](directshow-and-com.md) and [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>

<span data-ttu-id="5984c-180">Затем создайте диалоговое окно в качестве ресурса в проекте и создайте строковый ресурс, содержащий название диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5984c-180">Next, create the dialog as a resource in your project, and create a string resource that holds the dialog title.</span></span> <span data-ttu-id="5984c-181">Оба этих идентификатора ресурсов являются параметрами конструктора **кбасепропертипаже** .</span><span class="sxs-lookup"><span data-stu-id="5984c-181">Both of these resource IDs are parameters to the **CBasePropertyPage** constructor.</span></span> <span data-ttu-id="5984c-182">Хранение строки заголовка в ресурсе упрощает локализацию страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5984c-182">Keeping the title string in a resource makes it easier to localize your property page.</span></span>

<span data-ttu-id="5984c-183">Класс **кбасепропертипаже** предоставляет платформу для интерфейса **ипропертипаже** .</span><span class="sxs-lookup"><span data-stu-id="5984c-183">The **CBasePropertyPage** class provides a framework for the **IPropertyPage** interface.</span></span> <span data-ttu-id="5984c-184">Эта платформа вызывает ряд виртуальных методов, включая [**кбасепропертипаже:: OnActivate**](cbasepropertypage-onactivate.md), [**Кбасепропертипаже:: онаппличанжес**](cbasepropertypage-onapplychanges.md)и т. д.</span><span class="sxs-lookup"><span data-stu-id="5984c-184">This framework calls a number of virtual methods, including [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md), and so on.</span></span> <span data-ttu-id="5984c-185">В базовом классе эти методы просто возвращают S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5984c-185">In the base class, these methods simply return S\_OK.</span></span> <span data-ttu-id="5984c-186">Производный класс должен переопределять некоторые или все эти виртуальные методы.</span><span class="sxs-lookup"><span data-stu-id="5984c-186">Your derived class will need to override some or all of these virtual methods.</span></span> <span data-ttu-id="5984c-187">Дополнительные сведения см. в разделе Примечания для отдельных методов.</span><span class="sxs-lookup"><span data-stu-id="5984c-187">For details, see the remarks for the individual methods.</span></span>

<span data-ttu-id="5984c-188">Расширенный пример использования этого класса для создания страницы свойств см. в разделе [Создание страницы свойств фильтра](creating-a-filter-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="5984c-188">For an extended example of how to use this class to create a property page, see [Creating a Filter Property Page](creating-a-filter-property-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5984c-189">Требования</span><span class="sxs-lookup"><span data-stu-id="5984c-189">Requirements</span></span>



| <span data-ttu-id="5984c-190">Требование</span><span class="sxs-lookup"><span data-stu-id="5984c-190">Requirement</span></span> | <span data-ttu-id="5984c-191">Значение</span><span class="sxs-lookup"><span data-stu-id="5984c-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5984c-192">Header</span><span class="sxs-lookup"><span data-stu-id="5984c-192">Header</span></span><br/>  | <dl> <span data-ttu-id="5984c-193"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5984c-193"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5984c-194">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5984c-194">Library</span></span><br/> | <dl> <span data-ttu-id="5984c-195"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5984c-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




