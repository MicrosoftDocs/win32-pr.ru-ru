---
description: Сертификаты предоставляются в соответствии с политиками, которые определяют критерии, которым должны удовлетворять запросы для получения сертификата.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Независимость от политик
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0d99b5babeced0fb87d9e603038e23a40859b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346535"
---
# <a name="policy-independence"></a><span data-ttu-id="5626c-103">Независимость от политик</span><span class="sxs-lookup"><span data-stu-id="5626c-103">Policy Independence</span></span>

<span data-ttu-id="5626c-104">Сертификаты предоставляются в соответствии с политиками, которые определяют критерии, которым должны удовлетворять запросы для получения сертификата.</span><span class="sxs-lookup"><span data-stu-id="5626c-104">Certificates are granted according to policies that define criteria that requesters must meet to receive a certificate.</span></span> <span data-ttu-id="5626c-105">Например, одной из политик может быть предоставление коммерческих сертификатов только в том случае, если кандидаты предоставляют свои идентификационные сведения лично.</span><span class="sxs-lookup"><span data-stu-id="5626c-105">For example, one policy may be to grant commercial certificates only if applicants present their identification in person.</span></span> <span data-ttu-id="5626c-106">Другая политика может предоставлять [*учетные данные*](../secgloss/c-gly.md) на основе запросов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5626c-106">Another policy may grant [*credentials*](../secgloss/c-gly.md) based on email requests.</span></span> <span data-ttu-id="5626c-107">Агентство, которое выдает кредитные карты, может обращаться к базе данных и отправлять запросы на телефонные звонки перед выдачей карты.</span><span class="sxs-lookup"><span data-stu-id="5626c-107">An agency that issues credit cards may choose to consult a database and make phone inquiries before issuing a card.</span></span>

<span data-ttu-id="5626c-108">Политики реализуются в модулях политик, написанных на C++, C или Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5626c-108">Policies are implemented in policy modules written in C++, C, or Visual Basic.</span></span> <span data-ttu-id="5626c-109">Функции служб сертификации изолированы от любых изменений в политике, которые может реализовать агентство.</span><span class="sxs-lookup"><span data-stu-id="5626c-109">Certificate Services functions are isolated from any changes in policy that an agency might implement.</span></span> <span data-ttu-id="5626c-110">Изменения в политике можно полностью реализовать в коде модуля политики сервера.</span><span class="sxs-lookup"><span data-stu-id="5626c-110">Changes in policy can be fully implemented in the server policy module code.</span></span> <span data-ttu-id="5626c-111">В [*центре сертификации*](../secgloss/c-gly.md) предприятия (ЦС) должен использоваться только модуль политики предприятия, предоставленный корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5626c-111">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

 

 
