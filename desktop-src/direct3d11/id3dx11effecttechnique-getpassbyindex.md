---
title: Метод ID3DX11EffectTechnique Жетпассбиндекс (D3dx11effect. h)
description: Получение передаваемого по индексу.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- Метод Жетпассбиндекс Direct3D 11
- Метод Жетпассбиндекс Direct3D 11, интерфейс ID3DX11EffectTechnique
- Интерфейс ID3DX11EffectTechnique Direct3D 11, метод Жетпассбиндекс
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd22cd5e7745b8e5a11018b930f6b544036780b118e9c745b67e730b693cdd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565794"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a>Метод ID3DX11EffectTechnique:: Жетпассбиндекс

Получение передаваемого по индексу.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectPass* GetPassByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Отсчитываемый с нуля индекс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***

Указатель на [**ID3DX11EffectPass**](id3dx11effectpass.md).

## <a name="remarks"></a>Remarks

Метод содержит один или несколько проходов; Получите проход, используя имя или индекс.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

