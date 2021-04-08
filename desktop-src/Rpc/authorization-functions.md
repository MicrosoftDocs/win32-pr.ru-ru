---
title: Функции авторизации (RPC)
description: Каждый раз, когда серверная программа получает клиентский запрос на доступ к одной из удаленных процедур управления, Библиотека времени выполнения RPC вызывает функцию авторизации по умолчанию.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490c06ba8e40f132c17986edaef4dc02bbe056d7
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2019
ms.locfileid: "104069308"
---
# <a name="authorization-functions"></a><span data-ttu-id="81ca8-103">Функции авторизации</span><span class="sxs-lookup"><span data-stu-id="81ca8-103">Authorization Functions</span></span>

<span data-ttu-id="81ca8-104">Каждый раз, когда серверная программа получает клиентский запрос на доступ к одной из удаленных процедур управления, Библиотека времени выполнения RPC вызывает функцию авторизации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="81ca8-104">Each time a server program receives a client request for access to one of the management remote procedures, the RPC run-time library invokes a default authorization function.</span></span> <span data-ttu-id="81ca8-105">Эта функция использует поставщик общих служб для проверки учетных данных клиента и авторизации или отклонения запроса.</span><span class="sxs-lookup"><span data-stu-id="81ca8-105">This function uses the SSP to check the client's credentials and authorize or reject the request.</span></span>

<span data-ttu-id="81ca8-106">Серверная программа может переопределить функцию авторизации, предоставляемую поставщиком общих служб.</span><span class="sxs-lookup"><span data-stu-id="81ca8-106">Your server program can override the authorization function that the SSP provides.</span></span> <span data-ttu-id="81ca8-107">Вызовите функцию [**рпкмгмтсетаусоризатионфн**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) и передайте ее в адрес функции авторизации.</span><span class="sxs-lookup"><span data-stu-id="81ca8-107">Invoke the function [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) and pass it to the address of your authorization function.</span></span> <span data-ttu-id="81ca8-108">После того как серверная программа настроит функцию авторизации, Библиотека времени выполнения RPC вызывает ее каждый раз, когда серверная программа получает клиентский запрос одной из функций управления.</span><span class="sxs-lookup"><span data-stu-id="81ca8-108">Once the server program sets the authorization function, the RPC run-time library calls it every time the server program receives a client request to one of the management functions.</span></span> <span data-ttu-id="81ca8-109">Дополнительные сведения см. в разделе [**рпкмгмтиссерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**рпкмгмтинкифидс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**рпкмгмтинксерверпринкнаме**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)и [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span><span class="sxs-lookup"><span data-stu-id="81ca8-109">For more information, see [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname), and [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span></span>

 

 




