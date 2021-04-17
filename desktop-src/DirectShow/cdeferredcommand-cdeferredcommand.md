---
description: Метод конструктора.
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
ms.openlocfilehash: 4e92a2ffc5129ee38fc5061b28ea7ffef49da0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680013"
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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдеферредкомманд**](cdeferredcommand.md)
</dt> </dl>

 

 




