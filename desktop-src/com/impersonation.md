---
title: Олицетворение
description: Олицетворение — это способность потока выполняться в контексте безопасности, отличном от контекста процесса, владеющего потоком.
ms.assetid: b33ca3b0-0423-4338-b3d6-4bb3db3d3e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735fa12e175ecec5dc2a7ed741843d713532e19
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070697"
---
# <a name="impersonation"></a><span data-ttu-id="e87d3-103">Олицетворение</span><span class="sxs-lookup"><span data-stu-id="e87d3-103">Impersonation</span></span>

<span data-ttu-id="e87d3-104">Олицетворение — это способность потока выполняться в контексте безопасности, отличном от контекста процесса, владеющего потоком.</span><span class="sxs-lookup"><span data-stu-id="e87d3-104">Impersonation is the ability of a thread to execute in a security context that is different from the context of the process that owns the thread.</span></span> <span data-ttu-id="e87d3-105">При выполнении в контексте безопасности клиента сервер "является" клиентом, в некоторой степени.</span><span class="sxs-lookup"><span data-stu-id="e87d3-105">When running in the client's security context, the server "is" the client, to some degree.</span></span> <span data-ttu-id="e87d3-106">Поток сервера использует маркер доступа, представляющий учетные данные клиента для получения доступа к объектам, к которым у клиента есть доступ.</span><span class="sxs-lookup"><span data-stu-id="e87d3-106">The server thread uses an access token representing the client's credentials to obtain access to the objects to which the client has access.</span></span>

<span data-ttu-id="e87d3-107">Основная причина олицетворения — вызвать проверку доступа к удостоверению клиента.</span><span class="sxs-lookup"><span data-stu-id="e87d3-107">The primary reason for impersonation is to cause access checks to be performed against the client's identity.</span></span> <span data-ttu-id="e87d3-108">Использование удостоверения клиента для проверки доступа может привести к ограничению или расширению доступа в зависимости от того, что у клиента есть разрешение.</span><span class="sxs-lookup"><span data-stu-id="e87d3-108">Using the client's identity for access checks can cause access to be either restricted or expanded, depending on what the client has permission to do.</span></span> <span data-ttu-id="e87d3-109">Например, предположим, что файловый сервер содержит файлы, содержащие конфиденциальные сведения, и что каждый из этих файлов защищен ACL.</span><span class="sxs-lookup"><span data-stu-id="e87d3-109">For example, suppose a file server has files containing confidential information and that each of these files is protected by an ACL.</span></span> <span data-ttu-id="e87d3-110">Чтобы предотвратить несанкционированный доступ клиента к данным в этих файлах, сервер может олицетворять клиента перед доступом к файлам.</span><span class="sxs-lookup"><span data-stu-id="e87d3-110">To help prevent a client from obtaining unauthorized access to information in these files, the server can impersonate the client before accessing the files.</span></span>

## <a name="access-tokens-for-impersonation"></a><span data-ttu-id="e87d3-111">Маркеры доступа для олицетворения</span><span class="sxs-lookup"><span data-stu-id="e87d3-111">Access Tokens for Impersonation</span></span>

<span data-ttu-id="e87d3-112">Маркеры доступа — это объекты, описывающие контекст безопасности процесса или потока.</span><span class="sxs-lookup"><span data-stu-id="e87d3-112">Access tokens are objects that describe the security context of a process or thread.</span></span> <span data-ttu-id="e87d3-113">Они предоставляют сведения, включающие удостоверение учетной записи пользователя и подмножество привилегий, доступных для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="e87d3-113">They provide information that includes the identity of a user account and a subset of the privileges available to the user account.</span></span> <span data-ttu-id="e87d3-114">Каждый процесс имеет *основной маркер доступа* , описывающий контекст безопасности учетной записи пользователя, связанной с процессом.</span><span class="sxs-lookup"><span data-stu-id="e87d3-114">Every process has a *primary access token* that describes the security context of the user account associated with the process.</span></span> <span data-ttu-id="e87d3-115">По умолчанию система использует основной маркер, когда поток процесса взаимодействует с защищаемым объектом.</span><span class="sxs-lookup"><span data-stu-id="e87d3-115">By default, the system uses the primary token when a thread of the process interacts with a securable object.</span></span> <span data-ttu-id="e87d3-116">Однако когда поток олицетворяет клиента, поток олицетворения имеет как основной маркер доступа, так и *маркер олицетворения*.</span><span class="sxs-lookup"><span data-stu-id="e87d3-116">However, when a thread impersonates a client, the impersonating thread has both a primary access token and an *impersonation token*.</span></span> <span data-ttu-id="e87d3-117">Маркер олицетворения представляет контекст безопасности клиента, и этот маркер доступа используется для проверки доступа во время олицетворения.</span><span class="sxs-lookup"><span data-stu-id="e87d3-117">The impersonation token represents the client's security context, and this access token is the one that is used for access checks during impersonation.</span></span> <span data-ttu-id="e87d3-118">Когда используется олицетворение, поток возвращается к использованию только основного маркера доступа.</span><span class="sxs-lookup"><span data-stu-id="e87d3-118">When impersonation is over, the thread reverts to using only the primary access token.</span></span>

<span data-ttu-id="e87d3-119">Для получения маркера основного маркера процесса можно использовать функцию [**OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) .</span><span class="sxs-lookup"><span data-stu-id="e87d3-119">You can use the [**OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) function to get a handle to the primary token of a process.</span></span> <span data-ttu-id="e87d3-120">Используйте функцию [**опенсреадтокен**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) , чтобы получить маркер для маркера олицетворения потока.</span><span class="sxs-lookup"><span data-stu-id="e87d3-120">Use the [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function to get a handle to the impersonation token of a thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e87d3-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e87d3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e87d3-122">Маркеры доступа</span><span class="sxs-lookup"><span data-stu-id="e87d3-122">Access Tokens</span></span>](/windows/desktop/SecAuthZ/access-tokens)
</dt> <dt>

[<span data-ttu-id="e87d3-123">Делегирование и олицетворение</span><span class="sxs-lookup"><span data-stu-id="e87d3-123">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> </dl>

 

 