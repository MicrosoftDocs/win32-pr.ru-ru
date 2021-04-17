---
title: Интерфейсы элементов управления ActiveX
description: Интерфейсы элементов управления ActiveX
ms.assetid: c4ca5696-c461-4d65-b2a8-c689c056dac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd7c4e0b726e9f330910bd468c237c72462fa21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691170"
---
# <a name="activex-controls-interfaces"></a>Интерфейсы элементов управления ActiveX

Помимо других механизмов взаимодействия между элементом управления и его клиентом, технология элементов управления ActiveX указывает интерфейсы [**метод интерфейса IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) и [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) для обмена данными между клиентом. Существует также интерфейс [**исимплефрамесите**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) для простых контейнеров элементов управления.

Однако эти три интерфейса относятся к элементам управления и обычно не используются вне контекста элементов управления. Эти интерфейсы определяются следующим образом.

``` syntax
interface IOleControl : IUnknown 
  { 
    HRESULT GetControlInfo([out] CONTROLINFO *pCI); 
    HRESULT OnMnemonic([in] LPMSG pMsg); 
    HRESULT OnAmbientPropertyChange([in] DISPID dispID); 
    HRESULT FreezeEvents([in] BOOL bFreeze); 
  } 
 
interface IOleControlSite : IUnknown 
  { 
    HRESULT OnControlInfoChanged(void); 
    HRESULT LockInPlaceActive([in] BOOL fLock); 
    HRESULT GetExtendedControl([out] IDispatch **ppDisp); 
    HRESULT TransformCoords([in-out] POINTL *pptlHimetric, [in-out] POINTF *pptfContainer, [in] DWORD dwFlags); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg, [in] DWORD grfModifiers); 
    HRESULT OnFocus([in] BOOL fGotFocus); 
    HRESULT ShowPropertyFrame(void); 
  } 
 
interface ISimpleFrameSite : IUnknown 
  { 
    HRESULT PreMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [out] DWORD *pdwCookie); 
    HRESULT PostMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [in] DWORD dwCookie); 
  } 
 
```

Некоторые элементы управления, например поле группы, являются простым контейнером других элементов управления. В таких случаях простой элемент управления, называемый простым кадром, не должен реализовывать все требования к контейнеру. Она может делегировать большую часть вызовов интерфейсов из вложенных элементов управления в контейнер, управляющий простым фреймом. Помимо вызовов интерфейсов, простой фрейм также может работать с сообщениями Windows, которые потенциально поступают из элементов управления внутри него. По этой причине контейнер предоставляет [**исимплефрамесите**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) , позволяющий таким простым элементам управления Frame передавать сообщения в контейнер. [**Премессажефилтер**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) обрабатывает сообщение первыми; [**Постмессажефилтер**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) вызывается после того, как простой кадр обработал само сообщение.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Элементы управления ActiveX](activex-controls.md)
</dt> </dl>

 

 




