---
title: Перечисление Вмдисплайвидеомоде (Впккоминтерфацес. h)
description: Задает режим видеоизображения.
ms.assetid: 9ffd1bb5-115d-4554-92c6-5dcf86f904a5
keywords:
- Перечисление Вмдисплайвидеомоде Virtual PC
topic_type:
- apiref
api_name:
- VMDisplayVideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cc5ef5a82ab7a8a74f7613cb6a775f1a8c52210ff937108a58a735f5fa8620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056432"
---
# <a name="vmdisplayvideomode-enumeration"></a>Перечисление Вмдисплайвидеомоде

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Задает режим видеоизображения.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmVideoMode_TextMode  = 0,
  vmVideoMode_CGAMode   = 1,
  vmVideoMode_VGAMode   = 2,
  vmVideoMode_SVGAMode  = 3
} VMDisplayVideoMode;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**Вмвидеомоденый \_ TextMode**
</dt> <dd>

Текстовый режим.

</dd> <dt>

<span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**Вмвидеомоде \_ кгамоде**
</dt> <dd>

Режим КГА.

</dd> <dt>

<span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**Вмвидеомоде \_ вгамоде**
</dt> <dd>

Режим VGA.

</dd> <dt>

<span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**Вмвидеомоде \_ свгамоде**
</dt> <dd>

Режим SVGA.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Ивмдисплай:: Видеомоде**](ivmdisplay-videomode.md)
</dt> </dl>

 

