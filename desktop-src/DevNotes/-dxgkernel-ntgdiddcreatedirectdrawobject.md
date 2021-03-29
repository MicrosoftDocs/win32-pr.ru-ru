---
description: Создает представление объекта Microsoft DirectDraw на стороне ядра.
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: Функция Нтгдиддкреатедиректдравобжект (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 16dd140c7b205c92b34cb9bd397a4b8d2d3e1a60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140947"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a>Функция Нтгдиддкреатедиректдравобжект

\[Эта функция может быть изменена при каждой редакции операционной системы. Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]

Создает представление объекта Microsoft DirectDraw на стороне ядра.

## <a name="syntax"></a>Синтаксис


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HDC* \[ окне\]
</dt> <dd>

Любое устройство показа контроллеров домена, для которого должен быть создан объект DirectDraw.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха эта функция возвращает маркер в представление объекта режима ядра; в противном случае возвращается **значение NULL**.

## <a name="remarks"></a>Комментарии

В приложениях рекомендуется использовать интерфейсы API DirectDraw и [Direct3D](../direct3d10/d3d10-graphics-reference.md) для создания объектов графических устройств и управления ими. Эти конструкции являются абстрактным процессом создания устройств в упрощенном и независимом от операционной системе виде.

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

[**ддкреатедиректдравобжект**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
