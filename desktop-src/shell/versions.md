---
description: В этом разделе описывается, как определить версию библиотек DLL оболочки, на котором работает приложение, и как выбрать целевое приложение для конкретной версии.
title: 'Версии оболочки и Shlwapi DLL '
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 49fb1767b7074da6480a47c52eb1384fb935317b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264409"
---
# <a name="shell-and-shlwapi-dll-versions"></a><span data-ttu-id="3436c-103">Версии оболочки и Shlwapi DLL </span><span class="sxs-lookup"><span data-stu-id="3436c-103">Shell and Shlwapi DLL Versions</span></span>

<span data-ttu-id="3436c-104">В этом разделе описывается, как определить версию библиотек DLL оболочки, на котором работает приложение, и как выбрать целевое приложение для конкретной версии.</span><span class="sxs-lookup"><span data-stu-id="3436c-104">This section describes how to determine which version of the Shell DLLs your application is running on and how to target your application for a specific version.</span></span>

-   [<span data-ttu-id="3436c-105">Номера версий DLL</span><span class="sxs-lookup"><span data-stu-id="3436c-105">DLL Version Numbers</span></span>](#dll-version-numbers)
-   [<span data-ttu-id="3436c-106">Определение номера версии с помощью Дллжетверсион</span><span class="sxs-lookup"><span data-stu-id="3436c-106">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
    -   [<span data-ttu-id="3436c-107">Использование Дллжетверсион</span><span class="sxs-lookup"><span data-stu-id="3436c-107">Using DllGetVersion</span></span>](#using-dllgetversion)
-   [<span data-ttu-id="3436c-108">Версии проекта</span><span class="sxs-lookup"><span data-stu-id="3436c-108">Project Versions</span></span>](#project-versions)

## <a name="dll-version-numbers"></a><span data-ttu-id="3436c-109">Номера версий DLL</span><span class="sxs-lookup"><span data-stu-id="3436c-109">DLL Version Numbers</span></span>

<span data-ttu-id="3436c-110">Все элементы программирования, описанные в документации по оболочке, содержатся в двух библиотеках DLL: Shell32.dll и Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="3436c-110">All but a handful of the programming elements discussed in the Shell documentation are contained in two DLLs: Shell32.dll and Shlwapi.dll.</span></span> <span data-ttu-id="3436c-111">Из-за текущих улучшений различные версии этих библиотек DLL реализуют различные функции.</span><span class="sxs-lookup"><span data-stu-id="3436c-111">Because of ongoing enhancements, different versions of these DLLs implement different features.</span></span> <span data-ttu-id="3436c-112">В справочной документации по оболочке каждый программный элемент указывает минимальный поддерживаемый номер версии DLL.</span><span class="sxs-lookup"><span data-stu-id="3436c-112">Throughout the Shell reference documentation, each programming element specifies a minimum supported DLL version number.</span></span> <span data-ttu-id="3436c-113">Этот номер версии указывает, что программный элемент реализован в этой версии и последующих версиях библиотеки DLL, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="3436c-113">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="3436c-114">Если номер версии не указан, программный элемент реализуется во всех существующих версиях библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="3436c-114">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="3436c-115">До выхода Windows XP в новых версиях Windows Internet Explorer иногда появились новые Shell32.dll и Shlwapi.dll версии.</span><span class="sxs-lookup"><span data-stu-id="3436c-115">Before Windows XP, new Shell32.dll and Shlwapi.dll versions were sometimes provided with new versions of Windows Internet Explorer.</span></span> <span data-ttu-id="3436c-116">Начиная с Windows XP, эти библиотеки DLL больше не были предоставлены как распространяемые файлы за пределами новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="3436c-116">As of Windows XP, those DLLs were no longer provided as redistributable files outside of new versions of Windows itself.</span></span> <span data-ttu-id="3436c-117">В следующей таблице приведены различные версии DLL и способы их распространения датировано обратно в Microsoft Internet Explorer 3,0, Windows 95 и Microsoft Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="3436c-117">The following table outlines the different DLL versions and how they were distributed dating back to Microsoft Internet Explorer 3.0, Windows 95, and Microsoft Windows NT 4.0.</span></span>

<span data-ttu-id="3436c-118">Shell32.dll версии 4,0 находится в исходных версиях Windows 95 и Microsoft Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="3436c-118">Shell32.dll version 4.0 is found in the original versions of Windows 95 and Microsoft Windows NT 4.0.</span></span> <span data-ttu-id="3436c-119">Оболочка не была обновлена с выпуском Internet Explorer 3,0, поэтому Shell32.dll не имеет версии 4,70.</span><span class="sxs-lookup"><span data-stu-id="3436c-119">The Shell was not updated with the Internet Explorer 3.0 release, so Shell32.dll does not have a version 4.70.</span></span> <span data-ttu-id="3436c-120">Shell32.dll версии 4,71 и 4,72 были поставляются с соответствующими выпусками Internet Explorer, но они не обязательно были установлены (см. Примечание 1).</span><span class="sxs-lookup"><span data-stu-id="3436c-120">Shell32.dll versions 4.71 and 4.72 were shipped with the corresponding Internet Explorer releases, but they were not necessarily installed (see note 1).</span></span> <span data-ttu-id="3436c-121">Для выпусков, соответствующих Microsoft Internet Explorer 4,01 и Windows 98, Номера версий для Shell32.dll и Shlwapi.dll расходятся.</span><span class="sxs-lookup"><span data-stu-id="3436c-121">For releases subsequent to Microsoft Internet Explorer 4.01 and Windows 98, the version numbers for Shell32.dll and Shlwapi.dll diverge.</span></span> <span data-ttu-id="3436c-122">В общем случае следует предположить, что библиотеки DLL имеют разные номера версий и проверяют каждый из них отдельно.</span><span class="sxs-lookup"><span data-stu-id="3436c-122">In general, you should assume that the DLLs have different version numbers and test each one separately.</span></span>

#### <a name="shell32dll"></a><span data-ttu-id="3436c-123">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="3436c-123">Shell32.dll</span></span>

| <span data-ttu-id="3436c-124">Version</span><span class="sxs-lookup"><span data-stu-id="3436c-124">Version</span></span> | <span data-ttu-id="3436c-125">Платформа распространения</span><span class="sxs-lookup"><span data-stu-id="3436c-125">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="3436c-126">4,0</span><span class="sxs-lookup"><span data-stu-id="3436c-126">4.0</span></span>     | <span data-ttu-id="3436c-127">Windows 95 и Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="3436c-127">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="3436c-128">4,71</span><span class="sxs-lookup"><span data-stu-id="3436c-128">4.71</span></span>    | <span data-ttu-id="3436c-129">Microsoft Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="3436c-129">Microsoft Internet Explorer 4.0.</span></span> <span data-ttu-id="3436c-130">См. примечание 1.</span><span class="sxs-lookup"><span data-stu-id="3436c-130">See note 1.</span></span>                                |
| <span data-ttu-id="3436c-131">4,72</span><span class="sxs-lookup"><span data-stu-id="3436c-131">4.72</span></span>    | <span data-ttu-id="3436c-132">Internet Explorer 4,01 и Windows 98.</span><span class="sxs-lookup"><span data-stu-id="3436c-132">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="3436c-133">См. примечание 1.</span><span class="sxs-lookup"><span data-stu-id="3436c-133">See note 1.</span></span>                          |
| <span data-ttu-id="3436c-134">5.0</span><span class="sxs-lookup"><span data-stu-id="3436c-134">5.0</span></span>     | <span data-ttu-id="3436c-135">Windows 2000 и Windows Millennium Edition (Windows Me).</span><span class="sxs-lookup"><span data-stu-id="3436c-135">Windows 2000 and Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="3436c-136">См. Примечание 2.</span><span class="sxs-lookup"><span data-stu-id="3436c-136">See note 2.</span></span>       |
| <span data-ttu-id="3436c-137">6.0</span><span class="sxs-lookup"><span data-stu-id="3436c-137">6.0</span></span>     | <span data-ttu-id="3436c-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3436c-138">Windows XP</span></span>                                                                  |
| <span data-ttu-id="3436c-139">6.0.1</span><span class="sxs-lookup"><span data-stu-id="3436c-139">6.0.1</span></span>   | <span data-ttu-id="3436c-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3436c-140">Windows Vista</span></span>                                                               |
| <span data-ttu-id="3436c-141">6.1</span><span class="sxs-lookup"><span data-stu-id="3436c-141">6.1</span></span>     | <span data-ttu-id="3436c-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3436c-142">Windows 7</span></span>                                                                   |

#### <a name="shlwapidll"></a><span data-ttu-id="3436c-143">Shlwapi.dll</span><span class="sxs-lookup"><span data-stu-id="3436c-143">Shlwapi.dll</span></span>

| <span data-ttu-id="3436c-144">Version</span><span class="sxs-lookup"><span data-stu-id="3436c-144">Version</span></span> | <span data-ttu-id="3436c-145">Платформа распространения</span><span class="sxs-lookup"><span data-stu-id="3436c-145">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="3436c-146">4,0</span><span class="sxs-lookup"><span data-stu-id="3436c-146">4.0</span></span>     | <span data-ttu-id="3436c-147">Windows 95 и Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="3436c-147">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="3436c-148">4,71</span><span class="sxs-lookup"><span data-stu-id="3436c-148">4.71</span></span>    | <span data-ttu-id="3436c-149">Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="3436c-149">Internet Explorer 4.0.</span></span> <span data-ttu-id="3436c-150">См. примечание 1.</span><span class="sxs-lookup"><span data-stu-id="3436c-150">See note 1.</span></span>                                          |
| <span data-ttu-id="3436c-151">4,72</span><span class="sxs-lookup"><span data-stu-id="3436c-151">4.72</span></span>    | <span data-ttu-id="3436c-152">Internet Explorer 4,01 и Windows 98.</span><span class="sxs-lookup"><span data-stu-id="3436c-152">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="3436c-153">См. примечание 1.</span><span class="sxs-lookup"><span data-stu-id="3436c-153">See note 1.</span></span>                          |
| <span data-ttu-id="3436c-154">4.7</span><span class="sxs-lookup"><span data-stu-id="3436c-154">4.7</span></span>     | <span data-ttu-id="3436c-155">Internet Explorer 3. x</span><span class="sxs-lookup"><span data-stu-id="3436c-155">Internet Explorer 3.x</span></span>                                                       |
| <span data-ttu-id="3436c-156">5.0</span><span class="sxs-lookup"><span data-stu-id="3436c-156">5.0</span></span>     | <span data-ttu-id="3436c-157">Microsoft Internet Explorer 5 и Windows 98 SE.</span><span class="sxs-lookup"><span data-stu-id="3436c-157">Microsoft Internet Explorer 5 and Windows 98 SE.</span></span> <span data-ttu-id="3436c-158">См. Примечание 2.</span><span class="sxs-lookup"><span data-stu-id="3436c-158">See note 2.</span></span>                |
| <span data-ttu-id="3436c-159">5.5</span><span class="sxs-lookup"><span data-stu-id="3436c-159">5.5</span></span>     | <span data-ttu-id="3436c-160">Microsoft Internet Explorer 5,5 и Windows Millennium Edition (Windows Me)</span><span class="sxs-lookup"><span data-stu-id="3436c-160">Microsoft Internet Explorer 5.5 and Windows Millennium Edition (Windows Me)</span></span> |
| <span data-ttu-id="3436c-161">6.0</span><span class="sxs-lookup"><span data-stu-id="3436c-161">6.0</span></span>     | <span data-ttu-id="3436c-162">Windows XP и Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3436c-162">Windows XP and Windows Vista</span></span>                                                |



<span data-ttu-id="3436c-163">**Примечание 1.** Все системы с Internet Explorer 4,0 или 4,01 имеют связанную версию Shlwapi.dll (4,71 или 4,72 соответственно).</span><span class="sxs-lookup"><span data-stu-id="3436c-163">**Note 1:** All systems with Internet Explorer 4.0 or 4.01 had the associated version of Shlwapi.dll (4.71 or 4.72, respectively).</span></span> <span data-ttu-id="3436c-164">Однако для систем, предшествовавших Windows 98, Internet Explorer 4,0 и 4,01 можно установить с помощью среды или без нее, известной как *Интегрированная оболочка*.</span><span class="sxs-lookup"><span data-stu-id="3436c-164">However, for systems prior to Windows 98, Internet Explorer 4.0 and 4.01 can be installed with or without what was known as the *integrated Shell*.</span></span> <span data-ttu-id="3436c-165">Если Internet Explorer был установлен с интегрированной оболочкой, также была установлена соответствующая версия Shell32.dll (4,71 или 4,72).</span><span class="sxs-lookup"><span data-stu-id="3436c-165">If Internet Explorer was installed with the integrated Shell, the associated version of Shell32.dll (4.71 or 4.72) was also installed.</span></span> <span data-ttu-id="3436c-166">Если Internet Explorer был установлен без интегрированной оболочки, Shell32.dll остается версией 4,0.</span><span class="sxs-lookup"><span data-stu-id="3436c-166">If Internet Explorer was installed without the integrated Shell, Shell32.dll remained as version 4.0.</span></span> <span data-ttu-id="3436c-167">Иными словами, наличие версии 4,71 или 4,72 Shlwapi.dll в системе не гарантирует, что Shell32.dll имеет тот же номер версии.</span><span class="sxs-lookup"><span data-stu-id="3436c-167">In other words, the presence of version 4.71 or 4.72 of Shlwapi.dll on a system does not guarantee that Shell32.dll has the same version number.</span></span> <span data-ttu-id="3436c-168">Все системы Windows 98 имеют версию 4,72 Shell32.dll.</span><span class="sxs-lookup"><span data-stu-id="3436c-168">All Windows 98 systems have version 4.72 of Shell32.dll.</span></span>

<span data-ttu-id="3436c-169">**Примечание 2.** Версия 5,0 Shlwapi.dll была распространена с Internet Explorer 5 и обнаружена во всех системах, где был установлен Internet Explorer 5, за исключением Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3436c-169">**Note 2:** Version 5.0 of Shlwapi.dll was distributed with Internet Explorer 5 and was found on all systems on which Internet Explorer 5 was installed, with the exception of Windows 2000.</span></span> <span data-ttu-id="3436c-170">Версия 5,0 Shell32.dll была изначально распространена с Windows 2000 и Windows Millennium Edition (Windows Me) вместе с Shlwapi.dllом версии 5,0.</span><span class="sxs-lookup"><span data-stu-id="3436c-170">Version 5.0 of Shell32.dll was distributed natively with Windows 2000 and Windows Millennium Edition (Windows Me), together with version 5.0 of Shlwapi.dll.</span></span>

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="3436c-171">Определение номера версии с помощью Дллжетверсион</span><span class="sxs-lookup"><span data-stu-id="3436c-171">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="3436c-172">Начиная с версии 4,71 библиотеки DLL оболочки, в других случаях, начали экспортировать [**дллжетверсион**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="3436c-172">Starting with version 4.71, the Shell DLLs, among others, began exporting [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="3436c-173">Эта функция может быть вызвана приложением для определения версии библиотеки DLL, имеющейся в системе.</span><span class="sxs-lookup"><span data-stu-id="3436c-173">This function can be called by an application to determine which DLL version is present on the system.</span></span>

> [!Note]  
> <span data-ttu-id="3436c-174">Библиотеки DLL не обязательно экспортируют [**дллжетверсион**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="3436c-174">DLLs do not necessarily export [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="3436c-175">Прежде чем пытаться использовать его, всегда проверяйте его.</span><span class="sxs-lookup"><span data-stu-id="3436c-175">Always test for it before attempting to use it.</span></span>

<span data-ttu-id="3436c-176">Для версий Windows, предшествующих Windows 2000, [**дллжетверсион**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) возвращает структуру [**дллверсионинфо**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) , которая содержит основной и дополнительный номера версии, номер сборки и идентификатор платформы.</span><span class="sxs-lookup"><span data-stu-id="3436c-176">For Windows versions earlier than Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure that contains the major and minor version numbers, the build number, and a platform ID.</span></span> <span data-ttu-id="3436c-177">Для систем Windows 2000 и более поздних версий **дллжетверсион** может возвращать структуру [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="3436c-177">For Windows 2000 and later systems, **DllGetVersion** might instead return a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="3436c-178">Помимо информации, предоставляемой через **дллверсионинфо**, **DLLVERSIONINFO2** также предоставляет номер исправления, который определяет последний установленный пакет обновления, что обеспечивает более надежный способ сравнения номеров версий.</span><span class="sxs-lookup"><span data-stu-id="3436c-178">In addition to the information provided through **DLLVERSIONINFO**, **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="3436c-179">Поскольку первый элемент **DLLVERSIONINFO2** является структурой **дллверсионинфо** , более поздняя структура является обратно совместимой.</span><span class="sxs-lookup"><span data-stu-id="3436c-179">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>

### <a name="using-dllgetversion"></a><span data-ttu-id="3436c-180">Использование Дллжетверсион</span><span class="sxs-lookup"><span data-stu-id="3436c-180">Using DllGetVersion</span></span>

<span data-ttu-id="3436c-181">Следующий пример функции `GetVersion` загружает указанную библиотеку DLL и пытается вызвать ее функцию [**дллжетверсион**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) .</span><span class="sxs-lookup"><span data-stu-id="3436c-181">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="3436c-182">В случае успеха он использует макрос для упаковки основного и дополнительного номеров версий из структуры [**дллверсионинфо**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) в **DWORD** , возвращаемый вызывающему приложению.</span><span class="sxs-lookup"><span data-stu-id="3436c-182">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="3436c-183">Если библиотека DLL не экспортирует **дллжетверсион**, функция возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3436c-183">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="3436c-184">В Windows 2000 и более поздних системах можно изменить функцию, чтобы решить, что **дллжетверсион** возвращает структуру [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="3436c-184">With Windows 2000 and later systems, you can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="3436c-185">Если это так, используйте сведения в элементе **уллверсион** структуры **DLLVERSIONINFO2** для сравнения версий, номеров сборки и выпусков пакетов обновления.</span><span class="sxs-lookup"><span data-stu-id="3436c-185">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="3436c-186">Макрос [**македллверулл**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) упрощает задачу сравнения этих значений с ними в **уллверсион**.</span><span class="sxs-lookup"><span data-stu-id="3436c-186">The [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="3436c-187">Неправильное использование [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) может представлять угрозу безопасности.</span><span class="sxs-lookup"><span data-stu-id="3436c-187">Using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="3436c-188">Сведения о правильной загрузке библиотек DLL с разными версиями Windows см. в документации по **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="3436c-188">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


<span data-ttu-id="3436c-189">В следующем примере кода показано, как можно использовать `GetVersion` , чтобы проверить, имеет ли Shell32.dll версию 6,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="3436c-189">The following code example illustrates how you can use `GetVersion` to test whether Shell32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a><span data-ttu-id="3436c-190">Версии проекта</span><span class="sxs-lookup"><span data-stu-id="3436c-190">Project Versions</span></span>

<span data-ttu-id="3436c-191">Чтобы обеспечить совместимость приложения с различными целевыми версиями DLL-файла, в файлах заголовков есть макросы версии.</span><span class="sxs-lookup"><span data-stu-id="3436c-191">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="3436c-192">Эти макросы используются для определения, исключения или переопределения определенных определений для различных версий библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="3436c-192">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="3436c-193">Подробное описание этих макросов см. в разделе [Использование заголовков Windows](../winprog/using-the-windows-headers.md) .</span><span class="sxs-lookup"><span data-stu-id="3436c-193">See [Using the Windows Headers](../winprog/using-the-windows-headers.md) for an in-depth description of these macros.</span></span>

<span data-ttu-id="3436c-194">Например, имя макроса **\_ Win32 \_ IE** обычно находится в более старых заголовках.</span><span class="sxs-lookup"><span data-stu-id="3436c-194">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="3436c-195">Вы несете ответственность за определение макроса в виде шестнадцатеричного числа.</span><span class="sxs-lookup"><span data-stu-id="3436c-195">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="3436c-196">Этот номер версии определяет целевую версию приложения, использующего библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="3436c-196">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="3436c-197">В следующей таблице показаны доступные номера версий и их воздействие на приложение.</span><span class="sxs-lookup"><span data-stu-id="3436c-197">The following table shows the available version numbers and the effect each has on your application.</span></span>


| <span data-ttu-id="3436c-198">Версия</span><span class="sxs-lookup"><span data-stu-id="3436c-198">Version</span></span> | <span data-ttu-id="3436c-199">Описание</span><span class="sxs-lookup"><span data-stu-id="3436c-199">Description</span></span>                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3436c-200">0x0200</span><span class="sxs-lookup"><span data-stu-id="3436c-200">0x0200</span></span>  | <span data-ttu-id="3436c-201">Приложение совместимо с Shell32.dll версии 4,00 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3436c-201">The application is compatible with Shell32.dll version 4.00 and later.</span></span> <span data-ttu-id="3436c-202">Приложение не может реализовывать функции, которые были добавлены после версии 4,00.</span><span class="sxs-lookup"><span data-stu-id="3436c-202">The application cannot implement features that were added after version 4.00.</span></span>                                              |
| <span data-ttu-id="3436c-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="3436c-203">0x0300</span></span>  | <span data-ttu-id="3436c-204">Приложение совместимо с Shell32.dll версии 4,70 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3436c-204">The application is compatible with Shell32.dll version 4.70 and later.</span></span> <span data-ttu-id="3436c-205">Приложение не может реализовывать функции, которые были добавлены после версии 4,70.</span><span class="sxs-lookup"><span data-stu-id="3436c-205">The application cannot implement features that were added after version 4.70.</span></span>                                              |
| <span data-ttu-id="3436c-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="3436c-206">0x0400</span></span>  | <span data-ttu-id="3436c-207">Приложение совместимо с Shell32.dll версии 4,71 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3436c-207">The application is compatible with Shell32.dll version 4.71 and later.</span></span> <span data-ttu-id="3436c-208">Приложение не может реализовывать функции, которые были добавлены после версии 4,71.</span><span class="sxs-lookup"><span data-stu-id="3436c-208">The application cannot implement features that were added after version 4.71.</span></span>                                              |
| <span data-ttu-id="3436c-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="3436c-209">0x0401</span></span>  | <span data-ttu-id="3436c-210">Приложение совместимо с Shell32.dll версии 4,72 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3436c-210">The application is compatible with Shell32.dll version 4.72 and later.</span></span> <span data-ttu-id="3436c-211">Приложение не может реализовывать функции, которые были добавлены после версии 4,72.</span><span class="sxs-lookup"><span data-stu-id="3436c-211">The application cannot implement features that were added after version 4.72.</span></span>                                              |
| <span data-ttu-id="3436c-212">0x0500</span><span class="sxs-lookup"><span data-stu-id="3436c-212">0x0500</span></span>  | <span data-ttu-id="3436c-213">Приложение совместимо с Shell32.dll и Shlwapi.dll версии 5,0 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3436c-213">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="3436c-214">Приложение не может реализовывать функции, добавленные после Shell32.dll и Shlwapi.dll версии 5,0.</span><span class="sxs-lookup"><span data-stu-id="3436c-214">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="3436c-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="3436c-215">0x0501</span></span>  | <span data-ttu-id="3436c-216">Приложение совместимо с Shell32.dll и Shlwapi.dll версии 5,0 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3436c-216">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="3436c-217">Приложение не может реализовывать функции, добавленные после Shell32.dll и Shlwapi.dll версии 5,0.</span><span class="sxs-lookup"><span data-stu-id="3436c-217">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="3436c-218">0x0600</span><span class="sxs-lookup"><span data-stu-id="3436c-218">0x0600</span></span>  | <span data-ttu-id="3436c-219">Приложение совместимо с Shell32.dll и Shlwapi.dll версии 6,0 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3436c-219">The application is compatible with Shell32.dll and Shlwapi.dll version 6.0 and later.</span></span> <span data-ttu-id="3436c-220">Приложение не может реализовывать функции, добавленные после Shell32.dll и Shlwapi.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="3436c-220">The application cannot implement features that were added after version 6.0 of Shell32.dll and Shlwapi.dll.</span></span> |


<span data-ttu-id="3436c-221">Если в проекте не определен макрос **\_ Win32 \_ IE** , он автоматически определяется как 0x0500.</span><span class="sxs-lookup"><span data-stu-id="3436c-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="3436c-222">Чтобы определить другое значение, можно добавить следующий объект в директивы компилятора в файле make. Замените требуемый номер версии для 0x0400.</span><span class="sxs-lookup"><span data-stu-id="3436c-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>

```
/D _WIN32_IE=0x0400
```

<span data-ttu-id="3436c-223">Другой способ — добавить строку, аналогичную приведенной ниже, в исходный код перед включением файлов заголовков оболочки.</span><span class="sxs-lookup"><span data-stu-id="3436c-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="3436c-224">Замените требуемый номер версии для 0x0400.</span><span class="sxs-lookup"><span data-stu-id="3436c-224">Substitute the desired version number for 0x0400.</span></span>

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
