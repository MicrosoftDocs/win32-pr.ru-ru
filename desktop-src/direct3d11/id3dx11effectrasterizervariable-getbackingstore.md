---
title: Метод ID3DX11EffectRasterizerVariable Жетбаккингсторе (D3dx11effect. h)
description: Возвращает указатель на переменную, которая содержит состояние растерисер.
ms.assetid: aff62a6c-bdef-49ad-9492-5db0878f632e
keywords:
- Метод Жетбаккингсторе Direct3D 11
- Метод Жетбаккингсторе Direct3D 11, интерфейс ID3DX11EffectRasterizerVariable
- Интерфейс ID3DX11EffectRasterizerVariable Direct3D 11, метод Жетбаккингсторе
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80912da541d5d5386da4e9612216db3ce62904bdb32ba262b5a2d1ae773201cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534690"
---
# <a name="id3dx11effectrasterizervariablegetbackingstore-method"></a>Метод ID3DX11EffectRasterizerVariable:: Жетбаккингсторе

Возвращает указатель на переменную, которая содержит состояние растерисер.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetBackingStore(
   UINT                  Index,
   D3D11_RASTERIZER_DESC *pRasterizerDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс в массиве описаний растерисер-State. Если в результате присутствует только одна переменная растерисер, используйте значение 0.

</dd> <dt>

*прастеризердеск* 
</dt> <dd>

Тип: D3D11 средство программной **[ **\_ прорисовки \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***

Указатель на описание состояния растерисер (см. раздел [**D3D11 \_ растеризации \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Переменные эффектов сохраняются в памяти в резервном хранилище; При применении метода значения в резервном хранилище копируются на устройство. Резервные копии данных хранилища могут использоваться для повторного создания переменной при необходимости.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

