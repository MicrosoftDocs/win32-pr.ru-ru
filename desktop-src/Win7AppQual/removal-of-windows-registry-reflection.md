---
description: .
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Удаление отражения реестра Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c610cb0b6ce446e3105fd61cb940028f478892ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703025"
---
# <a name="removal-of-windows-registry-reflection"></a><span data-ttu-id="d9d90-103">Удаление отражения реестра Windows</span><span class="sxs-lookup"><span data-stu-id="d9d90-103">Removal of Windows Registry Reflection</span></span>

## <a name="platform"></a><span data-ttu-id="d9d90-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="d9d90-104">Platform</span></span>

<span data-ttu-id="d9d90-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="d9d90-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="d9d90-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d9d90-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="d9d90-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="d9d90-107">Feature Impact</span></span>

 <span data-ttu-id="d9d90-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="d9d90-108">**Severity** - Low</span></span>  
<span data-ttu-id="d9d90-109">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="d9d90-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="d9d90-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d9d90-110">Description</span></span>

<span data-ttu-id="d9d90-111">Процесс отражения реестра копирует разделы и значения реестра между двумя представлениями реестра, чтобы синхронизировать их. В предыдущих 64-разрядных установках Windows процесс отражал подмножество перенаправленных разделов реестра между 32-битным и 64-битным представлениями.</span><span class="sxs-lookup"><span data-stu-id="d9d90-111">The registry reflection process copies registry keys and values between two registry views to keep them in synch. In previous 64-bit installations of Windows, the process reflected a subset of the redirected registry keys between the 32-bit and 64-bit views.</span></span> <span data-ttu-id="d9d90-112">Однако реализация этого метода привела к несогласованности в состоянии реестра.</span><span class="sxs-lookup"><span data-stu-id="d9d90-112">However, the implementation of this caused some inconsistencies in the state of the registry.</span></span> <span data-ttu-id="d9d90-113">(Дополнительные сведения об отражении реестра см. в соответствующей статье MSDN в разделе *ссылки на другие ресурсы* ниже.)</span><span class="sxs-lookup"><span data-stu-id="d9d90-113">(For details on Registry Reflection, please refer to the corresponding MSDN article in the *Links to Other Resources* section below.)</span></span>

<span data-ttu-id="d9d90-114">Начиная с Windows 7, мы полностью удалили отражение реестра и объединили ключи, которые использовались для отражения:</span><span class="sxs-lookup"><span data-stu-id="d9d90-114">Starting with Windows 7, we have removed registry reflection completely and merged the keys that used to be reflected:</span></span>

-   <span data-ttu-id="d9d90-115">\_ \_ \\ Классы программного обеспечения для локального компьютера hKey \\</span><span class="sxs-lookup"><span data-stu-id="d9d90-115">HKEY\_LOCAL\_MACHINE\\Software\\Classes</span></span>
-   <span data-ttu-id="d9d90-116">HKEY \_ \_ \\ программное обеспечение на локальном компьютере \\ Microsoft \\ COM3</span><span class="sxs-lookup"><span data-stu-id="d9d90-116">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\COM3</span></span>
-   <span data-ttu-id="d9d90-117">HKEY \_ \_ по локального компьютера \\ программное обеспечение \\ Microsoft \\ EventSystem</span><span class="sxs-lookup"><span data-stu-id="d9d90-117">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\EventSystem</span></span>
-   <span data-ttu-id="d9d90-118">HKEY \_ по для локального \_ компьютера, \\ \\ Microsoft \\ OLE</span><span class="sxs-lookup"><span data-stu-id="d9d90-118">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Ole</span></span>
-   <span data-ttu-id="d9d90-119">HKEY \_ \_ \\ программное обеспечение локального компьютера \\ Microsoft \\ RPC</span><span class="sxs-lookup"><span data-stu-id="d9d90-119">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc</span></span>
-   <span data-ttu-id="d9d90-120">\_Классы пользовательских \\ \* \\ программ \\ hKey</span><span class="sxs-lookup"><span data-stu-id="d9d90-120">HKEY\_USERS\\\*\\Software\\Classes</span></span>
-   <span data-ttu-id="d9d90-121">\_Классы пользователей \\ \* \_ hKey</span><span class="sxs-lookup"><span data-stu-id="d9d90-121">HKEY\_USERS\\\*\_Classes</span></span>

