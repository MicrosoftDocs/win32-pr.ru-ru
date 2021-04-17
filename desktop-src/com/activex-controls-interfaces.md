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
# <a name="activex-controls-interfaces"></a><span data-ttu-id="90fde-103">Интерфейсы элементов управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="90fde-103">ActiveX Controls Interfaces</span></span>

<span data-ttu-id="90fde-104">Помимо других механизмов взаимодействия между элементом управления и его клиентом, технология элементов управления ActiveX указывает интерфейсы [**метод интерфейса IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) и [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) для обмена данными между клиентом.</span><span class="sxs-lookup"><span data-stu-id="90fde-104">In addition to other mechanisms for communicating between the control and its client, ActiveX controls technology specifies the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) and [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interfaces for client-control communication.</span></span> <span data-ttu-id="90fde-105">Существует также интерфейс [**исимплефрамесите**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) для простых контейнеров элементов управления.</span><span class="sxs-lookup"><span data-stu-id="90fde-105">There is also the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface for simple control containers.</span></span>

<span data-ttu-id="90fde-106">Однако эти три интерфейса относятся к элементам управления и обычно не используются вне контекста элементов управления.</span><span class="sxs-lookup"><span data-stu-id="90fde-106">These three interfaces are, however, specific to controls and are not generally useful outside the context of controls.</span></span> <span data-ttu-id="90fde-107">Эти интерфейсы определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="90fde-107">These interfaces are defined as follows.</span></span>

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

<span data-ttu-id="90fde-108">Некоторые элементы управления, например поле группы, являются простым контейнером других элементов управления.</span><span class="sxs-lookup"><span data-stu-id="90fde-108">Some controls, like a group box, are merely a simple container of other controls.</span></span> <span data-ttu-id="90fde-109">В таких случаях простой элемент управления, называемый простым кадром, не должен реализовывать все требования к контейнеру.</span><span class="sxs-lookup"><span data-stu-id="90fde-109">In such cases, the simple control, called a simple frame, doesn't have to implement all the container requirements.</span></span> <span data-ttu-id="90fde-110">Она может делегировать большую часть вызовов интерфейсов из вложенных элементов управления в контейнер, управляющий простым фреймом.</span><span class="sxs-lookup"><span data-stu-id="90fde-110">It can delegate most of the interface calls from its contained controls to the container that manages the simple frame.</span></span> <span data-ttu-id="90fde-111">Помимо вызовов интерфейсов, простой фрейм также может работать с сообщениями Windows, которые потенциально поступают из элементов управления внутри него.</span><span class="sxs-lookup"><span data-stu-id="90fde-111">Besides interface calls, the simple frame also has to deal with Windows messages that potentially come from controls within it.</span></span> <span data-ttu-id="90fde-112">По этой причине контейнер предоставляет [**исимплефрамесите**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) , позволяющий таким простым элементам управления Frame передавать сообщения в контейнер.</span><span class="sxs-lookup"><span data-stu-id="90fde-112">For this reason, a container supplies [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) to allow such simple frame controls to pass messages up to the container.</span></span> <span data-ttu-id="90fde-113">[**Премессажефилтер**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) обрабатывает сообщение первыми; [**Постмессажефилтер**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) вызывается после того, как простой кадр обработал само сообщение.</span><span class="sxs-lookup"><span data-stu-id="90fde-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) processes the message first; [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) is called after the simple frame has processed the message itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90fde-114">См. также</span><span class="sxs-lookup"><span data-stu-id="90fde-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90fde-115">Элементы управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="90fde-115">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




