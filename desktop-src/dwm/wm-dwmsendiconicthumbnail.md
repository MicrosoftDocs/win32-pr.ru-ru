---
title: Сообщение WM_DWMSENDICONICTHUMBNAIL (Двмапи. h)
description: Указывает окну указать статический точечный рисунок для использования в качестве эскиза этого окна.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- Сообщение WM_DWMSENDICONICTHUMBNAIL диспетчер окон рабочего стола
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3263f34cd59ba68ee895e5d5c77e297144cbadd6c8d8bbaa49ca6272248c2024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842654"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a>\_Сообщение ДВМСЕНДИКОНИКСУМБНАИЛ WM

Указывает окну указать статический точечный рисунок для использования в качестве эскиза этого окна.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) этого значения — это максимальная координата x эскиза. [**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это максимальная координата по оси y. Если размер эскиза превышает одно или оба этих значения, DWM не принимает эскиз.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

DWM отправляет это сообщение в окно, если выполняются все перечисленные ниже ситуации.

-   DWM отображает значок окна.
-   В окне задан атрибут [**\_ \_ \_ Bitmap двмва**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) .
-   Окно не установило кэшированный точечный рисунок.
-   Существует место в кэше для другого точечного рисунка.

Окно, которое получает это сообщение, должно ответить путем создания точечного рисунка, размер которого не превышает размера, запрошенного в параметрах сообщения. Затем окно вызывает функцию [**двмсетикониксумбнаил**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) для переопределения эскиза по умолчанию. Если окно не предоставляет точечный рисунок в течение заданного промежутка времени, DWM использует собственный значок по умолчанию для окна.

Окно должно принадлежать вызывающему процессу.

## <a name="examples"></a>Примеры

В следующем примере кода показано, как реагировать на сообщение **WM \_ двмсендикониксумбнаил** . В примере вызывается [**двмсетикониксумбнаил**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail)с маркером для настраиваемого аппаратно-независимого точечного рисунка, используемого в качестве представления Windows.


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



Полный пример см. в разделе [Настройка эскиза значка и пример динамического предварительного просмотра растрового изображения](dwm-sample-customizethumbnail.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>Двмапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**двминвалидатеиконикбитмапс**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**WM \_ двмсендиконикливепревиевбитмап**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

