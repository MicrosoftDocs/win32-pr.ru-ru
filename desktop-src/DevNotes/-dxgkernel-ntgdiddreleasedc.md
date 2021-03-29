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
ms.openlocfilehash: a7319b423f12d7e4415d78d995bfb1d7cd0341a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895385"
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

## <a name="remarks"></a>Комментарии

Приложения, которым требуется получить контроллер домена для поверхности DirectDraw, могут использовать [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), который предоставляет эту функциональность независимо от операционной системы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Нтгди. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поддержка клиентов низкого уровня графики](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**ддрелеаседк**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
