---
title: Функция D3DX11CreateEffectFromMemory (D3dx11effect. h)
description: Создает результат из бинарного действия или файла.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- D3DX11CreateEffectFromMemory функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998525"
---
# <a name="d3dx11createeffectfrommemory-function"></a>Функция D3DX11CreateEffectFromMemory

Создает результат из бинарного действия или файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* 
</dt> <dd>

Тип: **void \***

Большой двоичный объект данных скомпилированных эффектов.

</dd> <dt>

*DataLength* 
</dt> <dd>

Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

Длина большого двоичного объекта данных.

</dd> <dt>

*фксфлагс* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Флаги влияния не существуют. Задайте нулевое значение.

</dd> <dt>

*пдевице* 
</dt> <dd>

Тип: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Указатель на [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) , для которого необходимо создать ресурсы эффектов.

</dd> <dt>

*ппеффект* 
</dt> <dd>

Тип: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Адрес вновь созданного интерфейса [**ID3DX11Effect**](id3dx11effect.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Примечания

> [!Note]  
> Для создания приложения типа Effects необходимо использовать [Исходный текст Effects 11](https://github.com/Microsoft/FX11) . Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Эффекты 11 функций](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

