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
ms.openlocfilehash: 652007933669db4ed7977474858c7089ca0d577f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411854"
---
# <a name="wmwmcollectiongroupid"></a>WM/Вмколлектионграупид

Атрибут **WM/вмколлектионграупид** содержит идентификатор GUID, определяющий группу коллекции.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмвмколлектионграупид

## <a name="data-type"></a>Тип данных

**\_GUID типа \_ ВМТ**

## <a name="remarks"></a>Комментарии

Содержимое идентифицируется технологиями Windows Media с использованием трех значений: **WM/вмколлектионграупид**, **WM/вмколлектионид** и **WM/вмконтентид**. Эти значения определяют содержимое, коллекцию, к которой он принадлежит, и группу, к которой принадлежит коллекция. Все три из этих значений заполняются проигрывателем Windows Media при получении метаданных для содержимого. Приложение может записать эти значения и использовать их для поиска содержимого, но не следует изменять их, если они есть.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




