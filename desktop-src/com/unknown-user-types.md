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
# <a name="unknown-user-types"></a><span data-ttu-id="f3a88-103">Неизвестные типы пользователей</span><span class="sxs-lookup"><span data-stu-id="f3a88-103">Unknown User Types</span></span>

<span data-ttu-id="f3a88-104">Можно упростить локализацию продукта, добавив следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="f3a88-104">You can ease product localization by adding the following registry key:</span></span>

<span data-ttu-id="f3a88-105">**HKey \_ Локальные \_ Компьютеры \\ программное обеспечение \\ Microsoft \\ OLE2** \\ **ункновнусертипе**  =  *usertype*</span><span class="sxs-lookup"><span data-stu-id="f3a88-105">**HKEY\_LOCAL\_MACHINES\\SOFTWARE\\Microsoft\\OLE2**\\**UnknownUserType** = *usertype*</span></span>

<span data-ttu-id="f3a88-106">Этот ключ позволяет функциям возвращать указанную строку, а не значение по умолчанию "неизвестно", позволяя локализаторам указывать тип пользователя другого языка.</span><span class="sxs-lookup"><span data-stu-id="f3a88-106">This key allows functions to return a specified string rather than a default value of "Unknown", enabling localizers to specify a user type of a different language.</span></span>

<span data-ttu-id="f3a88-107">Реализация обработчика COM по умолчанию [**иолеобжект:: жетусертипе**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) проверяет реестр путем вызова [**олерегжетусертипе**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="f3a88-107">The COM default handler's implementation of [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examines the registry by calling [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span> <span data-ttu-id="f3a88-108">Если класс объекта не найден в реестре, возвращается тип пользователя из экземпляра [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) объекта.</span><span class="sxs-lookup"><span data-stu-id="f3a88-108">If the object's class is not found in the registry, the user type from the object's [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) instance is returned.</span></span> <span data-ttu-id="f3a88-109">Если класс не найден в экземпляре **IStorage** объекта, возвращается строка Unknown.</span><span class="sxs-lookup"><span data-stu-id="f3a88-109">If the class is not found in the object's **IStorage** instance, the string "Unknown" is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3a88-110">См. также</span><span class="sxs-lookup"><span data-stu-id="f3a88-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3a88-111">Регистрация приложений COM</span><span class="sxs-lookup"><span data-stu-id="f3a88-111">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 