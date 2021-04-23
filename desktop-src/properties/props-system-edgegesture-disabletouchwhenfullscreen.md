---
description: Предотвращает поведение пограничных жестов при активном окне приложения и в полноэкранном режиме (или в активном окне).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System. Еджежестуре. Дисаблетаучвхенфуллскрин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 208962f11b96420a8e0ef771ada846a3f802e815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656690"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a><span data-ttu-id="58a67-103">System. Еджежестуре. Дисаблетаучвхенфуллскрин</span><span class="sxs-lookup"><span data-stu-id="58a67-103">System.EdgeGesture.DisableTouchWhenFullscreen</span></span>

<span data-ttu-id="58a67-104">Предотвращает поведение пограничных жестов при активном окне приложения и в полноэкранном режиме (или в активном окне).</span><span class="sxs-lookup"><span data-stu-id="58a67-104">Prevents edge gesture behaviors when an application window is active and in full-screen mode (or an owned window is active).</span></span>

> [!Note]  
> <span data-ttu-id="58a67-105">В полноэкранном режиме размер окна приложения соответствует разрешению экрана.</span><span class="sxs-lookup"><span data-stu-id="58a67-105">In full-screen mode, the size of the application window matches the screen resolution.</span></span>

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="58a67-106">Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="58a67-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.EdgeGesture.DisableTouchWhenFullscreen
   shellPKey = PKEY_EdgeGesture_DisableTouchWhenFullscreen
   formatID = 32CE38B2-2C9A-41B1-9BC5-B3784394AA44
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="58a67-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58a67-107">Remarks</span></span>

<span data-ttu-id="58a67-108">В Windows 8 взаимодействие пользователя с краями экрана показывает пользовательский интерфейс системы, такой как панели приложений, чудо и выполняющиеся приложения.</span><span class="sxs-lookup"><span data-stu-id="58a67-108">In Windows 8, user interactions with the edges of the screen display system UI such as app bars, charms, and running apps.</span></span>

<span data-ttu-id="58a67-109">Для полноэкранных удаленных приложений это поведение пользовательского интерфейса на локальном компьютере может переопределяться и влиять на пользовательский интерфейс удаленного сеанса.</span><span class="sxs-lookup"><span data-stu-id="58a67-109">For full-screen, remote applications, this UI behavior on the local machine might override and interfere with the UI of the remote session.</span></span> <span data-ttu-id="58a67-110">Это свойство позволяет приложению отключить ребро пользовательского интерфейса на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="58a67-110">This property enables an application to disable the edge UI on the local machine.</span></span>

<span data-ttu-id="58a67-111">Чтобы отключить интерфейс ребра, присвойте этому свойству значение \_ true.</span><span class="sxs-lookup"><span data-stu-id="58a67-111">To disable edge UI, set this property to VARIANT\_TRUE.</span></span> <span data-ttu-id="58a67-112">Значение по умолчанию — VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="58a67-112">The default value is VARIANT\_FALSE.</span></span>

<span data-ttu-id="58a67-113">Это свойство не влияет на приложения Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="58a67-113">This property has no effect on Windows Store apps.</span></span>

<span data-ttu-id="58a67-114">В следующем примере показано, как задать пограничные поведения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58a67-114">The following example shows how to set edge UI behaviors.</span></span>


```
HRESULT SetTouchDisableProperty(HWND hwnd, BOOL fDisableTouch)
{
    IPropertyStore* pPropStore;
    HRESULT hrReturnValue = SHGetPropertyStoreForWindow(hwnd, IID_PPV_ARGS(&pPropStore));
    if (SUCCEEDED(hrReturnValue))
    {
        PROPVARIANT var;
        var.vt = VT_BOOL;
        var.boolVal = fDisableTouch ? VARIANT_TRUE : VARIANT_FALSE;
        hrReturnValue = pPropStore->SetValue(PKEY_EdgeGesture_DisableTouchWhenFullscreen, var);
        pPropStore->Release();
    }
    return hrReturnValue;
}
```



## <a name="related-topics"></a><span data-ttu-id="58a67-115">См. также</span><span class="sxs-lookup"><span data-stu-id="58a67-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58a67-116">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="58a67-116">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="58a67-117">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="58a67-117">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="58a67-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="58a67-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
