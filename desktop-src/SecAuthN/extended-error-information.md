---
description: Некоторые пакеты безопасности поддерживают расширенные сообщения об ошибках, позволяющие сторонам канала связи связываться с любыми причинами сбоя.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Расширенные сведения об ошибке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f59c53da452a3254ff6faaebeb30983498161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647440"
---
# <a name="extended-error-information"></a><span data-ttu-id="dabca-103">Расширенные сведения об ошибке</span><span class="sxs-lookup"><span data-stu-id="dabca-103">Extended Error Information</span></span>

<span data-ttu-id="dabca-104">Некоторые [*пакеты безопасности*](/windows/desktop/SecGloss/s-gly) поддерживают расширенные сообщения об ошибках, позволяющие сторонам канала связи связываться с любыми причинами сбоя.</span><span class="sxs-lookup"><span data-stu-id="dabca-104">Some [*security packages*](/windows/desktop/SecGloss/s-gly) support extended error messages that allow the sides of a communication link to communicate any reasons for a failure.</span></span> <span data-ttu-id="dabca-105">Например, [*протокол Kerberos*](/windows/desktop/SecGloss/k-gly) может завершиться сбоем из-за несоответствия времени между временем запроса билета Kerberos и временем выпуска билета.</span><span class="sxs-lookup"><span data-stu-id="dabca-105">For example, the [*Kerberos protocol*](/windows/desktop/SecGloss/k-gly) could fail because of a time discrepancy between the time of request for a Kerberos ticket and the ticket's time of issue.</span></span> <span data-ttu-id="dabca-106">При возвращении сведений из расширенных сведений об ошибках клиент может повторно синхронизировать свои часы и создать новое сообщение о соединении.</span><span class="sxs-lookup"><span data-stu-id="dabca-106">With information from returned extended error information, a client can resynchronize its clock and generate a new connection message.</span></span>

<span data-ttu-id="dabca-107">Пакет безопасности, устанавливающий флаг SECPKG " \_ \_ Extended \_ Error" в элементе **фкапабилитиес** структуры [**секпкгинфо**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) , указывает, что пакет безопасности поддерживает расширенные сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="dabca-107">A security package setting the SECPKG\_FLAG\_EXTENDED\_ERROR flag in the **fCapabilities** member of a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure indicates that the security package supports extended error messages.</span></span>

<span data-ttu-id="dabca-108">Клиентские приложения, для которых требуются расширенные сообщения об ошибках, задают \_ \_ флаг расширенной ошибки ISC, \_ при вызове функции [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .</span><span class="sxs-lookup"><span data-stu-id="dabca-108">Client applications requiring extended error messages specify the ISC\_REQ\_EXTENDED\_ERROR flag when calling the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span> <span data-ttu-id="dabca-109">Серверные приложения, для которых требуются расширенные сообщения об ошибках, устанавливают \_ \_ флаг расширенных ошибок "ASC req" \_ при вызове [**AcceptSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span><span class="sxs-lookup"><span data-stu-id="dabca-109">Server applications requiring extended error messages set the ASC\_REQ\_EXTENDED\_ERROR flag when calling [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span></span>

 

 
