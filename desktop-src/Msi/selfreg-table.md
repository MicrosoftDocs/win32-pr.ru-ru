---
description: Таблица Селфрег содержит сведения о модулях, которые должны быть зарегистрированы самостоятельно.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Таблица Селфрег
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5895b1d23369a7c121547fed841731b5d3e76ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818552"
---
# <a name="selfreg-table"></a><span data-ttu-id="d236e-103">Таблица Селфрег</span><span class="sxs-lookup"><span data-stu-id="d236e-103">SelfReg Table</span></span>

<span data-ttu-id="d236e-104">Таблица Селфрег содержит сведения о модулях, которые должны быть зарегистрированы самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="d236e-104">The SelfReg table contains information about modules that need to be self registered.</span></span> <span data-ttu-id="d236e-105">Установщик вызывает функцию [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) во время установки модуля. Он вызывает [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) во время удаления модуля.</span><span class="sxs-lookup"><span data-stu-id="d236e-105">The installer calls the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function during installation of the module; it calls [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) during uninstallation of the module.</span></span> <span data-ttu-id="d236e-106">Установщик не выполняет самостоятельную регистрацию EXE файлов.</span><span class="sxs-lookup"><span data-stu-id="d236e-106">The installer does not self register EXE files.</span></span>

<span data-ttu-id="d236e-107">Таблица Селфрег содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="d236e-107">The SelfReg table has the following columns.</span></span>



