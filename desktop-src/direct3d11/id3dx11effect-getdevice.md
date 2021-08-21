---
title: Метод ID3DX11Effect-Device (D3dx11effect. h)
description: Получите устройство, которое создало этот результат.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- Метод WebMethod Direct3D 11
- Метод метода WebMethod Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод WebMethod
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a27dece1915373699d130f8a537a22045f7e86f246402d85bbb400ceb1d8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124519"
---
# <a name="id3dx11effectgetdevice-method"></a>Метод ID3DX11Effect:: of Device

Получите устройство, которое создало этот результат.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдевице* 
</dt> <dd>

Тип: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***

Указатель на [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Для конкретного устройства создается действие путем вызова функции, такой как [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





