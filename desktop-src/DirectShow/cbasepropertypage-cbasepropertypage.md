---
description: Метод конструктора Кбасепропертипаже. Кбасепропертипаже.
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Конструктор Кбасепропертипаже. Кбасепропертипаже (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95821062b6b1199ea98a5329934d76e2197901d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119952"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a>Кбасепропертипаже. Кбасепропертипаже, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Строка, содержащая имя объекта для целей отладки. Дополнительные сведения см. в разделе [**кбасеобжект:: кбасеобжект**](cbaseobject-cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Указатель на агрегированный интерфейс **IUnknown** .

</dd> <dt>

*диалогид* 
</dt> <dd>

Идентификатор ресурса для этого диалогового окна.

</dd> <dt>

*титлеид* 
</dt> <dd>

Идентификатор ресурса для строки, содержащей заголовок диалогового окна.

</dd> </dl>

## <a name="examples"></a>Примеры


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кпроп. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




