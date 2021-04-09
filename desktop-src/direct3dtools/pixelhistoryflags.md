---
description: Перечисление, содержащее флаги, используемые для описания результата журнала пикселей. См. Пикселхисторйоператион.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление ПИКСЕЛХИСТОРИФЛАГС
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139758"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span id="vspixengine.pixelhistoryflags"></span>Перечисление ПИКСЕЛХИСТОРИФЛАГС

Перечисление, содержащее флаги, используемые для описания результата журнала пикселей. См. Пикселхисторйоператион.

## <a name="syntax"></a>Синтаксис


```C++
};
```

## <a name="constants"></a>Константы

<span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**ФФ \_ инитиалвалуе**  
Флаг, соответствующий начальному значению цвета (до кадра).

<span id="PHF_CLEAR"></span><span id="phf_clear"></span>**ФФ \_ очистить**  
Флаг, соответствующий результату очистки цвета.

<span id="PHF_DRAW"></span><span id="phf_draw"></span>**ФФ \_ Draw**  
Флаг, соответствующий цвету результат рисования.

<span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**ФФ \_ финалвалуе**  
Флаг, соответствующий последнему результату цвета.

<span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**ФФ \_ хасколор**  
Флаг, который соответствует тому, имеется ли в структуре Пикселхисторйоператион цветовой результат.

<span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**ФФ \_ хасфбколор**  
Флаг, который соответствует, имеется ли конечный результат цвета буфера в структуре Пикселхисторйоператион.

<span id="PHF_ERROR"></span><span id="phf_error"></span>**ФФ, \_ Ошибка**  

<span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**ФФ \_ вертекспроцессингскиппед**  
Не используется.

<span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**ФФ \_ модифиресаурце**  

<span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**ФФ \_ каннотрунфуллдепсстенЦилтест**  
Флаг, который соответствует невозможности выполнения теста глубины или трафарета.

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



