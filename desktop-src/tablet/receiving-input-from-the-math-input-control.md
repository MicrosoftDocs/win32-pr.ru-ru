---
description: В этом разделе объясняется, как получить разметку Масмл из элемента управления математическими вводами с помощью библиотеки ATL и модели COM.
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: Получение входных данных из элемента управления математическими данными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 830c8f57bb7b27c305928cf68b658dcc37ede5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703048"
---
# <a name="receiving-input-from-the-math-input-control"></a><span data-ttu-id="faf76-103">Получение входных данных из элемента управления математическими данными</span><span class="sxs-lookup"><span data-stu-id="faf76-103">Receiving Input from the Math Input Control</span></span>

<span data-ttu-id="faf76-104">В этом разделе объясняется, как получить разметку Масмл из элемента управления математическими вводами с помощью библиотеки ATL и модели COM.</span><span class="sxs-lookup"><span data-stu-id="faf76-104">This section explains how to retrieve the MathML markup from the math input control using the Active Template Library (ATL) and the Component Object Model (COM).</span></span>

<span data-ttu-id="faf76-105">Чтобы получить распознанное математическое уравнение из элемента управления математическими данными, можно переопределить поведение, которое происходит при нажатии кнопки вставки.</span><span class="sxs-lookup"><span data-stu-id="faf76-105">To retrieve the recognized math equation from the math input control, you can override the behavior that happens when the insert button is pressed.</span></span> <span data-ttu-id="faf76-106">Для этого необходимо настроить обработчик событий, который реализует различные события, поддерживаемые интерфейсом [**\_ имасинпутконтролевентс**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) .</span><span class="sxs-lookup"><span data-stu-id="faf76-106">To do this, you will need to set up an event handler that implements the various events that are supported by the [**\_IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) interface.</span></span> <span data-ttu-id="faf76-107">Настройка обработчика событий включает в себя выполнение следующих действий для событий, которые требуется поддерживать (Вставка в этом случае).</span><span class="sxs-lookup"><span data-stu-id="faf76-107">Setting up the events handler involves the performing the following steps for the events you want to support (insert in this case).</span></span>

