---
description: Установка непрерывного диапазона констант шейдера с копированием в памяти.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'Метод ID3DXEffect:: Сетраввалуе (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703699"
---
# <a name="id3dxeffectsetrawvalue-method"></a>Метод ID3DXEffect:: Сетраввалуе

Установка непрерывного диапазона констант шейдера с копированием в памяти.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Обработчик* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Обрабатываемое значение или имя значения, переданного в виде строки. Передача маркера более эффективна. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **void \***

Указатель на буфер, содержащий данные, которые необходимо задать. Сетраввалуе проверяет допустимость памяти, но не выполняет проверку допустимых данных.

</dd> <dt>

*Оффсетинбитес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число байтов между началом данных действия и началом константы результата, которые вы собираетесь задать.

</dd> <dt>

*Байт* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Размер устанавливаемого буфера в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: E \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Сетраввалуе — это очень быстрый способ установки констант эффектов, так как он выполняет копирование в памяти без выполнения проверки или преобразования данных (например, преобразование матрицы строкового типа в основную матрицу столбца). Используйте Сетраввалуе, чтобы задать ряд смежных констант эффектов. Например, можно задать массив из двадцати матриц с 20 вызовами в [**ID3DXBaseEffect:: сетматрикс**](id3dxbaseeffect--setmatrix.md) или с помощью одного сетраввалуе.

Все значения должны быть либо matrix4x4s, либо float4s, а все матрицы должны быть в основном порядке столбцов. Значения int или float приводятся к типу float4; Поэтому настоятельно рекомендуется использовать Сетраввалуе только с данными float4 или matrix4x4.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
