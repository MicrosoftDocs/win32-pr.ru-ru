---
description: Создает цепочку mipmap с помощью определенного фильтра текстуры.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: Функция D3DX10FilterTexture (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 225caf2c9b08a498e77723dbb7ab43c8fd4850262c1f58f5ae37a3157e953edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497644"
---
# <a name="d3dx10filtertexture-function"></a>Функция D3DX10FilterTexture

Создает цепочку mipmap с помощью определенного фильтра текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстуре* 
</dt> <dd>

Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Объект текстуры для фильтрации. См. [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*срклевел* 
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Уровень mipmap, данные которого используются для создания оставшейся части цепочки mipmap.

</dd> <dt>

*мипфилтер* 
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Флаги, управляющие фильтрацией каждого миплевел (или D3DX10 \_ умолчанию для D3DX10 \_ \_ поле фильтра). См [**. \_ \_ флаг фильтра D3DX10**](d3dx10-filter-flag.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
