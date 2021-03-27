---
title: Метод ID3DX11Effect Жетконстантбуффербиндекс (D3dx11effect. h)
description: Получение постоянного буфера по индексу.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Метод Жетконстантбуффербиндекс Direct3D 11
- Метод Жетконстантбуффербиндекс Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетконстантбуффербиндекс
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbc44b2d9ceea1bcfbf854a8d3c6998d03e3eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987098"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a>Метод ID3DX11Effect:: Жетконстантбуффербиндекс

Получение постоянного буфера по индексу.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
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

Тип: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Указатель на [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Примечания

Для действия, содержащего переменную, которая будет доступна для чтения и записи приложением, требуется по крайней мере один буфер константы. Для лучшей производительности результат должен организовывать переменные в один или несколько буферов констант в зависимости от частоты обновления.

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

 

