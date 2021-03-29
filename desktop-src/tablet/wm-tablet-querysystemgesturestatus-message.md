---
description: Посылается, когда система запрашивает окно, какие системные жесты хотели бы получить.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: Сообщение WM_TABLET_QUERYSYSTEMGESTURESTATUS (Тпкшрд. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897253"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a><span data-ttu-id="eae88-103">\_Сообщение WM планшет \_ куерисистемжестурестатус</span><span class="sxs-lookup"><span data-stu-id="eae88-103">WM\_TABLET\_QUERYSYSTEMGESTURESTATUS message</span></span>

<span data-ttu-id="eae88-104">Посылается, когда система запрашивает окно, какие системные жесты хотели бы получить.</span><span class="sxs-lookup"><span data-stu-id="eae88-104">Sent when the system asks a window which system gestures it would like to receive.</span></span>


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a><span data-ttu-id="eae88-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="eae88-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eae88-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eae88-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eae88-107">Не используется.</span><span class="sxs-lookup"><span data-stu-id="eae88-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="eae88-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eae88-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eae88-109">Значение точки, представляющее экранные координаты.</span><span class="sxs-lookup"><span data-stu-id="eae88-109">A point value that represents the screen coordinates.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eae88-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eae88-110">Remarks</span></span>

<span data-ttu-id="eae88-111">Обрабатывая это сообщение, можно динамически отключить жесты для областей окна.</span><span class="sxs-lookup"><span data-stu-id="eae88-111">By handling this message, you can dynamically disable flicks for regions of a window.</span></span>

> [!Note]  
> <span data-ttu-id="eae88-112">*LParam* можно преобразовать в координаты x и y с помощью `GET_X_LPARAM` `GET_Y_LPARAM` макросов и.</span><span class="sxs-lookup"><span data-stu-id="eae88-112">The *lParam* can be converted to x-coordinates and y-coordinates by using the `GET_X_LPARAM` and `GET_Y_LPARAM` macros.</span></span>

 

<span data-ttu-id="eae88-113">По умолчанию окно будет принимать все события системных жестов.</span><span class="sxs-lookup"><span data-stu-id="eae88-113">By default, your window will receive all system gesture events.</span></span> <span data-ttu-id="eae88-114">Вы можете выбрать события, которые должны быть получены в окне, и какие события вы хотите отключить, отменив ответ на **сообщение \_ \_ куерисистемжестурестатус WM планшета** в **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="eae88-114">You can choose which events you would like your window to receive and which events you would like disabled by responding to the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message in your **WndProc**.</span></span> <span data-ttu-id="eae88-115">Сообщение **WM \_ планшет \_ куерисистемжестурестатус** определено в тпкшрд. h.</span><span class="sxs-lookup"><span data-stu-id="eae88-115">The **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message is defined in tpcshrd.h.</span></span> <span data-ttu-id="eae88-116">Значения для включения и отключения системных жестов планшета также определяются в тпкшрд. h следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eae88-116">The values to enable and disable system tablet system gestures are also defined in tpcshrd.h as follows:</span></span>

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> <span data-ttu-id="eae88-117">Отключение нажатия и удерживания повысит скорость реагирования щелчков мыши, так как эта функция создает время ожидания для различения двух операций.</span><span class="sxs-lookup"><span data-stu-id="eae88-117">Disabling press and hold will improve responsiveness for mouse clicks because this functionality creates a wait time to distinguish between the two operations.</span></span>

 

<span data-ttu-id="eae88-118">Будьте внимательны при обработке сообщения **WM \_ планшета \_ куерисистемжестурестатус** .</span><span class="sxs-lookup"><span data-stu-id="eae88-118">Use caution when handling the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message.</span></span> <span data-ttu-id="eae88-119">**WM \_ Планшет \_ куерисистемжестурестатус** передается с помощью функции [**функции sendmessagetimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="eae88-119">**WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** is passed using the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="eae88-120">При вызове методов для COM-интерфейса этот объект должен находиться в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="eae88-120">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="eae88-121">В противном случае COM создает исключение.</span><span class="sxs-lookup"><span data-stu-id="eae88-121">If not, COM throws an exception.</span></span>

## <a name="examples"></a><span data-ttu-id="eae88-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="eae88-122">Examples</span></span>

<span data-ttu-id="eae88-123">В следующем примере показано, как отключить жесты для региона с помощью WM \_ планшета \_ куерисистемжестурестатус.</span><span class="sxs-lookup"><span data-stu-id="eae88-123">The following example shows how to disable flicks for a region using WM\_TABLET\_QUERYSYSTEMGESTURESTATUS.</span></span>


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



<span data-ttu-id="eae88-124">В следующем примере показано, как отключить различные функции жестов для всего окна.</span><span class="sxs-lookup"><span data-stu-id="eae88-124">The following example shows how to disable various flicks features for an entire window.</span></span>


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a><span data-ttu-id="eae88-125">Требования</span><span class="sxs-lookup"><span data-stu-id="eae88-125">Requirements</span></span>



| <span data-ttu-id="eae88-126">Требование</span><span class="sxs-lookup"><span data-stu-id="eae88-126">Requirement</span></span> | <span data-ttu-id="eae88-127">Значение</span><span class="sxs-lookup"><span data-stu-id="eae88-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eae88-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eae88-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eae88-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eae88-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="eae88-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eae88-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eae88-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eae88-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="eae88-132">Header</span><span class="sxs-lookup"><span data-stu-id="eae88-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="eae88-133"><dt>Тпкшрд. h</dt></span><span class="sxs-lookup"><span data-stu-id="eae88-133"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
