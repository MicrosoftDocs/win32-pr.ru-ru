---
title: Сеансы со значением NULL
description: Иногда вызов, поступающий в сеанс со значением NULL, может выглядеть как вызов с проверкой подлинности.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486992"
---
# <a name="null-sessions"></a><span data-ttu-id="4df51-103">Сеансы со значением NULL</span><span class="sxs-lookup"><span data-stu-id="4df51-103">Null Sessions</span></span>

<span data-ttu-id="4df51-104">Иногда вызов, поступающий в сеанс со значением NULL, может выглядеть как вызов с проверкой подлинности.</span><span class="sxs-lookup"><span data-stu-id="4df51-104">Sometimes a call arriving on the null session can appear like an authenticated call.</span></span> <span data-ttu-id="4df51-105">В частности, вызов функции [**рпкбиндингинкаусклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) возвращает уровень проверки подлинности и поставщика безопасности, используемого для вызова.</span><span class="sxs-lookup"><span data-stu-id="4df51-105">Specifically, calling the [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) function returns the authentication level and security provider used for the call.</span></span> <span data-ttu-id="4df51-106">Эта операция не означает, что вызов не находился в сеансе со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="4df51-106">This operation does not mean the call was not on a null session.</span></span> <span data-ttu-id="4df51-107">Эти две проблемы являются ортогональными.</span><span class="sxs-lookup"><span data-stu-id="4df51-107">The two issues are orthogonal.</span></span> <span data-ttu-id="4df51-108">В Microsoft Windows 2000 удаленный вызов процедур может попытаться олицетворить вызывающий объект и проверить разрешения после олицетворения.</span><span class="sxs-lookup"><span data-stu-id="4df51-108">On Microsoft Windows 2000, a remote procedure call can attempt to impersonate a caller and check the permissions after impersonation.</span></span> <span data-ttu-id="4df51-109">В Microsoft Windows XP быстрее вызывать функцию [**рпксерверинккаллаттрибутес**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) и проверять флаг **нуллсессион** .</span><span class="sxs-lookup"><span data-stu-id="4df51-109">On Microsoft Windows XP, it is faster to call the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function and check for the **NullSession** flag.</span></span>

<span data-ttu-id="4df51-110">Между Windows 2000 и Windows XP существует еще одно важное различие.</span><span class="sxs-lookup"><span data-stu-id="4df51-110">Another relevant difference exists between Windows 2000 and Windows XP.</span></span> <span data-ttu-id="4df51-111">Если \_ указан только флаг RPC \_ \_ , разрешен \_ только безопасный только для безопасности, вызовы в сеансе со значением null проходят через Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4df51-111">If only the RPC\_IF\_ALLOW\_SECURE\_ONLY flag is specified, calls on the null session go through in Windows 2000.</span></span> <span data-ttu-id="4df51-112">В Windows XP с общим усилением параметров безопасности по умолчанию при указании этого флага вызовы в сеансе со значением NULL отклоняются при отказе в доступе.</span><span class="sxs-lookup"><span data-stu-id="4df51-112">In Windows XP, with the general tightening of default security settings, when this flag is specified, calls on the null session are rejected with access denied.</span></span> <span data-ttu-id="4df51-113">Однако даже при использовании \_ \_ \_ флага RPC, если разрешить \_ только безопасный режим, RPC не гарантирует уровень привилегии вызывающего пользователя.</span><span class="sxs-lookup"><span data-stu-id="4df51-113">However, even with the RPC\_IF\_ALLOW\_SECURE\_ONLY flag, RPC does not guarantee the privilege level of the calling user.</span></span> <span data-ttu-id="4df51-114">Все проверки RPC — у пользователя есть действительные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="4df51-114">All RPC checks is that the user has valid credentials.</span></span> <span data-ttu-id="4df51-115">Возможно, вызывающий пользователь использует учетную запись гостя или другие учетные записи с низкими привилегиями.</span><span class="sxs-lookup"><span data-stu-id="4df51-115">It is possible that the calling user is using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="4df51-116">Убедитесь, что сервер не предполагает высокую привилегию \_ при использовании RPC \_ \_ , если \_ используется параметр Разрешить только безопасные.</span><span class="sxs-lookup"><span data-stu-id="4df51-116">Make sure the server does not assume high privilege once RPC\_IF\_ALLOW\_SECURE\_ONLY is used.</span></span>

 

 




