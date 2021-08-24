---
description: Удаляет все события из указанной записи анимации.
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: 'Метод ID3DXAnimationController:: Ункэйаллтраккевентс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 196f1041d725f8aed39e54626e00b849f2be09587d5ccd40fbc3d8a091fc1b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791114"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a>Метод ID3DXAnimationController:: Ункэйаллтраккевентс

Удаляет все события из указанной записи анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Track* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор записи, по которой должны быть удалены все события.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Этот метод предотвращает выполнение всех событий, ранее запланированных на дорожке, и отклоняет все данные, связанные с этими событиями.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
