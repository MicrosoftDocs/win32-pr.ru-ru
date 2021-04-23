---
description: Для регистрации пользователя или компьютера в иерархии сертификатов можно использовать следующие интерфейсы.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Интерфейсы регистрации сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684535"
---
# <a name="certificate-enrollment-interfaces"></a><span data-ttu-id="66731-103">Интерфейсы регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="66731-103">Certificate Enrollment Interfaces</span></span>

<span data-ttu-id="66731-104">Для регистрации пользователя или компьютера в иерархии сертификатов можно использовать следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="66731-104">The following interfaces can be used to enroll a user or a computer in a certificate hierarchy.</span></span>



| <span data-ttu-id="66731-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="66731-105">Interface</span></span>                                              | <span data-ttu-id="66731-106">Описание</span><span class="sxs-lookup"><span data-stu-id="66731-106">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66731-107">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="66731-107">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | <span data-ttu-id="66731-108">Регистрирует компьютер или пользователя в иерархии сертификатов.</span><span class="sxs-lookup"><span data-stu-id="66731-108">Enrolls a computer or user in a certificate hierarchy.</span></span>                                                                                                                              |
| [<span data-ttu-id="66731-109">**IX509Enrollment2**</span><span class="sxs-lookup"><span data-stu-id="66731-109">**IX509Enrollment2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | <span data-ttu-id="66731-110">Расширяет интерфейс [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , чтобы включить инициализацию из шаблона.</span><span class="sxs-lookup"><span data-stu-id="66731-110">Extends the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to enable initialization from a template.</span></span>                                                                          |
| [<span data-ttu-id="66731-111">**IX509EnrollmentHelper**</span><span class="sxs-lookup"><span data-stu-id="66731-111">**IX509EnrollmentHelper**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | <span data-ttu-id="66731-112">Определяет методы, позволяющие веб-приложению регистрировать сертификат, сохранять учетные данные сервера политики в кэше учетных данных и регистрировать серверы политик и серверы регистрации.</span><span class="sxs-lookup"><span data-stu-id="66731-112">Defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.</span></span> |
| [<span data-ttu-id="66731-113">**IX509EnrollmentStatus**</span><span class="sxs-lookup"><span data-stu-id="66731-113">**IX509EnrollmentStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | <span data-ttu-id="66731-114">Получение подробных сведений об ошибке для транзакции регистрации сертификата.</span><span class="sxs-lookup"><span data-stu-id="66731-114">Retrieves detailed error information about a certificate enrollment transaction.</span></span>                                                                                                    |
| [<span data-ttu-id="66731-115">**IX509SCEPEnrollment**</span><span class="sxs-lookup"><span data-stu-id="66731-115">**IX509SCEPEnrollment**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | <span data-ttu-id="66731-116">Интерфейс протокола регистрации простых компьютеров X. 509</span><span class="sxs-lookup"><span data-stu-id="66731-116">X.509 Simple Computer Enrollment Protocol Interface</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="66731-117">См. также</span><span class="sxs-lookup"><span data-stu-id="66731-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66731-118">Интерфейсы Цертенролл</span><span class="sxs-lookup"><span data-stu-id="66731-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 




