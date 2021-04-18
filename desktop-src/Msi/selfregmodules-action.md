---
description: Действие Селфрегмодулес обрабатывает все модули, перечисленные в таблице Селфрег, и регистрирует все установленные модули в системе. Установщик не выполняет самостоятельную регистрацию EXE-файлов.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: Действие Селфрегмодулес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75895b1886fad51f36113ce6e677ba6a534ab0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664577"
---
# <a name="selfregmodules-action"></a><span data-ttu-id="07ec2-104">Действие Селфрегмодулес</span><span class="sxs-lookup"><span data-stu-id="07ec2-104">SelfRegModules Action</span></span>

<span data-ttu-id="07ec2-105">Действие Селфрегмодулес обрабатывает все модули, перечисленные в таблице [селфрег](selfreg-table.md) , и регистрирует все установленные модули в системе.</span><span class="sxs-lookup"><span data-stu-id="07ec2-105">The SelfRegModules action processes all modules listed in the [SelfReg](selfreg-table.md) table and registers all installed modules with the system.</span></span> <span data-ttu-id="07ec2-106">Установщик не выполняет самостоятельную регистрацию EXE-файлов.</span><span class="sxs-lookup"><span data-stu-id="07ec2-106">The installer does not self-register EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="07ec2-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="07ec2-107">Sequence Restrictions</span></span>

<span data-ttu-id="07ec2-108">Действие [инсталлвалидате](installvalidate-action.md) должно быть вызвано до вызова действия селфрегмодулес.</span><span class="sxs-lookup"><span data-stu-id="07ec2-108">The [InstallValidate](installvalidate-action.md) action must be called before calling the SelfRegModules action.</span></span> <span data-ttu-id="07ec2-109">Если используется действие [инсталлфилес](installfiles-action.md) , оно должно находиться перед действием селфрегмодулес в последовательности.</span><span class="sxs-lookup"><span data-stu-id="07ec2-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear before the SelfRegModules action in the sequence.</span></span> <span data-ttu-id="07ec2-110">Так как действие Селфрегмодулес изменяет систему, Селфрегмодулес должно следовать после [действия инсталлинитиализе](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="07ec2-110">Because the SelfRegModules action changes the system, SelfRegModules should come after the [InstallInitialize action](installinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="07ec2-111">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="07ec2-111">ActionData Messages</span></span>



| <span data-ttu-id="07ec2-112">Поле</span><span class="sxs-lookup"><span data-stu-id="07ec2-112">Field</span></span> | <span data-ttu-id="07ec2-113">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="07ec2-113">Description of action data</span></span>                           |
|-------|------------------------------------------------------|
| <span data-ttu-id="07ec2-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="07ec2-114">\[1\]</span></span> | <span data-ttu-id="07ec2-115">Идентификатор зарегистрированного файла модуля.</span><span class="sxs-lookup"><span data-stu-id="07ec2-115">Identifier of registered module file.</span></span>                |
| <span data-ttu-id="07ec2-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="07ec2-116">\[2\]</span></span> | <span data-ttu-id="07ec2-117">Идентификатор папки, содержащей зарегистрированный файл модуля.</span><span class="sxs-lookup"><span data-stu-id="07ec2-117">Identifier of folder holding registered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="07ec2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07ec2-118">Remarks</span></span>

<span data-ttu-id="07ec2-119">Действие Селфрегмодулес пытается вызвать функцию [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) модуля, для которого запланирована регистрация.</span><span class="sxs-lookup"><span data-stu-id="07ec2-119">The SelfRegModules action attempts to call the [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function of the module scheduled to be registered.</span></span> <span data-ttu-id="07ec2-120">Это действие выполняется с повышенными привилегиями при запуске установки с повышенными привилегиями, например во время установки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="07ec2-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="07ec2-121">Во время установки для отдельного пользователя программа установки выполняет это действие с правами пользователя.</span><span class="sxs-lookup"><span data-stu-id="07ec2-121">During a per-user installation the installer runs this action with user privileges.</span></span>

<span data-ttu-id="07ec2-122">Обратите внимание, что нельзя указать порядок, в котором установщик регистрирует самостоятельную регистрацию библиотек DLL с помощью [действия селфунрегмодулес](selfunregmodules-action.md).</span><span class="sxs-lookup"><span data-stu-id="07ec2-122">Note that you cannot specify the order in which the installer registers self-registering DLLs by using the [SelfUnRegModules action](selfunregmodules-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="07ec2-123">См. также</span><span class="sxs-lookup"><span data-stu-id="07ec2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07ec2-124">Указание порядка самостоятельной регистрации</span><span class="sxs-lookup"><span data-stu-id="07ec2-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
