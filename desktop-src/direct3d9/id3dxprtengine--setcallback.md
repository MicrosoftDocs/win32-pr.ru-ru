---
description: Задает указатель на необязательную функцию обратного вызова, которая вычисляет процент завершенных расчетов между сферами (SH) и дает вызывающему объекту возможность прервать симулятор.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'Метод ID3DXPRTEngine:: Сеткаллбакк (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1ed2570c45380ce4faa0be42ddb9231d6420940dd9a6d669d6f2540154dc644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847363"
---
# <a name="id3dxprtenginesetcallback-method"></a>Метод ID3DXPRTEngine:: Сеткаллбакк

Задает указатель на необязательную функцию обратного вызова, которая вычисляет процент завершенных расчетов между сферами (SH) и дает вызывающему объекту возможность прервать симулятор.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПКБ* \[ окне\]
</dt> <dd>

Тип: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Указатель на функцию обратного вызова [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) , которая вычисляет процент завершенных вычислений sh. Функция обратного вызова должна быть реализована, чтобы вернуть значение S \_ ОК для сохранения запуска симулятора. Любое другое значение приведет к прерыванию симулятора.

</dd> <dt>

*Частота* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Частота вызовов обратного вызова. Обратная частота — приблизительно столько раз, когда будет вызываться функция обратного вызова.

</dd> <dt>

*лпусерконтекст* \[ окне\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Указатель на определяемое пользователем значение, которое передается функции обратного вызова. Обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение — S \_ .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
