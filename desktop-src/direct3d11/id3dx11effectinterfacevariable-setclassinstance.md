---
title: Метод ID3DX11EffectInterfaceVariable Сетклассинстанце (D3dx11effect. h)
description: Задает экземпляр класса.
ms.assetid: fc71a0d2-054a-48ed-86a5-54cf0017062a
keywords:
- Метод Сетклассинстанце Direct3D 11
- Метод Сетклассинстанце Direct3D 11, интерфейс ID3DX11EffectInterfaceVariable
- Интерфейс ID3DX11EffectInterfaceVariable Direct3D 11, метод Сетклассинстанце
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.SetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03d319d55b073393ff511b2e072aa07c244e5a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986948"
---
# <a name="id3dx11effectinterfacevariablesetclassinstance-method"></a>Метод ID3DX11EffectInterfaceVariable:: Сетклассинстанце

Задает экземпляр класса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetClassInstance(
   ID3DX11EffectClassInstanceVariable *pEffectClassInstance
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пеффектклассинстанце* 
</dt> <dd>

Тип: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***

Указатель на интерфейс [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) .

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

[ID3DX11EffectInterfaceVariable](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





