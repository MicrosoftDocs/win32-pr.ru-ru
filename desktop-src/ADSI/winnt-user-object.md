---
title: Объект пользователя WinNT
description: Объект пользователя WinNT представляет учетную запись пользователя в домене Windows NT 4,0.
ms.assetid: c57016e2-538b-4f37-a1bb-699fcf3c080d
ms.tgt_platform: multiple
keywords:
- Интерфейс ADSI для пользовательских объектов
- Службы WinNT Provider ADSI, объект User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2448fbc7cd77be9c76290777b16e23b2f7e97e61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986076"
---
# <a name="winnt-user-object"></a><span data-ttu-id="cb5e7-105">Объект пользователя WinNT</span><span class="sxs-lookup"><span data-stu-id="cb5e7-105">WinNT User Object</span></span>

<span data-ttu-id="cb5e7-106">Объект пользователя WinNT представляет учетную запись пользователя в домене Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-106">The WinNT User object represents a user account in a Windows NT 4.0 domain.</span></span> <span data-ttu-id="cb5e7-107">Объект содержит специальные функции.</span><span class="sxs-lookup"><span data-stu-id="cb5e7-107">The object exhibits special features.</span></span> <span data-ttu-id="cb5e7-108">В одном экземпляре он не поддерживает все методы свойств интерфейса [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .</span><span class="sxs-lookup"><span data-stu-id="cb5e7-108">In one instance, it does not support all the property methods of the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span> <span data-ttu-id="cb5e7-109">Во втором экземпляре он поддерживает некоторые пользовательские свойства, доступ к которым можно получить только с помощью метода [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) или [**iAds. постановки**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="cb5e7-109">In a second instance, it supports some custom properties that can be accessed only with the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method.</span></span>

<span data-ttu-id="cb5e7-110">Дополнительные сведения об объектах пользователя WinNT см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="cb5e7-110">For more information about WinNT user objects, see:</span></span>

-   [<span data-ttu-id="cb5e7-111">Неподдерживаемые свойства IADsUser</span><span class="sxs-lookup"><span data-stu-id="cb5e7-111">Unsupported IADsUser Properties</span></span>](unsupported-iadsuser-properties.md)
-   [<span data-ttu-id="cb5e7-112">Настраиваемые свойства пользователя WinNT</span><span class="sxs-lookup"><span data-stu-id="cb5e7-112">WinNT Custom User Properties</span></span>](winnt-custom-user-properties.md)
-   [<span data-ttu-id="cb5e7-113">Примеры управления учетными записями пользователей WinNT</span><span class="sxs-lookup"><span data-stu-id="cb5e7-113">WinNT User Account Management Examples</span></span>](winnt-user-account-management-examples.md)

 

 




