---
title: WM/Track
description: Атрибут WM/Track содержит номер записи для содержимого. Этот атрибут отсчитывается от нуля и поддерживается для обеспечения обратной совместимости. В новом содержимом вместо него следует использовать атрибут WM/Траккнумбер.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Track Windows Media Format
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1113fde7b0b29b6f1f7618e9d531df83070725b9e05e70e09f64f93b027abfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026942"
---
# <a name="wmtrack"></a>WM/Track

Атрибут **WM/Track** содержит номер записи для содержимого. Этот атрибут отсчитывается от нуля и поддерживается для обеспечения обратной совместимости. В новом содержимом вместо него следует использовать атрибут [**WM/траккнумбер**](wm-tracknumber.md) .

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмтракк

## <a name="data-type"></a>Тип данных

**\_Строка типа \_ ВМТ**

## <a name="remarks"></a>Remarks

Многие существующие приложения записывают значение для **WM/Track** как **DWORD**. При создании приложения, которое воспроизводит файлы из неизвестных источников, необходимо включить код, обрабатывающий значения String и **DWORD** .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




