---
description: Метод Жетлангфромлангид извлекает удобную для восприятия строку при получении идентификатора основного языка.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Метод Жетлангфромлангид
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894666"
---
# <a name="getlangfromlangid-method"></a>Метод Жетлангфромлангид

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`GetLangFromLangID`Метод получает строку, доступную для чтения, при наличии основного идентификатора языка.

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*ипримарилангид*
</dt> <dd>

Указывает основной идентификатор языка в виде целого числа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает строковое представление языка, который может отображаться в пользовательском интерфейсе приложения.

## <a name="remarks"></a>Комментарии

Хотя этот метод называется `GetLangFromLangID` , передаваемый параметр фактически является основным идентификатором языка, а не идентификатором языка.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетаудиолангуаже**](getaudiolanguage-method.md)
</dt> <dt>

[**жетдвдтекстлангуажелЦид**](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



