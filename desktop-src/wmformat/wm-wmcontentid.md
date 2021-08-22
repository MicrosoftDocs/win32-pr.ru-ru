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
ms.openlocfilehash: ef6b1b77bf0305fa0890ea7e85172d77d6e213864c1fc114136bc42e08a8507b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083868"
---
# <a name="wmwmcontentid"></a>WM/Вмконтентид

Атрибут **WM/вмконтентид** содержит идентификатор GUID, определяющий содержимое.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмвмконтентид

## <a name="data-type"></a>Тип данных

**\_GUID типа \_ ВМТ**

## <a name="remarks"></a>Remarks

содержимое определяется технологиями мультимедиа Windows с использованием трех значений: **WM/вмколлектионграупид**, **wm/вмколлектионид** и **WM/вмконтентид**. Эти значения определяют содержимое, коллекцию, к которой он принадлежит, и группу, к которой принадлежит коллекция. все три из этих значений заполняются проигрыватель Windows Media при получении метаданных для содержимого. Приложение может записать эти значения и использовать их для поиска содержимого, но не следует изменять их, если они есть.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




