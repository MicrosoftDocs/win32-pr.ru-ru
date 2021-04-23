---
title: Сведения о настройке реестра DLL администрирования RAS
description: Программа установки для библиотеки DLL администрирования RAS стороннего производителя должна зарегистрировать библиотеку DLL в службе RAS, предоставив сведения в следующем разделе реестра.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- Администрирование удаленного доступа RRAS, Настройка реестра DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf487f792a4add9ebf61e8f866b9f0577fb468d
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "103890060"
---
# <a name="about-ras-administration-dll-registry-setup"></a><span data-ttu-id="8d32e-104">Сведения о настройке реестра DLL администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="8d32e-104">About RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="8d32e-105">Программа установки для библиотеки DLL администрирования RAS стороннего производителя должна зарегистрировать библиотеку DLL в службе RAS, предоставив сведения в следующем разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="8d32e-105">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="8d32e-106">Чтобы зарегистрировать библиотеку DLL, задайте в этом разделе следующие значения.</span><span class="sxs-lookup"><span data-stu-id="8d32e-106">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="8d32e-107">Имя значения</span><span class="sxs-lookup"><span data-stu-id="8d32e-107">Value name</span></span>    | <span data-ttu-id="8d32e-108">Данные</span><span class="sxs-lookup"><span data-stu-id="8d32e-108">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="8d32e-109">*Отображаемое имя*</span><span class="sxs-lookup"><span data-stu-id="8d32e-109">*DisplayName*</span></span> | <span data-ttu-id="8d32e-110">Строка **reg \_ SZ** , которая содержит ПОНЯТНОЕ имя библиотеки DLL, отображаемое пользователем.</span><span class="sxs-lookup"><span data-stu-id="8d32e-110">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="8d32e-111">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="8d32e-111">*DLLPath*</span></span>     | <span data-ttu-id="8d32e-112">Строка **reg \_ SZ** , содержащая полный путь к библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="8d32e-112">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="8d32e-113">Поскольку служба RAS поддерживает несколько библиотек администрирования RAS, значение параметра реестра **DLLPath** может содержать список путей, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="8d32e-113">Because RAS supports multiple RAS Administration DLLs, the registry value **DLLPath** can contain a semi-colon delimited list of paths.</span></span> <span data-ttu-id="8d32e-114">Например, запись реестра для библиотеки администрирования RAS из вымышленной компании с названием «, Inc.» может быть следующей:</span><span class="sxs-lookup"><span data-stu-id="8d32e-114">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc., might be the following:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="8d32e-115">*DisplayName*: **reg \_ SZ** : Библиотека DLL администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="8d32e-115">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="8d32e-116">*DLLPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll; C: \\ NT \\ system32 \\ntwkadm2.dll</span><span class="sxs-lookup"><span data-stu-id="8d32e-116">*DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll; C:\\nt\\system32\\ntwkadm2.dll</span></span>

<span data-ttu-id="8d32e-117">Служба RAS вызывает библиотеки DLL в том порядке, в котором они перечислены в этом значении реестра.</span><span class="sxs-lookup"><span data-stu-id="8d32e-117">RAS calls the DLLs in the order in which they are listed in this registry value.</span></span> <span data-ttu-id="8d32e-118">Параметр реестра *DisplayName* по-прежнему содержит только одно отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="8d32e-118">The registry value *DisplayName* still contains only a single display name.</span></span>

<span data-ttu-id="8d32e-119">Программа установки библиотеки DLL администрирования RAS должна также предоставлять функции удаления и удаления.</span><span class="sxs-lookup"><span data-stu-id="8d32e-119">The setup program for a RAS administration DLL must also provide remove and uninstall functionality.</span></span> <span data-ttu-id="8d32e-120">Если пользователь удаляет библиотеку DLL, программа установки должна удалить записи реестра для библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="8d32e-120">If a user removes the DLL, the setup program must delete the registry entries for the DLL.</span></span>

<span data-ttu-id="8d32e-121">**Windows 2000/NT:** Служба RAS поддерживает только одну библиотеку DLL администрирования RAS, поэтому значение параметра реестра **DLLPath** не может содержать список путей, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="8d32e-121">**Windows 2000/NT:** RAS supports only one RAS Administration DLL, so the registry value **DLLPath** cannot contain a semi-colon delimited list of paths.</span></span>

 

 




