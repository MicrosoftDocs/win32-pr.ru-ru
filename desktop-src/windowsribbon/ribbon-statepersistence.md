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
# <a name="persisting-ribbon-state"></a>Сохранение состояния ленты

Платформа Windows рибон Framework (лента) предоставляет возможность сохранения состояния различных параметров и настроек пользователей во всех сеансах приложения.

-   [Введение](#introduction)
-   [Прогнозируемый опыт работы](#a-predictable-experience)
-   [Сохранить параметры ленты](#save-ribbon-settings)
-   [Загрузить параметры ленты](#load-ribbon-settings)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

Различные аспекты ленты, в том числе настройки конфигурации и взаимодействия, могут быть настроены пользователем во время выполнения для повышения удобства использования и производительности. Платформа Ribbon предоставляет функциональные возможности для сохранения этих параметров в сеансах приложений с помощью двух методов, определенных в реализации интерфейса [**иуириббон**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) : [**Иуириббон:: лоадсеттингсфромстреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) и [**иуириббон:: савесеттингстостреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).

## <a name="a-predictable-experience"></a>Прогнозируемый опыт работы

[Рекомендации по работе с лентой пользователей](https://msdn.microsoft.com/library/cc872782.aspx) рекомендуют, чтобы обеспечить наиболее предсказуемое взаимодействие с пользователем, если приложение ленты должно сохранять состояние ленты (помимо последней выбранной вкладки) при закрытии приложения. Таким образом, при запуске одного и того же приложения можно восстановить параметры и настройки из предыдущего сеанса, чтобы пользователь мог продолжить взаимодействие с приложением так же, как и в нем.

Параметры ленты, которые могут быть изменены во время выполнения и сохранены в сеансах приложений, перечислены в контекстном меню команды. К ним относятся следующие:

-   Команды, добавленные пользователем в список команд [панели быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md) . Задается объектом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) через ключ [свойства \_ \_ ItemsSource пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-itemssource.md) .

    На следующем снимке экрана показана команда контекстного меню **Добавить в панель быстрого доступа** .

    ![снимок экрана: контекстное меню команды на ленте Microsoft Paint.](images/controls/qat-contextmenu-add.png)

-   Предпочтительное состояние закрепления [панели быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md) . Определяется значением [**\_ Контролдокк пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) для ключа свойства [ \_ \_ куиккакцесстулбардокк UI PKEY](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) .

    На этом снимке экрана показана [панель быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md) в заголовке окна приложения по умолчанию и **панель инструментов быстрого доступа под** командой контекстного меню ленты.

    ![снимок экрана: контекстное меню команды на ленте Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    На этом снимке экрана показана [панель быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md) под лентой.

    ![снимок экрана панели быстрого доступа, закрепленной под лентой.](images/controls/qat-dockbottom.png)

-   Минимальное состояние ленты в соответствии с логическим значением ключа скрытого свойства [UI \_ PKEY \_ ](windowsribbon-reference-properties-uipkey-minimized.md) .

    > [!Note]  
    > Свернутое состояние ленты не эквивалентно свернутому состоянию ленты. В свернутом состоянии лента полностью скрыта и не может взаимодействовать с. Платформа вызывает это состояние автоматически, если размер окна приложения уменьшается на горизонтальном или вертикальном месте до того момента, когда лента скрывает рабочую область приложения. Платформа восстанавливает ленту при увеличении размера окна приложения.

     

    На этом снимке экрана показана команда сворачивания контекстного меню **ленты** .

    ![снимок экрана: контекстное меню команды на ленте Microsoft Paint.](images/controls/qat-contextmenu-add.png)

    На этом снимке экрана показана уменьшенная лента.

    ![снимок экрана: уменьшенная лента Microsoft Paint.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>Сохранить параметры ленты

Метод [**иуириббон:: савесеттингстостреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) записывает двоичное представление постоянного состояния ленты (описанное в предыдущем разделе) в объект [IStream](/windows/win32/api/objidl/nn-objidl-istream) . Затем приложение сохраняет содержимое объекта IStream в файл или реестр Windows.

В следующем примере показан базовый код, необходимый для записи состояния ленты в объект [IStream](/windows/win32/api/objidl/nn-objidl-istream) с помощью метода [**Иуириббон:: савесеттингстостреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) .


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



## <a name="load-ribbon-settings"></a>Загрузить параметры ленты

Метод [**иуириббон:: лоадсеттингсфромстреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) используется для получения постоянных сведений о состоянии ленты, хранящихся в виде объекта [IStream](/windows/win32/api/objidl/nn-objidl-istream) методом [**иуириббон:: савесеттингстостреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) . Сведения в объекте IStream применяются к ИНТЕРФЕЙСу Ribbon при инициализации приложения.

В следующем примере показан базовый код, необходимый для загрузки состояния ленты из объекта [IStream](/windows/win32/api/objidl/nn-objidl-istream) с помощью метода [**Иуириббон:: лоадсеттингсфромстреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .


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



Для оптимальной производительности метод [**иуириббон:: лоадсеттингсфромстреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) должен вызываться из функции обратного вызова [**Иуиаппликатион:: онвиевчанжед**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) на этапе инициализации платформы, как показано в следующем примере.


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



Несколько экземпляров одного приложения платформы Ribbon могут управлять состоянием ленты независимо друг от друга как отдельные объекты [IStream](/windows/win32/api/objidl/nn-objidl-istream) или как группу через один объект IStream.

При синхронизации состояния ленты в группе экземпляров приложения каждое окно верхнего уровня должно прослушивать уведомление об [ \_ активации WM](../inputdev/wm-activate.md) . Деактивируемое окно верхнего уровня сохраняет свое состояние ленты с помощью метода [**иуириббон:: савесеттингстостреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) , а активируемое окно верхнего уровня загружает свое состояние ленты с помощью метода [**Иуириббон:: лоадсеттингсфромстреам**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Панель быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 