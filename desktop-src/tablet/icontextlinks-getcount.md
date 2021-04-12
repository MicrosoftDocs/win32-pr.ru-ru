---
description: Возвращает число объектов Иконтекстлинк в данной коллекции.
ms.assetid: c3becacd-2df0-401c-88c8-5fad3e9f8c02
title: 'Метод Иконтекстлинкс:: NOCOUNT (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c12fae76eb41bf05d60712cf9f69639c713066c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263150"
---
# <a name="icontextlinksgetcount-method"></a>Метод Иконтекстлинкс:: NOCOUNT

Возвращает число объектов [**иконтекстлинк**](icontextlink.md) в данной коллекции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулкаунт* \[ out, retval\]
</dt> <dd>

Число объектов [**иконтекстлинк**](icontextlink.md) , содержащихся в этой коллекции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтекстлинкс**](icontextlinks.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




