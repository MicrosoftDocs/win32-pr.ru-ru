---
title: WM/Вмконтентид
description: Атрибут WM/Вмконтентид содержит идентификатор GUID, определяющий содержимое.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- Формат Windows Media WM/Вмконтентид
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef250e2e2e797ce5ba3c4492c2a3f8b71d30eb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411853"
---
# <a name="wmwmcontentid"></a>WM/Вмконтентид

Атрибут **WM/вмконтентид** содержит идентификатор GUID, определяющий содержимое.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмвмконтентид

## <a name="data-type"></a>Тип данных

**\_GUID типа \_ ВМТ**

## <a name="remarks"></a>Комментарии

Содержимое идентифицируется технологиями Windows Media с использованием трех значений: **WM/вмколлектионграупид**, **WM/вмколлектионид** и **WM/вмконтентид**. Эти значения определяют содержимое, коллекцию, к которой он принадлежит, и группу, к которой принадлежит коллекция. Все три из этих значений заполняются проигрывателем Windows Media при получении метаданных для содержимого. Приложение может записать эти значения и использовать их для поиска содержимого, но не следует изменять их, если они есть.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




