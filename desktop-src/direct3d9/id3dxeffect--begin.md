---
description: Запускает активный метод.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'Метод ID3DXEffect:: Begin (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f4e41830b0bb4507e3969c327c84a85c5336e5f07389fa12e05f3a92f4089a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675464"
---
# <a name="id3dxeffectbegin-method"></a>Метод ID3DXEffect:: Begin

Запускает активный метод.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппассес* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на возвращаемое значение, указывающее количество проходов, необходимых для отрисовки текущего метода.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Параметр DWORD, определяющий сохранение и восстановление состояния, измененного в результате действия. Значение по умолчанию 0 указывает, что **ID3DXEffect:: Begin** и [**ID3DXEffect:: end**](id3dxeffect--end.md) сохранит и восстановит все состояния, измененные этим действием (включая константы в пикселях и шейдере вершин). Допустимые флаги можно увидеть на странице [Флаги сохранения и восстановления состояния влияния](d3dxfx.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

Приложение устанавливает один активный метод в системе эффектов, вызывая **ID3DXEffect:: Begin**. Система влияния отвечает, записывая все состояния конвейера, которые могут быть изменены методом в блоке состояния. Приложение сигнализирует об окончании приемки, вызвав [**ID3DXEffect:: end**](id3dxeffect--end.md), который использует блок состояния для восстановления исходного состояния. Таким образом, система эффектов выполняет сохранение состояния, когда прием становится активным, и восстанавливает состояние при завершении метода. Если вы решили отключить эту функцию сохранения и восстановления, см. раздел [D3DXFX \_ донотсавесамплерстате](d3dxfx.md).

В паре **ID3DXEffect:: Begin** и [**ID3DXEffect:: end**](id3dxeffect--end.md) приложение использует [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) для установки активного прохода, [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) , если после активации прохода возникли какие либо изменения состояния, и [**ID3DXEffect:: ендпасс**](id3dxeffect--endpass.md) , чтобы завершить активный проход.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
