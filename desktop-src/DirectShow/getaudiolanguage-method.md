---
description: Метод Жетаудиолангуаже извлекает строку, указывающую, какой язык доступен в указанном звуковом потоке.
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: Метод Жетаудиолангуаже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af71ad7943fe5442ded09f0b599c64c4b7215dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536638"
---
# <a name="getaudiolanguage-method"></a>Метод Жетаудиолангуаже

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`GetAudioLanguage`Метод получает строку, указывающую, какой язык доступен в указанном звуковом потоке.

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Указывает номер звукового потока в текущем заголовке в виде целого числа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает читаемую строку, идентифицирующую язык аудиопотока в текущем заголовке.

 

 



