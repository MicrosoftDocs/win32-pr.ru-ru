---
title: WM/Вмколлектионграупид
description: Атрибут WM/Вмколлектионграупид содержит идентификатор GUID, определяющий группу коллекции.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- Формат Windows Media WM/Вмколлектионграупид
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b9d89724751e778eb9545b6c743dbfbcf077b860a8d85c5ab9297680deb930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698238"
---
# <a name="wmwmcollectiongroupid"></a>WM/Вмколлектионграупид

Атрибут **WM/вмколлектионграупид** содержит идентификатор GUID, определяющий группу коллекции.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмвмколлектионграупид

## <a name="data-type"></a>Тип данных

**\_GUID типа \_ ВМТ**

## <a name="remarks"></a>Remarks

содержимое определяется технологиями мультимедиа Windows с использованием трех значений: **WM/вмколлектионграупид**, **wm/вмколлектионид** и **WM/вмконтентид**. Эти значения определяют содержимое, коллекцию, к которой он принадлежит, и группу, к которой принадлежит коллекция. все три из этих значений заполняются проигрыватель Windows Media при получении метаданных для содержимого. Приложение может записать эти значения и использовать их для поиска содержимого, но не следует изменять их, если они есть.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




