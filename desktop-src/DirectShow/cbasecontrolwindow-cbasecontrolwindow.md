---
description: Метод конструктора.
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Конструктор Кбасеконтролвиндов. Кбасеконтролвиндов (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9eb3e50daef8ec4ad11bf96a8f0b605f4c8fe679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657059"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a>Кбасеконтролвиндов. Кбасеконтролвиндов, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфилтер* 
</dt> <dd>

Указатель на объект фильтра мультимедиа-владельца.

</dd> <dt>

*пинтерфацелокк* 
</dt> <dd>

Указатель на критическую секцию, используемую для блокировки.

</dd> <dt>

*pName* 
</dt> <dd>

Указатель на описание объекта.

</dd> <dt>

*pUnk* 
</dt> <dd>

Указатель на управляющий интерфейс **IUnknown** , если объект является частью статистической функции; в противном случае **значение должно быть равно NULL**.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на переменную, которая получает значение HRESULT, указывающее на успешность или ошибку метода конструктора.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




