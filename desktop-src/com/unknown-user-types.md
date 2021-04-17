---
title: Неизвестные типы пользователей
description: Неизвестные типы пользователей
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339396"
---
# <a name="unknown-user-types"></a>Неизвестные типы пользователей

Можно упростить локализацию продукта, добавив следующий раздел реестра:

**HKey \_ Локальные \_ Компьютеры \\ программное обеспечение \\ Microsoft \\ OLE2** \\ **ункновнусертипе**  =  *usertype*

Этот ключ позволяет функциям возвращать указанную строку, а не значение по умолчанию "неизвестно", позволяя локализаторам указывать тип пользователя другого языка.

Реализация обработчика COM по умолчанию [**иолеобжект:: жетусертипе**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) проверяет реестр путем вызова [**олерегжетусертипе**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype). Если класс объекта не найден в реестре, возвращается тип пользователя из экземпляра [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) объекта. Если класс не найден в экземпляре **IStorage** объекта, возвращается строка Unknown.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Регистрация приложений COM](registering-com-applications.md)
</dt> </dl>

 

 