<span data-ttu-id="d9d90-122">Фактически это обеспечивает то же поведение отражения, так как изменения этих ключей немедленно доступны как для 32-разрядных, так и для 64-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="d9d90-122">Effectively, this provides the same reflection behavior, since changes to these keys immediately are available for both 32-bit and 64-bit applications.</span></span>

<span data-ttu-id="d9d90-123">Ключи, которые были отражены условно, остаются разбитыми:</span><span class="sxs-lookup"><span data-stu-id="d9d90-123">The keys that were reflected conditionally remain split:</span></span>

-   <span data-ttu-id="d9d90-124">\_ \_ \\ Классы программного обеспечения для локального компьютера hKey \\ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="d9d90-124">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="d9d90-125">\_ \_ \\ Интерфейс классов программного \\ обеспечения \\ для локального компьютера hKey</span><span class="sxs-lookup"><span data-stu-id="d9d90-125">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="d9d90-126">\_Классы для пользователей \\ \* \\ программного обеспечения hKey \\ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="d9d90-126">HKEY\_USERS\\\*\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="d9d90-127">\_ \\ \* \\ Интерфейс классов пользователей программного обеспечения \\ \\ hKey</span><span class="sxs-lookup"><span data-stu-id="d9d90-127">HKEY\_USERS\\\*\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="d9d90-128">\_Классы пользователей hKey \\ \* \_ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="d9d90-128">HKEY\_USERS\\\*\_Classes\\CLSID</span></span>
-   <span data-ttu-id="d9d90-129">\_ \\ \* \_ Интерфейс классов пользователей \\ hKey</span><span class="sxs-lookup"><span data-stu-id="d9d90-129">HKEY\_USERS\\\*\_Classes\\Interface</span></span>

<span data-ttu-id="d9d90-130">Они используются для сохранения данных, которые не должны совместно использоваться для 32-разрядных и 64-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="d9d90-130">They are used to keep the data that should not be shared between 32-bit and 64-bit applications.</span></span>

## <a name="manifestation"></a><span data-ttu-id="d9d90-131">Проявление</span><span class="sxs-lookup"><span data-stu-id="d9d90-131">Manifestation</span></span>

<span data-ttu-id="d9d90-132">CLSID и ключи интерфейса из приведенного выше списка больше не отражаются, пока они еще перенаправляются.</span><span class="sxs-lookup"><span data-stu-id="d9d90-132">CLSID and Interface keys from the list above are not reflected anymore while they are still redirected.</span></span> <span data-ttu-id="d9d90-133">Хотя это желаемое поведение в большинстве случаев, приложения могут зависеть от их отраженного поведения в Vista.</span><span class="sxs-lookup"><span data-stu-id="d9d90-133">While this is the desired behavior in most of cases, it is possible that applications could take a dependency on their reflected behavior in Vista.</span></span>

<span data-ttu-id="d9d90-134">Функции, позволяющие приложениям управлять отражением (Регдисаблерефлектионкэй и Реженаблерефлектионкэй), — это не Ops в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d9d90-134">The functions allowing applications to control reflection (RegDisableReflectionKey and RegEnableReflectionKey) are no-ops in Windows 7.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="d9d90-135">Снижение влияния</span><span class="sxs-lookup"><span data-stu-id="d9d90-135">Mitigation of Impact</span></span>

