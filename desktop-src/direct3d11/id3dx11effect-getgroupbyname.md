---
title: Метод ID3DX11Effect Жетграупбинаме (D3dx11effect. h)
description: Возвращает группу эффектов по имени.
ms.assetid: 14b4b484-848a-409c-9a99-207ab25b7566
keywords:
- Метод Жетграупбинаме Direct3D 11
- Метод Жетграупбинаме Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетграупбинаме
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905fb9fb439dcf613e5abfee22f03bf968c81838c89af17d72e7f4a74d887c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046602"
---
# <a name="id3dx11effectgetgroupbyname-method"></a>Метод ID3DX11Effect:: Жетграупбинаме

Возвращает группу эффектов по имени.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectGroup* GetGroupByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя* 
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Имя группы эффектов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***

Указатель на интерфейс [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

