---
title: Неизвестные типы пользователей
description: Неизвестные типы пользователей
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ce5ee88d36399187bab24ce51f0ef1c3c074182f98ce30ff6dc7d370992ffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129466"
---
# <a name="unknown-user-types"></a>Неизвестные типы пользователей

Можно упростить локализацию продукта, добавив следующий раздел реестра:

**HKey \_ Локальные \_ Компьютеры \\ программное обеспечение \\ Microsoft \\ OLE2** \\ **ункновнусертипе**  =  *usertype*

Этот ключ позволяет функциям возвращать указанную строку, а не значение по умолчанию "неизвестно", позволяя локализаторам указывать тип пользователя другого языка.

Реализация обработчика COM по умолчанию [**иолеобжект:: жетусертипе**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) проверяет реестр путем вызова [**олерегжетусертипе**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype). Если класс объекта не найден в реестре, возвращается тип пользователя из экземпляра [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) объекта. Если класс не найден в экземпляре **IStorage** объекта, возвращается строка Unknown.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистрация приложений COM](registering-com-applications.md)
</dt> </dl>

 

 