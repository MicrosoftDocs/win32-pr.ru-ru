---
description: Метод конструктора Кдеферредкомманд. Кдеферредкомманд.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Конструктор Кдеферредкомманд. Кдеферредкомманд (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a10d8bba48902ed2d6fd66da8483cea1ba9aacc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119792"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a>Кдеферредкомманд. Кдеферредкомманд, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pQ* 
</dt> <dd>

Указатель на объект, который предоставляет интерфейс [**икуеуекомманд**](/windows/desktop/api/Control/nn-control-iqueuecommand) .

</dd> <dt>

*pUnk* 
</dt> <dd>

Указатель на внешний интерфейс **IUnknown** для агрегирования.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на возвращаемое значение **HRESULT** .

</dd> <dt>

*пункексекутор* 
</dt> <dd>

Указатель на объект, который будет выполнять эту команду.

</dd> <dt>

*time* 
</dt> <dd>

Время, когда будет выполняться команда.

</dd> <dt>

*IID* 
</dt> <dd>

Указатель на глобальный уникальный идентификатор (**GUID**) интерфейса, содержащего метод.

</dd> <dt>

*диспидмесод* 
</dt> <dd>

Вызываемый метод интерфейса.

</dd> <dt>

*вфлагс* 
</dt> <dd>

Контекст вызова.

</dd> <dt>

*каргс* 
</dt> <dd>

Число переданных аргументов.

</dd> <dt>

*пдисппарамс* 
</dt> <dd>

Указатель на список типов Variant аргументов.

</dd> <dt>

*пварресулт* 
</dt> <dd>

Указатель на возвращаемый список типов Variant, если таковой имеется.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Указатель на последний аргумент в списке параметров *пдисппарамс* с ошибкой.

</dd> <dt>

*бстреам* 
</dt> <dd>

Значение, указывающее, находится ли время отложенной команды во время потока (**true**) или во время презентации (**false**).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдеферредкомманд**](cdeferredcommand.md)
</dt> </dl>

 

 




