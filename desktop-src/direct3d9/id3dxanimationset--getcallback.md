---
description: 'Метод ID3DXAnimationSet:: callback — получает сведения о конкретном обратном вызове в наборе анимации.'
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'Метод ID3DXAnimationSet:: callback (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 563c1007cc471ab10a9609e776da69b7c5ed493b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097542"
---
# <a name="id3dxanimationsetgetcallback-method"></a>Метод ID3DXAnimationSet:: callback

Возвращает сведения о конкретном обратном вызове в наборе анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Расположение для поиска обратных вызовов.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Флаги поиска обратного вызова. Этому параметру можно присвоить сочетание из одного или нескольких флагов [**из \_ \_ флагов поиска D3DXCALLBACK**](./d3dxcallback-search-flags.md).

</dd> <dt>

*пкаллбаккпоситион* \[ заполняет\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)\***

Указатель на расположение обратного вызова.

</dd> <dt>

*ппкаллбаккдата* \[ заполняет\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)\***

Адрес указателя данных обратного вызова.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемые значения этого метода реализуются программистом приложения. Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК. В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке из [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
