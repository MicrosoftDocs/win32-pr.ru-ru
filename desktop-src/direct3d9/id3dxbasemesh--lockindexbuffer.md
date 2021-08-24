---
description: Блокирует буфер индексов и получает указатель на буфер памяти буфера индекса.
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: 'Метод ID3DXBaseMesh:: Локкиндексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2eab2806775572cb4e4c4a50899d48263c6ddf0d55138c37bcaff8367225c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118824"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a>Метод ID3DXBaseMesh:: Локкиндексбуффер

Блокирует буфер индексов и получает указатель на буфер памяти буфера индекса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание флагов блокировки (ноль или более), описывающих тип выполняемой блокировки. Для этого метода допустимы следующие флаги:

-   D3DLOCK \_ отбросить
-   D3DLOCK \_ без \_ "грязного" \_ обновления
-   D3DLOCK \_ носислокк
-   D3DLOCK \_ ReadOnly

Описание флагов см. в разделе [D3DLOCK](d3dlock.md).

</dd> <dt>

*ппдата* \[ out, retval\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)\***

Указатель типа VOID \* на буфер, содержащий данные индекса. Число индексов в этом буфере будет равно [**ID3DXBaseMesh:: жетнумфацес**](id3dxbasemesh--getnumfaces.md) \* 3.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

При работе с буферами индексов вы можете выполнять несколько вызовов блокировок. Однако необходимо убедиться, что количество вызовов блокировок соответствует числу вызовов Unlock. Вызовы Дравпримитиве не будут выполнены с необработанными счетчиками блокировок в любом буфере установленного индекса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
