---
title: Сведения о настройке реестра DLL администрирования RAS
description: Ознакомьтесь с требованиями к регистрации библиотеки DLL администрирования сторонней службы удаленного доступа (RAS) с помощью RAS. Служба RAS поддерживает несколько библиотек DLL администрирования службы удаленного доступа.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- Администрирование удаленного доступа RRAS, Настройка реестра DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9a7b7c48422264a890a74b1bab36e61672f11d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406667"
---
# <a name="about-ras-administration-dll-registry-setup"></a><span data-ttu-id="60ae5-105">Сведения о настройке реестра DLL администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="60ae5-105">About RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="60ae5-106">Программа установки для библиотеки DLL администрирования RAS стороннего производителя должна зарегистрировать библиотеку DLL в службе RAS, предоставив сведения в следующем разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="60ae5-106">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="60ae5-107">Чтобы зарегистрировать библиотеку DLL, задайте в этом разделе следующие значения.</span><span class="sxs-lookup"><span data-stu-id="60ae5-107">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="60ae5-108">Имя значения</span><span class="sxs-lookup"><span data-stu-id="60ae5-108">Value name</span></span>    | <span data-ttu-id="60ae5-109">Данные</span><span class="sxs-lookup"><span data-stu-id="60ae5-109">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="60ae5-110">*Отображаемое имя*</span><span class="sxs-lookup"><span data-stu-id="60ae5-110">*DisplayName*</span></span> | <span data-ttu-id="60ae5-111">Строка **reg \_ SZ** , которая содержит ПОНЯТНОЕ имя библиотеки DLL, отображаемое пользователем.</span><span class="sxs-lookup"><span data-stu-id="60ae5-111">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="60ae5-112">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="60ae5-112">*DLLPath*</span></span>     | <span data-ttu-id="60ae5-113">Строка **reg \_ SZ** , содержащая полный путь к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="60ae5-113">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="60ae5-114">Поскольку служба RAS поддерживает несколько библиотек администрирования RAS, значение параметра реестра **DLLPath** может содержать список путей, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="60ae5-114">Because RAS supports multiple RAS Administration DLLs, the registry value **DLLPath** can contain a semi-colon delimited list of paths.</span></span> <span data-ttu-id="60ae5-115">Например, запись реестра для библиотеки администрирования RAS из вымышленной компании с названием «, Inc.» может быть следующей:</span><span class="sxs-lookup"><span data-stu-id="60ae5-115">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc., might be the following:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="60ae5-116">*DisplayName*: **reg \_ SZ** : Библиотека DLL администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="60ae5-116">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="60ae5-117">*DLLPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll; C: \\ NT \\ system32 \\ntwkadm2.dll</span><span class="sxs-lookup"><span data-stu-id="60ae5-117">*DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll; C:\\nt\\system32\\ntwkadm2.dll</span></span>

<span data-ttu-id="60ae5-118">Служба RAS вызывает библиотеки DLL в том порядке, в котором они перечислены в этом значении реестра.</span><span class="sxs-lookup"><span data-stu-id="60ae5-118">RAS calls the DLLs in the order in which they are listed in this registry value.</span></span> <span data-ttu-id="60ae5-119">Параметр реестра *DisplayName* по-прежнему содержит только одно отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="60ae5-119">The registry value *DisplayName* still contains only a single display name.</span></span>

<span data-ttu-id="60ae5-120">Программа установки библиотеки DLL администрирования RAS должна также предоставлять функции удаления и удаления.</span><span class="sxs-lookup"><span data-stu-id="60ae5-120">The setup program for a RAS administration DLL must also provide remove and uninstall functionality.</span></span> <span data-ttu-id="60ae5-121">Если пользователь удаляет библиотеку DLL, программа установки должна удалить записи реестра для библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="60ae5-121">If a user removes the DLL, the setup program must delete the registry entries for the DLL.</span></span>

<span data-ttu-id="60ae5-122">**Windows 2000/NT:** Служба RAS поддерживает только одну библиотеку DLL администрирования RAS, поэтому значение параметра реестра **DLLPath** не может содержать список путей, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="60ae5-122">**Windows 2000/NT:** RAS supports only one RAS Administration DLL, so the registry value **DLLPath** cannot contain a semi-colon delimited list of paths.</span></span>

 

 




