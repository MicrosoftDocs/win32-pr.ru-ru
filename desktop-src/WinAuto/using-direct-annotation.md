---
title: Использование прямой аннотации
description: Использование прямой аннотации
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f0bdea5af896329b6836d21ca1dcee25bc2739
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338177"
---
# <a name="using-direct-annotation"></a><span data-ttu-id="02e02-103">Использование прямой аннотации</span><span class="sxs-lookup"><span data-stu-id="02e02-103">Using Direct Annotation</span></span>

<span data-ttu-id="02e02-104">**Использование прямой заметки для переопределения значения свойства**</span><span class="sxs-lookup"><span data-stu-id="02e02-104">**To use direct annotation to override the value of a property**</span></span>

1.  <span data-ttu-id="02e02-105">Используйте функцию [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) или [кокреатеинстанцеекс](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) для создания объекта [**иаккпропсервицес**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="02e02-105">Use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) function to create the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) object.</span></span>
2.  <span data-ttu-id="02e02-106">Вызовите [**иаккпропсервицес:: сесвндпроп**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), передав **HWND**, идентификатор объекта, дочерний идентификатор, переопределяемое свойство и [вариант](/windows/win32/api/oaidl/ns-oaidl-variant) , содержащий новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="02e02-106">Call [**IAccPropServices::SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passing the **HWND**, object ID, child ID, the property to be overridden, and a [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) containing the new value of the property.</span></span> <span data-ttu-id="02e02-107">Этот шаг заобъявляет значение.</span><span class="sxs-lookup"><span data-stu-id="02e02-107">This step annotates the value.</span></span>
3.  <span data-ttu-id="02e02-108">Освободите указатели интерфейса и свободную память.</span><span class="sxs-lookup"><span data-stu-id="02e02-108">Release the interface pointers and free memory.</span></span>

<span data-ttu-id="02e02-109">В следующем примере показано, как закомментировать свойство [**Role**](role-property.md) элемента управления "статический текст".</span><span class="sxs-lookup"><span data-stu-id="02e02-109">The following example shows how to annotate the [**Role**](role-property.md) property of a static text control.</span></span>


```C++
HRESULT CMyTextControl::SetAccessibleProperties()
{
  // COM is assumed to be initialized...
  IAccPropServices* pAccPropServices = NULL;

  HRESULT hr = CoCreateInstance(CLSID_AccPropServices,
    NULL, CLSCTX_SERVER, IID_IAccPropServices, 
    (void**)&pAccPropServices);

  if (SUCCEEDED(hr))
  {
    // Annotating the Role of this object to be STATICTEXT
    VARIANT var;
    var.vt = VT_I4;
    var.lVal = ROLE_SYSTEM_STATICTEXT;

    hr = pAccPropServices->SetHwndProp(_hwnd,
      OBJID_CLIENT,
      CHILDID_SELF,
      PROPID_ACC_ROLE,
      var);

    pAccPropServices->Release();
  }
  return hr;
}
```



## <a name="properties-supported-when-specifying-a-value"></a><span data-ttu-id="02e02-110">Свойства, поддерживаемые при указании значения</span><span class="sxs-lookup"><span data-stu-id="02e02-110">Properties Supported When Specifying a Value</span></span>

<span data-ttu-id="02e02-111">Следующие свойства Active Accessibility Microsoft можно закомментировать при указании значения (где значение должно иметь указанный тип) для прямой аннотации.</span><span class="sxs-lookup"><span data-stu-id="02e02-111">The following Microsoft Active Accessibility properties can be annotated when specifying a value (where the value must be of the noted type) for direct annotation.</span></span> <span data-ttu-id="02e02-112">Чтобы переопределить или добавить свойство Microsoft UI Automation в элемент управления, можно указать идентификатор свойства модели автоматизации пользовательского интерфейса вместо идентификатора свойства Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="02e02-112">To override or add a Microsoft UI Automation property to a control, you can specify the UI Automation property ID instead of the Microsoft Active Accessibility property ID.</span></span> <span data-ttu-id="02e02-113">Список идентификаторов автоматизации пользовательского интерфейса см. в разделе [идентификаторы свойств](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="02e02-113">For a list of UI Automation IDs, see [Property Identifiers](uiauto-entry-propids.md).</span></span>



| <span data-ttu-id="02e02-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="02e02-114">Property</span></span>                      | <span data-ttu-id="02e02-115">Тип</span><span class="sxs-lookup"><span data-stu-id="02e02-115">Type</span></span>     |
|-------------------------------|----------|
| <span data-ttu-id="02e02-116">\_имя счетов \_ PropID</span><span class="sxs-lookup"><span data-stu-id="02e02-116">PROPID\_ACC\_NAME</span></span>             | <span data-ttu-id="02e02-117">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="02e02-117">VT\_BSTR</span></span> |
| <span data-ttu-id="02e02-118">\_Описание счетов \_ PropID</span><span class="sxs-lookup"><span data-stu-id="02e02-118">PROPID\_ACC\_DESCRIPTION</span></span>      | <span data-ttu-id="02e02-119">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="02e02-119">VT\_BSTR</span></span> |
| <span data-ttu-id="02e02-120">\_роль PropID ACC \_</span><span class="sxs-lookup"><span data-stu-id="02e02-120">PROPID\_ACC\_ROLE</span></span>             | <span data-ttu-id="02e02-121">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="02e02-121">VT\_I4</span></span>   |
| <span data-ttu-id="02e02-122">\_состояние счетов \_ PropID</span><span class="sxs-lookup"><span data-stu-id="02e02-122">PROPID\_ACC\_STATE</span></span>            | <span data-ttu-id="02e02-123">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="02e02-123">VT\_I4</span></span>   |
| <span data-ttu-id="02e02-124">\_ \_ Справка по PropID</span><span class="sxs-lookup"><span data-stu-id="02e02-124">PROPID\_ACC\_HELP</span></span>             | <span data-ttu-id="02e02-125">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="02e02-125">VT\_BSTR</span></span> |
| <span data-ttu-id="02e02-126">PROPID \_ ACC \_ кэйбоардшорткут</span><span class="sxs-lookup"><span data-stu-id="02e02-126">PROPID\_ACC\_KEYBOARDSHORTCUT</span></span> | <span data-ttu-id="02e02-127">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="02e02-127">VT\_BSTR</span></span> |
| <span data-ttu-id="02e02-128">PROPID \_ ACC \_ DEFAULTACTION</span><span class="sxs-lookup"><span data-stu-id="02e02-128">PROPID\_ACC\_DEFAULTACTION</span></span>    | <span data-ttu-id="02e02-129">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="02e02-129">VT\_BSTR</span></span> |
| <span data-ttu-id="02e02-130">PROPID \_ ACC — \_ VALUEMAP</span><span class="sxs-lookup"><span data-stu-id="02e02-130">PROPID\_ACC\_VALUEMAP</span></span>         | <span data-ttu-id="02e02-131">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="02e02-131">VT\_BSTR</span></span> |
| <span data-ttu-id="02e02-132">PROPID \_ ACC \_ ролемап</span><span class="sxs-lookup"><span data-stu-id="02e02-132">PROPID\_ACC\_ROLEMAP</span></span>          | <span data-ttu-id="02e02-133">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="02e02-133">VT\_BSTR</span></span> |
| <span data-ttu-id="02e02-134">PROPID \_ ACC \_ статемап</span><span class="sxs-lookup"><span data-stu-id="02e02-134">PROPID\_ACC\_STATEMAP</span></span>         | <span data-ttu-id="02e02-135">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="02e02-135">VT\_BSTR</span></span> |



 

 

 