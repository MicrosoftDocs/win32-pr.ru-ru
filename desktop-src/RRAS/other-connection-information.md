---
title: Другие сведения о соединении
description: Члены структуры РАСДИАЛПАРАМС также могут задавать следующие сведения о соединении.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987617"
---
# <a name="other-connection-information"></a><span data-ttu-id="b88e2-103">Другие сведения о соединении</span><span class="sxs-lookup"><span data-stu-id="b88e2-103">Other Connection Information</span></span>

<span data-ttu-id="b88e2-104">Члены структуры [**расдиалпарамс**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) также могут задавать следующие сведения о соединении.</span><span class="sxs-lookup"><span data-stu-id="b88e2-104">The members of the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure can also specify the following connection information.</span></span>

-   <span data-ttu-id="b88e2-105">Номер телефона для переопределения номера в записи телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="b88e2-105">A phone number to override the number in the phone-book entry.</span></span>
-   <span data-ttu-id="b88e2-106">Номер телефона [обратного вызова](callback-connections.md) , который удаленный сервер может вызвать для установления соединения.</span><span class="sxs-lookup"><span data-stu-id="b88e2-106">A [callback](callback-connections.md) phone number that the remote server can call back to establish the connection.</span></span>
-   <span data-ttu-id="b88e2-107">Имя домена удаленной сети, в котором будет выполняться проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="b88e2-107">The name of the remote network domain on which the authentication is to occur.</span></span>

<span data-ttu-id="b88e2-108">Для номера обратного вызова и домена члены [**расдиалпарамс**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) могут указать, что служба RAS должна использовать информацию в записи телефонной книги, или предоставить сведения, переопределяющие данные телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="b88e2-108">For the callback number and the domain, the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) members can either indicate that RAS should use the information in the phone-book entry, or it can provide information that overrides the phone-book data.</span></span>

<span data-ttu-id="b88e2-109">Клиент RAS может использовать параметр *лпрасдиалекстенсионс* функции [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) для управления тем, использует ли RAS префикс номера телефона или суффикс, указанный в записи телефонной книги.</span><span class="sxs-lookup"><span data-stu-id="b88e2-109">A RAS client can use the *lpRasDialExtensions* parameter of the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function to control whether RAS uses a phone number prefix or suffix specified in a phone-book entry.</span></span>

 

 