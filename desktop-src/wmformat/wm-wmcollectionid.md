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
ms.openlocfilehash: 21d2ffe9ca827b19b4ce403b2e2929dea64ae684
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411855"
---
# <a name="wmwmcollectionid"></a>WM/Вмколлектионид

Атрибут **WM/вмколлектионид** содержит идентификатор GUID, определяющий коллекцию.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмвмколлектионид

## <a name="data-type"></a>Тип данных

**\_GUID типа \_ ВМТ**

## <a name="remarks"></a>Комментарии

Содержимое идентифицируется технологиями Windows Media с использованием трех значений: **WM/вмколлектионграупид**, **WM/вмколлектионид** и **WM/вмконтентид**. Эти значения определяют содержимое, коллекцию, к которой он принадлежит, и группу, к которой принадлежит коллекция. Все три из этих значений заполняются проигрывателем Windows Media при получении метаданных для содержимого. Приложение может записать эти значения и использовать их для поиска содержимого, но не следует изменять их, если они есть.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