<span data-ttu-id="d9d90-136">COM является основным потребителем отражения в реестре.</span><span class="sxs-lookup"><span data-stu-id="d9d90-136">COM is the major consumer of registry reflection.</span></span> <span data-ttu-id="d9d90-137">COM и другие потребители были обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="d9d90-137">COM and other consumers were updated to accommodate this change.</span></span> <span data-ttu-id="d9d90-138">Это изменение не влияет на приложения, использующие стандартные API-интерфейсы COM.</span><span class="sxs-lookup"><span data-stu-id="d9d90-138">This change does not affect applications that use standard COM APIs..</span></span>

## <a name="solution"></a><span data-ttu-id="d9d90-139">Решение</span><span class="sxs-lookup"><span data-stu-id="d9d90-139">Solution</span></span>

<span data-ttu-id="d9d90-140">Примените один из следующих вариантов, если вы полагаетесь на отражение реестра для синхронизации 32-разрядных и 64-разрядных представлений:</span><span class="sxs-lookup"><span data-stu-id="d9d90-140">Apply one of the following options if you are relying on registry reflection to synchronize 32bit and 64bit views:</span></span>

-   <span data-ttu-id="d9d90-141">Явное создание ключей в обоих представлениях во время установки</span><span class="sxs-lookup"><span data-stu-id="d9d90-141">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="d9d90-142">Перемещение ключей из области отраженных ключей</span><span class="sxs-lookup"><span data-stu-id="d9d90-142">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="d9d90-143">Проверьте оба представления реестра при запросе отраженного ключа.</span><span class="sxs-lookup"><span data-stu-id="d9d90-143">Check both views of the registry when querying for a reflected key</span></span>

    <span data-ttu-id="d9d90-144">**Примечание.** КЛЮЧ \_ WOW64 \_ 32KEY и ключ \_ WOW64 \_ 64KEY не могут быть объединены</span><span class="sxs-lookup"><span data-stu-id="d9d90-144">**Note:** KEY\_WOW64\_32KEY and KEY\_WOW64\_64KEY flags cannot be combined</span></span>

<span data-ttu-id="d9d90-145">Примените один из следующих вариантов, если вы используете функции Регдисаблерефлектионкэй для отключения отражения реестра:</span><span class="sxs-lookup"><span data-stu-id="d9d90-145">Apply one of the following options if you are relying on RegDisableReflectionKey functions to disable registry reflection:</span></span>

-   <span data-ttu-id="d9d90-146">Явное создание ключей в обоих представлениях во время установки</span><span class="sxs-lookup"><span data-stu-id="d9d90-146">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="d9d90-147">Перемещение ключей из области отраженных ключей</span><span class="sxs-lookup"><span data-stu-id="d9d90-147">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="d9d90-148">Использование подразделов, зависящих от платформы (например, x86, AMD64 и ia64), для разделения данных, зависящих от разрядности</span><span class="sxs-lookup"><span data-stu-id="d9d90-148">Use platform-specific subkeys (like x86, amd64 and ia64) to separate bitness-specific data</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="d9d90-149">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="d9d90-149">Links to Other Resources</span></span>

-   [<span data-ttu-id="d9d90-150">Статья о отражении реестра</span><span class="sxs-lookup"><span data-stu-id="d9d90-150">Registry Reflection article</span></span>](../winprog64/registry-reflection.md)
-   [<span data-ttu-id="d9d90-151">Список перенаправленных ключей в статье о перенаправлении реестра</span><span class="sxs-lookup"><span data-stu-id="d9d90-151">Redirected keys list within Registry Redirector article</span></span>](../winprog64/registry-redirector.md)
-   [<span data-ttu-id="d9d90-152">Рекомендации по использованию WOW64</span><span class="sxs-lookup"><span data-stu-id="d9d90-152">Best Practices for Wow64</span></span>](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> <span data-ttu-id="d9d90-153">Эти ресурсы могут быть недоступны в некоторых языках и странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="d9d90-153">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
