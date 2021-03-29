---
description: Создает контекст устройства (DC) для указанной поверхности.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Функция Нтгдидджетдк (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141487"
---
# <a name="ntgdiddgetdc-function"></a>Функция Нтгдидджетдк

\[Эта функция может быть изменена при каждой редакции операционной системы. Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]

Создает контекст устройства (DC) для указанной поверхности.

## <a name="syntax"></a>Синтаксис


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсурфаце* \[ окне\]
</dt> <dd>

Обработчик для поверхности DirectDraw в режиме ядра, который ранее возвращался [**нтгдиддкреатесурфаце**](-dxgkernel-ntgdiddcreatesurface.md) или [**нтгдиддкреатесурфацеобжект**](-dxgkernel-ntgdiddcreatesurfaceobject.md).

</dd> <dt>

*пуколортабле* \[ окне\]
</dt> <dd>

Указатель на таблицу цветов переопределения для возвращенного контроллера домена.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха эта функция возвращает допустимый **HDC**; в противном случае возвращается **значение NULL**.

## <a name="remarks"></a>Комментарии

В любой момент времени на одну поверхность может быть только один контроллер домена. Последующие вызовы **нтгдидджетдк** будут завершаться ошибкой, пока не будет освобожден предыдущий контроллер домена.

Приложениям рекомендуется вызывать метод [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) , который предоставляет те же функциональные возможности, что и не зависит от операционной системы.

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

[**дджетдк**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
