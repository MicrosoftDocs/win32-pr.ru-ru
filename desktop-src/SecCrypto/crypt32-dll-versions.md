---
description: Crypt32.dll — это модуль, который реализует многие функции CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Версии Crypt32.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809341"
---
# <a name="crypt32dll-versions"></a><span data-ttu-id="9c36a-103">Версии Crypt32.dll</span><span class="sxs-lookup"><span data-stu-id="9c36a-103">Crypt32.dll Versions</span></span>

<span data-ttu-id="9c36a-104">Crypt32.dll — это модуль, который реализует многие функции сертификатов и шифрования сообщений в интерфейсе CryptoAPI, например [**криптсигнмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span><span class="sxs-lookup"><span data-stu-id="9c36a-104">Crypt32.dll is the module that implements many of the Certificate and Cryptographic Messaging functions in the CryptoAPI, such as [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span></span> <span data-ttu-id="9c36a-105">Crypt32.dll — это модуль, входящий в состав операционных систем Windows и Windows Server, но разные версии этой библиотеки предоставляют различные возможности.</span><span class="sxs-lookup"><span data-stu-id="9c36a-105">Crypt32.dll is a module that comes with the Windows and Windows Server operating systems, but different versions of this DLL provide different capabilities.</span></span> <span data-ttu-id="9c36a-106">Нет API для определения используемой версии CryptoAPI, но вы можете определить версию Crypt32.dll, которая используется в данный момент с помощью функций [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) и [**веркуеривалуе**](/windows/win32/api/winver/nf-winver-verqueryvaluea) .</span><span class="sxs-lookup"><span data-stu-id="9c36a-106">There is no API to determine the version of CryptoAPI that is in use, but you can determine the version of Crypt32.dll that is currently in use by using the [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) and [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) functions.</span></span>

<span data-ttu-id="9c36a-107">В общем случае диапазоны версий Crypt32.dll сопоставляются с версиями операционной системы, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9c36a-107">In general, the version ranges of Crypt32.dll map to the operating system versions as shown in the following table.</span></span> <span data-ttu-id="9c36a-108">Однако эта таблица должна использоваться только в качестве рекомендации, так как это возможно благодаря другим способам обновления, что Crypt32.dll версия будет отличаться от указанной в таблице.</span><span class="sxs-lookup"><span data-stu-id="9c36a-108">However, this table should be used as a guideline only because it is possible, through other update avenues, that the Crypt32.dll version will differ from the one indicated in the table.</span></span>

| <span data-ttu-id="9c36a-109">Версия Crypt32.dll</span><span class="sxs-lookup"><span data-stu-id="9c36a-109">Crypt32.dll version</span></span>                               | <span data-ttu-id="9c36a-110">Операционная система</span><span class="sxs-lookup"><span data-stu-id="9c36a-110">Operating system</span></span>                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c36a-111">*версия* >= 5.131.3790.0</span><span class="sxs-lookup"><span data-stu-id="9c36a-111">*version* >= 5.131.3790.0</span></span>                      | <span data-ttu-id="9c36a-112">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c36a-112">Windows Server 2003</span></span>                                                                                                                                                             |
| <span data-ttu-id="9c36a-113">*версия* >= 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="9c36a-113">*version* >= 5.131.2600.1243</span></span>                   | <span data-ttu-id="9c36a-114">Windows XP с пакетом обновления 2 (SP2) Windows XP с пакетом обновления 1 (SP1) с исправлением [Q329433](https://support.microsoft.com/kb/329433)</span><span class="sxs-lookup"><span data-stu-id="9c36a-114">Windows XP with Service Pack 2 (SP2)Windows XP with Service Pack 1 (SP1) with hotfix [Q329433](https://support.microsoft.com/kb/329433)</span></span><br/> <span data-ttu-id="9c36a-115">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9c36a-115">Windows XP</span></span><br/> |
| <span data-ttu-id="9c36a-116">5.131.2600.0 <= *версия* < 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="9c36a-116">5.131.2600.0 <= *version* < 5.131.2600.1243</span></span> | <span data-ttu-id="9c36a-117">Windows XP с SP1Windows XP</span><span class="sxs-lookup"><span data-stu-id="9c36a-117">Windows XP with SP1Windows XP</span></span><br/>                                                                                                                                        |



 

 

 
