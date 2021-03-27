---
title: Метод ID3DX11Effect Клониффект (D3dx11effect. h)
description: Создает копию интерфейса Effect.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- Метод Клониффект Direct3D 11
- Метод Клониффект Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Клониффект
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dc7e47d1c50d0e41c29c90102afaaebdce8dda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987242"
---
# <a name="id3dx11effectcloneeffect-method"></a>Метод ID3DX11Effect:: Клониффект

Создает копию интерфейса Effect.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Флаги, влияющие на создание клонированного результата. Может иметь значение 0 или одно из следующих значений.



| Flag                                    | Описание                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX11 \_ воздействие \_ клона в \_ \_ неодном | Игнорировать все "одиночные" квалификаторы в cbuffer. Все cbuffer будут иметь собственные [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s, созданные в клонированном результате. |



 

</dd> <dt>

*ппклонедеффект* 
</dt> <dd>

Тип: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Указатель на указатель [**ID3DX11Effect**](id3dx11effect.md) , который будет установлен в копию результата.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Примечания

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

