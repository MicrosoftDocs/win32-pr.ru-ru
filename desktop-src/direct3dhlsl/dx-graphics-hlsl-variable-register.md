---
title: регистрация
description: регистрация
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- регистрация HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0102716529471b3e867e17b0e9b635274cdfc28ec603f239d66c76ffb0fdaa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983214"
---
# <a name="register"></a>регистрация

Необязательное ключевое слово для назначения переменной шейдера конкретному регистру, в котором используется следующий синтаксис:



| : Register ( *\[ \_ профиль \] шейдера*, *\# \[ \] подкомпонент типа* ) |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>зарегистрировать
</dt> <dd>

Обязательное ключевое слово.

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[Профиль шейдера \_\]*
</dt> <dd>

Необязательный [профиль шейдера](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax), который может быть целевым объектом шейдера или просто **PS** или **VS**.

</dd> <dt>

<span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Подкомпонент типа \# \[\]*
</dt> <dd>

Объявление типа, числа и подкомпонентов.

-   Тип является одним из следующих:

    

    | Тип | Описание регистра       |
    |------|----------------------------|
    | b    | Буфер констант            |
    | t    | Текстура и буфер текстуры |
    | с    | Смещение буфера              |
    | s    | Образец                    |
    | u    | Представление неупорядоченного доступа      |

    

     

-   *\#* номер регистра, который является целым числом.
-   *Подкомпонентом* является Необязательное целое число.

</dd> </dl>

## <a name="remarks"></a>Remarks

Вы можете добавить одно или несколько назначений Register в одно и то же объявление переменной, разделяя их пробелами.

Для переменных Direct3D 10 в глобальной области ключевое слово **Register** действует так же, как и ключевое слово [ПАККОФФСЕТ (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .

## <a name="examples"></a>Примеры

Ниже приведены некоторые примеры:


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Синтаксис переменных](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Переменные (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 