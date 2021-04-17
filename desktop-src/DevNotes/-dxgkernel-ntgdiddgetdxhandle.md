---
description: Возвращает маркер API Microsoft DirectX в режиме ядра для использования при последующих вызовах точек входа в режиме ядра, управляющих механизмом API DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Функция Нтгдидджетдксхандле (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655851"
---
# <a name="ntgdiddgetdxhandle-function"></a>Функция Нтгдидджетдксхандле

\[Эта функция может быть изменена при каждой редакции операционной системы. Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]

Возвращает маркер API Microsoft DirectX в режиме ядра для использования при последующих вызовах точек входа в режиме ядра, управляющих механизмом API DirectX.

## <a name="syntax"></a>Синтаксис


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдиректдрав* \[ окне\]
</dt> <dd>

Обработчик объекта DirectDraw, который владеет поверхностью. Этот параметр является необязательным и может иметь значение **null**.

</dd> <dt>

*хсурфаце* \[ окне\]
</dt> <dd>

Обработчик, для которого возвращается маркер API DirectX в режиме ядра. Этот параметр является необязательным и может иметь значение **null**.

</dd> <dt>

*брелеасе* \[ окне\]
</dt> <dd>

Задайте значение **true** , если необходимо освободить интерфейс режима ядра API DirectX. В противном случае — **значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Обработчик DirectX API, используемый в последующих точках входа ядра, ориентированных на API DirectX.

## <a name="remarks"></a>Комментарии

Если указаны оба *хдиректдрав* и *хсурфаце* , *хсурфаце* игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Нтгди. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поддержка клиентов низкого уровня графики](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




