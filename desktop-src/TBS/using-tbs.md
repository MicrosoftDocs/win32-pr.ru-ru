---
title: Использование TBS
description: Каждая команда, отправленная в TBS, связана с определенной сущностью. Это достигается путем создания одного или нескольких контекстов для сущности, которые затем связываются с каждой последующей командой, отправленной этой сущностью.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- TBS базовых служб TPM, примеры
- TBS базовых служб TPM, использование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986525"
---
# <a name="using-tbs"></a><span data-ttu-id="58357-106">Использование TBS</span><span class="sxs-lookup"><span data-stu-id="58357-106">Using TBS</span></span>

<span data-ttu-id="58357-107">Функция базовых служб TPM делится на четыре функциональные области:</span><span class="sxs-lookup"><span data-stu-id="58357-107">The TPM Base Services feature is divided into four functional areas:</span></span>

-   [<span data-ttu-id="58357-108">Виртуализация ресурсов</span><span class="sxs-lookup"><span data-stu-id="58357-108">Resource Virtualization</span></span>](resource-virtualization.md)
-   [<span data-ttu-id="58357-109">Планирование команд</span><span class="sxs-lookup"><span data-stu-id="58357-109">Command Scheduling</span></span>](command-scheduling.md)
-   [<span data-ttu-id="58357-110">Управление питанием</span><span class="sxs-lookup"><span data-stu-id="58357-110">Power Management</span></span>](power-management.md)
-   [<span data-ttu-id="58357-111">Блокировка команд</span><span class="sxs-lookup"><span data-stu-id="58357-111">Command Blocking</span></span>](command-blocking.md)

<span data-ttu-id="58357-112">Чтобы обеспечить доступ различных сущностей к ресурсам друг друга, каждая команда, отправленная в TBS, связана с определенной сущностью.</span><span class="sxs-lookup"><span data-stu-id="58357-112">To ensure that different entities cannot access each other's resources, each command submitted to the TBS is associated with a specific entity.</span></span> <span data-ttu-id="58357-113">Это достигается путем создания одного или нескольких контекстов для сущности, которые затем связываются с каждой последующей командой, отправленной этой сущностью.</span><span class="sxs-lookup"><span data-stu-id="58357-113">This is accomplished by creating one or more contexts for an entity, which are then associated with each subsequent command submitted by that entity.</span></span> <span data-ttu-id="58357-114">Каждая команда включает объект Context, который позволяет TBS выполнять команды доверенного платформенного модуля в соответствующем контексте.</span><span class="sxs-lookup"><span data-stu-id="58357-114">Each command includes a context object, which allows the TBS to execute TPM commands under the appropriate context.</span></span> <span data-ttu-id="58357-115">Все объекты, созданные командами, удаляются из доверенного платформенного модуля при закрытии контекста.</span><span class="sxs-lookup"><span data-stu-id="58357-115">All objects created by commands are flushed from the TPM when the context is closed.</span></span>

<span data-ttu-id="58357-116">Сущность создает контекст перед тем, как сначала обращается к TBS, и сохраняет контекст, пока не завершит выполнение доступа к TBS.</span><span class="sxs-lookup"><span data-stu-id="58357-116">An entity creates the context before it first accesses the TBS and maintains the context until it is finished performing TBS accesses.</span></span> <span data-ttu-id="58357-117">Например, в случае Тсс функция TCG Core Services (TCS) в Тсс создаст контекст TBS при запуске и сохранит этот контекст активным, пока не завершится.</span><span class="sxs-lookup"><span data-stu-id="58357-117">For example, in the case of a TSS, the TCG core services (TCS) feature of the TSS would create a TBS context when it starts up, and it would keep that context active until it shuts down.</span></span>

<span data-ttu-id="58357-118">Для Windows Server 2008 и Windows Vista TBS разрешает доступ к API TBS для учетных записей администратора, службы NT AUTHORITY \\ LocalService и NT Authority \\ NetworkService.</span><span class="sxs-lookup"><span data-stu-id="58357-118">For Windows Server 2008 and Windows Vista, the TBS restricts access to the TBS API to the Administrators, NT AUTHORITY\\LocalService, and NT AUTHORITY\\NetworkService accounts.</span></span> <span data-ttu-id="58357-119">По умолчанию эти учетные записи являются только теми, которые могут подключаться к TBS и создавать контексты.</span><span class="sxs-lookup"><span data-stu-id="58357-119">By default, these accounts are the only ones that can connect to TBS and create contexts.</span></span> <span data-ttu-id="58357-120">Ограничения доступа можно изменить, **создав ключ реестра** с именем String (**reg \_ SZ**) имя значения реестра **SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="58357-120">Access restrictions can be modified by creating a registry key **Access** with a string (**REG\_SZ**) registry value name **SecurityDescriptor**</span></span> <dl> <dt>

