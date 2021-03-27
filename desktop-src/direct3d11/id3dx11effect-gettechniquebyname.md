---
title: Метод ID3DX11Effect Жеттечникуебинаме (D3dx11effect. h)
description: Получите метод по имени. | Метод ID3DX11Effect Жеттечникуебинаме (D3dx11effect. h)
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- Метод Жеттечникуебинаме Direct3D 11
- Метод Жеттечникуебинаме Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жеттечникуебинаме
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26b6067352d4ca898cc1fc970524040d407bda1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987092"
---
# <a name="id3dx11effectgettechniquebyname-method"></a>Метод ID3DX11Effect:: Жеттечникуебинаме

Получите метод по имени.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*имя*; 
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Имя метода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Указатель на [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md). Если метод с соответствующим именем не найден, возвращается недопустимый метод. [**ID3DX11EffectTechnique:: IsValid**](id3dx11effecttechnique-isvalid.md) должен вызываться для возвращаемого метода, чтобы определить, является ли он допустимым.

## <a name="remarks"></a>Примечания

Результат содержит один или несколько методов. Каждый прием содержит один или несколько проходов. Можно получить доступ к методу, используя его имя или индекс.

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

 

