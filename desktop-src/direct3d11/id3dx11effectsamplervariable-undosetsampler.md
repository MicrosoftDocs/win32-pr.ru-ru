---
title: Метод ID3DX11EffectSamplerVariable Ундосетсамплер (D3dx11effect. h)
description: Отменить ранее установленное состояние образца.
ms.assetid: bb837b12-d6c3-47e9-a0a1-0bfcfe0f3e4e
keywords:
- Метод Ундосетсамплер Direct3D 11
- Метод Ундосетсамплер Direct3D 11, интерфейс ID3DX11EffectSamplerVariable
- Интерфейс ID3DX11EffectSamplerVariable Direct3D 11, метод Ундосетсамплер
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.UndoSetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e89d72130e92a477b3824f8e5f8fc935e99bd5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355760"
---
# <a name="id3dx11effectsamplervariableundosetsampler-method"></a>Метод ID3DX11EffectSamplerVariable:: Ундосетсамплер

Отменить ранее установленное состояние образца.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UndoSetSampler(
   UINT Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индекс в массиве интерфейсов образцов. Если имеется только один интерфейс выборки, используйте значение 0.

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

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

