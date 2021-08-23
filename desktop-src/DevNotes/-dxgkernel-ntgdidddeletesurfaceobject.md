---
description: Нтгдиддделетесурфацеобжект Удаляет ранее созданный объект поверхности режима ядра.
ms.assetid: 95ce6c73-7e41-4ac3-b849-9b8f53aa3ac3
title: Функция Нтгдиддделетесурфацеобжект (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 73418993e549bc3a72f1f4bc953b4f177a4b413d62f03e0c6e8b0c58b35998e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956533"
---
# <a name="ntgdidddeletesurfaceobject-function"></a>Функция Нтгдиддделетесурфацеобжект

\[Эта функция может быть изменена при каждой редакции операционной системы. Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]

**Нтгдиддделетесурфацеобжект** Удаляет ранее созданный объект поверхности режима ядра.

## <a name="syntax"></a>Синтаксис


```C++
BOOL APIENTRY NtGdiDdDeleteSurfaceObject(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсурфаце* \[ окне\]
</dt> <dd>

Обработчик для ранее созданного объекта поверхности режима ядра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха эта функция возвращает **значение true**. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

В приложениях рекомендуется использовать интерфейсы API DirectDraw и [Direct3D](../direct3d10/d3d10-graphics-reference.md) для создания объектов графических устройств и управления ими. Эти конструкции являются абстрактным процессом создания устройств в упрощенном и независимом от операционной системе виде.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Нтгди. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поддержка клиентов низкого уровня графики](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**ддделетесурфацеобжект**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletesurfaceobject)
</dt> <dt>

[**нтгдиддкреатесурфацеобжект**](-dxgkernel-ntgdiddcreatesurfaceobject.md)
</dt> </dl>

 

 
