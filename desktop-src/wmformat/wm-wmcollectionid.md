---
title: WM/Вмколлектионид
description: Атрибут WM/Вмколлектионид содержит идентификатор GUID, определяющий коллекцию.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- Формат Windows Media WM/Вмколлектионид
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ad7e22c6769d459dc3d99b964a2df8e4dc562c709a231163d05a1b6b0be911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928834"
---
# <a name="wmwmcollectionid"></a>WM/Вмколлектионид

Атрибут **WM/вмколлектионид** содержит идентификатор GUID, определяющий коллекцию.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмвмколлектионид

## <a name="data-type"></a>Тип данных

**\_GUID типа \_ ВМТ**

## <a name="remarks"></a>Remarks

содержимое определяется технологиями мультимедиа Windows с использованием трех значений: **WM/вмколлектионграупид**, **wm/вмколлектионид** и **WM/вмконтентид**. Эти значения определяют содержимое, коллекцию, к которой он принадлежит, и группу, к которой принадлежит коллекция. все три из этих значений заполняются проигрыватель Windows Media при получении метаданных для содержимого. Приложение может записать эти значения и использовать их для поиска содержимого, но не следует изменять их, если они есть.

## <a name="see-also"></a>См. также

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




