---
title: Метод Optimize ID3DX11Effect (D3dx11effect. h)
description: Сократите объем памяти, необходимый для воздействия.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Метод Optimize, Direct3D 11
- Оптимизация метода Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Optimize
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998603"
---
# <a name="id3dx11effectoptimize-method"></a>Метод ID3DX11Effect:: OPTIMIZE

Сократите объем памяти, необходимый для воздействия.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Optimize();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Примечания

В результате используется два разных способа использования пространства памяти: для хранения сведений, необходимых среде выполнения для выполнения действия, и для хранения метаданных, необходимых для отражения информации обратно в приложение с помощью API. Можно сократить объем памяти, необходимый для действия, вызвав **ID3DX11Effect:: optimize** , который удаляет метаданные отражения из памяти. Методы API для считывания переменных больше не будут работать после удаления данных отражения.

Следующие методы будут завершаться ошибкой после того, как будет вызвана оптимизация.

-   [**ID3DX11Effect:: Жетконстантбуффербиндекс**](id3dx11effect-getconstantbufferbyindex.md)
-   [**ID3DX11Effect:: Жетконстантбуффербинаме**](id3dx11effect-getconstantbufferbyname.md)
-   [**ID3DX11Effect:: DESC**](id3dx11effect-getdesc.md)
-   [**ID3DX11Effect:: наустройство**](id3dx11effect-getdevice.md)
-   [**ID3DX11Effect:: Жеттечникуебиндекс**](id3dx11effect-gettechniquebyindex.md)
-   [**ID3DX11Effect:: Жеттечникуебинаме**](id3dx11effect-gettechniquebyname.md)
-   [**ID3DX11Effect:: Жетвариаблебиндекс**](id3dx11effect-getvariablebyindex.md)
-   [**ID3DX11Effect:: Жетвариаблебинаме**](id3dx11effect-getvariablebyname.md)
-   [**ID3DX11Effect:: Жетвариаблебисемантик**](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> Ссылки, извлеченные с помощью этих методов перед вызовом **ID3DX11Effect:: optimize** , по-прежнему действительны после вызова **ID3DX11Effect:: optimize** . Это позволяет приложению получать все переменные, методы и передавать их, вызывать optimize, а затем использовать этот результат.

 

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

 

 





