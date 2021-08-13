---
description: Вызывает другой шейдер из шейдера.
ms.assetid: ''
title: Функция CallShader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: e411ef61c34eafcef71f3e68f6700651e4b3073423afd40451f139f02826e504
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119280354"
---
# <a name="callshader-function"></a>Функция CallShader

Вызывает другой шейдер из шейдера.

## <a name="syntax"></a>Синтаксис
Это встроенное определение функции эквивалентно следующему шаблону функции:

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a>Параметры

`ShaderIndex`

Целое число без знака, представляющее индекс в [вызываемой таблице шейдеров](callable-shader.md) , указанной в вызове [**диспатчрайс**] (/Windows/Desktop/API/d3d12/NF-d3d12-id3d12graphicscommandlist4-dispatchrays.

`Parameter`

Определяемые пользователем параметры для передачи в вызываемый шейдер.  Эта структура параметра должна соответствовать структуре параметров, используемой в вызываемом шейдере, на которую указывает в таблице шейдеров.


## <a name="return-value"></a>Возвращаемое значение

**void**

## <a name="remarks"></a>Remarks

Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Вызываемый шейдер**](callable-shader.md)
* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер непопаданий**](miss-shader.md)
* [**Шейдер создания лучей**](ray-generation-shader.md)



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




