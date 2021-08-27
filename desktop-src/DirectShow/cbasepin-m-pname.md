---
description: Имя ПИН-кода.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Элемент Кбасепин:: m_pName (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: d118ed76650b9ea580c0143ff4334a480d110c4a9d9531a23dda60c05c614630
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052684"
---
# <a name="cbasepinm_pname-member"></a>Элемент Кбасепин:: m \_ pName

Имя ПИН-кода.

## <a name="syntax"></a>Синтаксис


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Remarks

Метод [**кбасепин:: куерипининфо**](cbasepin-querypininfo.md) возвращает эту строку в качестве имени ПИН-кода, а метод [**Кбасепин:: QueryId**](cbasepin-queryid.md) возвращает его в качестве идентификатора ПИН-кода. Однако в общем случае имя и идентификатор ПИН-кода не должны совпадать. Идентификатор ПИН-кода используется для сохраняемости графа. Дополнительные сведения см. в разделе [**ибасефилтер:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




