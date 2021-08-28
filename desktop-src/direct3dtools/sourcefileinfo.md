---
description: Представляет сведения о файле исходного кода.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Саурцефилеинфо
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39fdb9e7236dea1c04eb55614d9ea9833f398a94
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623130"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span id="vspixengine.sourcefileinfo"></span>Структура Саурцефилеинфо

Представляет сведения о файле исходного кода.

## <a name="syntax"></a>Синтаксис


```C++
} SourceFileInfo;
```

## <a name="members"></a>Участники

**fileName**  
Строка COM, комтаининг путь к файлу для связанного исходного файла.

**чекксумбитекаунт**  
Число байтов в контрольной сумме. Если Чекксумалгорисм равен ЧЕККСУМАЛГОРИСМ:: MD5, Чекксумбитекаунт имеет значение 16. Если Чекксумалгорисм равен ЧЕККСУМАЛГОРИСМ:: SHA1, Чекксумбитекаунт — 20.

**чекксумалгорисм**  
Указывает алгоритм, используемый для формирования контрольной суммы файла. Поддерживаемые алгоритмы: MD5 и SHA1. Дополнительные сведения см. в разделе Перечисление ЧЕККСУМАЛГОРИСМ.

**чекксумфирстпарт**  
Первая 8 байт контрольной суммы.

**чекксумсекондпарт**  
Вторая 8 байт контрольной суммы.

**чекксумсирдпарт**  
Третья 8 байт контрольной суммы.

**чекксумфаурспарт**  
Четвертая 8 байта контрольной суммы.

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



