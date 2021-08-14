---
title: WM/Стреамтипеинфо
description: Атрибут WM/Стреамтипеинфо содержит сведения о конфигурации для указанного потока в файле ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- Формат Windows Media WM/Стреамтипеинфо
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb40926d5ecba3aea2c7f2db64850152c66a25861d4422fddf04670c76d8148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698276"
---
# <a name="wmstreamtypeinfo"></a>WM/Стреамтипеинфо

Атрибут **WM/стреамтипеинфо** содержит сведения о конфигурации для указанного потока в файле ASF.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмстреамтипеинфо

## <a name="data-type"></a>Тип данных

[**WM \_ \_ \_ сведения о типе потока**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**\_ \_ двоичный тип ВМТ**)

## <a name="remarks"></a>Remarks

Этот атрибут применяется к конкретным потокам. Этот атрибут нельзя получить для потока 0.

Этот атрибут доступен только для чтения.

Доступ к **WM/стреамтипеинфо** можно получить с помощью объекта редактора метаданных. Это единственный способ получить доступ к сведениям о конфигурации потока, не открывая файл с объектом Reader (или синхронным объектом Reader).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




