---
description: Метод Жетсубпиктурелангуаже извлекает язык для указанного потока субтитров.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Метод Жетсубпиктурелангуаже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdedc90789efb331b1438744a0f64a42782bf1d1e363170ce626ed023d2e542a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536934"
---
# <a name="getsubpicturelanguage-method"></a>Метод Жетсубпиктурелангуаже

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`GetSubpictureLanguage`Метод получает язык для указанного потока субтитров.

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Указывает номер потока субтитров, язык текста которого требуется получить в виде целого числа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает читаемую строку, идентифицирующую язык аудиопотока в текущем заголовке.

 

 



