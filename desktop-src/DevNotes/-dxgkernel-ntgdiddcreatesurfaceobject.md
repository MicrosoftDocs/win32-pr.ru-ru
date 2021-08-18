---
description: Создает объект поверхности режима ядра, представляющий объект поверхности пользовательского режима, на который ссылается Пусурфацелокал.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Функция Нтгдиддкреатесурфацеобжект (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7dac10cb5f648cc7281d95bcd83be9983a63abd76208f6f745e1bd6c5ec00b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956543"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a>Функция Нтгдиддкреатесурфацеобжект

\[Эта функция может быть изменена при каждой редакции операционной системы. Вместо этого используйте Microsoft DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]

Создает объект поверхности режима ядра, представляющий объект поверхности пользовательского режима, на который ссылается *пусурфацелокал*.

## <a name="syntax"></a>Синтаксис


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдиректдравлокал* \[ окне\]
</dt> <dd>

Обработчик для объекта DirectDraw режима ядра.

</dd> <dt>

*хсурфаце* \[ окне\]
</dt> <dd>

Предыдущий маркер на той же поверхности. Используется при повторном создании поверхности после переключения режима.

</dd> <dt>

*пусурфацелокал* \[ окне\]
</dt> <dd>

Указатель на [**\_ \_ локальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) , представляющую объект поверхности пользовательского режима DirectDraw, с которым необходимо связать выделенную память. Дополнительные сведения см. в документации по DDK.

</dd> <dt>

*пусурфацеморе* \[ окне\]
</dt> <dd>

Указатель на [**область DD \_ \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) , который содержит дополнительные локальные данные для каждого отдельного объекта Surface. Дополнительные сведения см. в документации по DDK.

</dd> <dt>

*пусурфацеглобал* \[ окне\]
</dt> <dd>

Указатель на [**\_ \_ глобальную структуру области DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) , которая содержит данные поверхности, совместно используемые глобально с несколькими поверхностями. Дополнительные сведения см. в документации по DDK.

</dd> <dt>

*бкомплете* \[ окне\]
</dt> <dd>

Флаг завершения объектов в режиме ядра. Может принимать одно из следующих значений.

<dt>



 УСЛОВИЯ


</dt> <dd>

Завершите всю обработку, касающуюся представления режима ядра.

</dd> <dt>



 ISFALSE


</dt> <dd>

Создайте объект, но не настраиваете внутренние данные, такие как указатель памяти. Объекты, созданные с помощью **false** , могут быть присоединены с помощью [**нтгдиддаттачсурфаце**](-dxgkernel-ntgdiddattachsurface.md) и завершаются вызовом [**нтгдиддкреатесурфаце**](-dxgkernel-ntgdiddcreatesurface.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха эта функция возвращает маркер в представление поверхности режима ядра; в противном случае возвращается **значение NULL**.

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

[**ддкреатесурфацеобжект**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[**нтгдиддделетесурфацеобжект**](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[**нтгдиддаттачсурфаце**](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[**нтгдиддкреатесурфаце**](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
