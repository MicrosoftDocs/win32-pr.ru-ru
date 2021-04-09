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
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069189"
---
# <a name="wmencodingtime"></a>WM/Енкодингтиме

Атрибут **WM/енкодингтиме** содержит метку времени, в которую было закодировано содержимое.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвменкодингтиме

## <a name="data-type"></a>Тип данных

**fileTime** (**тип ВМТ, \_ \_ QWORD**)

## <a name="remarks"></a>Комментарии

Этот атрибут использует значение FILETIME, которое представляет собой 64-разрядное значение, представляющее число единиц времени 100-наносекундных, истекших с 1 января 1601 г. Дополнительные сведения о параметре FILETIME см. в разделе "сведения о системе Windows" пакета Platform SDK.

Этот атрибут не является закодированным. Его необходимо задать вручную, если вы хотите включить его в файлы.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




