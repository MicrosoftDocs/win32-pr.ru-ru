---
description: Освобождает ранее созданный контекст устройства (DC) для указанного объекта поверхности Microsoft DirectDraw в режиме ядра.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: Функция Нтгдиддрелеаседк (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: daa4cad2f6f3937ebe29b3996ebbaa72b894ee743f97222cb1f6e2ff61f7dbb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824914"
---
# <a name="ntgdiddreleasedc-function"></a>Функция Нтгдиддрелеаседк

\[Эта функция может быть изменена при каждой редакции операционной системы. Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]

Освобождает ранее созданный контекст устройства (DC) для указанного объекта поверхности Microsoft DirectDraw в режиме ядра.

## <a name="syntax"></a>Синтаксис


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсурфаце* \[ окне\]
</dt> <dd>

Обработчик для ранее созданного объекта поверхности DirectDraw режима ядра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха эта функция возвращает **значение true**. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

Приложения, которым требуется получить контроллер домена для поверхности DirectDraw, могут использовать [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), который предоставляет эту функциональность независимо от операционной системы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Нтгди. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Поддержка клиентов низкого уровня графики](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**ддрелеаседк**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
