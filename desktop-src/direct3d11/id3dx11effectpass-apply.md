---
title: Метод Apply ID3DX11EffectPass (D3dx11effect. h)
description: Задайте состояние, которое содержится в передаче на устройство.
ms.assetid: d67fe968-bfb2-4f3a-b393-3f72f680211f
keywords:
- Применение метода Direct3D 11
- Применение метода Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод Apply
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.Apply
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e18d3d546a1bf6381103b7d38f7467fe4d66ed8e0d9702afcf7640197abb5c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046052"
---
# <a name="id3dx11effectpassapply-method"></a>Метод ID3DX11EffectPass:: Apply

Задайте состояние, которое содержится в передаче на устройство.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Apply(
   UINT                Flags,
   ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Не используется.

</dd> <dt>

*pContext* 
</dt> <dd>

Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

[**Ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) , к которому применяется передача.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

