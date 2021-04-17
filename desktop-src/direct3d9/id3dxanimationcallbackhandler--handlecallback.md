---
description: 'Приложение реализует этот метод. Этот метод вызывается при возникновении обратного вызова для набора анимации в одной из дорожек во время вызова ID3DXAnimationController:: AdvanceTime.'
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'Метод ID3DXAnimationCallbackHandler:: Хандлекаллбакк (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49de0adef71435dbcf35afae8cfa555999826a34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694296"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a>Метод ID3DXAnimationCallbackHandler:: Хандлекаллбакк

Приложение реализует этот метод. Этот метод вызывается при возникновении обратного вызова для набора анимации в одной из дорожек во время вызова [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Track* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор записи, в которой происходит обратный вызов.

</dd> <dt>

*пкаллбаккдата* \[ окне\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Указатель на данные обратного вызова, принадлежащие пользователю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемые значения этого метода реализуются программистом приложения. Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК. В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке из [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationCallbackHandler](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
