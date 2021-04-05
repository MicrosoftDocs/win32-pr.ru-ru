---
description: Оптимизирует сетку исправлений для эффективной тесселяции.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'Метод ID3DXPatchMesh:: optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000526"
---
# <a name="id3dxpatchmeshoptimize-method"></a>Метод ID3DXPatchMesh:: OPTIMIZE

Оптимизирует сетку исправлений для эффективной тесселяции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

В настоящее время не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ каннотаттрсорт.

## <a name="remarks"></a>Комментарии

После того как приложение создаст сведения о смежности для сетки, данные сетки могут быть оптимизированы (переупорядочены) для повышения производительности рисования. Этот метод определяет, какие исправления являются смежными (в пределах указанного допуска).

Для оптимизации тесселяции также используется соседеская информация. Однократное создание сведений о смежности и формирование мозаики путем вызова [**ID3DXPatchMesh:: тесселяции**](id3dxpatchmesh--tessellate.md). Выполняемая оптимизация не зависит от фактического используемого уровня тесселяции. Однако при изменении вершин сетки необходимо повторно создать сведения о соседических данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh:: Женератеаджаценци**](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
