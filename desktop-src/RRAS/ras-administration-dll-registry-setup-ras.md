---
title: Установка реестра DLL администрирования RAS
description: Ознакомьтесь с требованиями к регистрации библиотеки DLL администрирования сторонней службы удаленного доступа (RAS) с помощью RAS.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0af8e4b189de69f254429c18beb4756e01ad56
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406717"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="5d1b1-103">Установка реестра DLL администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="5d1b1-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="5d1b1-104">Программа установки для библиотеки DLL администрирования RAS стороннего производителя должна зарегистрировать библиотеку DLL в службе RAS, предоставив сведения в следующем разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="5d1b1-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="5d1b1-105">Чтобы зарегистрировать библиотеку DLL, задайте в этом разделе следующие значения.</span><span class="sxs-lookup"><span data-stu-id="5d1b1-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="5d1b1-106">Имя значения</span><span class="sxs-lookup"><span data-stu-id="5d1b1-106">Value name</span></span>    | <span data-ttu-id="5d1b1-107">Данные</span><span class="sxs-lookup"><span data-stu-id="5d1b1-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="5d1b1-108">*Отображаемое имя*</span><span class="sxs-lookup"><span data-stu-id="5d1b1-108">*DisplayName*</span></span> | <span data-ttu-id="5d1b1-109">Строка **reg \_ SZ** , которая содержит ПОНЯТНОЕ имя библиотеки DLL, отображаемое пользователем.</span><span class="sxs-lookup"><span data-stu-id="5d1b1-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="5d1b1-110">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="5d1b1-110">*DLLPath*</span></span>     | <span data-ttu-id="5d1b1-111">Строка **reg \_ SZ** , содержащая полный путь к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="5d1b1-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="5d1b1-112">Например, запись реестра для библиотеки DLL администрирования RAS из вымышленной компании с названием «прочисление» может быть:</span><span class="sxs-lookup"><span data-stu-id="5d1b1-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="5d1b1-113">*DisplayName* : **reg \_ SZ** : Библиотека DLL администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="5d1b1-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="5d1b1-114">*DLLPath* : **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="5d1b1-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="5d1b1-115">Программа установки библиотеки DLL администрирования RAS должна также предоставлять функции удаления и удаления.</span><span class="sxs-lookup"><span data-stu-id="5d1b1-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="5d1b1-116">Если пользователь удаляет библиотеку DLL, программа установки должна удалить записи реестра библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="5d1b1-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




