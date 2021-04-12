---
title: Сохранение состояния ленты
description: Платформа Windows рибон Framework (лента) предоставляет возможность сохранения состояния различных параметров и настроек пользователей во всех сеансах приложения.
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a3b704151b657bdfe95845c8473a0fd197e87b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338313"
---
# <a name="persisting-ribbon-state"></a><span data-ttu-id="861d2-103">Сохранение состояния ленты</span><span class="sxs-lookup"><span data-stu-id="861d2-103">Persisting Ribbon State</span></span>

<span data-ttu-id="861d2-104">Платформа Windows рибон Framework (лента) предоставляет возможность сохранения состояния различных параметров и настроек пользователей во всех сеансах приложения.</span><span class="sxs-lookup"><span data-stu-id="861d2-104">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

-   [<span data-ttu-id="861d2-105">Введение</span><span class="sxs-lookup"><span data-stu-id="861d2-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="861d2-106">Прогнозируемый опыт работы</span><span class="sxs-lookup"><span data-stu-id="861d2-106">A Predictable Experience</span></span>](#a-predictable-experience)
-   [<span data-ttu-id="861d2-107">Сохранить параметры ленты</span><span class="sxs-lookup"><span data-stu-id="861d2-107">Save Ribbon Settings</span></span>](#save-ribbon-settings)
-   [<span data-ttu-id="861d2-108">Загрузить параметры ленты</span><span class="sxs-lookup"><span data-stu-id="861d2-108">Load Ribbon Settings</span></span>](#load-ribbon-settings)
-   [<span data-ttu-id="861d2-109">См. также</span><span class="sxs-lookup"><span data-stu-id="861d2-109">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="861d2-110">Введение</span><span class="sxs-lookup"><span data-stu-id="861d2-110">Introduction</span></span>

<span data-ttu-id="861d2-111">Различные аспекты ленты, в том числе настройки конфигурации и взаимодействия, могут быть настроены пользователем во время выполнения для повышения удобства использования и производительности.</span><span class="sxs-lookup"><span data-stu-id="861d2-111">Various aspects of a ribbon, including configuration and interaction preferences, can be customized by a user at run time to improve usability and productivity.</span></span> <span data-ttu-id="861d2-112">Платформа Ribbon предоставляет функциональные возможности для сохранения этих параметров в сеансах приложений с помощью двух методов, определенных в реализации интерфейса [**иуириббон**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) : [**Иуириббон:: лоадсеттингсфромстреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) и [**иуириббон:: савесеттингстостреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span><span class="sxs-lookup"><span data-stu-id="861d2-112">The Ribbon framework provides the functionality to preserve these settings across application sessions through two methods defined in the implementation of the [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) interface: [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) and [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span></span>

## <a name="a-predictable-experience"></a><span data-ttu-id="861d2-113">Прогнозируемый опыт работы</span><span class="sxs-lookup"><span data-stu-id="861d2-113">A Predictable Experience</span></span>

<span data-ttu-id="861d2-114">[Рекомендации по работе с лентой пользователей](https://msdn.microsoft.com/library/cc872782.aspx) рекомендуют, чтобы обеспечить наиболее предсказуемое взаимодействие с пользователем, если приложение ленты должно сохранять состояние ленты (помимо последней выбранной вкладки) при закрытии приложения.</span><span class="sxs-lookup"><span data-stu-id="861d2-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) advise that, to provide the most predictable user experience possible, Ribbon applications should preserve the state of the ribbon (aside from the last selected tab) as the application is closed.</span></span> <span data-ttu-id="861d2-115">Таким образом, при запуске одного и того же приложения можно восстановить параметры и настройки из предыдущего сеанса, чтобы пользователь мог продолжить взаимодействие с приложением так же, как и в нем.</span><span class="sxs-lookup"><span data-stu-id="861d2-115">In this way, when the same application is launched, the settings and customizations from the previous session can be restored and the user can expect to continue interacting with the application in the same way as they left it.</span></span>

<span data-ttu-id="861d2-116">Параметры ленты, которые могут быть изменены во время выполнения и сохранены в сеансах приложений, перечислены в контекстном меню команды.</span><span class="sxs-lookup"><span data-stu-id="861d2-116">Ribbon settings that can be modified at run time and preserved across application sessions are listed in the Command context menu.</span></span> <span data-ttu-id="861d2-117">К ним относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="861d2-117">They include:</span></span>

-   <span data-ttu-id="861d2-118">Команды, добавленные пользователем в список команд [панели быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="861d2-118">Commands added to the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) Command list by the user.</span></span> <span data-ttu-id="861d2-119">Задается объектом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) через ключ [свойства \_ \_ ItemsSource пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-itemssource.md) .</span><span class="sxs-lookup"><span data-stu-id="861d2-119">Specified by an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span>

    <span data-ttu-id="861d2-120">На следующем снимке экрана показана команда контекстного меню **Добавить в панель быстрого доступа** .</span><span class="sxs-lookup"><span data-stu-id="861d2-120">The following screen shot shows the **Add to Quick Access Toolbar** context menu Command.</span></span>

    ![снимок экрана: контекстное меню команды на ленте Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   <span data-ttu-id="861d2-122">Предпочтительное состояние закрепления [панели быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="861d2-122">The preferred [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) docking state.</span></span> <span data-ttu-id="861d2-123">Определяется значением [**\_ Контролдокк пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) для ключа свойства [ \_ \_ куиккакцесстулбардокк UI PKEY](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) .</span><span class="sxs-lookup"><span data-stu-id="861d2-123">Specified by the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) value of the [UI\_PKEY\_QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) property key.</span></span>

    <span data-ttu-id="861d2-124">На этом снимке экрана показана [панель быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md) в заголовке окна приложения по умолчанию и **панель инструментов быстрого доступа под** командой контекстного меню ленты.</span><span class="sxs-lookup"><span data-stu-id="861d2-124">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) in its default application title bar location and the **Show Quick Access Toolbar below the Ribbon** context menu Command.</span></span>

    ![снимок экрана: контекстное меню команды на ленте Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="861d2-126">На этом снимке экрана показана [панель быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md) под лентой.</span><span class="sxs-lookup"><span data-stu-id="861d2-126">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) below the ribbon.</span></span>

    ![снимок экрана панели быстрого доступа, закрепленной под лентой.](images/controls/qat-dockbottom.png)

-   <span data-ttu-id="861d2-128">Минимальное состояние ленты в соответствии с логическим значением ключа скрытого свойства [UI \_ PKEY \_ ](windowsribbon-reference-properties-uipkey-minimized.md) .</span><span class="sxs-lookup"><span data-stu-id="861d2-128">The ribbon minimized state as specified by the boolean value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key.</span></span>

    > [!Note]  
    > <span data-ttu-id="861d2-129">Свернутое состояние ленты не эквивалентно свернутому состоянию ленты.</span><span class="sxs-lookup"><span data-stu-id="861d2-129">The ribbon minimized state is not equivalent to the ribbon collapsed state.</span></span> <span data-ttu-id="861d2-130">В свернутом состоянии лента полностью скрыта и не может взаимодействовать с.</span><span class="sxs-lookup"><span data-stu-id="861d2-130">When in collapsed state, the ribbon is completely hidden and cannot be interacted with.</span></span> <span data-ttu-id="861d2-131">Платформа вызывает это состояние автоматически, если размер окна приложения уменьшается на горизонтальном или вертикальном месте до того момента, когда лента скрывает рабочую область приложения.</span><span class="sxs-lookup"><span data-stu-id="861d2-131">The framework invokes this state automatically if the application window is reduced in size, either horizontally or vertically, to the point that the ribbon obscures the application workspace.</span></span> <span data-ttu-id="861d2-132">Платформа восстанавливает ленту при увеличении размера окна приложения.</span><span class="sxs-lookup"><span data-stu-id="861d2-132">The framework restores the ribbon when the size of the application window is increased.</span></span>

     

    <span data-ttu-id="861d2-133">На этом снимке экрана показана команда сворачивания контекстного меню **ленты** .</span><span class="sxs-lookup"><span data-stu-id="861d2-133">This screen shot shows the **Minimize the Ribbon** context menu Command.</span></span>

    ![снимок экрана: контекстное меню команды на ленте Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="861d2-135">На этом снимке экрана показана уменьшенная лента.</span><span class="sxs-lookup"><span data-stu-id="861d2-135">This screen shot shows a minimized ribbon.</span></span>

    ![снимок экрана: уменьшенная лента Microsoft Paint.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a><span data-ttu-id="861d2-137">Сохранить параметры ленты</span><span class="sxs-lookup"><span data-stu-id="861d2-137">Save Ribbon Settings</span></span>

<span data-ttu-id="861d2-138">Метод [**иуириббон:: савесеттингстостреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) записывает двоичное представление постоянного состояния ленты (описанное в предыдущем разделе) в объект [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="861d2-138">The [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method writes a binary representation of the persistent ribbon state (outlined in the previous section) to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span> <span data-ttu-id="861d2-139">Затем приложение сохраняет содержимое объекта IStream в файл или реестр Windows.</span><span class="sxs-lookup"><span data-stu-id="861d2-139">The application then saves the content of the IStream object to a file or the Windows registry.</span></span>

<span data-ttu-id="861d2-140">В следующем примере показан базовый код, необходимый для записи состояния ленты в объект [IStream](/windows/win32/api/objidl/nn-objidl-istream) с помощью метода [**Иуириббон:: савесеттингстостреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .</span><span class="sxs-lookup"><span data-stu-id="861d2-140">The following example demonstrates the basic code required to write the ribbon state to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span>


```C++
// pRibbon        - Pointer to the IUIRibbon interface
// ppStatusStream - Pointer to the location of a newly created IStream object
HRESULT CApplication::SaveRibbonStatusToStream(
                        __in IUIRibbon *pRibbon, 
                        __out IStream **ppStatusStream)
{
  HRESULT hr = E_FAIL; 

  *ppStatusStream = NULL;
  IStream* pStream;
  if (SUCCEEDED(hr = CreateStreamOnHGlobal(
                       NULL,  // Internally allocate a new shared memory.
                       FALSE, // Free hGlobal after IStream object released.
                       &pStream)))
  {
    if (SUCCEEDED(hr = pRibbon->SaveSettingsToStream(*ppStatusStream)))
    {                  
      pStream->AddRef();
      *ppStatusStream = pStream;
    }
    pStream->Release();
  }
  return hr;
}
```



## <a name="load-ribbon-settings"></a><span data-ttu-id="861d2-141">Загрузить параметры ленты</span><span class="sxs-lookup"><span data-stu-id="861d2-141">Load Ribbon Settings</span></span>

<span data-ttu-id="861d2-142">Метод [**иуириббон:: лоадсеттингсфромстреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) используется для получения постоянных сведений о состоянии ленты, хранящихся в виде объекта [IStream](/windows/win32/api/objidl/nn-objidl-istream) методом [**иуириббон:: савесеттингстостреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .</span><span class="sxs-lookup"><span data-stu-id="861d2-142">The [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method is used to retrieve the persistent ribbon state information stored as an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object by the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span> <span data-ttu-id="861d2-143">Сведения в объекте IStream применяются к ИНТЕРФЕЙСу Ribbon при инициализации приложения.</span><span class="sxs-lookup"><span data-stu-id="861d2-143">The information in the IStream object is applied to the ribbon UI when the application initializes.</span></span>

<span data-ttu-id="861d2-144">В следующем примере показан базовый код, необходимый для загрузки состояния ленты из объекта [IStream](/windows/win32/api/objidl/nn-objidl-istream) с помощью метода [**Иуириббон:: лоадсеттингсфромстреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="861d2-144">The following example demonstrates the basic code required to load the ribbon state from an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object with the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>


```C++
// pRibbon       - Pointer to the IUIRibbon interface
// pStatusStream - Pointer to the IStream object that contains the Ribbon state information
HRESULT CApplication::LoadRibbonStatusFromStream(
                        __in IUIRibbon *pRibbon, 
                        __in IStream *pStatusStream)
{     
  HRESULT hr = E_FAIL;
  if (pStatusStream)
  {
    // Set the stream position to the beginning first.
    LARGE_INTEGER liStart = {0, 0};
    ULARGE_INTEGER ulActual;
    pStatusStream->Seek(liStart, STREAM_SEEK_SET, &ulActual);
    hr = pRibbon->LoadSettingsFromStream(pStatusStream);
  }
  return hr;
}
```



<span data-ttu-id="861d2-145">Для оптимальной производительности метод [**иуириббон:: лоадсеттингсфромстреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) должен вызываться из функции обратного вызова [**Иуиаппликатион:: онвиевчанжед**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) на этапе инициализации платформы, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="861d2-145">For optimal performance, the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method should be called from the [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) callback function during the framework initialization phase, as shown in the following example.</span></span>


```C++
IFACEMETHODIMP CMyRibbonApplication::OnViewChanged(
                                       UINT nViewID, 
                                       __in UI_VIEWTYPE typeID, 
                                       __in IUnknown* pView, 
                                       UI_VIEWVERB verb, 
                                       INT iReasonCode)
{
  HRESULT hr = E_NOTIMPL;
  if (UI_VIEWVERB_CREATE == verb)
  {
    IUIRibbon* pRibbon = NULL;
    hr = pView->QueryInterface(IID_PPV_ARGS(&pRibbon));

    if (SUCCEEDED(hr))
    {
      hr = _LoadRibbonSettings(pRibbon);
      pRibbon->Release();
    }
  }
  return hr;
}

HRESULT CMyRibbonApplication::_LoadRibbonSettings(IUIRibbon* pRibbon)
{
  ...
  pRibbon->LoadSettingsFromStream(pStream);
  ...
}
```



<span data-ttu-id="861d2-146">Несколько экземпляров одного приложения платформы Ribbon могут управлять состоянием ленты независимо друг от друга как отдельные объекты [IStream](/windows/win32/api/objidl/nn-objidl-istream) или как группу через один объект IStream.</span><span class="sxs-lookup"><span data-stu-id="861d2-146">Multiple instances of the same Ribbon framework application can manage each ribbon state independently as separate [IStream](/windows/win32/api/objidl/nn-objidl-istream) objects or as a group through a single IStream object.</span></span>

<span data-ttu-id="861d2-147">При синхронизации состояния ленты в группе экземпляров приложения каждое окно верхнего уровня должно прослушивать уведомление об [ \_ активации WM](../inputdev/wm-activate.md) .</span><span class="sxs-lookup"><span data-stu-id="861d2-147">When synchronizing ribbon state across a group of application instances, each top-level window must listen for a [WM\_ACTIVATE](../inputdev/wm-activate.md) notification.</span></span> <span data-ttu-id="861d2-148">Деактивируемое окно верхнего уровня сохраняет свое состояние ленты с помощью метода [**иуириббон:: савесеттингстостреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) , а активируемое окно верхнего уровня загружает свое состояние ленты с помощью метода [**Иуириббон:: лоадсеттингсфромстреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="861d2-148">The top-level window being deactivated saves its ribbon state using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method, and the top-level window being activated loads its ribbon state using the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="861d2-149">См. также</span><span class="sxs-lookup"><span data-stu-id="861d2-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="861d2-150">Панель быстрого доступа</span><span class="sxs-lookup"><span data-stu-id="861d2-150">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 