---
title: Метод оптимизации ID3DX11Effect (D3dx11effect. h)
description: Протестируйте результат, чтобы проверить, были ли метаданные отражения удалены из памяти.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Метод оптимизации Direct3D 11
- Оптимизированный метод Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, оптимизированный метод
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd04bf43869f23bfec38db34be1b83b2c4f3953c7017120ebe2f0c985504b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124509"
---
# <a name="id3dx11effectisoptimized-method"></a>Метод ID3DX11Effect:: OPTIMIZE

Протестируйте результат, чтобы проверить, были ли метаданные отражения удалены из памяти.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**

**Значение true** , если результат оптимизирован. в противном случае — **false**.

## <a name="remarks"></a>Remarks

В результате используется два разных способа использования пространства памяти: для хранения сведений, необходимых среде выполнения для выполнения действия, и для хранения метаданных, необходимых для отражения информации обратно в приложение с помощью API. Можно сократить объем памяти, необходимый для действия, вызвав [**ID3DX11Effect:: optimize**](id3dx11effect-optimize.md) , который удаляет метаданные отражения из памяти. Разумеется, методы API для считывания переменных больше не будут работать после удаления данных отражения.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

