---
description: Метод конструктора Кбасеконтролвидео. Кбасеконтролвидео.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Конструктор Кбасеконтролвидео. Кбасеконтролвидео (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbd9ed452dbf0c0091c3f1813f6f671c476dfa52e31b402440a3b1d19db2d3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057374"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a>Кбасеконтролвидео. Кбасеконтролвидео, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
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

## <a name="remarks"></a>Remarks

Объект реализует интерфейс элемента управления [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .

Для всех методов интерфейса из [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) , реализуемых этим классом, требуется, чтобы фильтр был правильно подключен. По этой причине классу передается ПИН-код, с которым он должен синхронизироваться. При вызове метода интерфейса объект определяет, что ПИН-код все еще подключен.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




