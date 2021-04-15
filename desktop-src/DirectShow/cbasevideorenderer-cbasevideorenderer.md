---
description: Метод конструктора.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Конструктор Кбасевидеорендерер. Кбасевидеорендерер (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ed49be63d9c2c05e12a2ac92ae33f64705460b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675600"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a>Кбасевидеорендерер. Кбасевидеорендерер, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*рендеркласс* 
</dt> <dd>

Идентификатор класса для этого модуля подготовки отчетов.

</dd> <dt>

*pName* 
</dt> <dd>

Указатель на описание, используемое в целях отладки.

</dd> <dt>

*pUnk* 
</dt> <dd>

Указатель на обобщенный объект Owner.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на значение **HRESULT** .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




