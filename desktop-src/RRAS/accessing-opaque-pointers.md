---
title: Доступ к непрозрачным указателям
description: Клиенты могут получить доступ к информации, хранящейся в местах назначения, с помощью непрозрачных указателей.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532261"
---
# <a name="accessing-opaque-pointers"></a><span data-ttu-id="20881-103">Доступ к непрозрачным указателям</span><span class="sxs-lookup"><span data-stu-id="20881-103">Accessing Opaque Pointers</span></span>

<span data-ttu-id="20881-104">Клиенты могут получить доступ к информации, хранящейся в местах назначения, с помощью непрозрачных указателей.</span><span class="sxs-lookup"><span data-stu-id="20881-104">Clients are able to access the information stored in destinations by using opaque pointers.</span></span> <span data-ttu-id="20881-105">Чтобы использовать хранилище, клиент должен сначала вызвать [**ртмжетопакуеинформатионпоинтер**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) , чтобы получить указатель.</span><span class="sxs-lookup"><span data-stu-id="20881-105">To use the storage, the client must first call [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) to obtain the pointer.</span></span> <span data-ttu-id="20881-106">Всякий раз, когда требуется изменение сведений, клиент должен сначала заблокировать назначение, вызвав [**ртмлоккдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) с параметром *локкдест* , для которого установлено значение **true**.</span><span class="sxs-lookup"><span data-stu-id="20881-106">Whenever a change to the information is necessary, the client must first lock the destination by calling [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) with the *LockDest* parameter set to **TRUE**.</span></span> <span data-ttu-id="20881-107">После блокировки назначения клиент может внести необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="20881-107">Once the destination is locked, the client can make the necessary change.</span></span> <span data-ttu-id="20881-108">Назначение можно разблокировать с помощью другого вызова **ртмлоккдестинатион** с параметром *локкдест* , для которого задано **значение false**.</span><span class="sxs-lookup"><span data-stu-id="20881-108">The destination can be unlocked using another call to **RtmLockDestination** with the *LockDest* parameter set to **FALSE**.</span></span>

<span data-ttu-id="20881-109">Функция [**ртмлоккдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) также позволяет клиенту использовать блокировку чтения или запись, используя параметр *Exclusive* .</span><span class="sxs-lookup"><span data-stu-id="20881-109">The [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) function also allows a client to use either a read lock or a write lock, using the *Exclusive* parameter.</span></span> <span data-ttu-id="20881-110">Клиент должен использовать блокировку записи только при внесении изменений в данные, хранимые с помощью непрозрачного указателя.</span><span class="sxs-lookup"><span data-stu-id="20881-110">A client should use the write lock only when it is making changes to the information kept using the opaque pointer.</span></span> <span data-ttu-id="20881-111">Клиенты могут использовать блокировку чтения для просмотра сведений о непрозрачном указателе, хранящихся в назначении.</span><span class="sxs-lookup"><span data-stu-id="20881-111">Clients can use the read lock to view the opaque pointer information stored in a destination.</span></span>

<span data-ttu-id="20881-112">Пример кода, демонстрирующий использование этих функций, см. в разделе [доступ к непрозрачному указателю в назначении](access-the-opaque-pointer-in-a-destination.md).</span><span class="sxs-lookup"><span data-stu-id="20881-112">For sample code that shows how to use these functions, see [Access the Opaque Pointer in a Destination](access-the-opaque-pointer-in-a-destination.md).</span></span>

 

 




