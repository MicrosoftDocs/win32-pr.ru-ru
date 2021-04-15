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
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411702"
---
# <a name="wmstreamtypeinfo"></a>WM/Стреамтипеинфо

Атрибут **WM/стреамтипеинфо** содержит сведения о конфигурации для указанного потока в файле ASF.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмстреамтипеинфо

## <a name="data-type"></a>Тип данных

[**WM \_ \_ \_ сведения о типе потока**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**\_ \_ двоичный тип ВМТ**)

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к конкретным потокам. Этот атрибут нельзя получить для потока 0.

Этот атрибут доступен только для чтения.

Доступ к **WM/стреамтипеинфо** можно получить с помощью объекта редактора метаданных. Это единственный способ получить доступ к сведениям о конфигурации потока, не открывая файл с объектом Reader (или синхронным объектом Reader).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




