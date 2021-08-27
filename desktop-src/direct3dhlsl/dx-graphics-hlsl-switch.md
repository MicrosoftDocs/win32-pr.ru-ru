---
title: Оператор Switch (Urlmon. h)
description: Передает управление другому блоку операторов в теле переключателя в зависимости от значения селектора.
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- Оператор Switch HLSL
topic_type:
- apiref
api_name:
- switch Statement
api_location:
- urlmon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8527853bf88b073f3505f4b4170ff6165f7f9aa7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477490"
---
# <a name="switch-statement"></a>Оператор switch

Передает управление другому блоку операторов в теле переключателя в зависимости от значения селектора.


\[*Атрибут* \] переключатель ( *селектор* ) {Case 0: { *статементблокк*;}   разбиени   вариант 1: { *статементблокк*;}   разбиени   Case n: { *статементблокк*;}   разбиени   значение по умолчанию: { *статементблокк*;}   разбиени



 

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Версию*
</dt> <dd>

Необязательный параметр, управляющий компиляцией инструкции. Если атрибут не указан, компилятор может использовать аппаратный переключатель или порождать последовательность инструкций **If** .




| attribute | Описание | 
|-----------|-------------|
| преобразовать в плоский формат | Скомпилируйте оператор как ряд инструкций <strong>If</strong> , каждый с атрибутом <strong>спрямления</strong> . | 
| ветвь | Скомпилируйте оператор как ряд операторов <strong>If</strong> , каждый с атрибутом <strong>branch</strong> .<blockquote>[!Note]<br />При использовании <a href="dx-graphics-hlsl-sm2.md">модели шейдеров 2. x</a> или <a href="dx-graphics-hlsl-sm3.md">Shader Model 3,0</a>каждый раз при использовании динамического ветвления используются ресурсы. Поэтому при чрезмерном использовании динамической ветви при выборе этих профилей могут возникнуть ошибки компиляции.</blockquote><br /> | 
| форцекасе | Принудительно использовать оператор switch на оборудовании.<blockquote>[!Note]<br />Требуется 10_0 или более поздний <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">уровень</a> оборудования.</blockquote><br /> | 
| вызывает | Тексты отдельных вариантов в коммутаторе будут перемещены в подпрограммы оборудования, а коммутатор будет являться серией вызовов подпрограмм.<blockquote>[!Note]<br />Требуется 10_0 или более поздний <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">уровень</a> оборудования.</blockquote><br /> | 




 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Выбора*
</dt> <dd>

Переменная. Инструкции CASE внутри фигурных скобок будут проверять эту переменную, чтобы определить, соответствует ли SwitchValue их конкретному Касевалуе.

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*статементблокк*
</dt> <dd>

Одна или несколько [инструкций](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии


```
[branch] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



Эквивалентно следующему:


```
[branch] if( a == 2 )
    return 3;
else if( a == 1 )
    return 1;
else if( a == 0 )
    return 0;
else
    return 6;
```



Ниже приведены примеры использования атрибутов управления потоком форцекасе и Call.


```
[forcecase] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}

[call] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Urlmon. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Flow Элемента](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

