---
description: Метод Жетсубпиктурелангуаже извлекает язык для указанного потока субтитров.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Метод Жетсубпиктурелангуаже
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672949"
---
# <a name="getsubpicturelanguage-method"></a>Метод Жетсубпиктурелангуаже

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

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

 

 



