---
title: Метод ID3DX11EffectClassInstanceVariable Жетклассинстанце (D3dx11effect. h)
description: Возвращает экземпляр класса.
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- Метод Жетклассинстанце Direct3D 11
- Метод Жетклассинстанце Direct3D 11, интерфейс ID3DX11EffectClassInstanceVariable
- Интерфейс ID3DX11EffectClassInstanceVariable Direct3D 11, метод Жетклассинстанце
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae0f188c1ef72b688b4c1f227bac91139b5c6cfcb2749a5f2c1fa41dd61a179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046452"
---
# <a name="id3dx11effectclassinstancevariablegetclassinstance-method"></a>Метод ID3DX11EffectClassInstanceVariable:: Жетклассинстанце

Возвращает экземпляр класса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппклассинстанце* 
</dt> <dd>

Тип: **[ **ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***

Указатель на указатель [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) , который будет установлен в экземпляр класса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectClassInstanceVariable](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 





