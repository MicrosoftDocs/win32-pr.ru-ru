---
title: Метод обработки ID3DX11DataProcessor (D3DX11core. h)
description: обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. Обрабатывает данные.
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- Метод обработки Direct3D 11
- Метод Process Direct3D 11, интерфейс ID3DX11DataProcessor
- Интерфейс ID3DX11DataProcessor Direct3D 11, метод Process
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Process
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 458e7dc68c4a64099dc5cab327901fda38f8fd4e6cde4ca7d62e3def5472d86d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894924"
---
# <a name="id3dx11dataprocessorprocess-method"></a>ID3DX11DataProcessor: метод:P шаблоны

> [!Note]  
> библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.

 

Обрабатывает данные.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **void \***

Указатель на данные для обработки.

</dd> <dt>

*кбитес* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

Размер данных для обработки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Этот метод используется [**интерфейсом ID3DX11ThreadPump**](id3dx11threadpump.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

