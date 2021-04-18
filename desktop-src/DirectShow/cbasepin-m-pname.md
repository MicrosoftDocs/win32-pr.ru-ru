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
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657789"
---
# <a name="cbasepinm_pname-member"></a>Элемент Кбасепин:: m \_ pName

Имя ПИН-кода.

## <a name="syntax"></a>Синтаксис


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Примечания

Метод [**кбасепин:: куерипининфо**](cbasepin-querypininfo.md) возвращает эту строку в качестве имени ПИН-кода, а метод [**Кбасепин:: QueryId**](cbasepin-queryid.md) возвращает его в качестве идентификатора ПИН-кода. Однако в общем случае имя и идентификатор ПИН-кода не должны совпадать. Идентификатор ПИН-кода используется для сохраняемости графа. Дополнительные сведения см. в разделе [**ибасефилтер:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




