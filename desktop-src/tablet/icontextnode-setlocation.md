---
description: Обновляет область этого Иконтекстноде.
ms.assetid: e7001411-17e4-4f33-af04-dd3220275895
title: 'Метод Иконтекстноде:: SetLocation (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 20daefeab7a9e36d5e968d5d14bfa5110d733487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701605"
---
# <a name="icontextnodesetlocation-method"></a>Метод Иконтекстноде:: SetLocation

Обновляет область этого [**иконтекстноде**](icontextnode.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetLocation(
  [in] IAnalysisRegion *pIAnalysisRegion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пианалисисрегион* \[ окне\]
</dt> <dd>

[**Ианалисисрегион**](ianalysisregion.md) , описывающий область, в которую задается расположение объекта [**иконтекстноде**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Используйте этот метод для обновления расположения узла контекста (см. раздел [**иконтекстноде:: OnLocation**](icontextnode-getlocation.md)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**ианалисисрегион**](ianalysisregion.md)
</dt> <dt>

[**Иконтекстноде:: OnLocation**](icontextnode-getlocation.md)
</dt> <dt>

[**Иконтекстноде:: Жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




