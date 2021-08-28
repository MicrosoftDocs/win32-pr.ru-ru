---
title: Метод ID3DX11EffectVariable Сетраввалуе (D3dx11effect. h)
description: Настройка данных.
ms.assetid: c5d53aa6-6cd8-4a93-9851-2a93bc6a728a
keywords:
- Метод Сетраввалуе Direct3D 11
- Метод Сетраввалуе Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Сетраввалуе
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.SetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f097ce0c31c9892e57d0fe01d5acf2e2418547ef8c8a53be4f0f43fdecc8c9ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069604"
---
# <a name="id3dx11effectvariablesetrawvalue-method"></a>Метод ID3DX11EffectVariable:: Сетраввалуе

Настройка данных.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* 
</dt> <dd>

Тип: **void \***

Указатель на переменную.

</dd> <dt>

*Offset* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Смещение (в байтах) от начала указателя до данных.

</dd> <dt>

*Количество* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Число байтов, которое необходимо задать.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Этот метод не выполняет преобразование или проверку типа; Таким образом, очень быстрый способ доступа к элементам массива.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

