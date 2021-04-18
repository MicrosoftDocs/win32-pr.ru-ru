---
description: Повторно включает объект устройства режима ядра Microsoft DirectDraw после переключения режима.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Функция Нтгдиддринабледиректдравобжект (Нтгди. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142202"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a>Функция Нтгдиддринабледиректдравобжект

\[Эта функция может быть изменена при каждой редакции операционной системы. Вместо этого используйте DirectDraw и Microsoft Direct3DAPIs; Эти API разделяют приложения от таких изменений операционной системы и скрывают множество других трудностей, связанных с взаимодействием с драйверами экрана.\]

Повторно включает объект устройства режима ядра Microsoft DirectDraw после переключения режима.

## <a name="syntax"></a>Синтаксис


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдиректдравлокал* \[ окне\]
</dt> <dd>

Объект DirectDraw, который необходимо включить заново.

</dd> <dt>

*пубневмоде* \[ в, out\]
</dt> <dd>

Указатель на логическое значение, которое будет заполнено значением, которое указывает, изменился ли режим экрана.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха (устройство может быть повторно включено) Эта функция возвращает **значение true**. В противном случае (например, драйвер экрана был изменен), он возвращает **значение false**.

## <a name="remarks"></a>Комментарии

После повторного включения объекта можно повторно запросить возможности устройства с помощью вызова [**нтгдиддкуеридиректдравобжект**](-dxgkernel-ntgdiddquerydirectdrawobject.md).

В приложениях рекомендуется использовать API DirectDraw или [Direct3D](../direct3d10/d3d10-graphics-reference.md) версии 8, который автоматизирует и абстрагирует этот процесс независимо от операционной системы.

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

[**ддринабледиректдравобжект**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
