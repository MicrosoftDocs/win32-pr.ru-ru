---
description: Метод Трансадд добавляет переход к объекту. Объект может иметь несколько переходов, но они не должны перекрываться по времени. Переходы должны находиться в пределах временных границ объекта.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'Метод Иамтимелинетрансабле:: Трансадд (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 930c3ff43e11cfb71ffce6c7257d0124fe87aeaaf4ae065433f11b860020eeaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952753"
---
# <a name="iamtimelinetransabletransadd-method"></a>Метод Иамтимелинетрансабле:: Трансадд

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`TransAdd`Метод добавляет переход к объекту. Объект может иметь несколько переходов, но они не должны перекрываться по времени. Переходы должны находиться в пределах временных границ объекта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птранс* 
</dt> <dd>

Указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) добавляемого перехода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** :



| Код возврата                                                                                   | Описание                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>                                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Не удается вставить переход.<br/>              |
| <dl> <dt>**\_интерфейс E**</dt> </dl> | *птранс* не является указателем на переход.<br/> |



 

## <a name="remarks"></a>Remarks

Если переход перекрывает существующий переход, метод возвращает E \_ INVALIDARG.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иамтимелинетрансабле**](iamtimelinetransable.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