| <span data-ttu-id="d236e-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="d236e-108">Column</span></span> | <span data-ttu-id="d236e-109">Type</span><span class="sxs-lookup"><span data-stu-id="d236e-109">Type</span></span>                         | <span data-ttu-id="d236e-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="d236e-110">Key</span></span> | <span data-ttu-id="d236e-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="d236e-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="d236e-112">Файл\_</span><span class="sxs-lookup"><span data-stu-id="d236e-112">File\_</span></span> | [<span data-ttu-id="d236e-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="d236e-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="d236e-114">Да</span><span class="sxs-lookup"><span data-stu-id="d236e-114">Y</span></span>   | <span data-ttu-id="d236e-115">Нет</span><span class="sxs-lookup"><span data-stu-id="d236e-115">N</span></span>        |
| <span data-ttu-id="d236e-116">Стоимость</span><span class="sxs-lookup"><span data-stu-id="d236e-116">Cost</span></span>   | [<span data-ttu-id="d236e-117">Integer</span><span class="sxs-lookup"><span data-stu-id="d236e-117">Integer</span></span>](integer.md)       | <span data-ttu-id="d236e-118">Нет</span><span class="sxs-lookup"><span data-stu-id="d236e-118">N</span></span>   | <span data-ttu-id="d236e-119">Да</span><span class="sxs-lookup"><span data-stu-id="d236e-119">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d236e-120">Столбцы</span><span class="sxs-lookup"><span data-stu-id="d236e-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d236e-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="d236e-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="d236e-122">Внешний ключ в первый столбец [таблицы File](file-table.md) , указывающий модуль, который необходимо зарегистрировать.</span><span class="sxs-lookup"><span data-stu-id="d236e-122">External key into the first column of the [File table](file-table.md) indicating the module that needs to be registered.</span></span>

</dd> <dt>

<span data-ttu-id="d236e-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Маршрут</span><span class="sxs-lookup"><span data-stu-id="d236e-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="d236e-124">Стоимость регистрации модуля в байтах.</span><span class="sxs-lookup"><span data-stu-id="d236e-124">The cost of registering the module in bytes.</span></span> <span data-ttu-id="d236e-125">Это значение должно быть неотрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="d236e-125">This must be a non-negative number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d236e-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d236e-126">Remarks</span></span>

<span data-ttu-id="d236e-127">Авторы пакета установки настоятельно рекомендуется использовать самостоятельную регистрацию.</span><span class="sxs-lookup"><span data-stu-id="d236e-127">Installation package authors are strongly advised against using self registration.</span></span> <span data-ttu-id="d236e-128">Вместо этого они должны регистрировать модули путем создания одной или нескольких таблиц, предоставляемых установщиком для этой цели.</span><span class="sxs-lookup"><span data-stu-id="d236e-128">Instead they should register modules by authoring one or more tables provided by the installer for this purpose.</span></span> <span data-ttu-id="d236e-129">Дополнительные сведения см. в разделе « [таблицы реестра»](registry-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="d236e-129">For more information, see [Registry Tables Group](registry-tables-group.md).</span></span> <span data-ttu-id="d236e-130">Многие преимущества службы централизованного установщика теряются при самостоятельной регистрации, поскольку подпрограммы самостоятельной регистрации, как правило, скрывают важную информацию о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d236e-130">Many of the benefits of having a central installer service are lost with self registration because self-registration routines tend to hide critical configuration information.</span></span> <span data-ttu-id="d236e-131">Причины для предотвращения самостоятельной регистрации:</span><span class="sxs-lookup"><span data-stu-id="d236e-131">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="d236e-132">Откат установки с самостоятельными модулями не может быть безопасно выполнен с помощью [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) , так как нет способа определить, используются ли самостоятельные ключи другой функцией или приложением.</span><span class="sxs-lookup"><span data-stu-id="d236e-132">Rollback of an installation with self-registered modules cannot be safely done using [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) because there is no way of telling if the self-registered keys are used by another feature or application.</span></span>
-   <span data-ttu-id="d236e-133">Возможность использования объявления уменьшается, если регистрация сервера класса или расширения выполняется в подпрограммых самостоятельной регистрации.</span><span class="sxs-lookup"><span data-stu-id="d236e-133">The ability to use advertisement is reduced if Class or extension server registration is performed within self-registration routines.</span></span>
-   <span data-ttu-id="d236e-134">Установщик автоматически обрабатывает ключи HKCR в таблицах реестра для установки на уровне пользователя или на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d236e-134">The installer automatically handles HKCR keys in the registry tables for both per-user or per-machine installations.</span></span> <span data-ttu-id="d236e-135">В настоящее время подпрограммы [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) не поддерживают понятие ключа HKCR для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="d236e-135">[**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) routines currently do not support the notion of a per-user HKCR key.</span></span>
-   <span data-ttu-id="d236e-136">Если на одном компьютере используется самостоятельно зарегистрированное приложение, каждый пользователь должен установить приложение при первом его запуске.</span><span class="sxs-lookup"><span data-stu-id="d236e-136">If multiple users are using a self-registered application on the same computer, each user must install the application the first time they run it.</span></span> <span data-ttu-id="d236e-137">В противном случае установщик не сможет легко определить, что существуют соответствующие разделы реестра HKCU.</span><span class="sxs-lookup"><span data-stu-id="d236e-137">Otherwise the installer cannot easily determine that the proper HKCU registry keys exist.</span></span>
-   <span data-ttu-id="d236e-138">Функция [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) может запретить доступ к сетевым ресурсам, таким как библиотеки типов, если компонент задан как Run-from-Source и указан в таблице селфрег.</span><span class="sxs-lookup"><span data-stu-id="d236e-138">The [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) can be denied access to network resources such as type libraries if a component is both specified as run-from-source and is listed in the SelfReg table.</span></span> <span data-ttu-id="d236e-139">Это может привести к сбою установки компонента во время административной установки.</span><span class="sxs-lookup"><span data-stu-id="d236e-139">This can cause the installation of the component to fail to during an administrative installation.</span></span>
-   <span data-ttu-id="d236e-140">Библиотеки DLL с собственной регистрацией более уязвимы для ошибок программирования, поскольку новый код, необходимый для [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) , обычно отличается для каждой библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="d236e-140">Self-registering DLLs are more susceptible to coding errors because the new code required for [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) is commonly different for each DLL.</span></span> <span data-ttu-id="d236e-141">Вместо этого используйте таблицы реестра в базе данных, чтобы воспользоваться преимуществами существующего кода, предоставляемого установщиком.</span><span class="sxs-lookup"><span data-stu-id="d236e-141">Instead use the registry tables in the database to take advantage of existing code provided by the installer.</span></span>
-   <span data-ttu-id="d236e-142">Библиотеки DLL с собственной регистрацией иногда могут ссылаться на вспомогательные библиотеки DLL, которые отсутствуют или имеют неправильную версию.</span><span class="sxs-lookup"><span data-stu-id="d236e-142">Self-registering DLLs can sometimes link to auxiliary DLLs that are not present or are the wrong version.</span></span> <span data-ttu-id="d236e-143">В отличие от этого, установщик может зарегистрировать библиотеки DLL с помощью таблиц реестра без зависимости от текущего состояния системы.</span><span class="sxs-lookup"><span data-stu-id="d236e-143">In contrast, the installer can register the DLLs using the registry tables with no dependency on the current state of the system.</span></span>

> [!Note]  
> <span data-ttu-id="d236e-144">Нельзя указать порядок, в котором установщик регистрирует или отменяет регистрацию библиотек DLL с помощью действий [селфрегмодулес](selfregmodules-action.md) и [селфунрегмодулес](selfunregmodules-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d236e-144">You cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="d236e-145">См. раздел [Указание порядка самостоятельной регистрации](specifying-the-order-of-self-registration.md).</span><span class="sxs-lookup"><span data-stu-id="d236e-145">See [Specifying the Order of Self Registration](specifying-the-order-of-self-registration.md).</span></span>

 

## <a name="validation"></a><span data-ttu-id="d236e-146">Проверка</span><span class="sxs-lookup"><span data-stu-id="d236e-146">Validation</span></span>

<dl>

[<span data-ttu-id="d236e-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="d236e-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d236e-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="d236e-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d236e-149">ICE32</span><span class="sxs-lookup"><span data-stu-id="d236e-149">ICE32</span></span>](ice32.md)  
</dl>

 

 
