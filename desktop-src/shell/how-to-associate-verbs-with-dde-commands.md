---
description: Демонстрирует вызов команды DDE с помощью команды оболочки.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Связывание команд с командами DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7174a22c993d93c347c8a0368fa7d1798362070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985464"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a><span data-ttu-id="2ce25-103">Связывание команд с командами DDE</span><span class="sxs-lookup"><span data-stu-id="2ce25-103">How to Associate Verbs with DDE Commands</span></span>

<span data-ttu-id="2ce25-104">При вызове глагола обычно запускается приложение, указанное в подразделе команд команды.</span><span class="sxs-lookup"><span data-stu-id="2ce25-104">Invoking a verb ordinarily launches the application that is specified by the verb's command subkey.</span></span> <span data-ttu-id="2ce25-105">Тем не менее, если приложение поддерживает платформа динамических данных Exchange (DDE), можно запустить оболочку сеанса DDE.</span><span class="sxs-lookup"><span data-stu-id="2ce25-105">However, if your application supports Dynamic Data Exchange (DDE), you can instead have the Shell initiate a DDE conversation.</span></span>

<span data-ttu-id="2ce25-106">Чтобы указать, что вызов команды должен инициировать сеанс DDE, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2ce25-106">To specify that invoking a verb should initiate a DDE conversation, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="2ce25-107">Инструкции</span><span class="sxs-lookup"><span data-stu-id="2ce25-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="2ce25-108">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="2ce25-108">Step 1:</span></span>

<span data-ttu-id="2ce25-109">Добавьте подраздел **ддиксек** в ключ команды.</span><span class="sxs-lookup"><span data-stu-id="2ce25-109">Add a **ddeexec** subkey to the verb's key.</span></span>

### <a name="step-2"></a><span data-ttu-id="2ce25-110">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="2ce25-110">Step 2:</span></span>

<span data-ttu-id="2ce25-111">Установите значение по умолчанию **ддиксек** в строку команды DDE.</span><span class="sxs-lookup"><span data-stu-id="2ce25-111">Set the default value of **ddeexec** to the DDE command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce25-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="2ce25-112">Remarks</span></span>

<span data-ttu-id="2ce25-113">Ключ **ддиксек** содержит три дополнительных подраздела, которые обеспечивают некоторый контроль над процессом DDE:</span><span class="sxs-lookup"><span data-stu-id="2ce25-113">The **ddeexec** key has three optional subkeys that provide some control over the DDE process:</span></span>

-   <span data-ttu-id="2ce25-114">**приложение**.</span><span class="sxs-lookup"><span data-stu-id="2ce25-114">**application**.</span></span> <span data-ttu-id="2ce25-115">В качестве значения по умолчанию для этого подраздела задайте имя приложения, которое будет использоваться для установки диалога DDE.</span><span class="sxs-lookup"><span data-stu-id="2ce25-115">Set the default value of this subkey to the application name to be used to establish the DDE conversation.</span></span> <span data-ttu-id="2ce25-116">Если подраздел **приложения** отсутствует, в качестве имени приложения используется значение по умолчанию для подраздела **Command команды** .</span><span class="sxs-lookup"><span data-stu-id="2ce25-116">If there is no **application** subkey, the default value of the verb's **command** subkey is used as the application name.</span></span>
-   <span data-ttu-id="2ce25-117">**раздел**.</span><span class="sxs-lookup"><span data-stu-id="2ce25-117">**topic**.</span></span> <span data-ttu-id="2ce25-118">В качестве значения по умолчанию для этого подраздела укажите имя раздела диалога DDE.</span><span class="sxs-lookup"><span data-stu-id="2ce25-118">Set the default value of this subkey to the topic name of the DDE conversation.</span></span> <span data-ttu-id="2ce25-119">Если подраздел **раздела** отсутствует, в качестве имени раздела используется система.</span><span class="sxs-lookup"><span data-stu-id="2ce25-119">If there is no **topic** subkey, System is used as the topic name.</span></span>
-   <span data-ttu-id="2ce25-120">**ифексек**.</span><span class="sxs-lookup"><span data-stu-id="2ce25-120">**ifexec**.</span></span> <span data-ttu-id="2ce25-121">Задайте для этого подраздела по умолчанию команду DDE, которая будет использоваться, если невозможно запустить сеанс DDE.</span><span class="sxs-lookup"><span data-stu-id="2ce25-121">Set the default value of this subkey to the DDE command to be used if DDE conversation cannot be initiated.</span></span> <span data-ttu-id="2ce25-122">При сбое инициации запускается приложение, указанное значением по умолчанию для подраздела **команд** команды.</span><span class="sxs-lookup"><span data-stu-id="2ce25-122">When initiation fails, the application that is specified by the default value of the verb's **command** subkey is launched.</span></span> <span data-ttu-id="2ce25-123">Если ключ **ифексек** существует, его значение по умолчанию будет использоваться в качестве команды DDE.</span><span class="sxs-lookup"><span data-stu-id="2ce25-123">If an **ifexec** key exists, its default value will then be used as the DDE command.</span></span> <span data-ttu-id="2ce25-124">Если подраздел **ифексек** отсутствует, в качестве команды DDE будет использоваться значение по умолчанию ключа **ддиксек** .</span><span class="sxs-lookup"><span data-stu-id="2ce25-124">If there is no **ifexec** subkey, the default value of the **ddeexec** key will be used again as the DDE command.</span></span>

<span data-ttu-id="2ce25-125">В следующем примере указывается, что вызов команды Open для MyProgram. 1 инициирует сеанс DDE с помощью команды DDE Open ("%1") и имени приложения MyProgram.</span><span class="sxs-lookup"><span data-stu-id="2ce25-125">The following example specifies that invoking the open verb for MyProgram.1 initiates a DDE conversation with a DDE command of Open("%1") and an application name of MyProgram.</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
            ddeexec
               (Default) = Open("%1")
               application
                  (Default) = MyProgram
```

 

 



