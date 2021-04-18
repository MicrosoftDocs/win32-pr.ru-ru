---
title: Предоставление доступа к элементам управления на основе системных элементов управления
description: Предоставление доступа к элементам управления на основе системных элементов управления
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2fe31eae8c2283c020de93b0c1f3350bd0f417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413424"
---
# <a name="exposing-controls-based-on-system-controls"></a><span data-ttu-id="583ce-103">Предоставление доступа к элементам управления на основе системных элементов управления</span><span class="sxs-lookup"><span data-stu-id="583ce-103">Exposing Controls Based on System Controls</span></span>

<span data-ttu-id="583ce-104">Прежде чем приступать к приему, описанному в этом разделе, следует рассмотреть возможность использования динамической аннотации (прямой, картой значений или сервера).</span><span class="sxs-lookup"><span data-stu-id="583ce-104">You should consider using some form of Dynamic Annotation—Direct, Value Map, or Server—before attempting the technique described in this section.</span></span> <span data-ttu-id="583ce-105">Дополнительные сведения см. в разделе [Динамическая Аннотация API](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="583ce-105">For more information, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

<span data-ttu-id="583ce-106">В большинстве случаев Microsoft Active Accessibility предоставляет сведения об элементах управления класса или подклассов.</span><span class="sxs-lookup"><span data-stu-id="583ce-106">In most cases, Microsoft Active Accessibility exposes information about superclassed or subclassed controls.</span></span> <span data-ttu-id="583ce-107">Создание классов и подклассов позволяет разработчику приложения создавать пользовательские элементы управления с базовой функциональностью системного элемента управления и включать улучшения, предоставляемые приложением.</span><span class="sxs-lookup"><span data-stu-id="583ce-107">Superclassing and subclassing allow an application developer to create a custom control with the basic functionality of a system control and include enhancements provided by the application.</span></span> <span data-ttu-id="583ce-108">Элемент управления "веб-класс" имеет имя класса окна, отличное от имени системного элемента управления, на котором он основан.</span><span class="sxs-lookup"><span data-stu-id="583ce-108">A superclassed control has a different window class name than the system control on which it is based.</span></span> <span data-ttu-id="583ce-109">Элемент управления с подклассом имеет то же имя класса окна.</span><span class="sxs-lookup"><span data-stu-id="583ce-109">A subclassed control has the same window class name.</span></span> <span data-ttu-id="583ce-110">Дополнительные сведения о классах и подклассах см. в документации по пакету средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="583ce-110">For more information about superclassing and subclassing, see the Windows Software Development Kit (SDK) documentation.</span></span>

<span data-ttu-id="583ce-111">Поскольку Microsoft Active Accessibility предоставляет сведения о предоставляемых системой элементах управления, Microsoft Active Accessibility предоставляет измененный элемент управления, если только он не сильно отличается от базового элемента управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-111">Because Microsoft Active Accessibility exposes information about system-provided controls, Microsoft Active Accessibility exposes the modified control unless a superclassed or subclassed control is significantly different from the base control.</span></span> <span data-ttu-id="583ce-112">Чтобы определить, доступен ли измененный элемент управления, разработчики приложений должны использовать такие служебные программы, как [Проверка](inspect-objects.md) и [доступ к наблюдателю событий](accessible-event-watcher.md) , чтобы сравнить поведение измененного элемента управления с базовым элементом управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-112">To determine if the modified control is accessible, application developers should use utilities such as [Inspect](inspect-objects.md) and [Accessible Event Watcher](accessible-event-watcher.md) to compare the behavior of the modified control with the base control.</span></span>

<span data-ttu-id="583ce-113">Если после использования этих служебных программ вы определили, что измененный элемент управления недоступен, элемент управления необходимо рассматривать как любой другой пользовательский элемент управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-113">If after using these utilities you determine that the modified control is not accessible, you must treat the control as any other custom control.</span></span> <span data-ttu-id="583ce-114">Элемент управления должен активировать события, а процедура окна приложения должна реагировать на сообщение [**WM \_ GetObject**](wm-getobject.md), предоставив интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , используемый клиентскими приложениями для получения сведений об элементе управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-114">The control must trigger events, and the application's window procedure must respond to the [**WM\_GETOBJECT**](wm-getobject.md)message by supplying an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface that client applications use to obtain information about the control.</span></span>

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a><span data-ttu-id="583ce-115">Креатестдакцессиблепрокси и Креатестдакцессиблеобжект</span><span class="sxs-lookup"><span data-stu-id="583ce-115">CreateStdAccessibleProxy and CreateStdAccessibleObject</span></span>

<span data-ttu-id="583ce-116">Если все или большинство свойств [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для измененного элемента управления совпадают с базовым элементом управления, используйте [**креатестдакцессиблепрокси**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) или [**креатестдакцессиблеобжект**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) , чтобы упростить реализацию интерфейса **IAccessible** элемента управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-116">If all or most of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for the modified control are the same as the base control, use [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) or [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) to simplify the implementation of the control's **IAccessible** interface.</span></span>

> [!Note]  
> <span data-ttu-id="583ce-117">При использовании класса, реализующего класс, или подклассом, необходимо учитывать, что объект, полученный функцией [**креатестдакцессиблеобжект**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) , может реализовывать не только интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="583ce-117">When superclassing or subclassing an accessible control, be aware that the object retrieved by the [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) function may implement more than just the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="583ce-118">Он может включать другие интерфейсы, такие как [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span><span class="sxs-lookup"><span data-stu-id="583ce-118">It may include other interfaces such as [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span></span> <span data-ttu-id="583ce-119">Возможно, потребуется обернуть эти дополнительные интерфейсы, чтобы обеспечить поддержку специальных возможностей, предоставляемых исходным историей элемента управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-119">You might need to wrap these additional interfaces to retain the accessibility support provided by the original implemenation of the control.</span></span>

 

<span data-ttu-id="583ce-120">Функции [**креатестдакцессиблепрокси**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) и [**креатестдакцессиблеобжект**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) извлекают указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для указанного системного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-120">The [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) and [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) functions retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the specified system control.</span></span> <span data-ttu-id="583ce-121">Разница в этих функциях заключается в том, что **креатестдакцессиблеобжект** использует имя класса Window, полученное из параметра *HWND* , тогда как **креатестдакцессиблепрокси** использует имя класса Window, указанное в его параметре *сзкласснаме* .</span><span class="sxs-lookup"><span data-stu-id="583ce-121">The difference in these functions is that **CreateStdAccessibleObject** uses the window class name obtained from its *hwnd* parameter whereas **CreateStdAccessibleProxy** uses the window class name specified in its *szClassName* parameter.</span></span> <span data-ttu-id="583ce-122">Таким образом, если вы решили использовать эти функции, используйте **креатестдакцессиблепрокси** , чтобы предоставить сведения о элементах управления с помощью класса, и либо функцию с подклассом Controls.</span><span class="sxs-lookup"><span data-stu-id="583ce-122">Therefore, if you decide to use these functions, use **CreateStdAccessibleProxy** to expose information about superclassed controls, and either function with subclassed controls.</span></span>

<span data-ttu-id="583ce-123">После получения указателя интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) на системный элемент управления используйте указатель в реализации интерфейса **IAccessible** для измененного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-123">After obtaining an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to the system control, use the pointer in your implementation of the **IAccessible** interface for the modified control.</span></span> <span data-ttu-id="583ce-124">Если свойство или метод для измененного элемента управления совпадает с базовым элементом управления, используйте указатель **IAccessible** , чтобы получить сведения, предоставленные базовым элементом управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-124">If a property or method for the modified control is the same as the base control, use the **IAccessible** pointer to return the information provided by the base control.</span></span> <span data-ttu-id="583ce-125">Если свойство измененного элемента управления отличается от базового элемента управления, переопределите свойство базового элемента управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-125">If a property for the modified control is different from the base control, override the base control's property.</span></span>

<span data-ttu-id="583ce-126">В следующем примере **какккустомбуттон** — это определяемый приложением класс, производный от [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="583ce-126">In the following example, **CAccCustomButton** is the application-defined class derived from [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="583ce-127">Переменная-член **m \_ паккдефаултбуттон** является указателем на интерфейс **IAccessible** , который был получен из [**креатестдакцессиблеобжект**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) во время процедуры инициализации элемента управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-127">The member variable **m\_pAccDefaultButton** is a pointer to an **IAccessible** interface that was retrieved from [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) during the initialization procedure for the control.</span></span> <span data-ttu-id="583ce-128">В этом примере свойство **Role** для пользовательского элемента управления совпадает со свойством **Role** элемента управления System, поэтому возвращается свойство **Role** базового элемента управления.</span><span class="sxs-lookup"><span data-stu-id="583ce-128">In this example, the **Role** property for the custom control is the same as the **Role** property of the system control, so the **Role** property of the base control is returned.</span></span> <span data-ttu-id="583ce-129">Однако свойство **Description** отличается от базового элемента управления, поэтому это свойство переопределяется.</span><span class="sxs-lookup"><span data-stu-id="583ce-129">However, the **Description** property is different from that of the base control, so this property is overridden.</span></span>


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



<span data-ttu-id="583ce-130">Дополнительные сведения о свойствах и методах [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) системных элементов управления см. [в приложении A: Поддерживаемые ссылки на элементы пользовательского интерфейса](appendix-a--supported-user-interface-elements-reference.md).</span><span class="sxs-lookup"><span data-stu-id="583ce-130">For more information about the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of system controls, see [Appendix A: Supported User Interface Elements Reference](appendix-a--supported-user-interface-elements-reference.md).</span></span>

 

 