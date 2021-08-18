---
title: Сообщение WM_DWMSENDICONICLIVEPREVIEWBITMAP (Двмапи. h)
description: Указывает окну указать статический точечный рисунок для использования в качестве динамического предварительного просмотра (также известного как предварительный просмотр) этого окна.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- Сообщение WM_DWMSENDICONICLIVEPREVIEWBITMAP диспетчер окон рабочего стола
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7742b70afad62a42378e50a06a6e40e503bee72309f5f233f9cf8bf62cf41d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985253"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a>\_Сообщение ДВМСЕНДИКОНИКЛИВЕПРЕВИЕВБИТМАП WM

Указывает окну указать статический точечный рисунок для использования в качестве *динамического предварительного просмотра* (также известного как *Предварительный просмотр*) этого окна.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

*Динамический просмотр* (также называемый *предварительным просмотром*) окна появляется, когда пользователь перемещает указатель мыши над эскизом окна на панели задач или передает фокус в окно ALT + TAB. Это представление является полным предварительным просмотром окна и может быть динамическим моментальным снимком или значком.

Диспетчер окон рабочего стола (DWM) отправляет это сообщение в окно, если выполняются все следующие ситуации:

-   В окне был вызван динамический просмотр.
-   В окне задан атрибут [**\_ \_ \_ Bitmap двмва**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) .
-   Для этого окна существует только значок.

Окно, которое получает это сообщение, должно реагировать путем создания полной масштабируемой битовой карты. Затем окно вызывает функцию [**двмсетиконикливепревиевбитмап**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) для задания динамического просмотра. Если окно не устанавливает точечный рисунок в течение заданного промежутка времени, DWM использует собственный значок по умолчанию для окна.

## <a name="examples"></a>Примеры

В следующем примере демонстрируется ответ на сообщение **\_ двмсендиконикливепревиевбитмап WM** . В примере вызывается функция [**двмсетиконикливепревиевбитмап**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) с маркером для настраиваемого, независимого от устройства точечного рисунка, используемого в качестве представления окна.


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



Полный код см. в разделе [Настройка эскиза значка и пример динамического предварительного просмотра растрового изображения](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>Двмапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**WM \_ двмсендикониксумбнаил**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**двминвалидатеиконикбитмапс**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





