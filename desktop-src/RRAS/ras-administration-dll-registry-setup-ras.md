---
title: Установка реестра DLL администрирования RAS
description: Программа установки для библиотеки DLL администрирования RAS стороннего производителя должна зарегистрировать библиотеку DLL в службе RAS, предоставив сведения в следующем разделе реестра.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aed28fc41334c161a11ce5575b6395c4bb5da5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532408"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="6eaf9-103">Установка реестра DLL администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="6eaf9-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="6eaf9-104">Программа установки для библиотеки DLL администрирования RAS стороннего производителя должна зарегистрировать библиотеку DLL в службе RAS, предоставив сведения в следующем разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="6eaf9-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="6eaf9-105">Чтобы зарегистрировать библиотеку DLL, задайте в этом разделе следующие значения.</span><span class="sxs-lookup"><span data-stu-id="6eaf9-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="6eaf9-106">Имя значения</span><span class="sxs-lookup"><span data-stu-id="6eaf9-106">Value name</span></span>    | <span data-ttu-id="6eaf9-107">Данные</span><span class="sxs-lookup"><span data-stu-id="6eaf9-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="6eaf9-108">*Отображаемое имя*</span><span class="sxs-lookup"><span data-stu-id="6eaf9-108">*DisplayName*</span></span> | <span data-ttu-id="6eaf9-109">Строка **reg \_ SZ** , которая содержит ПОНЯТНОЕ имя библиотеки DLL, отображаемое пользователем.</span><span class="sxs-lookup"><span data-stu-id="6eaf9-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="6eaf9-110">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="6eaf9-110">*DLLPath*</span></span>     | <span data-ttu-id="6eaf9-111">Строка **reg \_ SZ** , содержащая полный путь к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="6eaf9-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="6eaf9-112">Например, запись реестра для библиотеки DLL администрирования RAS из вымышленной компании с названием «прочисление» может быть:</span><span class="sxs-lookup"><span data-stu-id="6eaf9-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="6eaf9-113">*DisplayName* : **reg \_ SZ** : Библиотека DLL администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="6eaf9-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="6eaf9-114">*DLLPath* : **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="6eaf9-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="6eaf9-115">Программа установки библиотеки DLL администрирования RAS должна также предоставлять функции удаления и удаления.</span><span class="sxs-lookup"><span data-stu-id="6eaf9-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="6eaf9-116">Если пользователь удаляет библиотеку DLL, программа установки должна удалить записи реестра библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="6eaf9-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