-   [<span data-ttu-id="faf76-108">Создание класса шаблона, который содержит приемники событий</span><span class="sxs-lookup"><span data-stu-id="faf76-108">Create a template class that contains event sinks</span></span>](#create-a-template-class-that-contains-event-sinks)
-   [<span data-ttu-id="faf76-109">Настройка обработчиков событий</span><span class="sxs-lookup"><span data-stu-id="faf76-109">Set up the event handlers</span></span>](#set-up-the-event-handlers)
-   [<span data-ttu-id="faf76-110">Наследовать класс обработчика событий в основном классе</span><span class="sxs-lookup"><span data-stu-id="faf76-110">Inherit the event handler class in your main class</span></span>](#inherit-the-event-handler-class-in-your-main-class)
-   [<span data-ttu-id="faf76-111">Инициализация класса для наследования приемников событий</span><span class="sxs-lookup"><span data-stu-id="faf76-111">Initialize your class to inherit the event sink(s)</span></span>](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a><span data-ttu-id="faf76-112">Создание класса шаблона, который содержит приемники событий</span><span class="sxs-lookup"><span data-stu-id="faf76-112">Create a template class that contains event sinks</span></span>

<span data-ttu-id="faf76-113">При реализации приемника событий, использующего элемент управления математическими данными, необходимо сначала указать идентификатор приемника. Затем необходимо создать класс шаблона, наследующий от события, обработчика управления событиями и интерфейсов событий элемента управления для ввода математических символов.</span><span class="sxs-lookup"><span data-stu-id="faf76-113">When you are implementing an event sink that uses the math input control, you must first specify a sink id. You must then create a template class that inherits from the event, event control handler, and math input control event interfaces.</span></span> <span data-ttu-id="faf76-114">В следующем коде показано, как задать идентификатор приемника и создать такой класс шаблона Кмасинпутконтролевенсандлер, который наследуется от требуемых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="faf76-114">The following code shows how to set a sink id and create such a template class, CMathInputControlEventHandler, that inherits from the requisite interfaces.</span></span> <span data-ttu-id="faf76-115">Этот класс шаблона также настроен для создания закрытого неизвестного указателя интерфейса, который будет использоваться для передачи элемента управления математическими данными при инициализации и \_ элемента m уладвисекаунт для подсчета числа вызовов advise/unadvise.</span><span class="sxs-lookup"><span data-stu-id="faf76-115">This template class also is set up to have a private unknown interface pointer that will be used to pass the math input control to it on initialization and the m\_ulAdviseCount member to count the number of calls to advise / unadvise.</span></span>


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
> <span data-ttu-id="faf76-116">Если диалоговое окно не используется, член **m \_ пмаин** должен быть другим в вашей реализации.</span><span class="sxs-lookup"><span data-stu-id="faf76-116">The member **m\_pMain** should be different in your implementation if you are not using a dialog.</span></span>

 

<span data-ttu-id="faf76-117">Теперь, когда у вас есть базовый класс шаблона, необходимо предоставить прямую декларацию для обработчиков событий, которые будут переопределяться, и затем настроить карту приемников для обрабатываемых событий.</span><span class="sxs-lookup"><span data-stu-id="faf76-117">Now that you have the basic template class, you must give a forward declaration for the event handlers that you will be overriding and must then set up a sink map for the events you will be handling.</span></span> <span data-ttu-id="faf76-118">В следующем коде показано, как настроить обработчики событий для метода [**INSERT**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , который вызывается, когда пользователь нажимает кнопку «Вставить» в элементе управления Math input, и метод [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , вызываемый при нажатии пользователем кнопки «Отмена» для элемента управления Math input.</span><span class="sxs-lookup"><span data-stu-id="faf76-118">The following code shows how to set up event handlers for the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) method, called when a user clicks the insert button on the math input control, and the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) method, called when a user clicks the cancel button on the math input control.</span></span>


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



<span data-ttu-id="faf76-119">Поскольку вы будете работать с элементом управления математическими данными, вам будет полезно задать внутреннюю ссылку на соответствующий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="faf76-119">Since you will be working with the math input control, it will be useful to set an internal reference to the relevant interface.</span></span> <span data-ttu-id="faf76-120">Следующая служебная функция создается в классе example для установки этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="faf76-120">The following utility function is created in the example class to set this reference.</span></span>


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a><span data-ttu-id="faf76-121">Настройка обработчиков событий</span><span class="sxs-lookup"><span data-stu-id="faf76-121">Set up the event handlers</span></span>

<span data-ttu-id="faf76-122">После настройки приемников событий необходимо создать свои реализации приемников событий служб.</span><span class="sxs-lookup"><span data-stu-id="faf76-122">Once you have set up the event sinks, you will need to create your implementations of the event sinks.</span></span> <span data-ttu-id="faf76-123">В обоих методах в следующем примере кода приемники событий извлекают маркер в интерфейс элемента управления Math.</span><span class="sxs-lookup"><span data-stu-id="faf76-123">In both of the methods in the following code example, the event sinks retrieve a handle to the math input control interface.</span></span> <span data-ttu-id="faf76-124">В функции [**INSERT**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) результат распознавания отображается как масмл, а элемент управления скрыт.</span><span class="sxs-lookup"><span data-stu-id="faf76-124">In the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) function, the recognition result is displayed as MathML and the control is hidden.</span></span> <span data-ttu-id="faf76-125">В функции [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) элемент управления математическими данными является скрытым.</span><span class="sxs-lookup"><span data-stu-id="faf76-125">In the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) function, the math input control is hidden.</span></span>


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



## <a name="inherit-the-event-handler-class-in-your-main-class"></a><span data-ttu-id="faf76-126">Наследовать класс обработчика событий в основном классе</span><span class="sxs-lookup"><span data-stu-id="faf76-126">Inherit the event handler class in your main class</span></span>

<span data-ttu-id="faf76-127">После реализации класса шаблона его необходимо наследовать в классе, в котором будет настраиваться элемент управления математическим вводом в.</span><span class="sxs-lookup"><span data-stu-id="faf76-127">After you have your template class implemented, you will need to inherit it into the class that you will be setting up your math input control in.</span></span> <span data-ttu-id="faf76-128">Для целей данного руководством этот класс является диалоговым окном CMIC \_ Test \_ евентсдлг.</span><span class="sxs-lookup"><span data-stu-id="faf76-128">For the purposes of this guide, this class is a dialog, CMIC\_TEST\_EVENTSDlg.</span></span> <span data-ttu-id="faf76-129">В заголовке диалогового окна должны быть добавлены заголовки реквизита, и созданный класс шаблона должен быть унаследован.</span><span class="sxs-lookup"><span data-stu-id="faf76-129">In the dialog header, the requisite headers must be included and the template class you created must be inherited.</span></span> <span data-ttu-id="faf76-130">Класс, который наследуется внутри, и обработчики событий должны иметь прямые объявления, чтобы шаблон можно было реализовать.</span><span class="sxs-lookup"><span data-stu-id="faf76-130">The class you're inheriting within and the event handlers must have forward declarations so that the template can be implemented.</span></span> <span data-ttu-id="faf76-131">В следующем примере кода показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="faf76-131">The following code example shows how this is done.</span></span>


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
> <span data-ttu-id="faf76-132">Тип шаблона, **CMIC \_ Test \_ евентсдлг**, будет отличаться, если вы не настроили свой класс так же, как в примере.</span><span class="sxs-lookup"><span data-stu-id="faf76-132">The template type, **CMIC\_TEST\_EventsDlg**, will be different unless you have named your class the same as the example.</span></span>

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a><span data-ttu-id="faf76-133">Инициализация класса для наследования приемников событий</span><span class="sxs-lookup"><span data-stu-id="faf76-133">Initialize your class to inherit the event sink(s)</span></span>

<span data-ttu-id="faf76-134">После настройки класса для наследования от класса шаблона можно приступать к его настройке для управления событиями.</span><span class="sxs-lookup"><span data-stu-id="faf76-134">Once you have set up your class to inherit from the template class, you are ready to set it up to handle events.</span></span> <span data-ttu-id="faf76-135">Это будет состоять из инициализации класса, чтобы иметь обработчик для элемента управления математическими вводом и вызывающего класса.</span><span class="sxs-lookup"><span data-stu-id="faf76-135">This will consist of initializing the class to have a handle to the math input control and the calling class.</span></span> <span data-ttu-id="faf76-136">Кроме того, элемент управления математическим вводом для работы с событиями должен отправляться в метод Диспевентадвисе, который наследуется классом Кмасинпутконтролевенсандлер example.</span><span class="sxs-lookup"><span data-stu-id="faf76-136">Additionally, the math input control to handle events from must be sent to the DispEventAdvise method that the CMathInputControlEventHandler example class inherits.</span></span> <span data-ttu-id="faf76-137">Следующий код вызывается из метода Онинитдиалог класса Example для выполнения этих действий.</span><span class="sxs-lookup"><span data-stu-id="faf76-137">The following code is called from the OnInitDialog method in the example class to perform these actions.</span></span>


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
> <span data-ttu-id="faf76-138">Тип шаблона, CMIC \_ Test \_ евентсдлг в этом примере, будет отличаться, если вы не настроили класс так же, как в примере.</span><span class="sxs-lookup"><span data-stu-id="faf76-138">The template type, CMIC\_TEST\_EventsDlg in this example, will be different unless you have named your class the same as the example.</span></span>

 

 

 
