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
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490893"
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

## <a name="remarks"></a>Комментарии

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                          |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                             |
| Header<br/>                   | <dl> <dt>Двмапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**WM \_ двмсендикониксумбнаил**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**двминвалидатеиконикбитмапс**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





