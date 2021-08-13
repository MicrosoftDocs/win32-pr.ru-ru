---
title: WM/Енкодингтиме
description: Атрибут WM/Енкодингтиме содержит метку времени, в которую было закодировано содержимое.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- Формат Windows Media WM/Енкодингтиме
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c76de789bd6ca88a9bbc2f3bb68381b3816524a07cbf97dc1a35b2526179a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431845"
---
# <a name="wmencodingtime"></a>WM/Енкодингтиме

Атрибут **WM/енкодингтиме** содержит метку времени, в которую было закодировано содержимое.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвменкодингтиме

## <a name="data-type"></a>Тип данных

**fileTime** (**тип ВМТ, \_ \_ QWORD**)

## <a name="remarks"></a>Remarks

Этот атрибут использует значение FILETIME, которое представляет собой 64-разрядное значение, представляющее число единиц времени 100-наносекундных, истекших с 1 января 1601 г. дополнительные сведения о FILETIME см. в разделе Windows Сведения о системе пакета Platform SDK.

Этот атрибут не является закодированным. Его необходимо задать вручную, если вы хотите включить его в файлы.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




