---
title: Сообщение TTM_GETTOOLINFO (Коммктрл. h)
description: Извлекает сведения о средстве, которые поддерживает элемент управления ToolTip.
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- Элементы управления Windows для TTM_GETTOOLINFO сообщений
topic_type:
- apiref
api_name:
- TTM_GETTOOLINFO
- TTM_GETTOOLINFOA
- TTM_GETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc0de37b97be3bec495c8777b2ddd1cc6fc1bd42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135934"
---
# <a name="ttm_gettoolinfo-message"></a><span data-ttu-id="2a0bb-104">\_Сообщение ТТМ жеттулинфо</span><span class="sxs-lookup"><span data-stu-id="2a0bb-104">TTM\_GETTOOLINFO message</span></span>

<span data-ttu-id="2a0bb-105">Извлекает сведения о средстве, которые поддерживает элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="2a0bb-105">Retrieves the information that a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a0bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a0bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a0bb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a0bb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2a0bb-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2a0bb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2a0bb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a0bb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a0bb-110">Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="2a0bb-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="2a0bb-111">При отправке сообщения элементы **HWND** и **uId** определяют средство, а член **кбсизе** должен задавать размер структуры.</span><span class="sxs-lookup"><span data-stu-id="2a0bb-111">When sending the message, the **hwnd** and **uId** members identify a tool, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="2a0bb-112">При использовании этого сообщения для получения текста подсказки убедитесь, что элемент **лпсзтекст** структуры **тулинфо** указывает на допустимый буфер адкуате размера.</span><span class="sxs-lookup"><span data-stu-id="2a0bb-112">When using this message to retrieve the tooltip text, ensure that the **lpszText** member of the **TOOLINFO** structure points to a valid buffer of adquate size</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a0bb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a0bb-113">Return value</span></span>

<span data-ttu-id="2a0bb-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2a0bb-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a0bb-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a0bb-115">Remarks</span></span>

<span data-ttu-id="2a0bb-116">Если элемент управления ToolTip включает средство, структура [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) получает сведения о средстве.</span><span class="sxs-lookup"><span data-stu-id="2a0bb-116">If the tooltip control includes the tool, the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure receives information about the tool.</span></span>

## <a name="examples"></a><span data-ttu-id="2a0bb-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="2a0bb-117">Examples</span></span>

<span data-ttu-id="2a0bb-118">В следующем примере перемещается элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="2a0bb-118">The following example repositions a tooltip control.</span></span>


```C++
HRESULT MyToolTipClass::OffsetTooltip(int xOffset, int yOffset)  
{  
    HRESULT hr = S_OK;   
    DWORD   dwError = 0;  
  
    if (NULL != m_hWndToolTip)  
    {  
        TOOLINFO ti = {0};  
  
        ti.cbSize = sizeof(TOOLINFO);  
        ti.hwnd   = m_hWndToolTipOwner;  
  
        // Get the current tooltip definition.          
        if( SendMessage(m_hWndToolTip, TTM_GETTOOLINFO, 0, (LPARAM)&ti))  
        {  
            // Offset the tooltip rectangle as specified.              
            OffsetRect(&ti.rect, xOffset, yOffset);  
  
            // Apply the new rectangle to the tooltip.
            SendMessage(m_hWndToolTip, TTM_NEWTOOLRECT, 0, (LPARAM)&ti);  
        }  
        else  
        {  
            dwError = GetLastError();  
            hr = HRESULT_FROM_WIN32(dwError);  
            MyErrorHandler(hr);
       }  
    }  
    return hr;  
}  
```



## <a name="requirements"></a><span data-ttu-id="2a0bb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2a0bb-119">Requirements</span></span>



| <span data-ttu-id="2a0bb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2a0bb-120">Requirement</span></span> | <span data-ttu-id="2a0bb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2a0bb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0bb-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a0bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2a0bb-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a0bb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a0bb-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a0bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2a0bb-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a0bb-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a0bb-126">Header</span><span class="sxs-lookup"><span data-stu-id="2a0bb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a0bb-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a0bb-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2a0bb-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="2a0bb-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2a0bb-129">**ТТМ \_ ЖЕТТУЛИНФОВ** (Юникод) и **ТТМ \_ жеттулинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2a0bb-129">**TTM\_GETTOOLINFOW** (Unicode) and **TTM\_GETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





