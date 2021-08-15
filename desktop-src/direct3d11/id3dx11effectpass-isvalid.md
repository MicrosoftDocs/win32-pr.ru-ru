---
title: ID3DX11EffectPass-метод IsValid (D3dx11effect. h)
description: Протестируйте пройденный тест, чтобы увидеть, содержит ли он допустимый синтаксис.
ms.assetid: 3c6ddcef-1303-4161-889c-c3ca271b6ad0
keywords:
- Метод IsValid Direct3D 11
- Метод IsValid Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d184f1912e3518c63e3e1720c0438acee9c84eba52b7a3a6717bbb2d9e091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534950"
---
# <a name="id3dx11effectpassisvalid-method"></a>Метод ID3DX11EffectPass:: IsValid

Протестируйте пройденный тест, чтобы увидеть, содержит ли он допустимый синтаксис.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**

**Значение true** , если синтаксис кода допустим; в противном случае — **false**.

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

 