<span data-ttu-id="58357-121">Тип данных</span><span class="sxs-lookup"><span data-stu-id="58357-121">Data type</span></span>
</dt> <dd><span data-ttu-id="58357-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="58357-122">REG_SZ</span></span></dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

<span data-ttu-id="58357-123">Пример.</span><span class="sxs-lookup"><span data-stu-id="58357-123">Example:</span></span>

<span data-ttu-id="58357-124">**О:БАГ: ОШИБКА: (A;; 0 x00000001;;; BA) (A;; 0 x00000001;;; NS) (A;; 0 x00000001;;; Местоположение**</span><span class="sxs-lookup"><span data-stu-id="58357-124">**O:BAG:BAD:(A;;0x00000001;;;BA)(A;;0x00000001;;;NS)(A;;0x00000001;;;LS)**</span></span>

<span data-ttu-id="58357-125">По умолчанию максимальное число контекстов, поддерживаемых TBS, равно 25.</span><span class="sxs-lookup"><span data-stu-id="58357-125">By default, the maximum number of contexts supported by the TBS is 25.</span></span> <span data-ttu-id="58357-126">Это число можно изменить путем создания или изменения значения реестра **DWORD** с именем **максконтекстс** в разделе **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **TPM**.</span><span class="sxs-lookup"><span data-stu-id="58357-126">This number can be altered by creating or modifying a **DWORD** registry value named **MaxContexts** under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Tpm**.</span></span> <span data-ttu-id="58357-127">Использование контекста TBS в режиме реального времени можно наблюдать с помощью средства "системный монитор" для отслеживания количества контекстов TBS.</span><span class="sxs-lookup"><span data-stu-id="58357-127">Real-time TBS context usage can be observed by using the performance monitor tool to track the number of TBS contexts.</span></span>

<span data-ttu-id="58357-128">Для Windows 8, Windows Server 2012 и более поздних версий TBS предоставляет доступ к стандартным пользователям и администраторам.</span><span class="sxs-lookup"><span data-stu-id="58357-128">For Windows 8, Windows Server 2012 and later, the TBS allows access to standard users and administrators.</span></span> <span data-ttu-id="58357-129">Разделы реестра **SecurityDescriptor** и **максконтекстс** стали устаревшими.</span><span class="sxs-lookup"><span data-stu-id="58357-129">The **SecurityDescriptor** and **MaxContexts** registry keys became obsolete.</span></span> <span data-ttu-id="58357-130">Для Windows 8, Windows Server 2012 и более поздних версий TBS разрешает доступ к определенным командам с помощью блокировки команд.</span><span class="sxs-lookup"><span data-stu-id="58357-130">For Windows 8, Windows Server 2012 and later, the TBS restricts access to certain commands using Command Blocking.</span></span>

<span data-ttu-id="58357-131">Для Windows 10 версии 1607 TBS разрешает доступ из приложений AppContainer.</span><span class="sxs-lookup"><span data-stu-id="58357-131">For Windows 10, version 1607, the TBS allows access from AppContainer applications.</span></span> <span data-ttu-id="58357-132">Для каждой версии TPM ключи **блоккедаппконтаинеркоммандс** и **AllowedW8AppContainerCommands** были добавлены с соответствующими списками заблокированных и разрешенных команд TPM соответственно.</span><span class="sxs-lookup"><span data-stu-id="58357-132">For each TPM version, the keys **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands** have been added with the matching lists of blocked and allowed TPM commands, respectively.</span></span>

<span data-ttu-id="58357-133">В Windows 1803 10 разделы реестра в разделе **AllowedW8AppContainerCommands** больше не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="58357-133">For Windows 10, version 1803, the registry keys under **AllowedW8AppContainerCommands** are no longer supported.</span></span>

 

 




