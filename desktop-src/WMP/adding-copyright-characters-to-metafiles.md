---
title: Добавление символов авторского права в метафайлы
description: Символы для авторского права и символов регистрации товарного знака (\ 169; или \ 174;) могут отображаться неправильно, если метафайл не кодируется с помощью схемы кодировки UTF-8.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- добавление знаков авторского права в метафайлы проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b0ab5fc4e539331406bb776a4bcdacbed6578a234dd9e84a3c358cdbe9936ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865164"
---
# <a name="adding-copyright-characters-to-metafiles"></a>Добавление символов авторского права в метафайлы

Символы для авторского права и символов регистрации товарного знака (© или®) могут отображаться неправильно, если метафайл не кодируется с помощью схемы кодировки UTF-8. В этом случае для правильного отображения любого из этих символов для всех пользователей можно использовать эквиваленты ASCII (c) и (r) внутри элемента **Copyright** , как показано в следующем коде.


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



Если метафайл кодируется с помощью UTF-8, то авторские знаки и символы товарных знаков будут отображаться правильно.

## <a name="see-also"></a>См. также

<dl> <dt>

[**Windows Справочник по элементам метафайлов мультимедиа**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




