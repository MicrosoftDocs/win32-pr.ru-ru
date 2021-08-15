---
title: Метод ID3DX11EffectTechnique Жетпассбинаме (D3dx11effect. h)
description: Получение передачи по имени.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- Метод Жетпассбинаме Direct3D 11
- Метод Жетпассбинаме Direct3D 11, интерфейс ID3DX11EffectTechnique
- Интерфейс ID3DX11EffectTechnique Direct3D 11, метод Жетпассбинаме
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfad489fe6c4eda8ea417a9f272bcc0a7d4035eb04bc675cf599e4f5381234db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532366"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a>Метод ID3DX11EffectTechnique:: Жетпассбинаме

Получение передачи по имени.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя* 
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Имя прохода.

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

