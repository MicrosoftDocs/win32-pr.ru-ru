---
title: Расширенные сообщения об ошибках ADSI
description: Этот раздел содержит список разделов, в которых объясняется, как работать с сообщениями об ошибках ADSI, возвращаемыми функцией IADs, Иадсконтаинер, Идиректорйобжект и IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Расширенные сообщения об ошибках ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067341"
---
# <a name="adsi-extended-error-messages"></a><span data-ttu-id="2d5c7-104">Расширенные сообщения об ошибках ADSI</span><span class="sxs-lookup"><span data-stu-id="2d5c7-104">ADSI Extended Error Messages</span></span>

<span data-ttu-id="2d5c7-105">Помимо значений **HRESULT** , несколько поставщиков систем ADSI (в основном LDAP) возвращают дополнительные данные об ошибке для операций, выполняемых следующими интерфейсами:</span><span class="sxs-lookup"><span data-stu-id="2d5c7-105">Apart from the **HRESULT** values, several ADSI system providers (mostly LDAP) return additional error data for operations performed by the following interfaces:</span></span>

-   [<span data-ttu-id="2d5c7-106">**IADs**</span><span class="sxs-lookup"><span data-stu-id="2d5c7-106">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="2d5c7-107">**иадсконтаинер**</span><span class="sxs-lookup"><span data-stu-id="2d5c7-107">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="2d5c7-108">**идиректорйобжект**</span><span class="sxs-lookup"><span data-stu-id="2d5c7-108">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="2d5c7-109">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="2d5c7-109">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="2d5c7-110">Частью таких расширенных данных об ошибках является строка, отправленная сервером как часть результата сообщения.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-110">A part of such extended error data is the string sent by the server as a part of the message result.</span></span>

<span data-ttu-id="2d5c7-111">Вызовите [**адсжетластеррор**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) для получения таких расширенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-111">Call [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) to retrieve such extended error messages.</span></span> <span data-ttu-id="2d5c7-112">Первым параметром этой функции, *лперрор*, является значение **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2d5c7-112">The first parameter of this function, *lpError*, is a **DWORD** value.</span></span> <span data-ttu-id="2d5c7-113">Для сервера Active Directory ADSI пытается сопоставить сообщение об ошибке LDAP с соответствующим кодом ошибки Win32 и присваивает *лперрор* значение кода ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-113">For an Active Directory server, ADSI attempts to map an LDAP error message to an appropriate Win32 error code and assigns the Win32 error code value to *lpError*.</span></span> <span data-ttu-id="2d5c7-114">Если не удается разрешить сопоставление, ADSI присваивает **ошибке \_ недопустимые \_ данные** *лперрор*, как и для любого другого сервера каталога.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-114">Failing to resolve the mapping, ADSI assigns **ERROR\_INVALID\_DATA** to *lpError*, as it does for any other directory server.</span></span> <span data-ttu-id="2d5c7-115">Во всех случаях ADSI точно передает строку описания ошибки с сервера клиенту через *лперрорбуф*, второй параметр функции **адсжетластеррор** .</span><span class="sxs-lookup"><span data-stu-id="2d5c7-115">In all cases, ADSI faithfully relays the string of the error description from the server to the client through *lpErrorBuf*, the second parameter of the **ADsGetLastError** function.</span></span>

 

 




