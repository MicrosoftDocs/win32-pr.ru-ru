---
description: Следующие функции можно использовать для определения текущей версии операционной системы или для определения того, является ли выпуск Windows или Windows Server.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Вспомогательные функции версии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746e6488d949fe6512355d7ef9910c26aaf3b54b
ms.sourcegitcommit: 49df0f62429d21bca96d8704205048267ee0eb59
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "105669521"
---
# <a name="version-helper-functions"></a><span data-ttu-id="4180d-103">Вспомогательные функции версии</span><span class="sxs-lookup"><span data-stu-id="4180d-103">Version Helper functions</span></span>

<span data-ttu-id="4180d-104">Следующие функции можно использовать для определения текущей версии операционной системы или для определения того, является ли выпуск Windows или Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4180d-104">The following functions can be used to determine the current operating system version or identify whether it is a Windows or Windows Server release.</span></span> <span data-ttu-id="4180d-105">Эти функции предоставляют простые тесты, в которых используется функция [верифиверсионинфо](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) и рекомендованное значение "больше или равно" для сравнений, проверенных как надежные средства для определения версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4180d-105">These functions provide simple tests that use the [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) function and the recommended greater than or equal to comparisons that are proven as a robust means to determine the operating system version.</span></span>

> [!Note]  
> <span data-ttu-id="4180d-106">Эти API-интерфейсы определяются **версионхелперс. h**, который входит в состав пакета средств разработки программного обеспечения (SDK) для Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="4180d-106">These APIs are defined by **versionhelpers.h**, which is included in the Windows 8.1 software development kit (SDK).</span></span> <span data-ttu-id="4180d-107">Этот файл можно использовать с другими выпусками Microsoft Visual Studio для реализации тех же функций для версий Windows, которые были выпущены до Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="4180d-107">This file can be used with other Microsoft Visual Studio releases to implement the same functionality for Windows versions prior to Windows 8.1.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4180d-108">Функция</span><span class="sxs-lookup"><span data-stu-id="4180d-108">Function</span></span></th>
<th><span data-ttu-id="4180d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4180d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4180d-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>исвиндовскспоргреатер</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-111">Указывает, совпадает ли текущая версия ОС с версией Windows XP или превышает ее.</span><span class="sxs-lookup"><span data-stu-id="4180d-111">Indicates if the current OS version matches, or is greater than, the Windows XP version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4180d-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-113">Указывает, совпадает ли текущая версия ОС с версией Windows XP с пакетом обновления 1 (SP1) или больше нее.</span><span class="sxs-lookup"><span data-stu-id="4180d-113">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4180d-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-115">Указывает, совпадает ли текущая версия ОС с версией Windows XP с пакетом обновления 2 (SP2) или больше нее.</span><span class="sxs-lookup"><span data-stu-id="4180d-115">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4180d-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-117">Указывает, совпадает ли текущая версия ОС с версией Windows XP с пакетом обновления 3 (SP3) или больше нее.</span><span class="sxs-lookup"><span data-stu-id="4180d-117">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 3 (SP3) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4180d-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>исвиндовсвистаоргреатер</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-119">Указывает, совпадает ли текущая версия ОС с версией Windows Vista или превышает ее.</span><span class="sxs-lookup"><span data-stu-id="4180d-119">Indicates if the current OS version matches, or is greater than, the Windows Vista version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4180d-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-121">Указывает, совпадает ли текущая версия ОС с версией Windows Vista с пакетом обновления 1 (SP1) или больше.</span><span class="sxs-lookup"><span data-stu-id="4180d-121">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4180d-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-123">Указывает, совпадает ли текущая версия ОС с версией Windows Vista с пакетом обновления 2 (SP2) или больше.</span><span class="sxs-lookup"><span data-stu-id="4180d-123">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4180d-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-125">Указывает, совпадает ли текущая версия ОС с версией Windows 7 или превышает ее.</span><span class="sxs-lookup"><span data-stu-id="4180d-125">Indicates if the current OS version matches, or is greater than, the Windows 7 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4180d-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-127">Указывает, совпадает ли текущая версия ОС с версией Windows 7 с пакетом обновления 1 (SP1) или больше нее.</span><span class="sxs-lookup"><span data-stu-id="4180d-127">Indicates if the current OS version matches, or is greater than, the Windows 7 with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4180d-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-129">Указывает, совпадает ли текущая версия ОС с версией Windows 8 или превышает ее.</span><span class="sxs-lookup"><span data-stu-id="4180d-129">Indicates if the current OS version matches, or is greater than, the Windows 8 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4180d-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-131">Указывает, совпадает ли текущая версия ОС с версией Windows 8.1 или больше нее.</span><span class="sxs-lookup"><span data-stu-id="4180d-131">Indicates if the current OS version matches, or is greater than, the Windows 8.1 version.</span></span><br/> <span data-ttu-id="4180d-132">Для Windows 10 <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> возвращает значение false, если приложение не содержит манифест, включающий в себя раздел Compatibility, содержащий идентификаторы GUID, указывающие Windows 8.1 и (или) Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4180d-132">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUIDs that designate Windows 8.1 and/or Windows 10.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4180d-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="4180d-134">Указывает, совпадает ли текущая версия ОС с версией Windows 10 или превышает ее.</span><span class="sxs-lookup"><span data-stu-id="4180d-134">Indicates if the current OS version matches, or is greater than, the Windows 10 version.</span></span><br/> <span data-ttu-id="4180d-135">Для Windows 10 <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> возвращает значение false, если приложение не содержит манифест, включающий в себя раздел Compatibility, содержащий идентификатор GUID, обозначающий Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4180d-135">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUID that designates Windows 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4180d-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>исвиндовссервер</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span></span></td>
<td><span data-ttu-id="4180d-137">Указывает, является ли текущая ОС выпуском Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4180d-137">Indicates if the current OS is a Windows Server release.</span></span> <span data-ttu-id="4180d-138">Приложения, которым необходимо различать серверные и клиентские версии Windows, должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="4180d-138">Applications that need to distinguish between server and client versions of Windows should call this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4180d-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>исвиндовсверсионоргреатер</strong></a></span><span class="sxs-lookup"><span data-stu-id="4180d-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span></span></td>
<td>
<blockquote><span data-ttu-id="4180d-140">Эту функцию следует использовать только в том случае, если другие предоставляемые вспомогательные функции версий не соответствуют вашему сценарию.</span><span class="sxs-lookup"><span data-stu-id="4180d-140">You should only use this function if the other provided version helper functions do not fit your scenario.</span></span></blockquote>
<br/><span data-ttu-id="4180d-141">Указывает, совпадает ли текущая версия ОС с предоставленными сведениями о версии или больше.</span><span class="sxs-lookup"><span data-stu-id="4180d-141">Indicates if the current OS version matches, or is greater than, the provided version information.</span></span> <span data-ttu-id="4180d-142">Эта функция полезна при подтверждении версии Windows Server, которая не поддерживает общий номер версии с выпуском клиента.</span><span class="sxs-lookup"><span data-stu-id="4180d-142">This function is useful in confirming a version of Windows Server that doesn't share a version number with a client release.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="4180d-143">Пример</span><span class="sxs-lookup"><span data-stu-id="4180d-143">Example</span></span>

<span data-ttu-id="4180d-144">Встроенные функции, определенные в файле заголовка **версионхелперс. h** , позволяют проверить версию операционной системы, возвращая **логическое** значение при тестировании для версии Windows.</span><span class="sxs-lookup"><span data-stu-id="4180d-144">The inline functions defined in the **VersionHelpers.h** header file let you verify the operating system version by returning a **Boolean** value when testing for a version of Windows.</span></span>

<span data-ttu-id="4180d-145">Например, если приложению требуется Windows 8 или более поздней версии, используйте следующий тест.</span><span class="sxs-lookup"><span data-stu-id="4180d-145">For example, if your application requires Windows 8 or later, use the following test.</span></span>

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a><span data-ttu-id="4180d-146">См. также</span><span class="sxs-lookup"><span data-stu-id="4180d-146">Related topics</span></span>

- [<span data-ttu-id="4180d-147">осверсионинфоекс</span><span class="sxs-lookup"><span data-stu-id="4180d-147">OSVERSIONINFOEX</span></span>](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
