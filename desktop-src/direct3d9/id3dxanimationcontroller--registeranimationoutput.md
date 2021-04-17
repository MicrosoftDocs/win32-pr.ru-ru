---
description: Добавляет выходные данные анимации в контроллер анимации и регистрирует указатели для преобразований масштабирования, вращения и преобразования (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'Метод ID3DXAnimationController:: Регистераниматионаутпут (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670f8b311532d096b9957ebbefcf1f6fb15d952
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703923"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a>Метод ID3DXAnimationController:: Регистераниматионаутпут

Добавляет выходные данные анимации в контроллер анимации и регистрирует указатели для преобразований масштабирования, вращения и преобразования (SRT).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Имя выходных данных анимации.

</dd> <dt>

*пматрикс* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , содержащую данные преобразования SRT. Может иметь **значение NULL**.

</dd> <dt>

*пскале* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , описывающий масштаб набора анимации. Может иметь **значение NULL**.

</dd> <dt>

 \[ окне\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Указатель на кватернион [**D3DXQUATERNION**](d3dxquaternion.md) , описывающий поворот набора анимации. Может иметь **значение NULL**.

</dd> <dt>

*птранслатион* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , описывающий перевод набора анимации. Может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Если выходные данные анимации уже зарегистрированы, Пматрикс будет заполнен данными преобразования входных данных.

Наборы анимации, созданные с помощью [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) , автоматически регистрируют все загруженные наборы анимации.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
