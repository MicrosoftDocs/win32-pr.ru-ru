---
description: Следующий фрагмент кода иллюстрирует публикацию объекта пользователя на сервере ILS. После публикации объекта пользователя удаленные стороны могут использовать объект пользователя для выполнения вызовов указанного пользователя.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Добавление объекта пользователя на сервер ILS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809238"
---
# <a name="adding-a-user-object-to-an-ils-server"></a>Добавление объекта пользователя на сервер ILS

\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Следующий фрагмент кода иллюстрирует публикацию объекта пользователя на сервере ILS. После публикации объекта пользователя удаленные стороны могут использовать объект пользователя для выполнения вызовов указанного пользователя.

В этом фрагменте предполагается, что [соединение с сервером ILS](connecting-to-an-ils-server.md) уже выполнено.


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**итдиректори**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**итдиректорйобжект**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[**итдиректорйобжектусер**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



