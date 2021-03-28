---
title: ID3DX11Effect-метод IsValid (D3dx11effect. h)
description: Протестируйте результат, чтобы проверить, содержит ли он допустимый синтаксис. | ID3DX11Effect-метод IsValid (D3dx11effect. h)
ms.assetid: 42bf0069-1828-4f55-99f5-d0f81eb04336
keywords:
- Метод IsValid Direct3D 11
- Метод IsValid Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод IsValid
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88aef9e3864fc77380b3459860178c8537a6a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998606"
---
# <a name="id3dx11effectisvalid-method"></a>Метод ID3DX11Effect:: IsValid

Протестируйте результат, чтобы проверить, содержит ли он допустимый синтаксис.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**

**Значение true** , если синтаксис кода допустим; в противном случае — **false**.

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

 

