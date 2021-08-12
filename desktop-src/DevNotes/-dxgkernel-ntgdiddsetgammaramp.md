---
description: Задает гамму-шкалу для устройства.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: Функция Нтгдиддсетгаммарамп (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 78e68a76fed6db78a2f3d247c5bec1b73f3df3b6fe204e0d09b1bc5f14a014b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668813"
---
# <a name="ntgdiddsetgammaramp-function"></a>Функция Нтгдиддсетгаммарамп

\[Эта функция может быть изменена при каждой редакции операционной системы. Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]

Задает гамму-шкалу для устройства.

## <a name="syntax"></a>Синтаксис


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдиректдрав* \[ окне\]
</dt> <dd>

Обработчик объекта драйвера режима ядра, для которого задается пандус.

</dd> <dt>

*HDC* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*лпгаммарамп* \[ окне\]
</dt> <dd>

Указатель на массив структур **ддгаммарамп** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение **true** . В противном случае он имеет **значение NULL**.

## <a name="remarks"></a>Remarks

Рекомендуется, чтобы приложения использовали методы **идиректдравгаммаконтрол:: сетгаммарамп** или [**IDirect3DDevice9:: сетгаммарамп**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) , так как эти методы предлагают те же функциональные возможности, которые не зависят от операционной системы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Нтгди. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поддержка клиентов низкого уровня графики](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
