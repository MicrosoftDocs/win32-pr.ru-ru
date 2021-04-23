---
title: Регистрация библиотеки DLL безопасности RAS
description: Программа установки DLL-библиотеки безопасности RAS должна зарегистрировать библиотеку DLL на сервере удаленного доступа Windows NT или Windows 2000.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775395"
---
# <a name="registering-a-ras-security-dll"></a><span data-ttu-id="ebd11-103">Регистрация библиотеки DLL безопасности RAS</span><span class="sxs-lookup"><span data-stu-id="ebd11-103">Registering a RAS Security DLL</span></span>

<span data-ttu-id="ebd11-104">Программа установки DLL-библиотеки безопасности RAS должна зарегистрировать библиотеку DLL на сервере удаленного доступа Windows NT или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ebd11-104">The setup program for a RAS security DLL must register the DLL with the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="ebd11-105">Только одна DLL-библиотека безопасности RAS может быть зарегистрирована, так как поддержка нескольких библиотек DLL безопасности не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="ebd11-105">Only one RAS security DLL can be registered as support for multiple security DLLs is not provided.</span></span> <span data-ttu-id="ebd11-106">Чтобы зарегистрировать библиотеку DLL безопасности RAS, установите значение *DLLPath* в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="ebd11-106">To register a RAS security DLL, set the *DLLPath* value under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| <span data-ttu-id="ebd11-107">Имя значения</span><span class="sxs-lookup"><span data-stu-id="ebd11-107">Value name</span></span> | <span data-ttu-id="ebd11-108">Данные</span><span class="sxs-lookup"><span data-stu-id="ebd11-108">Value data</span></span>                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd11-109">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="ebd11-109">*DLLPath*</span></span>  | <span data-ttu-id="ebd11-110">Строка **reg \_ SZ** , содержащая путь к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="ebd11-110">A **REG\_SZ** string that contains the path of the DLL.</span></span> <span data-ttu-id="ebd11-111">Эта строка должна указывать полный путь, если только библиотека DLL не находится в каталоге, указанном в системном пути.</span><span class="sxs-lookup"><span data-stu-id="ebd11-111">This string should specify the full path unless the DLL is in a directory listed in the system path.</span></span> |



 

<span data-ttu-id="ebd11-112">Программа установки DLL-библиотеки безопасности RAS также должна предоставлять функции удаления и удаления.</span><span class="sxs-lookup"><span data-stu-id="ebd11-112">The setup program for a RAS security DLL must also provide remove/uninstall functionality.</span></span> <span data-ttu-id="ebd11-113">Если пользователь удаляет библиотеку DLL, программа установки должна удалить значение *DLLPath* из реестра.</span><span class="sxs-lookup"><span data-stu-id="ebd11-113">If a user removes the DLL, the setup program must delete the *DLLPath* value from the registry.</span></span> <span data-ttu-id="ebd11-114">Служба RAS не запускается, если значение *DLLPath* указывает библиотеку DLL, которую не удается найти.</span><span class="sxs-lookup"><span data-stu-id="ebd11-114">The RAS service does not start if the *DLLPath* value specifies a DLL that cannot be found.</span></span>

<span data-ttu-id="ebd11-115">DLL-библиотека безопасности RAS должна экспортировать функции [**рассекуритидиалогбегин**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) и [**рассекуритидиаложенд**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) .</span><span class="sxs-lookup"><span data-stu-id="ebd11-115">A RAS security DLL must export the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) and [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) functions.</span></span>

 

 




