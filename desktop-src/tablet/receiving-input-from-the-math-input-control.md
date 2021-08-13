---
description: В этом разделе объясняется, как получить разметку Масмл из элемента управления математическими вводами с помощью библиотеки ATL и модели COM.
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: Получение входных данных из элемента управления математическими данными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50325b8e9980907b91f4cd6400ed6cfd0ef3f04367a2bc753e5d4065e189bc44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449334"
---
# <a name="receiving-input-from-the-math-input-control"></a>Получение входных данных из элемента управления математическими данными

В этом разделе объясняется, как получить разметку Масмл из элемента управления математическими вводами с помощью библиотеки ATL и модели COM.

Чтобы получить распознанное математическое уравнение из элемента управления математическими данными, можно переопределить поведение, которое происходит при нажатии кнопки вставки. Для этого необходимо настроить обработчик событий, который реализует различные события, поддерживаемые интерфейсом [**\_ имасинпутконтролевентс**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) . Настройка обработчика событий включает в себя выполнение следующих действий для событий, которые требуется поддерживать (Вставка в этом случае).

-   [Создание класса шаблона, который содержит приемники событий](#create-a-template-class-that-contains-event-sinks)
-   [Настройка обработчиков событий](#set-up-the-event-handlers)
-   [Наследовать класс обработчика событий в основном классе](#inherit-the-event-handler-class-in-your-main-class)
-   [Инициализация класса для наследования приемников событий](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a>Создание класса шаблона, который содержит приемники событий

При реализации приемника событий, использующего элемент управления математическими данными, необходимо сначала указать идентификатор приемника. Затем необходимо создать класс шаблона, наследующий от события, обработчика управления событиями и интерфейсов событий элемента управления для ввода математических символов. В следующем коде показано, как задать идентификатор приемника и создать такой класс шаблона Кмасинпутконтролевенсандлер, который наследуется от требуемых интерфейсов. Этот класс шаблона также настроен для создания закрытого неизвестного указателя интерфейса, который будет использоваться для передачи элемента управления математическими данными при инициализации и \_ элемента m уладвисекаунт для подсчета числа вызовов advise/unadvise.


```
  
#pragma once
static const int MATHINPUTCONTROL_SINK_ID = 1 ;

template <class T>
class ATL_NO_VTABLE CMathInputControlEventHandler :
    public IDispEventSimpleImpl<MATHINPUTCONTROL_SINK_ID, CMathInputControlEventHandler<T>, &__uuidof(_IMathInputControlEvents)>
{
private:
    IUnknown    *m_pUnknown;
    ULONG m_ulAdviseCount;
    CDialog *m_pMain;

```



> [!Note]  
> Если диалоговое окно не используется, член **m \_ пмаин** должен быть другим в вашей реализации.

 

Теперь, когда у вас есть базовый класс шаблона, необходимо предоставить прямую декларацию для обработчиков событий, которые будут переопределяться, и затем настроить карту приемников для обрабатываемых событий. В следующем коде показано, как настроить обработчики событий для метода [**INSERT**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , который вызывается, когда пользователь нажимает кнопку «Вставить» в элементе управления Math input, и метод [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , вызываемый при нажатии пользователем кнопки «Отмена» для элемента управления Math input.


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



Поскольку вы будете работать с элементом управления математическими данными, вам будет полезно задать внутреннюю ссылку на соответствующий интерфейс. Следующая служебная функция создается в классе example для установки этой ссылки.


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a>Настройка обработчиков событий

После настройки приемников событий необходимо создать свои реализации приемников событий служб. В обоих методах в следующем примере кода приемники событий извлекают маркер в интерфейс элемента управления Math. В функции [**INSERT**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) результат распознавания отображается как масмл, а элемент управления скрыт. В функции [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) элемент управления математическими данными является скрытым.


```
  
    // Methods
    HRESULT __stdcall OnMICInsert( BSTR bstrRecoResult)
    {
        CComQIPtr<IMathInputControl> spMIC(m_pUnknown);
        HRESULT hr=S_OK;
        if (spMIC)
        {           
            MessageBox(NULL,bstrRecoResult,L"Recognition Result",MB_OK);
            hr = spMIC->Hide();
            return hr;  
        }
        return E_FAIL;          
    }

    HRESULT __stdcall OnMICClose()
    {
        CComPtr<IMathInputControl> spMIC;
        HRESULT hr = m_pUnknown->QueryInterface<IMathInputControl>(&spMIC);
        if (SUCCEEDED(hr))
        {           
            hr = spMIC->Hide();
            return hr;  
        }
        return hr;                  
    }
};  
```



## <a name="inherit-the-event-handler-class-in-your-main-class"></a>Наследовать класс обработчика событий в основном классе

После реализации класса шаблона его необходимо наследовать в классе, в котором будет настраиваться элемент управления математическим вводом в. Для целей данного руководством этот класс является диалоговым окном CMIC \_ Test \_ евентсдлг. В заголовке диалогового окна должны быть добавлены заголовки реквизита, и созданный класс шаблона должен быть унаследован. Класс, который наследуется внутри, и обработчики событий должны иметь прямые объявления, чтобы шаблон можно было реализовать. В следующем примере кода показано, как это сделать.


```
#pragma once
#include <atlbase.h>
#include <atlwin.h>

// include for MIC
#include "micaut.h"

// include for event sinks
#include <iacom.h>
#include "mathinputcontroleventhandler.h"

class CMIC_TEST_EVENTSDlg;

const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICInsertInfo = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICCloseInfo = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

// CMIC_TEST_EVENTSDlg dialog
class CMIC_TEST_EVENTSDlg : public CDialog,
    public CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>
{
  public:
  CComPtr<IMathInputControl> m_spMIC; // Math Input Control

  
```



> [!Note]  
> Тип шаблона, **CMIC \_ Test \_ евентсдлг**, будет отличаться, если вы не настроили свой класс так же, как в примере.

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a>Инициализация класса для наследования приемников событий

После настройки класса для наследования от класса шаблона можно приступать к его настройке для управления событиями. Это будет состоять из инициализации класса, чтобы иметь обработчик для элемента управления математическими вводом и вызывающего класса. Кроме того, элемент управления математическим вводом для работы с событиями должен отправляться в метод Диспевентадвисе, который наследуется классом Кмасинпутконтролевенсандлер example. Следующий код вызывается из метода Онинитдиалог класса Example для выполнения этих действий.


```
// includes for implementation
#include "micaut_i.c"

// include for event handler
#include "mathinputcontroleventhandler.h"

...

OnInitDialog{
  ...

  // TODO: Add extra initialization here
  CoInitialize(NULL);
  HRESULT hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
  if (SUCCEEDED(hr)){
    hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::Initialize(m_spMIC, this);
      if (SUCCEEDED(hr)){
        hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::DispEventAdvise(m_spMIC);            
        if (SUCCEEDED(hr)){
          hr = m_spMIC->Show();  
        }
      }
    }
  }  
}
  
```



> [!Note]  
> Тип шаблона, CMIC \_ Test \_ евентсдлг в этом примере, будет отличаться, если вы не настроили класс так же, как в примере.

 

 

 
