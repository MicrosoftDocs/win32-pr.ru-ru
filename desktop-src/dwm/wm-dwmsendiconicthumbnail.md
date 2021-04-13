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
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492657"
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

## <a name="remarks"></a>Комментарии

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                          |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                             |
| Header<br/>                   | <dl> <dt>Двмапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**двминвалидатеиконикбитмапс**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**WM \_ двмсендиконикливепревиевбитмап**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

