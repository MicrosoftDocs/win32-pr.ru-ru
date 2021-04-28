---
description: 'Метод ID3DXCompressedAnimationSet:: Жеткаллбакккэйс — заполняет массив данными ключа обратного вызова, используемыми для анимации ключевых кадров.'
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: 'Метод ID3DXCompressedAnimationSet:: Жеткаллбакккэйс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d7c430358b5ba7f66c5a79b08ae01925141e659f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115332"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a>Метод ID3DXCompressedAnimationSet:: Жеткаллбакккэйс

Заполняет массив данными ключа обратного вызова, используемым для анимации ключевых кадров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкаллбакккэйс* \[ заполняет\]
</dt> <dd>

Тип: **[ **\_ обратный вызов LPD3DXKEY**](d3dxkey-callback.md)**

Указатель на выделенный пользователем массив структур [**\_ обратного вызова D3DXKEY**](d3dxkey-callback.md) , который метод должен заполнить данными обратного вызова.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet:: Жетнумкаллбакккэйс**](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




