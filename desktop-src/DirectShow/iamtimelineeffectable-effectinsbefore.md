---
description: Метод Еффектинсбефоре вставляет результат в объект с указанным уровнем приоритета.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'Метод Иамтимелиниффектабле:: Еффектинсбефоре (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680071"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a>Метод Иамтимелиниффектабле:: Еффектинсбефоре

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`EffectInsBefore`Метод вставляет результат в объект с указанным уровнем приоритета.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сохраняется* 
</dt> <dd>

Указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) этого действия.

</dd> <dt>

*Приоритет* 
</dt> <dd>

Уровень приоритета, на который следует вставить результат. Чтобы вставить результат в конец списка приоритетов, используйте значение-1.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При \_ успешном выполнении или E нотимпл возвращает значение ОК, \_ Если объект не является результатом. В противном случае возвращает другое значение **HRESULT** , указывающее причину ошибки.

## <a name="remarks"></a>Комментарии

Время начала и окончания действия обрезается в пределах диапазона времени объекта, если это необходимо. Если на указанном уровне приоритета уже действует, все эффекты, произведенные с этого момента, перемещаются вниз по списку приоритетов, чтобы освободить место для нового эффекта.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелиниффектабле**](iamtimelineeffectable.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




