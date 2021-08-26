---
description: 'Метод Чекккапабилитиес запрашивает, есть ли у потока указанные возможности поиска. Этот метод реализует метод Имедиасикинг:: Чекккапабилитиес.'
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Кпоспасссру. Чекккапабилитиес, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f1146e11097dbb2d717bd025d414b4510a219cc5f131e2fa7d56687128ddfd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108424"
---
# <a name="cpospassthrucheckcapabilities-method"></a>Кпоспасссру. Чекккапабилитиес, метод

`CheckCapabilities`Метод запрашивает, имеет ли поток указанные возможности поиска. Этот метод реализует метод [**имедиасикинг:: чекккапабилитиес**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкапабилитиес* 
</dt> <dd>

Указатель на побитовую комбинацию одного или нескольких атрибутов [**\_ \_ \_ возможностей**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) поиска. При возврате из метода значение указывает, какие из этих атрибутов доступны.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




