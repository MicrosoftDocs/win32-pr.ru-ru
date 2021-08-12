---
description: Уведомляет DWM о входящем обновлении к общей поверхности окна.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: Функция Двмдксупдатевиндовшаредсурфаце
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 9eac390cd6ccf79ed3f916f4c9605b938ab9fd338df3643301d7f5e5c900c0d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280124"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a>Функция Двмдксупдатевиндовшаредсурфаце

Уведомляет DWM о входящем обновлении к общей поверхности окна.

## <a name="syntax"></a>Синтаксис

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a>Параметры

`hwnd`

[**HWND**](/windows/desktop/winprog/windows-data-types) , указывающий обновляемое окно.

`uiUpdateId`

ИДЕНТИФИКАТОР обновления, полученный из [**двмдксжетвиндовшаредсурфаце**](dwmdxgetwindowsharedsurface.md).

`dwFlags`

Зарезервировано.

`hmonitorAssociation`

Зарезервировано.

`prc`

Rect обновляемого окна в пространстве координат окна. Прямоугольник со значением NULL указывает, что регион не обновлялся.

## <a name="return-value"></a>Возвращаемое значение

**С \_ ОК** в случае успеха, в противном случае — значение **HRESULT.**

## <a name="remarks"></a>Remarks

Этот API предназначен для реализации графического драйвера или среды выполнения. Приложение не может вызывать этот метод. эта документация действительна только для Windows 7, и этот API не гарантируется и не работает аналогичным образом в других версиях Windows. Эта функция отсутствует в заголовке или библиотеке статической компоновки, она находится по порядковому номеру 101 в dwmapi.dll.

Этот метод следует вызывать только после того, как [**двмдксжетвиндовшаредсурфаце**](dwmdxgetwindowsharedsurface.md) возвращает " **\_ ОК**", и должен вызываться в этом сценарии независимо от того, обновлена ли поверхность.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Минимальная версия клиента | только Windows 7 \[ настольных приложений\] |
| Минимальная версия сервера | Ни одна версия не поддерживается |
| Окончание поддержки клиента | Windows 7 |
| Заголовок | Н/Д |
| DLL | Dwmapi.dll |
