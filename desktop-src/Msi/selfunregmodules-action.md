---
description: Действие Селфунрегмодулес отменяет регистрацию всех модулей, перечисленных в таблице Селфрег, для которых запланировано удаление. Установщик не выполняет самостоятельную регистрацию. EXE файлы.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Действие Селфунрегмодулес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3a0d98d8a8afe45b9b78f5c8af8ca2f84b2244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651164"
---
# <a name="selfunregmodules-action"></a><span data-ttu-id="3d53a-104">Действие Селфунрегмодулес</span><span class="sxs-lookup"><span data-stu-id="3d53a-104">SelfUnregModules Action</span></span>

<span data-ttu-id="3d53a-105">Действие Селфунрегмодулес отменяет регистрацию всех модулей, перечисленных в [таблице селфрег](selfreg-table.md) , для которых запланировано удаление.</span><span class="sxs-lookup"><span data-stu-id="3d53a-105">The SelfUnregModules action unregisters all modules listed in the [SelfReg table](selfreg-table.md) that are scheduled to be uninstalled.</span></span> <span data-ttu-id="3d53a-106">Установщик не выполняет самостоятельную регистрацию. EXE файлы.</span><span class="sxs-lookup"><span data-stu-id="3d53a-106">The installer does not self-register .EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3d53a-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="3d53a-107">Sequence Restrictions</span></span>

<span data-ttu-id="3d53a-108">Действие [инсталлвалидате](installvalidate-action.md) должно находиться перед действием селфунрегмодулес в последовательности.</span><span class="sxs-lookup"><span data-stu-id="3d53a-108">The [InstallValidate](installvalidate-action.md) action must appear before the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="3d53a-109">Если используется действие [селфрегмодулес](selfregmodules-action.md) , оно должно появиться после действия селфунрегмодулес в последовательности.</span><span class="sxs-lookup"><span data-stu-id="3d53a-109">If a [SelfRegModules](selfregmodules-action.md) action is used it must appear after the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="3d53a-110">Если используется [действие ремовефилес](removefiles-action.md) , оно должно появиться после действия селфунрегмодулес в последовательности.</span><span class="sxs-lookup"><span data-stu-id="3d53a-110">If a [RemoveFiles action](removefiles-action.md) is used it must appear after the SelfUnregModules action in the sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3d53a-111">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="3d53a-111">ActionData Messages</span></span>



| <span data-ttu-id="3d53a-112">Поле</span><span class="sxs-lookup"><span data-stu-id="3d53a-112">Field</span></span> | <span data-ttu-id="3d53a-113">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="3d53a-113">Description of action data</span></span>                             |
|-------|--------------------------------------------------------|
| <span data-ttu-id="3d53a-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="3d53a-114">\[1\]</span></span> | <span data-ttu-id="3d53a-115">Идентификатор незарегистрированного файла модуля.</span><span class="sxs-lookup"><span data-stu-id="3d53a-115">Identifier of unregistered module file.</span></span>                |
| <span data-ttu-id="3d53a-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="3d53a-116">\[2\]</span></span> | <span data-ttu-id="3d53a-117">Идентификатор папки, содержащей незарегистрированный файл модуля.</span><span class="sxs-lookup"><span data-stu-id="3d53a-117">Identifier of folder holding unregistered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3d53a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d53a-118">Remarks</span></span>

<span data-ttu-id="3d53a-119">Действие Селфунрегмодулес пытается вызвать функцию [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) модуля, для которого необходимо отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="3d53a-119">The SelfUnregModules action attempts to call the [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) function of the module that is to be unregistered.</span></span> <span data-ttu-id="3d53a-120">Это действие выполняется с повышенными привилегиями при запуске установки с повышенными привилегиями, например во время установки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3d53a-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="3d53a-121">Во время установки на уровне пользователя Установщик выполняет это действие с правами пользователя.</span><span class="sxs-lookup"><span data-stu-id="3d53a-121">During a per-user installation, the installer runs this action with user privileges.</span></span>

<span data-ttu-id="3d53a-122">Обратите внимание, что нельзя указать порядок, в котором установщик отменяет регистрацию библиотек DLL с собственной регистрацией с помощью действия Селфунрегмодулес.</span><span class="sxs-lookup"><span data-stu-id="3d53a-122">Note that you cannot specify the order in which the installer unregisters self-registering DLLs by using the SelfUnRegModules action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d53a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="3d53a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d53a-124">Указание порядка самостоятельной регистрации</span><span class="sxs-lookup"><span data-stu-id="3d53a-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
