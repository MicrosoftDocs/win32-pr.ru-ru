---
title: Метод ID3DX11EffectStringVariable GetString (D3dx11effect. h)
description: Получите строку.
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- Метод GetString Direct3D 11
- Метод GetString Direct3D 11, интерфейс ID3DX11EffectStringVariable
- Интерфейс ID3DX11EffectStringVariable Direct3D 11, метод GetString
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edef49fd0965e06693fb995434c0579080f1e6243522ca4ea1489dedb791f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533002"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a>Метод ID3DX11EffectStringVariable:: GetString

Получите строку.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппстринг* 
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***

Указатель на строку.

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

[ID3DX11EffectStringVariable](id3dx11effectstringvariable.md)
</dt> </dl>

 

