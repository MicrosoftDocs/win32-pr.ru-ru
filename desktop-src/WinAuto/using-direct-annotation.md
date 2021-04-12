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
# <a name="using-direct-annotation"></a>Использование прямой аннотации

**Использование прямой заметки для переопределения значения свойства**

1.  Используйте функцию [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) или [кокреатеинстанцеекс](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) для создания объекта [**иаккпропсервицес**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
2.  Вызовите [**иаккпропсервицес:: сесвндпроп**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), передав **HWND**, идентификатор объекта, дочерний идентификатор, переопределяемое свойство и [вариант](/windows/win32/api/oaidl/ns-oaidl-variant) , содержащий новое значение свойства. Этот шаг заобъявляет значение.
3.  Освободите указатели интерфейса и свободную память.

В следующем примере показано, как закомментировать свойство [**Role**](role-property.md) элемента управления "статический текст".


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



## <a name="properties-supported-when-specifying-a-value"></a>Свойства, поддерживаемые при указании значения

Следующие свойства Active Accessibility Microsoft можно закомментировать при указании значения (где значение должно иметь указанный тип) для прямой аннотации. Чтобы переопределить или добавить свойство Microsoft UI Automation в элемент управления, можно указать идентификатор свойства модели автоматизации пользовательского интерфейса вместо идентификатора свойства Microsoft Active Accessibility. Список идентификаторов автоматизации пользовательского интерфейса см. в разделе [идентификаторы свойств](uiauto-entry-propids.md).



| Свойство                      | Тип     |
|-------------------------------|----------|
| \_имя счетов \_ PropID             | VT \_ BSTR |
| \_Описание счетов \_ PropID      | VT \_ BSTR |
| \_роль PropID ACC \_             | VT \_ I4   |
| \_состояние счетов \_ PropID            | VT \_ I4   |
| \_ \_ Справка по PropID             | VT \_ BSTR |
| PROPID \_ ACC \_ кэйбоардшорткут | VT \_ BSTR |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR |
| PROPID \_ ACC — \_ VALUEMAP         | VT \_ BSTR |
| PROPID \_ ACC \_ ролемап          | VT \_ BSTR |
| PROPID \_ ACC \_ статемап         | VT \_ BSTR |



 

 

 