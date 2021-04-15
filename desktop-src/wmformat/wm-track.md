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
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411541"
---
# <a name="wmtrack"></a>WM/Track

Атрибут **WM/Track** содержит номер записи для содержимого. Этот атрибут отсчитывается от нуля и поддерживается для обеспечения обратной совместимости. В новом содержимом вместо него следует использовать атрибут [**WM/траккнумбер**](wm-tracknumber.md) .

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмтракк

## <a name="data-type"></a>Тип данных

**\_Строка типа \_ ВМТ**

## <a name="remarks"></a>Комментарии

Многие существующие приложения записывают значение для **WM/Track** как **DWORD**. При создании приложения, которое воспроизводит файлы из неизвестных источников, необходимо включить код, обрабатывающий значения String и **DWORD** .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




