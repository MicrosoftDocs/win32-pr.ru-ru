---
title: Структуры API WebDAV
description: В API WebDAV используются следующие структуры.
ms.assetid: 1fa7b740-ac93-4756-ac9f-6a8cb4ea8bc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe54d58ef03bc8057336cb0e4bbbe3e833fb59c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338356"
---
# <a name="webdav-api-structures"></a><span data-ttu-id="8d834-103">Структуры API WebDAV</span><span class="sxs-lookup"><span data-stu-id="8d834-103">WebDAV API Structures</span></span>

<span data-ttu-id="8d834-104">В API WebDAV используются следующие структуры.</span><span class="sxs-lookup"><span data-stu-id="8d834-104">The following structures are used in the WebDAV API.</span></span>



| <span data-ttu-id="8d834-105">Структура</span><span class="sxs-lookup"><span data-stu-id="8d834-105">Structure</span></span>                                                   | <span data-ttu-id="8d834-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8d834-106">Description</span></span>                                                                                                                                                                                         |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d834-107">**\_BLOB- \_ объект проверки обратного вызова DAV \_**</span><span class="sxs-lookup"><span data-stu-id="8d834-107">**DAV\_CALLBACK\_AUTH\_BLOB**</span></span>](/windows/desktop/api/Davclnt/ns-davclnt-dav_callback_auth_blob) | <span data-ttu-id="8d834-108">Эта структура используется для хранения [*большого двоичного объекта*](/windows/desktop/SecGloss/b-gly) проверки подлинности, полученного функцией обратного вызова [*даваускаллбакк*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) .</span><span class="sxs-lookup"><span data-stu-id="8d834-108">This structure is used to store an authentication [*BLOB*](/windows/desktop/SecGloss/b-gly) that was retrieved by the [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) callback function.</span></span> |
| [<span data-ttu-id="8d834-109">**\_обратный вызов \_ DAV \_ УНП auth**</span><span class="sxs-lookup"><span data-stu-id="8d834-109">**DAV\_CALLBACK\_AUTH\_UNP**</span></span>](/windows/desktop/api/Davclnt/ns-davclnt-dav_callback_auth_unp)   | <span data-ttu-id="8d834-110">Эта структура используется для хранения сведений об имени пользователя и пароле, которые были получены функцией обратного вызова [*даваускаллбакк*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) .</span><span class="sxs-lookup"><span data-stu-id="8d834-110">This structure is used to store user name and password information that was retrieved by the [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) callback function.</span></span>                                               |
| [<span data-ttu-id="8d834-111">**\_cred обратного вызова DAV \_**</span><span class="sxs-lookup"><span data-stu-id="8d834-111">**DAV\_CALLBACK\_CRED**</span></span>](/windows/desktop/api/Davclnt/ns-davclnt-dav_callback_cred)            | <span data-ttu-id="8d834-112">Функция обратного вызова [*даваускаллбакк*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) использует эту структуру для хранения учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="8d834-112">The [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) callback function uses this structure to store user credential information.</span></span>                                                                               |



 

 

 