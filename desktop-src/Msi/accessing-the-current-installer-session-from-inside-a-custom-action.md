---
description: Пользовательские действия нондеферред, вызывающие библиотеки или скрипты динамической компоновки, могут получить доступ к выполняющейся установке для запроса или изменения атрибутов текущего сеанса установки.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Доступ к текущему сеансу установщика из пользовательского действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a870247f70742d408c0f5d1d0e67f20cef65d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998315"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a><span data-ttu-id="4f51e-103">Доступ к текущему сеансу установщика из пользовательского действия</span><span class="sxs-lookup"><span data-stu-id="4f51e-103">Accessing the Current Installer Session from Inside a Custom Action</span></span>

<span data-ttu-id="4f51e-104">Пользовательские действия нондеферред, вызывающие библиотеки или [скрипты](scripts.md) [динамической компоновки](dynamic-link-libraries.md) , могут получить доступ к выполняющейся установке для запроса или изменения атрибутов текущего сеанса установки.</span><span class="sxs-lookup"><span data-stu-id="4f51e-104">Nondeferred custom actions that call [dynamic-link libraries](dynamic-link-libraries.md) or [scripts](scripts.md) may access a running installation to query or modify the attributes of the current installation session.</span></span> <span data-ttu-id="4f51e-105">Для каждого процесса может существовать только один объект **сеанса** , а сценарии настраиваемых действий не должны пытаться создать другой сеанс.</span><span class="sxs-lookup"><span data-stu-id="4f51e-105">Only one **Session** object can exist for each process, and custom action scripts must not attempt to create another session.</span></span>

<span data-ttu-id="4f51e-106">Настраиваемые действия могут добавлять, изменять или удалять временные строки, столбцы или таблицы из базы данных.</span><span class="sxs-lookup"><span data-stu-id="4f51e-106">Custom actions can only add, modify, or remove temporary rows, columns, or tables from a database.</span></span> <span data-ttu-id="4f51e-107">Настраиваемые действия не могут изменять постоянные данные в базе данных, например данные, которые являются частью базы данных, хранящейся на диске.</span><span class="sxs-lookup"><span data-stu-id="4f51e-107">Custom actions cannot modify persistent data in a database, for example, data that is a part of the database stored on disk.</span></span>

[<span data-ttu-id="4f51e-108">Библиотеки динамической компоновки</span><span class="sxs-lookup"><span data-stu-id="4f51e-108">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)

<span data-ttu-id="4f51e-109">Для доступа к выполняющейся установке настраиваемые действия, вызывающие библиотеки динамической компоновки (DLL), передаются в качестве единственного аргумента для точки входа DLL, именуемой в столбце Target [таблицы CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="4f51e-109">To access a running installation, custom actions that call dynamic-link libraries (DLL) are passed a handle of the type MSIHANDLE for the current session as the only argument to the DLL entry point named in the Target column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="4f51e-110">Поскольку установщик предоставляет этот обработчик, пользовательское действие не должно закрывать его, например, для получения маркера *хинсталл* из установщика, функция настраиваемого действия объявляется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="4f51e-110">Because the installer provides this handle, the custom action should not close it, for example, to receive the handle *hInstall* from the installer, the custom action function is declared as follows.</span></span>


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="4f51e-111">Для доступа только для чтения к текущей базе данных получите маркер базы данных путем вызова [**метод msigetactivedatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span><span class="sxs-lookup"><span data-stu-id="4f51e-111">For read-only access to the current database obtain the database handle by calling [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span></span> <span data-ttu-id="4f51e-112">Дополнительные сведения см. [в разделе Получение маркера базы данных](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="4f51e-112">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

[<span data-ttu-id="4f51e-113">Создание и запуск скриптов PowerShell из консоли Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4f51e-113">Scripts</span></span>](scripts.md)

<span data-ttu-id="4f51e-114">Настраиваемые действия, написанные на языке VBScript или JScript, могут обращаться к текущему сеансу установки с помощью [**объекта Session**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="4f51e-114">Custom actions written in VBScript or JScript can access the current installation session by using the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="4f51e-115">Установщик создает объект **сеанса** с именем Session, который ссылается на текущую установку.</span><span class="sxs-lookup"><span data-stu-id="4f51e-115">The installer creates a **Session** object named "Session" that references the current installation.</span></span> <span data-ttu-id="4f51e-116">Для доступа только для чтения к текущей базе данных используйте свойство [**Database**](session-database.md) объекта **Session** .</span><span class="sxs-lookup"><span data-stu-id="4f51e-116">For read-only access to the current database use the [**Database**](session-database.md) property of the **Session** object.</span></span>

<span data-ttu-id="4f51e-117">Поскольку скрипт запускается из контекста объекта [**Session**](session-object.md) , не всегда нужно указывать полные свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="4f51e-117">Because a script is run from the context of the [**Session**](session-object.md) object, it is not always necessary to fully qualify properties and methods.</span></span> <span data-ttu-id="4f51e-118">В следующем примере при использовании VBScript ссылка Me может заменить объект **Session** , например, следующие три строки эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="4f51e-118">In the following example, when using VBScript, the Me reference can replace the **Session** object, for example, the following three lines are equivalent.</span></span>


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[<span data-ttu-id="4f51e-119">Исполняемые файлы</span><span class="sxs-lookup"><span data-stu-id="4f51e-119">Executable Files</span></span>](executable-files.md)

<span data-ttu-id="4f51e-120">Невозможно получить доступ к текущему сеансу установщика из пользовательских действий, которые вызывают исполняемые файлы, запускаемые с помощью командной строки, например, [тип настраиваемого действия 2](custom-action-type-2.md) и [тип настраиваемого действия 18](custom-action-type-18.md).</span><span class="sxs-lookup"><span data-stu-id="4f51e-120">You cannot access the current installer session from custom actions that call executable files launched with a command-line, for example, [Custom Action Type 2](custom-action-type-2.md) and [Custom Action Type 18](custom-action-type-18.md).</span></span>

[<span data-ttu-id="4f51e-121">Пользовательские действия отложенного выполнения</span><span class="sxs-lookup"><span data-stu-id="4f51e-121">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)

<span data-ttu-id="4f51e-122">Невозможно получить доступ к текущему сеансу установщика или ко всем данным свойств из настраиваемого действия отложенного выполнения.</span><span class="sxs-lookup"><span data-stu-id="4f51e-122">You cannot access the current installer session or all property data from a deferred execution custom action.</span></span> <span data-ttu-id="4f51e-123">Дополнительные сведения см. в разделе [Получение контекстных сведений для отложенного выполнения настраиваемых действий](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="4f51e-123">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f51e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="4f51e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f51e-125">Доступ к базе данных или сеансу из настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="4f51e-125">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



