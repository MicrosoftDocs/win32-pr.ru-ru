---
title: Сообщение TTM_GETTOOLINFO (Коммктрл. h)
description: Извлекает сведения о средстве, которые поддерживает элемент управления ToolTip.
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- элементы управления Windows сообщений TTM_GETTOOLINFO
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
ms.openlocfilehash: 77f19243603ab5d2ba62d498a5595528e39b33658c7a8e4aa0638888806684ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166377"
---
# <a name="ttm_gettoolinfo-message"></a>\_Сообщение ТТМ жеттулинфо

Извлекает сведения о средстве, которые поддерживает элемент управления ToolTip.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . При отправке сообщения элементы **HWND** и **uId** определяют средство, а член **кбсизе** должен задавать размер структуры. При использовании этого сообщения для получения текста подсказки убедитесь, что элемент **лпсзтекст** структуры **тулинфо** указывает на допустимый буфер адкуате размера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Remarks

Если элемент управления ToolTip включает средство, структура [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) получает сведения о средстве.

## <a name="examples"></a>Примеры

В следующем примере перемещается элемент управления ToolTip.


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТТМ \_ ЖЕТТУЛИНФОВ** (Юникод) и **ТТМ \_ жеттулинфоа** (ANSI)<br/>           |



 

 





