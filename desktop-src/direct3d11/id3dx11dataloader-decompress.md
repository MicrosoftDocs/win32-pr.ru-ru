---
title: Метод распаковки ID3DX11DataLoader (D3DX11core. h)
description: обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows. Распаковывает закодированные данные.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Метод распаковки Direct3D 11
- Распаковка метода Direct3D 11, интерфейс ID3DX11DataLoader
- Интерфейс ID3DX11DataLoader Direct3D 11, метод unуплотнения
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4f2424d46748b33918c8b6870c07dbaf4486217f8f3ba7a0a64f881792b81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633034"
---
# <a name="id3dx11dataloaderdecompress-method"></a>ID3DX11DataLoader: метод:D екомпресс

> [!Note]  
> библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.

 

Распаковывает закодированные данные.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдата* \[ заполняет\]
</dt> <dd>

Тип: **void \* \***

Указатель на необработанные данные для распаковки.

</dd> <dt>

*пкбитес* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)\***

Размер данных, на которые указывает Ппдата.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Используйте этот метод для загрузки ресурсов из файловых систем, таких как ZIP-файлы. При загрузке из несжатого ресурса стадия распаковки не должна выполнять никаких действий.

[**Интерфейс ID3DX11DataLoader**](id3dx11dataloader.md) может быть унаследован и его члены переопределяются для поддержки пользовательских форматов файлов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

