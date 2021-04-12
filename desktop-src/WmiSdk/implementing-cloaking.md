---
description: Маскировка — это расширение для олицетворения, позволяющее лучше контролировать, как COM олицетворяет клиента через прокси-сервер. Как и многие формы системы безопасности WMI, вы устанавливаете маскировку с помощью интерфейсов CoSetProxyBlanket и CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Реализация маскировки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265604"
---
# <a name="implementing-cloaking"></a><span data-ttu-id="d3887-104">Реализация маскировки</span><span class="sxs-lookup"><span data-stu-id="d3887-104">Implementing Cloaking</span></span>

<span data-ttu-id="d3887-105">Маскировка — это расширение для олицетворения, позволяющее лучше контролировать, как COM олицетворяет клиента через прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="d3887-105">Cloaking is an extension to impersonation that allows for better control over how COM impersonates a client over a proxy.</span></span> <span data-ttu-id="d3887-106">Как и многие формы системы безопасности WMI, вы устанавливаете маскировку с помощью интерфейсов [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="d3887-106">Like many forms of WMI security, you set cloaking through the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interfaces.</span></span>

<span data-ttu-id="d3887-107">Модель COM предоставляет следующие формы маскировки:</span><span class="sxs-lookup"><span data-stu-id="d3887-107">COM provides the following forms of cloaking:</span></span>

-   <span data-ttu-id="d3887-108">Статические</span><span class="sxs-lookup"><span data-stu-id="d3887-108">Static</span></span>

    <span data-ttu-id="d3887-109">COM устанавливает удостоверение маркера потоком или маркером процесса при первом вызове прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="d3887-109">COM establishes the token identity by the thread or process token on the first call to the proxy.</span></span> <span data-ttu-id="d3887-110">Если вы используете статическую маскировку с помощью [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), вы задаете удостоверение прокси-сервера в течение жизненного цикла прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="d3887-110">If you use static cloaking with [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), you set the identity of the proxy for the life of the proxy.</span></span>

-   <span data-ttu-id="d3887-111">Динамический</span><span class="sxs-lookup"><span data-stu-id="d3887-111">Dynamic</span></span>

    <span data-ttu-id="d3887-112">COM повторно устанавливает удостоверение маркера из токена потока или процесса при каждом вызове прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="d3887-112">COM reestablishes the token identity from the thread or process token on each call to the proxy.</span></span> <span data-ttu-id="d3887-113">Так как COM проверяет удостоверение при каждом вызове, динамическое Маскировка позволяет более точно контролировать удостоверение клиента.</span><span class="sxs-lookup"><span data-stu-id="d3887-113">Because COM checks the identity on each call, dynamic cloaking allows for finer control over the client identity.</span></span> <span data-ttu-id="d3887-114">Однако динамическая маскировка менее эффективна, чем статическая маскировка.</span><span class="sxs-lookup"><span data-stu-id="d3887-114">However, dynamic cloaking is less efficient than static cloaking.</span></span>

<span data-ttu-id="d3887-115">При установке маскировки в сочетании с уровнем делегирования олицетворения сервер может распространять удостоверение клиента между серверами, даже если эти серверы являются удаленными.</span><span class="sxs-lookup"><span data-stu-id="d3887-115">When you set cloaking in conjunction with the delegation level of impersonation, a server can propagate the identity of a client across servers, even if the servers are remote.</span></span> <span data-ttu-id="d3887-116">Если не включить маскировку, COM выполняет любой вызов с локального сервера на удаленном сервере в контексте фактического серверного процесса.</span><span class="sxs-lookup"><span data-stu-id="d3887-116">If you do not enable cloaking, COM makes any call from a local server to a remote server under the context of the actual server process.</span></span>

<span data-ttu-id="d3887-117">Маскировка позволяет WMI олицетворять клиента для доступа к локальным и удаленным сетевым ресурсам на нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="d3887-117">Cloaking lets WMI impersonate a client to access both local and remote network resources across multiple computer boundaries.</span></span> <span data-ttu-id="d3887-118">Инструментарий WMI может передавать удостоверение клиента локальным и удаленным серверам, например другим удаленным экземплярам WMI.</span><span class="sxs-lookup"><span data-stu-id="d3887-118">WMI can pass the identity of the client to local and remote servers, such as other remote instances of WMI.</span></span> <span data-ttu-id="d3887-119">Эти удаленные серверы могут затем выполнять операции в исходном контексте клиента.</span><span class="sxs-lookup"><span data-stu-id="d3887-119">Those remote servers can then perform operations under the initial client context.</span></span>

<span data-ttu-id="d3887-120">В следующей процедуре описывается совместное использование маскировки и делегирования.</span><span class="sxs-lookup"><span data-stu-id="d3887-120">The following procedure describes how to use cloaking and delegation together.</span></span>

<span data-ttu-id="d3887-121">**Совместное использование маскировки и делегирования**</span><span class="sxs-lookup"><span data-stu-id="d3887-121">**To use cloaking and delegation together**</span></span>

1.  <span data-ttu-id="d3887-122">Задайте для службы проверки подлинности значение Kerberos.</span><span class="sxs-lookup"><span data-stu-id="d3887-122">Set the authentication service to Kerberos.</span></span>

    <span data-ttu-id="d3887-123">Kerberos — единственная служба проверки подлинности, поддерживающая удаленное маскировку и делегирование.</span><span class="sxs-lookup"><span data-stu-id="d3887-123">Kerberos is the only authentication service that supports remote cloaking and delegation.</span></span> <span data-ttu-id="d3887-124">Это означает, что маскировка и делегирование можно использовать только на удаленных серверах.</span><span class="sxs-lookup"><span data-stu-id="d3887-124">This means that cloaking and delegation can only be used on remote servers.</span></span>

2.  <span data-ttu-id="d3887-125">Пометьте учетную запись входа сервера как доверенную для делегирования в службах Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d3887-125">Mark the server login account as "Trusted for Delegation" in the Active Directory services.</span></span>
3.  <span data-ttu-id="d3887-126">Пометьте учетную запись входа клиента как "учетная запись важна и не может быть делегирована" в Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="d3887-126">Mark the client login account as "Account is sensitive and cannot be delegated" in Active Directory services.</span></span>

<span data-ttu-id="d3887-127">Например, вызов поставщика представления, который может вернуть объекты из нескольких экземпляров инструментария WMI на нескольких компьютерах, может воспользоваться преимуществами делегирования и маскировки.</span><span class="sxs-lookup"><span data-stu-id="d3887-127">For example, a call to the View Provider, which may return objects from multiple instances of WMI on multiple computers, can benefit from delegation and cloaking.</span></span>

 

 
