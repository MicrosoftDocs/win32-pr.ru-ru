---
description: Задает свойства выборки, используемые симулятором предварительно вычисленной радианценой пересылки (PRT).
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'Метод ID3DXPRTEngine:: Сетсамплингинфо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ab229652fe9e333519acce7d8474d3c4f0cf7ef9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821189"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a>Метод ID3DXPRTEngine:: Сетсамплингинфо

Задает свойства выборки, используемые симулятором предварительно вычисленной радианценой пересылки (PRT).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Нумрайс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число лучей, которые нужно направить в каждом примере. Должен быть больше нуля.

</dd> <dt>

*Усесфере* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Если **значение — true**, выборки будут вычисляться в полной сфере. Если **значение равно false**, выборки будут вычисляться в течение полушария.

</dd> <dt>

*Усекосине* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Если **значение равно true**, используйте для выборки коэффициент косинуса. Если оба Усекосине и Усесфере имеют **значение true**, то метод завершится ошибкой и будет возвращена ошибка.

</dd> <dt>

*Адаптивное* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Значение должно быть **равно false**. Адаптивная выборка в настоящее время не реализована.

</dd> <dt>

*Адаптивесреш* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Не обрабатывается.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, e \_ Нотимпл, e \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
