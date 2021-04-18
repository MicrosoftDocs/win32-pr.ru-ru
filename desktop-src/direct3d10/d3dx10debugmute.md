---
description: Включение или отключение сообщений отладки.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: Функция D3DX10DebugMute (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f331e3f074a4b77a1f1a7f1a8117cf660940f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713861"
---
# <a name="d3dx10debugmute-function"></a>Функция D3DX10DebugMute

Включение или отключение сообщений отладки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Отключить звук* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Задайте значение **true** , чтобы включить сообщения отладки. Задайте значение **false** , чтобы отключить сообщения отладки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Комментарии

Эта функция используется для отключения сообщений об ошибках для API-интерфейсов D3DX10 во время отладки. Использование этой функции должно быть защищено \_ параметром компилятора debug D3D10.


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



Состояние по умолчанию — **true** для отладочной сборки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
