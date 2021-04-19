---
Description: Константы КНОВНФОЛДЕРИД представляют идентификаторы GUID, которые определяют стандартные папки, зарегистрированные в системе как известные папки.
ms.assetid: f2c08ade-3083-44e4-82b0-dde45f0e3094
title: КНОВНФОЛДЕРИД (Кновнфолдерс. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 97748d074d6b0982708f51ea679f0629e8abfad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987434"
---
# <a name="knownfolderid"></a><span data-ttu-id="33615-103">кновнфолдерид</span><span class="sxs-lookup"><span data-stu-id="33615-103">KNOWNFOLDERID</span></span>

<span data-ttu-id="33615-104">Константы **кновнфолдерид** представляют идентификаторы GUID, которые определяют стандартные папки, зарегистрированные в системе как [известные папки](known-folders.md).</span><span class="sxs-lookup"><span data-stu-id="33615-104">The **KNOWNFOLDERID** constants represent GUIDs that identify standard folders registered with the system as [Known Folders](known-folders.md).</span></span> <span data-ttu-id="33615-105">Эти папки устанавливаются вместе с Windows Vista и более поздними операционными системами, и на компьютере будут находиться только папки, соответствующие установленной версии.</span><span class="sxs-lookup"><span data-stu-id="33615-105">These folders are installed with Windows Vista and later operating systems, and a computer will have only folders appropriate to it installed.</span></span> <span data-ttu-id="33615-106">Описания этих папок см. в разделе [**CSid**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="33615-106">For descriptions of these folders, see [**CSIDL**](csidl.md).</span></span>

## <a name="example"></a><span data-ttu-id="33615-107">Например, .</span><span class="sxs-lookup"><span data-stu-id="33615-107">Example</span></span>

```c
HRESULT CExplorerBrowserHostDialog::_FillViewWithKnownFolders(IResultsFolder *prf)
{
    IKnownFolderManager *pManager;
    HRESULT hr = CoCreateInstance(CLSID_KnownFolderManager, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pManager));
    if (SUCCEEDED(hr))
    {
        UINT cCount;
        KNOWNFOLDERID *pkfid;

        hr = pManager->GetFolderIds(&pkfid, &cCount);
        if (SUCCEEDED(hr))
        {
            for (UINT i = 0; i < cCount; i++)
            {
                IKnownFolder *pKnownFolder;
                hr = pManager->GetFolder(pkfid[i], &pKnownFolder);
                if (SUCCEEDED(hr))
                {
                    IShellItem *psi;
                    hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                    if (SUCCEEDED(hr))
                    {
                        hr = prf->AddItem(psi);
                        psi->Release();
                    }
                    pKnownFolder->Release();
                }
            }
            CoTaskMemFree(pkfid);
        }
        pManager->Release();
    }
    return hr;
}

```

<span data-ttu-id="33615-108">Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="33615-108">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="33615-109">Константы</span><span class="sxs-lookup"><span data-stu-id="33615-109">Constants</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="33615-110">Константа</span><span class="sxs-lookup"><span data-stu-id="33615-110">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="33615-111">Описание</span><span class="sxs-lookup"><span data-stu-id="33615-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AccountPictures"></span><span id="folderid_accountpictures"></span><span id="FOLDERID_ACCOUNTPICTURES"></span><dl> <span data-ttu-id="33615-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-113">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-113">GUID</span></span></td>
<td><span data-ttu-id="33615-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span><span class="sxs-lookup"><span data-stu-id="33615-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-115">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-115">Display Name</span></span></td>
<td><span data-ttu-id="33615-116">Аватары</span><span class="sxs-lookup"><span data-stu-id="33615-116">Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-117">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-117">Folder Type</span></span></td>
<td><span data-ttu-id="33615-118">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-118">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-119">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-119">Default Path</span></span></td>
<td><span data-ttu-id="33615-120">%аппдата%\микрософт\виндовс\аккаунтпиктурес</span><span class="sxs-lookup"><span data-stu-id="33615-120">%APPDATA%\Microsoft\Windows\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-121">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-121">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-122">Нет, значение, введенное в Windows 8</span><span class="sxs-lookup"><span data-stu-id="33615-122">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-123">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-123">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-124">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-124">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-125">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-125">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-126">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-126">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AddNewPrograms"></span><span id="folderid_addnewprograms"></span><span id="FOLDERID_ADDNEWPROGRAMS"></span><dl> <span data-ttu-id="33615-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-128">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-128">GUID</span></span></td>
<td><span data-ttu-id="33615-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span><span class="sxs-lookup"><span data-stu-id="33615-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-130">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-130">Display Name</span></span></td>
<td><span data-ttu-id="33615-131">Получение программ</span><span class="sxs-lookup"><span data-stu-id="33615-131">Get Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-132">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-132">Folder Type</span></span></td>
<td><span data-ttu-id="33615-133">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-133">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-134">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-134">Default Path</span></span></td>
<td><span data-ttu-id="33615-135">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-135">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-136">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-136">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-137">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-137">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-138">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-138">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-139">Добавление новых программ (находящихся в элементе <strong>Установка и удаление программ</strong> на панели управления)</span><span class="sxs-lookup"><span data-stu-id="33615-139">Add New Programs (found in the <strong>Add or Remove Programs</strong> item in the Control Panel)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-140">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-140">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-141">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-141">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AdminTools"></span><span id="folderid_admintools"></span><span id="FOLDERID_ADMINTOOLS"></span><dl> <span data-ttu-id="33615-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-143">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-143">GUID</span></span></td>
<td><span data-ttu-id="33615-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span><span class="sxs-lookup"><span data-stu-id="33615-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-145">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-145">Display Name</span></span></td>
<td><span data-ttu-id="33615-146">«Администрирование»</span><span class="sxs-lookup"><span data-stu-id="33615-146">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-147">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-147">Folder Type</span></span></td>
<td><span data-ttu-id="33615-148">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-148">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-149">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-149">Default Path</span></span></td>
<td><span data-ttu-id="33615-150">Средства%Аппдата%\микрософт\виндовс\старт</span><span class="sxs-lookup"><span data-stu-id="33615-150">%APPDATA%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-151">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-151">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-152">CSIDL_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="33615-152">CSIDL_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-153">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-153">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-154">«Администрирование»</span><span class="sxs-lookup"><span data-stu-id="33615-154">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-155">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-155">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-156">Средства%Усерпрофиле%\старт</span><span class="sxs-lookup"><span data-stu-id="33615-156">%USERPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataDesktop"></span><span id="folderid_appdatadesktop"></span><span id="FOLDERID_APPDATADESKTOP"></span><dl> <span data-ttu-id="33615-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-158">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-158">GUID</span></span></td>
<td><span data-ttu-id="33615-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span><span class="sxs-lookup"><span data-stu-id="33615-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-160">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-160">Display Name</span></span></td>
<td><span data-ttu-id="33615-161">аппдатадесктоп</span><span class="sxs-lookup"><span data-stu-id="33615-161">AppDataDesktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-162">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-162">Folder Type</span></span></td>
<td><span data-ttu-id="33615-163">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-163">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-164">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-164">Default Path</span></span></td>
<td><span data-ttu-id="33615-165">%локалаппдата%\десктоп</span><span class="sxs-lookup"><span data-stu-id="33615-165">%LOCALAPPDATA%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-166">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-166">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-167">Нет, значение введено в Windows 10, версия 1709</span><span class="sxs-lookup"><span data-stu-id="33615-167">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-168">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-168">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-169">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-169">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-170">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-170">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-171">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-171">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="33615-172">Этот FOLDERID используется внутренне приложениями .NET для реализации функциональных возможностей приложений на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="33615-172">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="33615-173">Он не предназначен для использования непосредственно из приложения.</span><span class="sxs-lookup"><span data-stu-id="33615-173">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataDocuments"></span><span id="folderid_appdatadocuments"></span><span id="FOLDERID_APPDATADOCUMENTS"></span><dl> <span data-ttu-id="33615-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-175">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-175">GUID</span></span></td>
<td><span data-ttu-id="33615-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span><span class="sxs-lookup"><span data-stu-id="33615-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-177">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-177">Display Name</span></span></td>
<td><span data-ttu-id="33615-178">аппдатадокументс</span><span class="sxs-lookup"><span data-stu-id="33615-178">AppDataDocuments</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-179">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-179">Folder Type</span></span></td>
<td><span data-ttu-id="33615-180">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-180">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-181">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-181">Default Path</span></span></td>
<td><span data-ttu-id="33615-182">%локалаппдата%\документс</span><span class="sxs-lookup"><span data-stu-id="33615-182">%LOCALAPPDATA%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-183">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-183">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-184">Нет, значение введено в Windows 10, версия 1709</span><span class="sxs-lookup"><span data-stu-id="33615-184">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-185">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-185">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-186">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-186">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-187">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-187">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-188">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-188">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="33615-189">Этот FOLDERID используется внутренне приложениями .NET для реализации функциональных возможностей приложений на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="33615-189">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="33615-190">Он не предназначен для использования непосредственно из приложения.</span><span class="sxs-lookup"><span data-stu-id="33615-190">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataFavorites"></span><span id="folderid_appdatafavorites"></span><span id="FOLDERID_APPDATAFAVORITES"></span><dl> <span data-ttu-id="33615-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-192">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-192">GUID</span></span></td>
<td><span data-ttu-id="33615-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span><span class="sxs-lookup"><span data-stu-id="33615-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-194">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-194">Display Name</span></span></td>
<td><span data-ttu-id="33615-195">аппдатафаворитес</span><span class="sxs-lookup"><span data-stu-id="33615-195">AppDataFavorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-196">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-196">Folder Type</span></span></td>
<td><span data-ttu-id="33615-197">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-197">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-198">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-198">Default Path</span></span></td>
<td><span data-ttu-id="33615-199">%локалаппдата%\фаворитес</span><span class="sxs-lookup"><span data-stu-id="33615-199">%LOCALAPPDATA%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-200">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-200">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-201">Нет, значение введено в Windows 10, версия 1709</span><span class="sxs-lookup"><span data-stu-id="33615-201">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-202">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-202">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-203">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-203">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-204">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-204">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-205">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-205">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="33615-206">Этот FOLDERID используется внутренне приложениями .NET для реализации функциональных возможностей приложений на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="33615-206">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="33615-207">Он не предназначен для использования непосредственно из приложения.</span><span class="sxs-lookup"><span data-stu-id="33615-207">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataProgramData"></span><span id="folderid_appdataprogramdata"></span><span id="FOLDERID_APPDATAPROGRAMDATA"></span><dl> <span data-ttu-id="33615-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-209">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-209">GUID</span></span></td>
<td><span data-ttu-id="33615-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span><span class="sxs-lookup"><span data-stu-id="33615-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-211">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-211">Display Name</span></span></td>
<td><span data-ttu-id="33615-212">аппдатапрограмдата</span><span class="sxs-lookup"><span data-stu-id="33615-212">AppDataProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-213">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-213">Folder Type</span></span></td>
<td><span data-ttu-id="33615-214">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-214">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-215">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-215">Default Path</span></span></td>
<td><span data-ttu-id="33615-216">%локалаппдата%\програмдата</span><span class="sxs-lookup"><span data-stu-id="33615-216">%LOCALAPPDATA%\ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-217">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-217">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-218">Нет, значение введено в Windows 10, версия 1709</span><span class="sxs-lookup"><span data-stu-id="33615-218">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-219">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-219">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-220">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-220">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-221">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-221">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-222">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-222">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="33615-223">Этот FOLDERID используется внутренне приложениями .NET для реализации функциональных возможностей приложений на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="33615-223">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="33615-224">Он не предназначен для использования непосредственно из приложения.</span><span class="sxs-lookup"><span data-stu-id="33615-224">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ApplicationShortcuts"></span><span id="folderid_applicationshortcuts"></span><span id="FOLDERID_APPLICATIONSHORTCUTS"></span><dl> <span data-ttu-id="33615-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-226">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-226">GUID</span></span></td>
<td><span data-ttu-id="33615-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span><span class="sxs-lookup"><span data-stu-id="33615-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-228">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-228">Display Name</span></span></td>
<td><span data-ttu-id="33615-229">Ярлыки приложений</span><span class="sxs-lookup"><span data-stu-id="33615-229">Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-230">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-230">Folder Type</span></span></td>
<td><span data-ttu-id="33615-231">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-231">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-232">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-232">Default Path</span></span></td>
<td><span data-ttu-id="33615-233">Сочетания клавиш%Локалаппдата%\микрософт\виндовс\аппликатион</span><span class="sxs-lookup"><span data-stu-id="33615-233">%LOCALAPPDATA%\Microsoft\Windows\Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-234">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-234">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-235">Нет, значение, введенное в Windows 8</span><span class="sxs-lookup"><span data-stu-id="33615-235">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-236">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-236">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-237">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-237">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-238">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-238">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-239">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-239">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppsFolder"></span><span id="folderid_appsfolder"></span><span id="FOLDERID_APPSFOLDER"></span><dl> <span data-ttu-id="33615-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-241">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-241">GUID</span></span></td>
<td><span data-ttu-id="33615-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span><span class="sxs-lookup"><span data-stu-id="33615-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-243">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-243">Display Name</span></span></td>
<td><span data-ttu-id="33615-244">Приложения</span><span class="sxs-lookup"><span data-stu-id="33615-244">Applications</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-245">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-245">Folder Type</span></span></td>
<td><span data-ttu-id="33615-246">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-246">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-247">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-247">Default Path</span></span></td>
<td><span data-ttu-id="33615-248">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-248">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-249">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-249">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-250">Нет, значение, введенное в Windows 8</span><span class="sxs-lookup"><span data-stu-id="33615-250">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-251">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-251">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-252">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-252">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-253">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-253">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-254">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-254">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppUpdates"></span><span id="folderid_appupdates"></span><span id="FOLDERID_APPUPDATES"></span><dl> <span data-ttu-id="33615-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-256">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-256">GUID</span></span></td>
<td><span data-ttu-id="33615-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span><span class="sxs-lookup"><span data-stu-id="33615-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-258">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-258">Display Name</span></span></td>
<td><span data-ttu-id="33615-259">Установленные обновления</span><span class="sxs-lookup"><span data-stu-id="33615-259">Installed Updates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-260">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-260">Folder Type</span></span></td>
<td><span data-ttu-id="33615-261">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-261">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-262">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-262">Default Path</span></span></td>
<td><span data-ttu-id="33615-263">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-263">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-264">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-264">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-265">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-265">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-266">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-266">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-267">Нет, значение, введенное в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="33615-267">None, value introduced in Windows Vista.</span></span> <span data-ttu-id="33615-268">В более ранних версиях Windows сведения на этой странице были включены в компонент " <strong>Установка и удаление программ</strong> ", если флажок " <strong>Показывать обновления</strong> " установлен.</span><span class="sxs-lookup"><span data-stu-id="33615-268">In earlier versions of Windows, the information on this page was included in <strong>Add or Remove Programs</strong> if the <strong>Show updates</strong> box was checked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-269">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-269">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-270">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-270">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CameraRoll"></span><span id="folderid_cameraroll"></span><span id="FOLDERID_CAMERAROLL"></span><dl> <span data-ttu-id="33615-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-272">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-272">GUID</span></span></td>
<td><span data-ttu-id="33615-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span><span class="sxs-lookup"><span data-stu-id="33615-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-274">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-274">Display Name</span></span></td>
<td><span data-ttu-id="33615-275">Пленка</span><span class="sxs-lookup"><span data-stu-id="33615-275">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-276">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-276">Folder Type</span></span></td>
<td><span data-ttu-id="33615-277">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-277">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-278">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-278">Default Path</span></span></td>
<td><span data-ttu-id="33615-279">%Усерпрофиле%\пиктурес\камера</span><span class="sxs-lookup"><span data-stu-id="33615-279">%USERPROFILE%\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-280">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-280">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-281">Нет, значение, введенное в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33615-281">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-282">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-282">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-283">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-283">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-284">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-284">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-285">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-285">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CDBurning"></span><span id="folderid_cdburning"></span><span id="FOLDERID_CDBURNING"></span><dl> <span data-ttu-id="33615-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-287">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-287">GUID</span></span></td>
<td><span data-ttu-id="33615-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span><span class="sxs-lookup"><span data-stu-id="33615-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-289">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-289">Display Name</span></span></td>
<td><span data-ttu-id="33615-290">Временная папка для записи</span><span class="sxs-lookup"><span data-stu-id="33615-290">Temporary Burn Folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-291">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-291">Folder Type</span></span></td>
<td><span data-ttu-id="33615-292">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-292">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-293">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-293">Default Path</span></span></td>
<td><span data-ttu-id="33615-294">%локалаппдата%\микрософт\виндовс\бурн\бурн</span><span class="sxs-lookup"><span data-stu-id="33615-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-295">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-295">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-296">CSIDL_CDBURN_AREA</span><span class="sxs-lookup"><span data-stu-id="33615-296">CSIDL_CDBURN_AREA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-297">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-297">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-298">Запись компакт-диска</span><span class="sxs-lookup"><span data-stu-id="33615-298">CD Burning</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-299">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-299">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-300">%Усерпрофиле%\локал Settings\Application Дата\микрософт\кд запись</span><span class="sxs-lookup"><span data-stu-id="33615-300">%USERPROFILE%\Local Settings\Application Data\Microsoft\CD Burning</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ChangeRemovePrograms"></span><span id="folderid_changeremoveprograms"></span><span id="FOLDERID_CHANGEREMOVEPROGRAMS"></span><dl> <span data-ttu-id="33615-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-302">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-302">GUID</span></span></td>
<td><span data-ttu-id="33615-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span><span class="sxs-lookup"><span data-stu-id="33615-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-304">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-304">Display Name</span></span></td>
<td><span data-ttu-id="33615-305">"Программы и компоненты",</span><span class="sxs-lookup"><span data-stu-id="33615-305">Programs and Features</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-306">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-306">Folder Type</span></span></td>
<td><span data-ttu-id="33615-307">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-307">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-308">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-308">Default Path</span></span></td>
<td><span data-ttu-id="33615-309">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-309">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-310">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-310">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-311">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-311">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-312">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-312">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-313">Установка и удаление программ</span><span class="sxs-lookup"><span data-stu-id="33615-313">Add or Remove Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-314">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-314">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-315">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-315">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonAdminTools"></span><span id="folderid_commonadmintools"></span><span id="FOLDERID_COMMONADMINTOOLS"></span><dl> <span data-ttu-id="33615-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-317">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-317">GUID</span></span></td>
<td><span data-ttu-id="33615-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span><span class="sxs-lookup"><span data-stu-id="33615-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-319">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-319">Display Name</span></span></td>
<td><span data-ttu-id="33615-320">«Администрирование»</span><span class="sxs-lookup"><span data-stu-id="33615-320">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-321">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-321">Folder Type</span></span></td>
<td><span data-ttu-id="33615-322">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-322">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-323">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-323">Default Path</span></span></td>
<td><span data-ttu-id="33615-324">Средства%Аллусерспрофиле%\микрософт\виндовс\старт</span><span class="sxs-lookup"><span data-stu-id="33615-324">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-325">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-325">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-326">CSIDL_COMMON_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="33615-326">CSIDL_COMMON_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-327">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-327">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-328">«Администрирование»</span><span class="sxs-lookup"><span data-stu-id="33615-328">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-329">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-329">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-330">Средства%Аллусерспрофиле%\старт</span><span class="sxs-lookup"><span data-stu-id="33615-330">%ALLUSERSPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonOEMLinks"></span><span id="folderid_commonoemlinks"></span><span id="FOLDERID_COMMONOEMLINKS"></span><dl> <span data-ttu-id="33615-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-332">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-332">GUID</span></span></td>
<td><span data-ttu-id="33615-333">{C1BAE2D0-10DF-4334-7AA20B227A9D}</span><span class="sxs-lookup"><span data-stu-id="33615-333">{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-334">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-334">Display Name</span></span></td>
<td><span data-ttu-id="33615-335">Ссылки OEM</span><span class="sxs-lookup"><span data-stu-id="33615-335">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-336">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-336">Folder Type</span></span></td>
<td><span data-ttu-id="33615-337">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-337">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-338">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-338">Default Path</span></span></td>
<td><span data-ttu-id="33615-339">Ссылки%АЛЛУСЕРСПРОФИЛЕ%\ОЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-339">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-340">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-340">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-341">CSIDL_COMMON_OEM_LINKS</span><span class="sxs-lookup"><span data-stu-id="33615-341">CSIDL_COMMON_OEM_LINKS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-342">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-342">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-343">Ссылки OEM</span><span class="sxs-lookup"><span data-stu-id="33615-343">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-344">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-344">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-345">Ссылки%АЛЛУСЕРСПРОФИЛЕ%\ОЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-345">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonPrograms"></span><span id="folderid_commonprograms"></span><span id="FOLDERID_COMMONPROGRAMS"></span><dl> <span data-ttu-id="33615-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-347">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-347">GUID</span></span></td>
<td><span data-ttu-id="33615-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span><span class="sxs-lookup"><span data-stu-id="33615-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-349">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-349">Display Name</span></span></td>
<td><span data-ttu-id="33615-350">Programs</span><span class="sxs-lookup"><span data-stu-id="33615-350">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-351">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-351">Folder Type</span></span></td>
<td><span data-ttu-id="33615-352">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-352">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-353">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-353">Default Path</span></span></td>
<td><span data-ttu-id="33615-354">%Аллусерспрофиле%\микрософт\виндовс\старт Мену\програмс</span><span class="sxs-lookup"><span data-stu-id="33615-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-355">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-355">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-356">CSIDL_COMMON_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="33615-356">CSIDL_COMMON_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-357">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-357">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-358">Programs</span><span class="sxs-lookup"><span data-stu-id="33615-358">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-359">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-359">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-360">%Аллусерспрофиле%\старт Мену\програмс</span><span class="sxs-lookup"><span data-stu-id="33615-360">%ALLUSERSPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonStartMenu"></span><span id="folderid_commonstartmenu"></span><span id="FOLDERID_COMMONSTARTMENU"></span><dl> <span data-ttu-id="33615-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-362">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-362">GUID</span></span></td>
<td><span data-ttu-id="33615-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span><span class="sxs-lookup"><span data-stu-id="33615-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-364">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-364">Display Name</span></span></td>
<td><span data-ttu-id="33615-365">Меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="33615-365">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-366">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-366">Folder Type</span></span></td>
<td><span data-ttu-id="33615-367">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-367">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-368">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-368">Default Path</span></span></td>
<td><span data-ttu-id="33615-369">Меню%Аллусерспрофиле%\микрософт\виндовс\старт</span><span class="sxs-lookup"><span data-stu-id="33615-369">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-370">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-370">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-371">CSIDL_COMMON_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="33615-371">CSIDL_COMMON_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-372">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-372">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-373">Меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="33615-373">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-374">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-374">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-375">Меню%Аллусерспрофиле%\старт</span><span class="sxs-lookup"><span data-stu-id="33615-375">%ALLUSERSPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonStartup"></span><span id="folderid_commonstartup"></span><span id="FOLDERID_COMMONSTARTUP"></span><dl> <span data-ttu-id="33615-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-377">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-377">GUID</span></span></td>
<td><span data-ttu-id="33615-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span><span class="sxs-lookup"><span data-stu-id="33615-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-379">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-379">Display Name</span></span></td>
<td><span data-ttu-id="33615-380">Запуск</span><span class="sxs-lookup"><span data-stu-id="33615-380">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-381">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-381">Folder Type</span></span></td>
<td><span data-ttu-id="33615-382">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-382">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-383">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-383">Default Path</span></span></td>
<td><span data-ttu-id="33615-384">%Аллусерспрофиле%\микрософт\виндовс\старт Мену\програмс\стартуп</span><span class="sxs-lookup"><span data-stu-id="33615-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-385">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-385">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="33615-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-387">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-387">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-388">Запуск</span><span class="sxs-lookup"><span data-stu-id="33615-388">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-389">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-389">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-390">%Аллусерспрофиле%\старт Мену\програмс\стартуп</span><span class="sxs-lookup"><span data-stu-id="33615-390">%ALLUSERSPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonTemplates"></span><span id="folderid_commontemplates"></span><span id="FOLDERID_COMMONTEMPLATES"></span><dl> <span data-ttu-id="33615-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-392">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-392">GUID</span></span></td>
<td><span data-ttu-id="33615-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span><span class="sxs-lookup"><span data-stu-id="33615-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-394">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-394">Display Name</span></span></td>
<td><span data-ttu-id="33615-395">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="33615-395">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-396">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-396">Folder Type</span></span></td>
<td><span data-ttu-id="33615-397">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-397">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-398">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-398">Default Path</span></span></td>
<td><span data-ttu-id="33615-399">%аллусерспрофиле%\микрософт\виндовс\темплатес</span><span class="sxs-lookup"><span data-stu-id="33615-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-400">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-400">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-401">CSIDL_COMMON_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="33615-401">CSIDL_COMMON_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-402">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-402">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-403">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="33615-403">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-404">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-404">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-405">%аллусерспрофиле%\темплатес</span><span class="sxs-lookup"><span data-stu-id="33615-405">%ALLUSERSPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ComputerFolder"></span><span id="folderid_computerfolder"></span><span id="FOLDERID_COMPUTERFOLDER"></span><dl> <span data-ttu-id="33615-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-407">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-407">GUID</span></span></td>
<td><span data-ttu-id="33615-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span><span class="sxs-lookup"><span data-stu-id="33615-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-409">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-409">Display Name</span></span></td>
<td><span data-ttu-id="33615-410">Компьютер</span><span class="sxs-lookup"><span data-stu-id="33615-410">Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-411">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-411">Folder Type</span></span></td>
<td><span data-ttu-id="33615-412">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-412">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-413">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-413">Default Path</span></span></td>
<td><span data-ttu-id="33615-414">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-414">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-415">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-415">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-416">CSIDL_DRIVES</span><span class="sxs-lookup"><span data-stu-id="33615-416">CSIDL_DRIVES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-417">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-417">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-418">Мой компьютер</span><span class="sxs-lookup"><span data-stu-id="33615-418">My Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-419">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-419">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-420">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-420">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ConflictFolder"></span><span id="folderid_conflictfolder"></span><span id="FOLDERID_CONFLICTFOLDER"></span><dl> <span data-ttu-id="33615-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-422">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-422">GUID</span></span></td>
<td><span data-ttu-id="33615-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span><span class="sxs-lookup"><span data-stu-id="33615-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-424">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-424">Display Name</span></span></td>
<td><span data-ttu-id="33615-425">Конфликты</span><span class="sxs-lookup"><span data-stu-id="33615-425">Conflicts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-426">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-426">Folder Type</span></span></td>
<td><span data-ttu-id="33615-427">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-427">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-428">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-428">Default Path</span></span></td>
<td><span data-ttu-id="33615-429">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-429">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-430">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-430">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-431">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-431">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-432">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-432">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-433">Не применяется</span><span class="sxs-lookup"><span data-stu-id="33615-433">Not applicable.</span></span> <span data-ttu-id="33615-434">Этот <strong>кновнфолдерид</strong> относится к диспетчеру синхронизации Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="33615-434">This <strong>KNOWNFOLDERID</strong> refers to the Windows Vista Synchronization Manager.</span></span> <span data-ttu-id="33615-435">Это не папка, на которую ссылается более старая <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>исинкмгрконфликтфолдер</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="33615-435">It is not the folder referenced by the older <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-436">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-436">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-437">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-437">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ConnectionsFolder"></span><span id="folderid_connectionsfolder"></span><span id="FOLDERID_CONNECTIONSFOLDER"></span><dl> <span data-ttu-id="33615-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-439">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-439">GUID</span></span></td>
<td><span data-ttu-id="33615-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span><span class="sxs-lookup"><span data-stu-id="33615-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-441">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-441">Display Name</span></span></td>
<td><span data-ttu-id="33615-442">Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="33615-442">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-443">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-443">Folder Type</span></span></td>
<td><span data-ttu-id="33615-444">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-444">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-445">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-445">Default Path</span></span></td>
<td><span data-ttu-id="33615-446">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-446">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-447">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-447">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-448">CSIDL_CONNECTIONS</span><span class="sxs-lookup"><span data-stu-id="33615-448">CSIDL_CONNECTIONS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-449">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-449">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-450">Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="33615-450">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-451">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-451">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-452">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-452">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Contacts"></span><span id="folderid_contacts"></span><span id="FOLDERID_CONTACTS"></span><dl> <span data-ttu-id="33615-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-454">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-454">GUID</span></span></td>
<td><span data-ttu-id="33615-455">{56784854-C6CB-462b-8169-88E350ACB882}</span><span class="sxs-lookup"><span data-stu-id="33615-455">{56784854-C6CB-462b-8169-88E350ACB882}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-456">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-456">Display Name</span></span></td>
<td><span data-ttu-id="33615-457">Контакты</span><span class="sxs-lookup"><span data-stu-id="33615-457">Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-458">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-458">Folder Type</span></span></td>
<td><span data-ttu-id="33615-459">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-459">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-460">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-460">Default Path</span></span></td>
<td><span data-ttu-id="33615-461">%усерпрофиле%\контактс</span><span class="sxs-lookup"><span data-stu-id="33615-461">%USERPROFILE%\Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-462">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-462">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-463">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-463">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-464">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-464">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-465">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-465">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-466">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-466">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-467">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-467">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ControlPanelFolder"></span><span id="folderid_controlpanelfolder"></span><span id="FOLDERID_CONTROLPANELFOLDER"></span><dl> <span data-ttu-id="33615-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-469">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-469">GUID</span></span></td>
<td><span data-ttu-id="33615-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span><span class="sxs-lookup"><span data-stu-id="33615-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-471">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-471">Display Name</span></span></td>
<td><span data-ttu-id="33615-472">Панель управления</span><span class="sxs-lookup"><span data-stu-id="33615-472">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-473">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-473">Folder Type</span></span></td>
<td><span data-ttu-id="33615-474">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-474">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-475">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-475">Default Path</span></span></td>
<td><span data-ttu-id="33615-476">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-476">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-477">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-477">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-478">CSIDL_CONTROLS</span><span class="sxs-lookup"><span data-stu-id="33615-478">CSIDL_CONTROLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-479">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-479">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-480">Панель управления</span><span class="sxs-lookup"><span data-stu-id="33615-480">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-481">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-481">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-482">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-482">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Cookies"></span><span id="folderid_cookies"></span><span id="FOLDERID_COOKIES"></span><dl> <span data-ttu-id="33615-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-484">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-484">GUID</span></span></td>
<td><span data-ttu-id="33615-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span><span class="sxs-lookup"><span data-stu-id="33615-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-486">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-486">Display Name</span></span></td>
<td><span data-ttu-id="33615-487">Файлы cookie</span><span class="sxs-lookup"><span data-stu-id="33615-487">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-488">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-488">Folder Type</span></span></td>
<td><span data-ttu-id="33615-489">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-489">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-490">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-490">Default Path</span></span></td>
<td><span data-ttu-id="33615-491">%аппдата%\микрософт\виндовс\кукиес</span><span class="sxs-lookup"><span data-stu-id="33615-491">%APPDATA%\Microsoft\Windows\Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-492">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-492">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-493">CSIDL_COOKIES</span><span class="sxs-lookup"><span data-stu-id="33615-493">CSIDL_COOKIES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-494">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-494">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-495">Файлы cookie</span><span class="sxs-lookup"><span data-stu-id="33615-495">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-496">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-496">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-497">%усерпрофиле%\кукиес</span><span class="sxs-lookup"><span data-stu-id="33615-497">%USERPROFILE%\Cookies</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Desktop"></span><span id="folderid_desktop"></span><span id="FOLDERID_DESKTOP"></span><dl> <span data-ttu-id="33615-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-499">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-499">GUID</span></span></td>
<td><span data-ttu-id="33615-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span><span class="sxs-lookup"><span data-stu-id="33615-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-501">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-501">Display Name</span></span></td>
<td><span data-ttu-id="33615-502">Персональный компьютер</span><span class="sxs-lookup"><span data-stu-id="33615-502">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-503">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-503">Folder Type</span></span></td>
<td><span data-ttu-id="33615-504">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-504">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-505">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-505">Default Path</span></span></td>
<td><span data-ttu-id="33615-506">%усерпрофиле%\десктоп</span><span class="sxs-lookup"><span data-stu-id="33615-506">%USERPROFILE%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-507">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-507">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="33615-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-509">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-509">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-510">Персональный компьютер</span><span class="sxs-lookup"><span data-stu-id="33615-510">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-511">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-511">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-512">%усерпрофиле%\десктоп</span><span class="sxs-lookup"><span data-stu-id="33615-512">%USERPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DeviceMetadataStore"></span><span id="folderid_devicemetadatastore"></span><span id="FOLDERID_DEVICEMETADATASTORE"></span><dl> <span data-ttu-id="33615-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-514">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-514">GUID</span></span></td>
<td><span data-ttu-id="33615-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span><span class="sxs-lookup"><span data-stu-id="33615-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-516">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-516">Display Name</span></span></td>
<td><span data-ttu-id="33615-517">девицеметадатасторе</span><span class="sxs-lookup"><span data-stu-id="33615-517">DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-518">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-518">Folder Type</span></span></td>
<td><span data-ttu-id="33615-519">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-519">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-520">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-520">Default Path</span></span></td>
<td><span data-ttu-id="33615-521">%аллусерспрофиле%\микрософт\виндовс\девицеметадатасторе</span><span class="sxs-lookup"><span data-stu-id="33615-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-522">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-522">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-523">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-523">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-524">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-524">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-525">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-525">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-526">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-526">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-527">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-527">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Documents"></span><span id="folderid_documents"></span><span id="FOLDERID_DOCUMENTS"></span><dl> <span data-ttu-id="33615-528"><dt><strong>FOLDERID_Documents</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-528"><dt><strong>FOLDERID_Documents</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-529">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-529">GUID</span></span></td>
<td><span data-ttu-id="33615-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span><span class="sxs-lookup"><span data-stu-id="33615-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-531">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-531">Display Name</span></span></td>
<td><span data-ttu-id="33615-532">Документы</span><span class="sxs-lookup"><span data-stu-id="33615-532">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-533">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-533">Folder Type</span></span></td>
<td><span data-ttu-id="33615-534">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-534">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-535">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-535">Default Path</span></span></td>
<td><span data-ttu-id="33615-536">%усерпрофиле%\документс</span><span class="sxs-lookup"><span data-stu-id="33615-536">%USERPROFILE%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-537">Эквиваленты CSID</span><span class="sxs-lookup"><span data-stu-id="33615-537">CSIDL Equivalents</span></span></td>
<td><span data-ttu-id="33615-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="33615-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-539">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-539">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-540">Мои документы</span><span class="sxs-lookup"><span data-stu-id="33615-540">My Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-541">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-541">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-542">Документы%USERPROFILE%\My</span><span class="sxs-lookup"><span data-stu-id="33615-542">%USERPROFILE%\My Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DocumentsLibrary"></span><span id="folderid_documentslibrary"></span><span id="FOLDERID_DOCUMENTSLIBRARY"></span><dl> <span data-ttu-id="33615-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-544">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-544">GUID</span></span></td>
<td><span data-ttu-id="33615-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span><span class="sxs-lookup"><span data-stu-id="33615-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-546">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-546">Display Name</span></span></td>
<td><span data-ttu-id="33615-547">Документы</span><span class="sxs-lookup"><span data-stu-id="33615-547">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-548">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-548">Folder Type</span></span></td>
<td><span data-ttu-id="33615-549">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-549">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-550">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-550">Default Path</span></span></td>
<td><span data-ttu-id="33615-551">%аппдата%\микрософт\виндовс\либрариес\документс.либрари-мс</span><span class="sxs-lookup"><span data-stu-id="33615-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-552">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-552">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-553">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-553">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-554">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-554">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-555">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-555">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-556">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-556">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-557">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-557">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Downloads"></span><span id="folderid_downloads"></span><span id="FOLDERID_DOWNLOADS"></span><dl> <span data-ttu-id="33615-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-559">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-559">GUID</span></span></td>
<td><span data-ttu-id="33615-560">{374DE290-123F-4565-9164-39C4925E467B}</span><span class="sxs-lookup"><span data-stu-id="33615-560">{374DE290-123F-4565-9164-39C4925E467B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-561">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-561">Display Name</span></span></td>
<td><span data-ttu-id="33615-562">Скачиваемые файлы</span><span class="sxs-lookup"><span data-stu-id="33615-562">Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-563">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-563">Folder Type</span></span></td>
<td><span data-ttu-id="33615-564">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-564">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-565">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-565">Default Path</span></span></td>
<td><span data-ttu-id="33615-566">%усерпрофиле%\довнлоадс</span><span class="sxs-lookup"><span data-stu-id="33615-566">%USERPROFILE%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-567">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-567">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-568">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-568">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-569">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-569">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-570">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-570">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-571">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-571">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-572">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-572">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Favorites"></span><span id="folderid_favorites"></span><span id="FOLDERID_FAVORITES"></span><dl> <span data-ttu-id="33615-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-574">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-574">GUID</span></span></td>
<td><span data-ttu-id="33615-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span><span class="sxs-lookup"><span data-stu-id="33615-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-576">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-576">Display Name</span></span></td>
<td><span data-ttu-id="33615-577">Избранное</span><span class="sxs-lookup"><span data-stu-id="33615-577">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-578">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-578">Folder Type</span></span></td>
<td><span data-ttu-id="33615-579">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-579">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-580">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-580">Default Path</span></span></td>
<td><span data-ttu-id="33615-581">%усерпрофиле%\фаворитес</span><span class="sxs-lookup"><span data-stu-id="33615-581">%USERPROFILE%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-582">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-582">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span><span class="sxs-lookup"><span data-stu-id="33615-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-584">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-584">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-585">Избранное</span><span class="sxs-lookup"><span data-stu-id="33615-585">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-586">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-586">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-587">%усерпрофиле%\фаворитес</span><span class="sxs-lookup"><span data-stu-id="33615-587">%USERPROFILE%\Favorites</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Fonts"></span><span id="folderid_fonts"></span><span id="FOLDERID_FONTS"></span><dl> <span data-ttu-id="33615-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-589">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-589">GUID</span></span></td>
<td><span data-ttu-id="33615-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span><span class="sxs-lookup"><span data-stu-id="33615-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-591">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-591">Display Name</span></span></td>
<td><span data-ttu-id="33615-592">Шрифты</span><span class="sxs-lookup"><span data-stu-id="33615-592">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-593">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-593">Folder Type</span></span></td>
<td><span data-ttu-id="33615-594">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-594">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-595">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-595">Default Path</span></span></td>
<td><span data-ttu-id="33615-596">%виндир%\фонтс</span><span class="sxs-lookup"><span data-stu-id="33615-596">%windir%\Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-597">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-597">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-598">CSIDL_FONTS</span><span class="sxs-lookup"><span data-stu-id="33615-598">CSIDL_FONTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-599">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-599">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-600">Шрифты</span><span class="sxs-lookup"><span data-stu-id="33615-600">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-601">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-601">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-602">%виндир%\фонтс</span><span class="sxs-lookup"><span data-stu-id="33615-602">%windir%\Fonts</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Games"></span><span id="folderid_games"></span><span id="FOLDERID_GAMES"></span><dl> <span data-ttu-id="33615-603"><dt><strong>FOLDERID_Games</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-603"><dt><strong>FOLDERID_Games</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="33615-604">Этот FOLDERID является устаревшим в Windows 10, версии 1803 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="33615-604">This FOLDERID is deprecated in Windows 10, version 1803 and later versions.</span></span> <span data-ttu-id="33615-605">В этих версиях возвращается <strong>0x80070057-E_INVALIDARG</strong>
</span><span class="sxs-lookup"><span data-stu-id="33615-605">In these versions, it returns <strong>0x80070057 - E_INVALIDARG</strong>
</span></span></blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-606">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-606">GUID</span></span></td>
<td><span data-ttu-id="33615-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span><span class="sxs-lookup"><span data-stu-id="33615-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-608">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-608">Display Name</span></span></td>
<td><span data-ttu-id="33615-609">Игры</span><span class="sxs-lookup"><span data-stu-id="33615-609">Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-610">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-610">Folder Type</span></span></td>
<td><span data-ttu-id="33615-611">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-611">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-612">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-612">Default Path</span></span></td>
<td><span data-ttu-id="33615-613">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-613">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-614">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-614">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-615">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-615">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-616">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-616">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-617">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-617">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-618">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-618">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-619">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-619">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_GameTasks"></span><span id="folderid_gametasks"></span><span id="FOLDERID_GAMETASKS"></span><dl> <span data-ttu-id="33615-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-621">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-621">GUID</span></span></td>
<td><span data-ttu-id="33615-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span><span class="sxs-lookup"><span data-stu-id="33615-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-623">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-623">Display Name</span></span></td>
<td><span data-ttu-id="33615-624">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="33615-624">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-625">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-625">Folder Type</span></span></td>
<td><span data-ttu-id="33615-626">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-626">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-627">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-627">Default Path</span></span></td>
<td><span data-ttu-id="33615-628">%локалаппдата%\микрософт\виндовс\гамиксплорер</span><span class="sxs-lookup"><span data-stu-id="33615-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-629">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-629">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-630">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-630">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-631">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-631">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-632">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-632">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-633">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-633">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-634">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-634">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_History"></span><span id="folderid_history"></span><span id="FOLDERID_HISTORY"></span><dl> <span data-ttu-id="33615-635"><dt><strong>FOLDERID_History</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-635"><dt><strong>FOLDERID_History</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-636">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-636">GUID</span></span></td>
<td><span data-ttu-id="33615-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span><span class="sxs-lookup"><span data-stu-id="33615-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-638">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-638">Display Name</span></span></td>
<td><span data-ttu-id="33615-639">Журнал</span><span class="sxs-lookup"><span data-stu-id="33615-639">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-640">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-640">Folder Type</span></span></td>
<td><span data-ttu-id="33615-641">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-641">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-642">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-642">Default Path</span></span></td>
<td><span data-ttu-id="33615-643">%локалаппдата%\микрософт\виндовс\хистори</span><span class="sxs-lookup"><span data-stu-id="33615-643">%LOCALAPPDATA%\Microsoft\Windows\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-644">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-644">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-645">CSIDL_HISTORY</span><span class="sxs-lookup"><span data-stu-id="33615-645">CSIDL_HISTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-646">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-646">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-647">Журнал</span><span class="sxs-lookup"><span data-stu-id="33615-647">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-648">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-648">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-649">%Усерпрофиле%\локал Сеттингс\хистори</span><span class="sxs-lookup"><span data-stu-id="33615-649">%USERPROFILE%\Local Settings\History</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_HomeGroup"></span><span id="folderid_homegroup"></span><span id="FOLDERID_HOMEGROUP"></span><dl> <span data-ttu-id="33615-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-651">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-651">GUID</span></span></td>
<td><span data-ttu-id="33615-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span><span class="sxs-lookup"><span data-stu-id="33615-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-653">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-653">Display Name</span></span></td>
<td><span data-ttu-id="33615-654">Домашняя группа</span><span class="sxs-lookup"><span data-stu-id="33615-654">Homegroup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-655">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-655">Folder Type</span></span></td>
<td><span data-ttu-id="33615-656">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-656">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-657">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-657">Default Path</span></span></td>
<td><span data-ttu-id="33615-658">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-658">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-659">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-659">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-660">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-660">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-661">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-661">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-662">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-662">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-663">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-663">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-664">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-664">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_HomeGroupCurrentUser"></span><span id="folderid_homegroupcurrentuser"></span><span id="FOLDERID_HOMEGROUPCURRENTUSER"></span><dl> <span data-ttu-id="33615-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-666">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-666">GUID</span></span></td>
<td><span data-ttu-id="33615-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span><span class="sxs-lookup"><span data-stu-id="33615-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-668">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-668">Display Name</span></span></td>
<td><span data-ttu-id="33615-669">Имя пользователя (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="33615-669">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-670">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-670">Folder Type</span></span></td>
<td><span data-ttu-id="33615-671">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-671">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-672">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-672">Default Path</span></span></td>
<td><span data-ttu-id="33615-673">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-673">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-674">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-674">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-675">Нет, значение, введенное в Windows 8</span><span class="sxs-lookup"><span data-stu-id="33615-675">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-676">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-676">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-677">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-677">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-678">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-678">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-679">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-679">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ImplicitAppShortcuts"></span><span id="folderid_implicitappshortcuts"></span><span id="FOLDERID_IMPLICITAPPSHORTCUTS"></span><dl> <span data-ttu-id="33615-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-681">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-681">GUID</span></span></td>
<td><span data-ttu-id="33615-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span><span class="sxs-lookup"><span data-stu-id="33615-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-683">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-683">Display Name</span></span></td>
<td><span data-ttu-id="33615-684">имплиЦитаппшорткутс</span><span class="sxs-lookup"><span data-stu-id="33615-684">ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-685">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-685">Folder Type</span></span></td>
<td><span data-ttu-id="33615-686">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-686">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-687">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-687">Default Path</span></span></td>
<td><span data-ttu-id="33615-688">%Аппдата%\микрософт\интернет Експлорер\куикк Лаунч\усер Пиннед\имплиЦитаппшорткутс</span><span class="sxs-lookup"><span data-stu-id="33615-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-689">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-689">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-690">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-690">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-691">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-691">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-692">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-692">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-693">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-693">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-694">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-694">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_InternetCache"></span><span id="folderid_internetcache"></span><span id="FOLDERID_INTERNETCACHE"></span><dl> <span data-ttu-id="33615-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-696">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-696">GUID</span></span></td>
<td><span data-ttu-id="33615-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span><span class="sxs-lookup"><span data-stu-id="33615-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-698">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-698">Display Name</span></span></td>
<td><span data-ttu-id="33615-699">"Временные файлы Интернета".</span><span class="sxs-lookup"><span data-stu-id="33615-699">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-700">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-700">Folder Type</span></span></td>
<td><span data-ttu-id="33615-701">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-701">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-702">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-702">Default Path</span></span></td>
<td><span data-ttu-id="33615-703">%Локалаппдата%\микрософт\виндовс\темпорари файлы Интернета</span><span class="sxs-lookup"><span data-stu-id="33615-703">%LOCALAPPDATA%\Microsoft\Windows\Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-704">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-704">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-705">CSIDL_INTERNET_CACHE</span><span class="sxs-lookup"><span data-stu-id="33615-705">CSIDL_INTERNET_CACHE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-706">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-706">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-707">"Временные файлы Интернета".</span><span class="sxs-lookup"><span data-stu-id="33615-707">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-708">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-708">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-709">%Усерпрофиле%\локал Сеттингс\темпорари файлы Интернета</span><span class="sxs-lookup"><span data-stu-id="33615-709">%USERPROFILE%\Local Settings\Temporary Internet Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_InternetFolder"></span><span id="folderid_internetfolder"></span><span id="FOLDERID_INTERNETFOLDER"></span><dl> <span data-ttu-id="33615-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-711">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-711">GUID</span></span></td>
<td><span data-ttu-id="33615-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span><span class="sxs-lookup"><span data-stu-id="33615-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-713">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-713">Display Name</span></span></td>
<td><span data-ttu-id="33615-714">сеть Интернет;</span><span class="sxs-lookup"><span data-stu-id="33615-714">The Internet</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-715">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-715">Folder Type</span></span></td>
<td><span data-ttu-id="33615-716">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-716">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-717">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-717">Default Path</span></span></td>
<td><span data-ttu-id="33615-718">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-718">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-719">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-719">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-720">CSIDL_INTERNET</span><span class="sxs-lookup"><span data-stu-id="33615-720">CSIDL_INTERNET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-721">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-721">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-722">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="33615-722">Internet Explorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-723">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-723">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-724">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-724">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Libraries"></span><span id="folderid_libraries"></span><span id="FOLDERID_LIBRARIES"></span><dl> <span data-ttu-id="33615-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-726">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-726">GUID</span></span></td>
<td><span data-ttu-id="33615-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span><span class="sxs-lookup"><span data-stu-id="33615-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-728">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-728">Display Name</span></span></td>
<td><span data-ttu-id="33615-729">Библиотеки</span><span class="sxs-lookup"><span data-stu-id="33615-729">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-730">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-730">Folder Type</span></span></td>
<td><span data-ttu-id="33615-731">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-731">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-732">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-732">Default Path</span></span></td>
<td><span data-ttu-id="33615-733">%аппдата%\микрософт\виндовс\либрариес</span><span class="sxs-lookup"><span data-stu-id="33615-733">%APPDATA%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-734">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-734">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-735">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-735">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-736">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-736">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-737">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-737">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-738">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-738">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-739">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-739">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Links"></span><span id="folderid_links"></span><span id="FOLDERID_LINKS"></span><dl> <span data-ttu-id="33615-740"><dt><strong>FOLDERID_Links</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-740"><dt><strong>FOLDERID_Links</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-741">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-741">GUID</span></span></td>
<td><span data-ttu-id="33615-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span><span class="sxs-lookup"><span data-stu-id="33615-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-743">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-743">Display Name</span></span></td>
<td><span data-ttu-id="33615-744">Ссылки</span><span class="sxs-lookup"><span data-stu-id="33615-744">Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-745">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-745">Folder Type</span></span></td>
<td><span data-ttu-id="33615-746">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-746">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-747">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-747">Default Path</span></span></td>
<td><span data-ttu-id="33615-748">%усерпрофиле%\линкс</span><span class="sxs-lookup"><span data-stu-id="33615-748">%USERPROFILE%\Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-749">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-749">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-750">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-750">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-751">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-751">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-752">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-752">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-753">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-753">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-754">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-754">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalAppData"></span><span id="folderid_localappdata"></span><span id="FOLDERID_LOCALAPPDATA"></span><dl> <span data-ttu-id="33615-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-756">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-756">GUID</span></span></td>
<td><span data-ttu-id="33615-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span><span class="sxs-lookup"><span data-stu-id="33615-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-758">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-758">Display Name</span></span></td>
<td><span data-ttu-id="33615-759">Локальная</span><span class="sxs-lookup"><span data-stu-id="33615-759">Local</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-760">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-760">Folder Type</span></span></td>
<td><span data-ttu-id="33615-761">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-761">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-762">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-762">Default Path</span></span></td>
<td><span data-ttu-id="33615-763">% LOCALAPPDATA% (%Усерпрофиле%\аппдата\локал)</span><span class="sxs-lookup"><span data-stu-id="33615-763">%LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-764">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-764">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-765">CSIDL_LOCAL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="33615-765">CSIDL_LOCAL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-766">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-766">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-767">Данные приложений</span><span class="sxs-lookup"><span data-stu-id="33615-767">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-768">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-768">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-769">%Усерпрофиле%\локал Settings\Application данные</span><span class="sxs-lookup"><span data-stu-id="33615-769">%USERPROFILE%\Local Settings\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_LocalAppDataLow"></span><span id="folderid_localappdatalow"></span><span id="FOLDERID_LOCALAPPDATALOW"></span><dl> <span data-ttu-id="33615-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-771">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-771">GUID</span></span></td>
<td><span data-ttu-id="33615-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span><span class="sxs-lookup"><span data-stu-id="33615-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-773">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-773">Display Name</span></span></td>
<td><span data-ttu-id="33615-774">локаллов</span><span class="sxs-lookup"><span data-stu-id="33615-774">LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-775">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-775">Folder Type</span></span></td>
<td><span data-ttu-id="33615-776">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-776">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-777">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-777">Default Path</span></span></td>
<td><span data-ttu-id="33615-778">%усерпрофиле%\аппдата\локаллов</span><span class="sxs-lookup"><span data-stu-id="33615-778">%USERPROFILE%\AppData\LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-779">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-779">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-780">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-780">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-781">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-781">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-782">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-782">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-783">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-783">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-784">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-784">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalizedResourcesDir"></span><span id="folderid_localizedresourcesdir"></span><span id="FOLDERID_LOCALIZEDRESOURCESDIR"></span><dl> <span data-ttu-id="33615-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-786">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-786">GUID</span></span></td>
<td><span data-ttu-id="33615-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span><span class="sxs-lookup"><span data-stu-id="33615-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-788">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-788">Display Name</span></span></td>
<td><span data-ttu-id="33615-789">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-789">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-790">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-790">Folder Type</span></span></td>
<td><span data-ttu-id="33615-791">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-791">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-792">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-792">Default Path</span></span></td>
<td><span data-ttu-id="33615-793">%WINDIR%\resources\0409 (кодовая страница)</span><span class="sxs-lookup"><span data-stu-id="33615-793">%windir%\resources\0409 (code page)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-794">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-794">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-795">CSIDL_RESOURCES_LOCALIZED</span><span class="sxs-lookup"><span data-stu-id="33615-795">CSIDL_RESOURCES_LOCALIZED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-796">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-796">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-797">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-797">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-798">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-798">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-799">%WINDIR%\resources\0409 (кодовая страница)</span><span class="sxs-lookup"><span data-stu-id="33615-799">%windir%\resources\0409 (code page)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Music"></span><span id="folderid_music"></span><span id="FOLDERID_MUSIC"></span><dl> <span data-ttu-id="33615-800"><dt><strong>FOLDERID_Music</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-800"><dt><strong>FOLDERID_Music</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-801">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-801">GUID</span></span></td>
<td><span data-ttu-id="33615-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span><span class="sxs-lookup"><span data-stu-id="33615-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-803">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-803">Display Name</span></span></td>
<td><span data-ttu-id="33615-804">Музыка</span><span class="sxs-lookup"><span data-stu-id="33615-804">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-805">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-805">Folder Type</span></span></td>
<td><span data-ttu-id="33615-806">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-806">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-807">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-807">Default Path</span></span></td>
<td><span data-ttu-id="33615-808">%усерпрофиле%\мусик</span><span class="sxs-lookup"><span data-stu-id="33615-808">%USERPROFILE%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-809">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-809">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-810">CSIDL_MYMUSIC</span><span class="sxs-lookup"><span data-stu-id="33615-810">CSIDL_MYMUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-811">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-811">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-812">Моя музыка</span><span class="sxs-lookup"><span data-stu-id="33615-812">My Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-813">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-813">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-814">%USERPROFILE%\My документы \ Моя музыка</span><span class="sxs-lookup"><span data-stu-id="33615-814">%USERPROFILE%\My Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_MusicLibrary"></span><span id="folderid_musiclibrary"></span><span id="FOLDERID_MUSICLIBRARY"></span><dl> <span data-ttu-id="33615-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-816">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-816">GUID</span></span></td>
<td><span data-ttu-id="33615-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span><span class="sxs-lookup"><span data-stu-id="33615-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-818">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-818">Display Name</span></span></td>
<td><span data-ttu-id="33615-819">Музыка</span><span class="sxs-lookup"><span data-stu-id="33615-819">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-820">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-820">Folder Type</span></span></td>
<td><span data-ttu-id="33615-821">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-821">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-822">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-822">Default Path</span></span></td>
<td><span data-ttu-id="33615-823">%аппдата%\микрософт\виндовс\либрариес\мусик.либрари-мс</span><span class="sxs-lookup"><span data-stu-id="33615-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-824">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-824">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-825">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-825">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-826">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-826">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-827">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-827">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-828">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-828">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-829">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-829">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_NetHood"></span><span id="folderid_nethood"></span><span id="FOLDERID_NETHOOD"></span><dl> <span data-ttu-id="33615-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-831">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-831">GUID</span></span></td>
<td><span data-ttu-id="33615-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span><span class="sxs-lookup"><span data-stu-id="33615-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-833">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-833">Display Name</span></span></td>
<td><span data-ttu-id="33615-834">Ярлыки сети</span><span class="sxs-lookup"><span data-stu-id="33615-834">Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-835">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-835">Folder Type</span></span></td>
<td><span data-ttu-id="33615-836">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-836">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-837">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-837">Default Path</span></span></td>
<td><span data-ttu-id="33615-838">Сочетания клавиш%Аппдата%\микрософт\виндовс\нетворк</span><span class="sxs-lookup"><span data-stu-id="33615-838">%APPDATA%\Microsoft\Windows\Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-839">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-839">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-840">CSIDL_NETHOOD</span><span class="sxs-lookup"><span data-stu-id="33615-840">CSIDL_NETHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-841">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-841">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-842">несуд</span><span class="sxs-lookup"><span data-stu-id="33615-842">NetHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-843">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-843">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-844">%усерпрофиле%\несуд</span><span class="sxs-lookup"><span data-stu-id="33615-844">%USERPROFILE%\NetHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_NetworkFolder"></span><span id="folderid_networkfolder"></span><span id="FOLDERID_NETWORKFOLDER"></span><dl> <span data-ttu-id="33615-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-846">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-846">GUID</span></span></td>
<td><span data-ttu-id="33615-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span><span class="sxs-lookup"><span data-stu-id="33615-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-848">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-848">Display Name</span></span></td>
<td><span data-ttu-id="33615-849">Сеть</span><span class="sxs-lookup"><span data-stu-id="33615-849">Network</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-850">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-850">Folder Type</span></span></td>
<td><span data-ttu-id="33615-851">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-851">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-852">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-852">Default Path</span></span></td>
<td><span data-ttu-id="33615-853">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-853">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-854">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-854">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span><span class="sxs-lookup"><span data-stu-id="33615-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-856">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-856">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-857">Мое сетевое окружение</span><span class="sxs-lookup"><span data-stu-id="33615-857">My Network Places</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-858">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-858">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-859">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-859">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Objects3D"></span><span id="folderid_objects3d"></span><span id="FOLDERID_OBJECTS3D"></span><dl> <span data-ttu-id="33615-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-861">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-861">GUID</span></span></td>
<td><span data-ttu-id="33615-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span><span class="sxs-lookup"><span data-stu-id="33615-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-863">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-863">Display Name</span></span></td>
<td><span data-ttu-id="33615-864">Трехмерные объекты</span><span class="sxs-lookup"><span data-stu-id="33615-864">3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-865">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-865">Folder Type</span></span></td>
<td><span data-ttu-id="33615-866">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-866">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-867">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-867">Default Path</span></span></td>
<td><span data-ttu-id="33615-868">Объекты%USERPROFILE%\3D</span><span class="sxs-lookup"><span data-stu-id="33615-868">%USERPROFILE%\3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-869">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-869">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-870">Нет, значение введено в Windows 10, версия 1703</span><span class="sxs-lookup"><span data-stu-id="33615-870">None, value introduced in Windows 10, version 1703</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-871">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-871">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-872">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-872">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-873">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-873">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-874">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-874">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_OriginalImages"></span><span id="folderid_originalimages"></span><span id="FOLDERID_ORIGINALIMAGES"></span><dl> <span data-ttu-id="33615-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-876">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-876">GUID</span></span></td>
<td><span data-ttu-id="33615-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span><span class="sxs-lookup"><span data-stu-id="33615-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-878">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-878">Display Name</span></span></td>
<td><span data-ttu-id="33615-879">Исходные образы</span><span class="sxs-lookup"><span data-stu-id="33615-879">Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-880">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-880">Folder Type</span></span></td>
<td><span data-ttu-id="33615-881">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-881">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-882">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-882">Default Path</span></span></td>
<td><span data-ttu-id="33615-883">Изображения%Локалаппдата%\микрософт\виндовс Photo Галлери\оригинал</span><span class="sxs-lookup"><span data-stu-id="33615-883">%LOCALAPPDATA%\Microsoft\Windows Photo Gallery\Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-884">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-884">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-885">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-885">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-886">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-886">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-887">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-887">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-888">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-888">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-889">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-889">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PhotoAlbums"></span><span id="folderid_photoalbums"></span><span id="FOLDERID_PHOTOALBUMS"></span><dl> <span data-ttu-id="33615-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-891">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-891">GUID</span></span></td>
<td><span data-ttu-id="33615-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span><span class="sxs-lookup"><span data-stu-id="33615-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-893">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-893">Display Name</span></span></td>
<td><span data-ttu-id="33615-894">Слайдовые шоу</span><span class="sxs-lookup"><span data-stu-id="33615-894">Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-895">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-895">Folder Type</span></span></td>
<td><span data-ttu-id="33615-896">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-896">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-897">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-897">Default Path</span></span></td>
<td><span data-ttu-id="33615-898">%Усерпрофиле%\пиктурес\слиде показывает</span><span class="sxs-lookup"><span data-stu-id="33615-898">%USERPROFILE%\Pictures\Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-899">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-899">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-900">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-900">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-901">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-901">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-902">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-902">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-903">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-903">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-904">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-904">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PicturesLibrary"></span><span id="folderid_pictureslibrary"></span><span id="FOLDERID_PICTURESLIBRARY"></span><dl> <span data-ttu-id="33615-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-906">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-906">GUID</span></span></td>
<td><span data-ttu-id="33615-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span><span class="sxs-lookup"><span data-stu-id="33615-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-908">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-908">Display Name</span></span></td>
<td><span data-ttu-id="33615-909">Изображения</span><span class="sxs-lookup"><span data-stu-id="33615-909">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-910">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-910">Folder Type</span></span></td>
<td><span data-ttu-id="33615-911">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-911">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-912">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-912">Default Path</span></span></td>
<td><span data-ttu-id="33615-913">%аппдата%\микрософт\виндовс\либрариес\пиктурес.либрари-мс</span><span class="sxs-lookup"><span data-stu-id="33615-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-914">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-914">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-915">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-915">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-916">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-916">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-917">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-917">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-918">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-918">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-919">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-919">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Pictures"></span><span id="folderid_pictures"></span><span id="FOLDERID_PICTURES"></span><dl> <span data-ttu-id="33615-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-921">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-921">GUID</span></span></td>
<td><span data-ttu-id="33615-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span><span class="sxs-lookup"><span data-stu-id="33615-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-923">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-923">Display Name</span></span></td>
<td><span data-ttu-id="33615-924">Изображения</span><span class="sxs-lookup"><span data-stu-id="33615-924">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-925">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-925">Folder Type</span></span></td>
<td><span data-ttu-id="33615-926">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-926">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-927">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-927">Default Path</span></span></td>
<td><span data-ttu-id="33615-928">%усерпрофиле%\пиктурес</span><span class="sxs-lookup"><span data-stu-id="33615-928">%USERPROFILE%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-929">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-929">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-930">CSIDL_MYPICTURES</span><span class="sxs-lookup"><span data-stu-id="33615-930">CSIDL_MYPICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-931">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-931">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-932">Мои рисунки</span><span class="sxs-lookup"><span data-stu-id="33615-932">My Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-933">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-933">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-934">%USERPROFILE%\My документы \ мои рисунки</span><span class="sxs-lookup"><span data-stu-id="33615-934">%USERPROFILE%\My Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Playlists"></span><span id="folderid_playlists"></span><span id="FOLDERID_PLAYLISTS"></span><dl> <span data-ttu-id="33615-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-936">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-936">GUID</span></span></td>
<td><span data-ttu-id="33615-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span><span class="sxs-lookup"><span data-stu-id="33615-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-938">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-938">Display Name</span></span></td>
<td><span data-ttu-id="33615-939">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="33615-939">Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-940">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-940">Folder Type</span></span></td>
<td><span data-ttu-id="33615-941">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-941">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-942">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-942">Default Path</span></span></td>
<td><span data-ttu-id="33615-943">%усерпрофиле%\мусик\плайлистс</span><span class="sxs-lookup"><span data-stu-id="33615-943">%USERPROFILE%\Music\Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-944">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-944">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-945">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-945">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-946">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-946">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-947">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-947">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-948">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-948">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-949">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-949">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PrintersFolder"></span><span id="folderid_printersfolder"></span><span id="FOLDERID_PRINTERSFOLDER"></span><dl> <span data-ttu-id="33615-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-951">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-951">GUID</span></span></td>
<td><span data-ttu-id="33615-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span><span class="sxs-lookup"><span data-stu-id="33615-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-953">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-953">Display Name</span></span></td>
<td><span data-ttu-id="33615-954">принтеры;</span><span class="sxs-lookup"><span data-stu-id="33615-954">Printers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-955">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-955">Folder Type</span></span></td>
<td><span data-ttu-id="33615-956">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-956">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-957">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-957">Default Path</span></span></td>
<td><span data-ttu-id="33615-958">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-958">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-959">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-959">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-960">CSIDL_PRINTERS</span><span class="sxs-lookup"><span data-stu-id="33615-960">CSIDL_PRINTERS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-961">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-961">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-962">Принтеры и факсы</span><span class="sxs-lookup"><span data-stu-id="33615-962">Printers and Faxes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-963">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-963">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-964">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-964">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PrintHood"></span><span id="folderid_printhood"></span><span id="FOLDERID_PRINTHOOD"></span><dl> <span data-ttu-id="33615-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-966">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-966">GUID</span></span></td>
<td><span data-ttu-id="33615-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span><span class="sxs-lookup"><span data-stu-id="33615-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-968">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-968">Display Name</span></span></td>
<td><span data-ttu-id="33615-969">Ярлыки принтеров</span><span class="sxs-lookup"><span data-stu-id="33615-969">Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-970">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-970">Folder Type</span></span></td>
<td><span data-ttu-id="33615-971">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-971">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-972">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-972">Default Path</span></span></td>
<td><span data-ttu-id="33615-973">Сочетания клавиш%Аппдата%\микрософт\виндовс\принтер</span><span class="sxs-lookup"><span data-stu-id="33615-973">%APPDATA%\Microsoft\Windows\Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-974">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-974">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-975">CSIDL_PRINTHOOD</span><span class="sxs-lookup"><span data-stu-id="33615-975">CSIDL_PRINTHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-976">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-976">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-977">принсуд</span><span class="sxs-lookup"><span data-stu-id="33615-977">PrintHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-978">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-978">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-979">%усерпрофиле%\принсуд</span><span class="sxs-lookup"><span data-stu-id="33615-979">%USERPROFILE%\PrintHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Profile"></span><span id="folderid_profile"></span><span id="FOLDERID_PROFILE"></span><dl> <span data-ttu-id="33615-980"><dt><strong>FOLDERID_Profile</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-980"><dt><strong>FOLDERID_Profile</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-981">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-981">GUID</span></span></td>
<td><span data-ttu-id="33615-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span><span class="sxs-lookup"><span data-stu-id="33615-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-983">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-983">Display Name</span></span></td>
<td><span data-ttu-id="33615-984">Имя пользователя (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="33615-984">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-985">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-985">Folder Type</span></span></td>
<td><span data-ttu-id="33615-986">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-986">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-987">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-987">Default Path</span></span></td>
<td><span data-ttu-id="33615-988">% USERPROFILE% (%Системдриве%\усерс \% имя пользователя%)</span><span class="sxs-lookup"><span data-stu-id="33615-988">%USERPROFILE% (%SystemDrive%\Users\%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-989">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-989">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-990">CSIDL_PROFILE</span><span class="sxs-lookup"><span data-stu-id="33615-990">CSIDL_PROFILE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-991">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-991">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-992">Имя пользователя (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="33615-992">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-993">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-993">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-994">% USERPROFILE% (%Системдриве%\документс и параметры \% username%)</span><span class="sxs-lookup"><span data-stu-id="33615-994">%USERPROFILE% (%SystemDrive%\Documents and Settings\%USERNAME%)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramData"></span><span id="folderid_programdata"></span><span id="FOLDERID_PROGRAMDATA"></span><dl> <span data-ttu-id="33615-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-996">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-996">GUID</span></span></td>
<td><span data-ttu-id="33615-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span><span class="sxs-lookup"><span data-stu-id="33615-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-998">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-998">Display Name</span></span></td>
<td><span data-ttu-id="33615-999">ProgramData</span><span class="sxs-lookup"><span data-stu-id="33615-999">ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1000">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1000">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1001">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1001">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1002">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1002">Default Path</span></span></td>
<td><span data-ttu-id="33615-1003">% ALLUSERSPROFILE% (% папка ProgramData%,%Системдриве%\програмдата)</span><span class="sxs-lookup"><span data-stu-id="33615-1003">%ALLUSERSPROFILE% (%ProgramData%, %SystemDrive%\ProgramData)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1004">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1004">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1005">CSIDL_COMMON_APPDATA</span><span class="sxs-lookup"><span data-stu-id="33615-1005">CSIDL_COMMON_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1006">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1006">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1007">Данные приложений</span><span class="sxs-lookup"><span data-stu-id="33615-1007">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1008">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1008">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1009">Данные%Аллусерспрофиле%\аппликатион</span><span class="sxs-lookup"><span data-stu-id="33615-1009">%ALLUSERSPROFILE%\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFiles"></span><span id="folderid_programfiles"></span><span id="FOLDERID_PROGRAMFILES"></span><dl> <span data-ttu-id="33615-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="33615-1011">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="33615-1011">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1012">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1012">GUID</span></span></td>
<td><span data-ttu-id="33615-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span><span class="sxs-lookup"><span data-stu-id="33615-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1014">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1014">Display Name</span></span></td>
<td><span data-ttu-id="33615-1015">Program Files</span><span class="sxs-lookup"><span data-stu-id="33615-1015">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1016">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1016">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1017">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1017">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1018">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1018">Default Path</span></span></td>
<td><span data-ttu-id="33615-1019">% ProgramFiles% (файлов%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="33615-1019">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1020">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1020">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1021">CSIDL_PROGRAM_FILES</span><span class="sxs-lookup"><span data-stu-id="33615-1021">CSIDL_PROGRAM_FILES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1022">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1022">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1023">Program Files</span><span class="sxs-lookup"><span data-stu-id="33615-1023">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1024">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1024">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1025">% ProgramFiles% (файлов%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="33615-1025">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX64"></span><span id="folderid_programfilesx64"></span><span id="FOLDERID_PROGRAMFILESX64"></span><dl> <span data-ttu-id="33615-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="33615-1027">Это значение не поддерживается в 32-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="33615-1027">This value is not supported on 32-bit operating systems.</span></span> <span data-ttu-id="33615-1028">Он также не поддерживается для 32-разрядных приложений, работающих в 64-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="33615-1028">It also is not supported for 32-bit applications running on 64-bit operating systems.</span></span> <span data-ttu-id="33615-1029">Попытка использовать FOLDERID_ProgramFilesX64 в любой ситуации приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="33615-1029">Attempting to use FOLDERID_ProgramFilesX64 in either situation results in an error.</span></span> <span data-ttu-id="33615-1030">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="33615-1030">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1031">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1031">GUID</span></span></td>
<td><span data-ttu-id="33615-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span><span class="sxs-lookup"><span data-stu-id="33615-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1033">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1033">Display Name</span></span></td>
<td><span data-ttu-id="33615-1034">Program Files</span><span class="sxs-lookup"><span data-stu-id="33615-1034">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1035">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1035">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1036">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1036">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1037">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1037">Default Path</span></span></td>
<td><span data-ttu-id="33615-1038">% ProgramFiles% (файлов%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="33615-1038">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1039">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1039">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1040">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1040">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1041">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1041">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1042">Program Files</span><span class="sxs-lookup"><span data-stu-id="33615-1042">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1043">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1043">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1044">% ProgramFiles% (файлов%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="33615-1044">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX86"></span><span id="folderid_programfilesx86"></span><span id="FOLDERID_PROGRAMFILESX86"></span><dl> <span data-ttu-id="33615-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="33615-1046">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="33615-1046">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1047">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1047">GUID</span></span></td>
<td><span data-ttu-id="33615-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span><span class="sxs-lookup"><span data-stu-id="33615-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1049">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1049">Display Name</span></span></td>
<td><span data-ttu-id="33615-1050">Program Files</span><span class="sxs-lookup"><span data-stu-id="33615-1050">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1051">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1051">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1052">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1052">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1053">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1053">Default Path</span></span></td>
<td><span data-ttu-id="33615-1054">% ProgramFiles% (файлов%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="33615-1054">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1055">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1055">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1056">CSIDL_PROGRAM_FILESX86</span><span class="sxs-lookup"><span data-stu-id="33615-1056">CSIDL_PROGRAM_FILESX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1057">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1057">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1058">Program Files</span><span class="sxs-lookup"><span data-stu-id="33615-1058">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1059">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1059">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1060">% ProgramFiles% (файлов%SystemDrive%\Program)</span><span class="sxs-lookup"><span data-stu-id="33615-1060">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommon"></span><span id="folderid_programfilescommon"></span><span id="FOLDERID_PROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="33615-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="33615-1062">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="33615-1062">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1063">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1063">GUID</span></span></td>
<td><span data-ttu-id="33615-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span><span class="sxs-lookup"><span data-stu-id="33615-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1065">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1065">Display Name</span></span></td>
<td><span data-ttu-id="33615-1066">Общие файлы</span><span class="sxs-lookup"><span data-stu-id="33615-1066">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1067">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1067">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1068">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1068">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1069">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1069">Default Path</span></span></td>
<td><span data-ttu-id="33615-1070">Файлы%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="33615-1070">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1071">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1071">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1072">CSIDL_PROGRAM_FILES_COMMON</span><span class="sxs-lookup"><span data-stu-id="33615-1072">CSIDL_PROGRAM_FILES_COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1073">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1073">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1074">Общие файлы</span><span class="sxs-lookup"><span data-stu-id="33615-1074">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1075">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1075">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1076">Файлы%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="33615-1076">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX64"></span><span id="folderid_programfilescommonx64"></span><span id="FOLDERID_PROGRAMFILESCOMMONX64"></span><dl> <span data-ttu-id="33615-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="33615-1078">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="33615-1078">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1079">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1079">GUID</span></span></td>
<td><span data-ttu-id="33615-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span><span class="sxs-lookup"><span data-stu-id="33615-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1081">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1081">Display Name</span></span></td>
<td><span data-ttu-id="33615-1082">Общие файлы</span><span class="sxs-lookup"><span data-stu-id="33615-1082">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1083">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1083">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1084">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1084">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1085">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1085">Default Path</span></span></td>
<td><span data-ttu-id="33615-1086">Файлы%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="33615-1086">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1087">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1087">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1088">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1088">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1089">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1089">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1090">Общие файлы</span><span class="sxs-lookup"><span data-stu-id="33615-1090">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1091">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1091">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1092">Файлы%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="33615-1092">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX86"></span><span id="folderid_programfilescommonx86"></span><span id="FOLDERID_PROGRAMFILESCOMMONX86"></span><dl> <span data-ttu-id="33615-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="33615-1094">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="33615-1094">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1095">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1095">GUID</span></span></td>
<td><span data-ttu-id="33615-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span><span class="sxs-lookup"><span data-stu-id="33615-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1097">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1097">Display Name</span></span></td>
<td><span data-ttu-id="33615-1098">Общие файлы</span><span class="sxs-lookup"><span data-stu-id="33615-1098">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1099">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1099">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1100">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1100">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1101">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1101">Default Path</span></span></td>
<td><span data-ttu-id="33615-1102">Файлы%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="33615-1102">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1103">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1103">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1104">CSIDL_PROGRAM_FILES_COMMONX86</span><span class="sxs-lookup"><span data-stu-id="33615-1104">CSIDL_PROGRAM_FILES_COMMONX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1105">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1105">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1106">Общие файлы</span><span class="sxs-lookup"><span data-stu-id="33615-1106">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1107">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1107">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1108">Файлы%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="33615-1108">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Programs"></span><span id="folderid_programs"></span><span id="FOLDERID_PROGRAMS"></span><dl> <span data-ttu-id="33615-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1110">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1110">GUID</span></span></td>
<td><span data-ttu-id="33615-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span><span class="sxs-lookup"><span data-stu-id="33615-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1112">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1112">Display Name</span></span></td>
<td><span data-ttu-id="33615-1113">Programs</span><span class="sxs-lookup"><span data-stu-id="33615-1113">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1114">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1114">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1115">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1115">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1116">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1116">Default Path</span></span></td>
<td><span data-ttu-id="33615-1117">%Аппдата%\микрософт\виндовс\старт Мену\програмс</span><span class="sxs-lookup"><span data-stu-id="33615-1117">%APPDATA%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1118">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1118">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1119">CSIDL_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="33615-1119">CSIDL_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1120">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1120">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1121">Programs</span><span class="sxs-lookup"><span data-stu-id="33615-1121">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1122">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1122">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1123">%Усерпрофиле%\старт Мену\програмс</span><span class="sxs-lookup"><span data-stu-id="33615-1123">%USERPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Public"></span><span id="folderid_public"></span><span id="FOLDERID_PUBLIC"></span><dl> <span data-ttu-id="33615-1124"><dt><strong>FOLDERID_Public</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1124"><dt><strong>FOLDERID_Public</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1125">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1125">GUID</span></span></td>
<td><span data-ttu-id="33615-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span><span class="sxs-lookup"><span data-stu-id="33615-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1127">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1127">Display Name</span></span></td>
<td><span data-ttu-id="33615-1128">Общие</span><span class="sxs-lookup"><span data-stu-id="33615-1128">Public</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1129">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1129">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1130">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1130">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1131">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1131">Default Path</span></span></td>
<td><span data-ttu-id="33615-1132">% ОБЩЕГО% (%Системдриве%\усерс\публик)</span><span class="sxs-lookup"><span data-stu-id="33615-1132">%PUBLIC% (%SystemDrive%\Users\Public)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1133">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1133">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1134">Нет, новое для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-1134">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1135">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1135">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1136">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1136">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1137">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1137">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1138">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1138">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDesktop"></span><span id="folderid_publicdesktop"></span><span id="FOLDERID_PUBLICDESKTOP"></span><dl> <span data-ttu-id="33615-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1140">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1140">GUID</span></span></td>
<td><span data-ttu-id="33615-1141">{C4AA340D-F20F-4863-АФЕФ-F87EF2E6BA25}</span><span class="sxs-lookup"><span data-stu-id="33615-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1142">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1142">Display Name</span></span></td>
<td><span data-ttu-id="33615-1143">Общедоступный Рабочий стол</span><span class="sxs-lookup"><span data-stu-id="33615-1143">Public Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1144">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1144">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1145">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1145">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1146">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1146">Default Path</span></span></td>
<td><span data-ttu-id="33615-1147">%публик%\десктоп</span><span class="sxs-lookup"><span data-stu-id="33615-1147">%PUBLIC%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1148">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1148">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="33615-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1150">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1150">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1151">Персональный компьютер</span><span class="sxs-lookup"><span data-stu-id="33615-1151">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1152">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1152">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1153">%аллусерспрофиле%\десктоп</span><span class="sxs-lookup"><span data-stu-id="33615-1153">%ALLUSERSPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicDocuments"></span><span id="folderid_publicdocuments"></span><span id="FOLDERID_PUBLICDOCUMENTS"></span><dl> <span data-ttu-id="33615-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1155">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1155">GUID</span></span></td>
<td><span data-ttu-id="33615-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span><span class="sxs-lookup"><span data-stu-id="33615-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1157">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1157">Display Name</span></span></td>
<td><span data-ttu-id="33615-1158">Общие документы</span><span class="sxs-lookup"><span data-stu-id="33615-1158">Public Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1159">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1159">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1160">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1160">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1161">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1161">Default Path</span></span></td>
<td><span data-ttu-id="33615-1162">%публик%\документс</span><span class="sxs-lookup"><span data-stu-id="33615-1162">%PUBLIC%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1163">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1163">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1164">CSIDL_COMMON_DOCUMENTS</span><span class="sxs-lookup"><span data-stu-id="33615-1164">CSIDL_COMMON_DOCUMENTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1165">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1165">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1166">Общие документы</span><span class="sxs-lookup"><span data-stu-id="33615-1166">Shared Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1167">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1167">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1168">%аллусерспрофиле%\документс</span><span class="sxs-lookup"><span data-stu-id="33615-1168">%ALLUSERSPROFILE%\Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDownloads"></span><span id="folderid_publicdownloads"></span><span id="FOLDERID_PUBLICDOWNLOADS"></span><dl> <span data-ttu-id="33615-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1170">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1170">GUID</span></span></td>
<td><span data-ttu-id="33615-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span><span class="sxs-lookup"><span data-stu-id="33615-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1172">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1172">Display Name</span></span></td>
<td><span data-ttu-id="33615-1173">Общие загрузки</span><span class="sxs-lookup"><span data-stu-id="33615-1173">Public Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1174">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1174">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1175">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1175">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1176">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1176">Default Path</span></span></td>
<td><span data-ttu-id="33615-1177">%публик%\довнлоадс</span><span class="sxs-lookup"><span data-stu-id="33615-1177">%PUBLIC%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1178">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1178">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1179">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-1179">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1180">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1180">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1181">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1181">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1182">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1182">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1183">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1183">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicGameTasks"></span><span id="folderid_publicgametasks"></span><span id="FOLDERID_PUBLICGAMETASKS"></span><dl> <span data-ttu-id="33615-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1185">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1185">GUID</span></span></td>
<td><span data-ttu-id="33615-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span><span class="sxs-lookup"><span data-stu-id="33615-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1187">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1187">Display Name</span></span></td>
<td><span data-ttu-id="33615-1188">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="33615-1188">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1189">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1189">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1190">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1190">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1191">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1191">Default Path</span></span></td>
<td><span data-ttu-id="33615-1192">%аллусерспрофиле%\микрософт\виндовс\гамиксплорер</span><span class="sxs-lookup"><span data-stu-id="33615-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1193">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1193">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1194">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-1194">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1195">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1195">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1196">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1196">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1197">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1197">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1198">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1198">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicLibraries"></span><span id="folderid_publiclibraries"></span><span id="FOLDERID_PUBLICLIBRARIES"></span><dl> <span data-ttu-id="33615-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1200">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1200">GUID</span></span></td>
<td><span data-ttu-id="33615-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span><span class="sxs-lookup"><span data-stu-id="33615-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1202">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1202">Display Name</span></span></td>
<td><span data-ttu-id="33615-1203">Библиотеки</span><span class="sxs-lookup"><span data-stu-id="33615-1203">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1204">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1204">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1205">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1205">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1206">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1206">Default Path</span></span></td>
<td><span data-ttu-id="33615-1207">%аллусерспрофиле%\микрософт\виндовс\либрариес</span><span class="sxs-lookup"><span data-stu-id="33615-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1208">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1208">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1209">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-1209">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1210">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1210">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1211">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1211">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1212">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1212">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1213">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1213">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicMusic"></span><span id="folderid_publicmusic"></span><span id="FOLDERID_PUBLICMUSIC"></span><dl> <span data-ttu-id="33615-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1215">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1215">GUID</span></span></td>
<td><span data-ttu-id="33615-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span><span class="sxs-lookup"><span data-stu-id="33615-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1217">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1217">Display Name</span></span></td>
<td><span data-ttu-id="33615-1218">Общая музыка</span><span class="sxs-lookup"><span data-stu-id="33615-1218">Public Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1219">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1219">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1220">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1220">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1221">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1221">Default Path</span></span></td>
<td><span data-ttu-id="33615-1222">%публик%\мусик</span><span class="sxs-lookup"><span data-stu-id="33615-1222">%PUBLIC%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1223">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1223">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1224">CSIDL_COMMON_MUSIC</span><span class="sxs-lookup"><span data-stu-id="33615-1224">CSIDL_COMMON_MUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1225">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1225">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1226">Общая музыка</span><span class="sxs-lookup"><span data-stu-id="33615-1226">Shared Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1227">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1227">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1228">%Аллусерспрофиле%\документс\ми музыка</span><span class="sxs-lookup"><span data-stu-id="33615-1228">%ALLUSERSPROFILE%\Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicPictures"></span><span id="folderid_publicpictures"></span><span id="FOLDERID_PUBLICPICTURES"></span><dl> <span data-ttu-id="33615-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1230">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1230">GUID</span></span></td>
<td><span data-ttu-id="33615-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span><span class="sxs-lookup"><span data-stu-id="33615-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1232">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1232">Display Name</span></span></td>
<td><span data-ttu-id="33615-1233">Общедоступные рисунки</span><span class="sxs-lookup"><span data-stu-id="33615-1233">Public Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1234">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1234">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1235">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1235">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1236">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1236">Default Path</span></span></td>
<td><span data-ttu-id="33615-1237">%публик%\пиктурес</span><span class="sxs-lookup"><span data-stu-id="33615-1237">%PUBLIC%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1238">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1238">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1239">CSIDL_COMMON_PICTURES</span><span class="sxs-lookup"><span data-stu-id="33615-1239">CSIDL_COMMON_PICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1240">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1240">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1241">Общие рисунки</span><span class="sxs-lookup"><span data-stu-id="33615-1241">Shared Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1242">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1242">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1243">%Аллусерспрофиле%\документс\ми изображения</span><span class="sxs-lookup"><span data-stu-id="33615-1243">%ALLUSERSPROFILE%\Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicRingtones"></span><span id="folderid_publicringtones"></span><span id="FOLDERID_PUBLICRINGTONES"></span><dl> <span data-ttu-id="33615-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1245">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1245">GUID</span></span></td>
<td><span data-ttu-id="33615-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span><span class="sxs-lookup"><span data-stu-id="33615-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1247">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1247">Display Name</span></span></td>
<td><span data-ttu-id="33615-1248">Мелодии звонка</span><span class="sxs-lookup"><span data-stu-id="33615-1248">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1249">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1249">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1250">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1250">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1251">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1251">Default Path</span></span></td>
<td><span data-ttu-id="33615-1252">%аллусерспрофиле%\микрософт\виндовс\рингтонес</span><span class="sxs-lookup"><span data-stu-id="33615-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1253">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1253">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1254">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-1254">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1255">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1255">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1256">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1256">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1257">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1257">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1258">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1258">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicUserTiles"></span><span id="folderid_publicusertiles"></span><span id="FOLDERID_PUBLICUSERTILES"></span><dl> <span data-ttu-id="33615-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1260">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1260">GUID</span></span></td>
<td><span data-ttu-id="33615-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span><span class="sxs-lookup"><span data-stu-id="33615-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1262">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1262">Display Name</span></span></td>
<td><span data-ttu-id="33615-1263">Изображения общедоступной учетной записи</span><span class="sxs-lookup"><span data-stu-id="33615-1263">Public Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1264">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1264">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1265">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1265">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1266">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1266">Default Path</span></span></td>
<td><span data-ttu-id="33615-1267">%публик%\аккаунтпиктурес</span><span class="sxs-lookup"><span data-stu-id="33615-1267">%PUBLIC%\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1268">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1268">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1269">Нет, значение, введенное в Windows 8</span><span class="sxs-lookup"><span data-stu-id="33615-1269">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1270">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1270">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1271">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1271">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1272">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1272">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1273">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1273">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicVideos"></span><span id="folderid_publicvideos"></span><span id="FOLDERID_PUBLICVIDEOS"></span><dl> <span data-ttu-id="33615-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1275">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1275">GUID</span></span></td>
<td><span data-ttu-id="33615-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span><span class="sxs-lookup"><span data-stu-id="33615-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1277">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1277">Display Name</span></span></td>
<td><span data-ttu-id="33615-1278">Общие видео</span><span class="sxs-lookup"><span data-stu-id="33615-1278">Public Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1279">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1279">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1280">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1280">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1281">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1281">Default Path</span></span></td>
<td><span data-ttu-id="33615-1282">%публик%\видеос</span><span class="sxs-lookup"><span data-stu-id="33615-1282">%PUBLIC%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1283">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1283">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1284">CSIDL_COMMON_VIDEO</span><span class="sxs-lookup"><span data-stu-id="33615-1284">CSIDL_COMMON_VIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1285">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1285">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1286">Общее видео</span><span class="sxs-lookup"><span data-stu-id="33615-1286">Shared Video</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1287">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1287">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1288">Видео%Аллусерспрофиле%\документс\ми</span><span class="sxs-lookup"><span data-stu-id="33615-1288">%ALLUSERSPROFILE%\Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_QuickLaunch"></span><span id="folderid_quicklaunch"></span><span id="FOLDERID_QUICKLAUNCH"></span><dl> <span data-ttu-id="33615-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1290">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1290">GUID</span></span></td>
<td><span data-ttu-id="33615-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span><span class="sxs-lookup"><span data-stu-id="33615-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1292">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1292">Display Name</span></span></td>
<td><span data-ttu-id="33615-1293">Быстрый запуск</span><span class="sxs-lookup"><span data-stu-id="33615-1293">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1294">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1294">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1295">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1295">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1296">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1296">Default Path</span></span></td>
<td><span data-ttu-id="33615-1297">Запуск Експлорер\куикк%Аппдата%\микрософт\интернет</span><span class="sxs-lookup"><span data-stu-id="33615-1297">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1298">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1298">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1299">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1299">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1300">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1300">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1301">Быстрый запуск</span><span class="sxs-lookup"><span data-stu-id="33615-1301">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1302">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1302">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1303">Запуск Експлорер\куикк%Аппдата%\микрософт\интернет</span><span class="sxs-lookup"><span data-stu-id="33615-1303">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Recent"></span><span id="folderid_recent"></span><span id="FOLDERID_RECENT"></span><dl> <span data-ttu-id="33615-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1305">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1305">GUID</span></span></td>
<td><span data-ttu-id="33615-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span><span class="sxs-lookup"><span data-stu-id="33615-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1307">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1307">Display Name</span></span></td>
<td><span data-ttu-id="33615-1308">Недавние элементы</span><span class="sxs-lookup"><span data-stu-id="33615-1308">Recent Items</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1309">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1309">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1310">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1310">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1311">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1311">Default Path</span></span></td>
<td><span data-ttu-id="33615-1312">%аппдата%\микрософт\виндовс\рецент</span><span class="sxs-lookup"><span data-stu-id="33615-1312">%APPDATA%\Microsoft\Windows\Recent</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1313">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1313">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1314">CSIDL_RECENT</span><span class="sxs-lookup"><span data-stu-id="33615-1314">CSIDL_RECENT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1315">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1315">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1316">Мои недавние документы</span><span class="sxs-lookup"><span data-stu-id="33615-1316">My Recent Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1317">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1317">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1318">%усерпрофиле%\рецент</span><span class="sxs-lookup"><span data-stu-id="33615-1318">%USERPROFILE%\Recent</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecordedTV"></span><span id="folderid_recordedtv"></span><span id="FOLDERID_RECORDEDTV"></span><dl> <span data-ttu-id="33615-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="33615-1320">Не используется.</span><span class="sxs-lookup"><span data-stu-id="33615-1320">Not used.</span></span> <span data-ttu-id="33615-1321">Это значение не определено в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="33615-1321">This value is undefined as of Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RecordedTVLibrary"></span><span id="folderid_recordedtvlibrary"></span><span id="FOLDERID_RECORDEDTVLIBRARY"></span><dl> <span data-ttu-id="33615-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1323">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1323">GUID</span></span></td>
<td><span data-ttu-id="33615-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span><span class="sxs-lookup"><span data-stu-id="33615-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1325">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1325">Display Name</span></span></td>
<td><span data-ttu-id="33615-1326">ТВ-записи</span><span class="sxs-lookup"><span data-stu-id="33615-1326">Recorded TV</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1327">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1327">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1328">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1328">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1329">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1329">Default Path</span></span></td>
<td><span data-ttu-id="33615-1330">%публик%\рекордедтв.либрари-мс</span><span class="sxs-lookup"><span data-stu-id="33615-1330">%PUBLIC%\RecordedTV.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1331">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1331">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1332">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-1332">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1333">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1333">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1334">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1334">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1335">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1335">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1336">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecycleBinFolder"></span><span id="folderid_recyclebinfolder"></span><span id="FOLDERID_RECYCLEBINFOLDER"></span><dl> <span data-ttu-id="33615-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1338">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1338">GUID</span></span></td>
<td><span data-ttu-id="33615-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span><span class="sxs-lookup"><span data-stu-id="33615-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1340">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1340">Display Name</span></span></td>
<td><span data-ttu-id="33615-1341">Корзина</span><span class="sxs-lookup"><span data-stu-id="33615-1341">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1342">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1342">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1343">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-1343">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1344">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1344">Default Path</span></span></td>
<td><span data-ttu-id="33615-1345">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-1345">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1346">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1346">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1347">CSIDL_BITBUCKET</span><span class="sxs-lookup"><span data-stu-id="33615-1347">CSIDL_BITBUCKET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1348">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1348">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1349">Корзина</span><span class="sxs-lookup"><span data-stu-id="33615-1349">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1350">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1350">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1351">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-1351">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ResourceDir"></span><span id="folderid_resourcedir"></span><span id="FOLDERID_RESOURCEDIR"></span><dl> <span data-ttu-id="33615-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1353">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1353">GUID</span></span></td>
<td><span data-ttu-id="33615-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span><span class="sxs-lookup"><span data-stu-id="33615-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1355">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1355">Display Name</span></span></td>
<td><span data-ttu-id="33615-1356">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="33615-1356">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1357">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1357">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1358">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1358">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1359">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1359">Default Path</span></span></td>
<td><span data-ttu-id="33615-1360">%виндир%\ресаурцес</span><span class="sxs-lookup"><span data-stu-id="33615-1360">%windir%\Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1361">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1361">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1362">CSIDL_RESOURCES</span><span class="sxs-lookup"><span data-stu-id="33615-1362">CSIDL_RESOURCES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1363">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1363">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1364">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="33615-1364">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1365">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1365">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1366">%виндир%\ресаурцес</span><span class="sxs-lookup"><span data-stu-id="33615-1366">%windir%\Resources</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Ringtones"></span><span id="folderid_ringtones"></span><span id="FOLDERID_RINGTONES"></span><dl> <span data-ttu-id="33615-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1368">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1368">GUID</span></span></td>
<td><span data-ttu-id="33615-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span><span class="sxs-lookup"><span data-stu-id="33615-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1370">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1370">Display Name</span></span></td>
<td><span data-ttu-id="33615-1371">Мелодии звонка</span><span class="sxs-lookup"><span data-stu-id="33615-1371">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1372">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1372">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1373">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1373">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1374">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1374">Default Path</span></span></td>
<td><span data-ttu-id="33615-1375">%локалаппдата%\микрософт\виндовс\рингтонес</span><span class="sxs-lookup"><span data-stu-id="33615-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1376">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1376">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1377">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-1377">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1378">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1378">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1379">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1379">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1380">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1380">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1381">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1381">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingAppData"></span><span id="folderid_roamingappdata"></span><span id="FOLDERID_ROAMINGAPPDATA"></span><dl> <span data-ttu-id="33615-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1383">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1383">GUID</span></span></td>
<td><span data-ttu-id="33615-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span><span class="sxs-lookup"><span data-stu-id="33615-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1385">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1385">Display Name</span></span></td>
<td><span data-ttu-id="33615-1386">Роуминг</span><span class="sxs-lookup"><span data-stu-id="33615-1386">Roaming</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1387">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1387">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1388">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1388">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1389">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1389">Default Path</span></span></td>
<td><span data-ttu-id="33615-1390">% APPDATA% (%Усерпрофиле%\аппдата\роаминг)</span><span class="sxs-lookup"><span data-stu-id="33615-1390">%APPDATA% (%USERPROFILE%\AppData\Roaming)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1391">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1391">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1392">CSIDL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="33615-1392">CSIDL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1393">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1393">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1394">Данные приложений</span><span class="sxs-lookup"><span data-stu-id="33615-1394">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1395">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1395">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1396">% APPDATA% (данные%USERPROFILE%\Application)</span><span class="sxs-lookup"><span data-stu-id="33615-1396">%APPDATA% (%USERPROFILE%\Application Data)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RoamedTileImages"></span><span id="folderid_roamedtileimages"></span><span id="FOLDERID_ROAMEDTILEIMAGES"></span><dl> <span data-ttu-id="33615-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1398">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1398">GUID</span></span></td>
<td><span data-ttu-id="33615-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span><span class="sxs-lookup"><span data-stu-id="33615-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1400">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1400">Display Name</span></span></td>
<td><span data-ttu-id="33615-1401">роамедтилеимажес</span><span class="sxs-lookup"><span data-stu-id="33615-1401">RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1402">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1402">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1403">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1403">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1404">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1404">Default Path</span></span></td>
<td><span data-ttu-id="33615-1405">%локалаппдата%\микрософт\виндовс\роамедтилеимажес</span><span class="sxs-lookup"><span data-stu-id="33615-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1406">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1406">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1407">Нет, значение, введенное в Windows 8</span><span class="sxs-lookup"><span data-stu-id="33615-1407">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1408">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1408">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1409">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1409">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1410">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1410">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1411">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1411">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingTiles"></span><span id="folderid_roamingtiles"></span><span id="FOLDERID_ROAMINGTILES"></span><dl> <span data-ttu-id="33615-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1413">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1413">GUID</span></span></td>
<td><span data-ttu-id="33615-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span><span class="sxs-lookup"><span data-stu-id="33615-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1415">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1415">Display Name</span></span></td>
<td><span data-ttu-id="33615-1416">роамингтилес</span><span class="sxs-lookup"><span data-stu-id="33615-1416">RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1417">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1417">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1418">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1418">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1419">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1419">Default Path</span></span></td>
<td><span data-ttu-id="33615-1420">%локалаппдата%\микрософт\виндовс\роамингтилес</span><span class="sxs-lookup"><span data-stu-id="33615-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1421">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1421">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1422">Нет, значение, введенное в Windows 8</span><span class="sxs-lookup"><span data-stu-id="33615-1422">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1423">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1423">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1424">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1424">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1425">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1425">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1426">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1426">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SampleMusic"></span><span id="folderid_samplemusic"></span><span id="FOLDERID_SAMPLEMUSIC"></span><dl> <span data-ttu-id="33615-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1428">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1428">GUID</span></span></td>
<td><span data-ttu-id="33615-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span><span class="sxs-lookup"><span data-stu-id="33615-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1430">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1430">Display Name</span></span></td>
<td><span data-ttu-id="33615-1431">Пример музыки</span><span class="sxs-lookup"><span data-stu-id="33615-1431">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1432">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1432">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1433">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1433">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1434">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1434">Default Path</span></span></td>
<td><span data-ttu-id="33615-1435">%Публик%\мусик\сампле музыка</span><span class="sxs-lookup"><span data-stu-id="33615-1435">%PUBLIC%\Music\Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1436">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1436">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1437">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1437">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1438">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1438">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1439">Пример музыки</span><span class="sxs-lookup"><span data-stu-id="33615-1439">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1440">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1440">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1441">%Аллусерспрофиле%\документс\ми Мусик\сампле музыка</span><span class="sxs-lookup"><span data-stu-id="33615-1441">%ALLUSERSPROFILE%\Documents\My Music\Sample Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SamplePictures"></span><span id="folderid_samplepictures"></span><span id="FOLDERID_SAMPLEPICTURES"></span><dl> <span data-ttu-id="33615-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1443">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1443">GUID</span></span></td>
<td><span data-ttu-id="33615-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span><span class="sxs-lookup"><span data-stu-id="33615-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1445">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1445">Display Name</span></span></td>
<td><span data-ttu-id="33615-1446">Образцы изображений</span><span class="sxs-lookup"><span data-stu-id="33615-1446">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1447">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1447">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1448">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1448">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1449">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1449">Default Path</span></span></td>
<td><span data-ttu-id="33615-1450">%Публик%\пиктурес\сампле изображения</span><span class="sxs-lookup"><span data-stu-id="33615-1450">%PUBLIC%\Pictures\Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1451">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1451">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1452">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1452">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1453">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1453">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1454">Образцы изображений</span><span class="sxs-lookup"><span data-stu-id="33615-1454">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1455">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1455">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1456">%Аллусерспрофиле%\документс\ми рисунки \ образцы изображения</span><span class="sxs-lookup"><span data-stu-id="33615-1456">%ALLUSERSPROFILE%\Documents\My Pictures\Sample Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SamplePlaylists"></span><span id="folderid_sampleplaylists"></span><span id="FOLDERID_SAMPLEPLAYLISTS"></span><dl> <span data-ttu-id="33615-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1458">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1458">GUID</span></span></td>
<td><span data-ttu-id="33615-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span><span class="sxs-lookup"><span data-stu-id="33615-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1460">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1460">Display Name</span></span></td>
<td><span data-ttu-id="33615-1461">Образцы списков воспроизведения</span><span class="sxs-lookup"><span data-stu-id="33615-1461">Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1462">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1462">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1463">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1463">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1464">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1464">Default Path</span></span></td>
<td><span data-ttu-id="33615-1465">Списки воспроизведения%публик%\мусик\сампле</span><span class="sxs-lookup"><span data-stu-id="33615-1465">%PUBLIC%\Music\Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1466">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1466">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1467">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-1467">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1468">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1468">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1469">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1469">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1470">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1470">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1471">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1471">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SampleVideos"></span><span id="folderid_samplevideos"></span><span id="FOLDERID_SAMPLEVIDEOS"></span><dl> <span data-ttu-id="33615-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1473">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1473">GUID</span></span></td>
<td><span data-ttu-id="33615-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span><span class="sxs-lookup"><span data-stu-id="33615-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1475">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1475">Display Name</span></span></td>
<td><span data-ttu-id="33615-1476">Примеры видеороликов</span><span class="sxs-lookup"><span data-stu-id="33615-1476">Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1477">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1477">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1478">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1478">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1479">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1479">Default Path</span></span></td>
<td><span data-ttu-id="33615-1480">Видео%публик%\видеос\сампле</span><span class="sxs-lookup"><span data-stu-id="33615-1480">%PUBLIC%\Videos\Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1481">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1481">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1482">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1482">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1483">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1483">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1484">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1484">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1485">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1485">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1486">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1486">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedGames"></span><span id="folderid_savedgames"></span><span id="FOLDERID_SAVEDGAMES"></span><dl> <span data-ttu-id="33615-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1488">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1488">GUID</span></span></td>
<td><span data-ttu-id="33615-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span><span class="sxs-lookup"><span data-stu-id="33615-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1490">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1490">Display Name</span></span></td>
<td><span data-ttu-id="33615-1491">Сохраненные игры</span><span class="sxs-lookup"><span data-stu-id="33615-1491">Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1492">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1492">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1493">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1493">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1494">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1494">Default Path</span></span></td>
<td><span data-ttu-id="33615-1495">%Усерпрофиле%\савед игры</span><span class="sxs-lookup"><span data-stu-id="33615-1495">%USERPROFILE%\Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1496">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1496">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1497">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-1497">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1498">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1498">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1499">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1499">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1500">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1500">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1501">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1501">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedPictures"></span><span id="folderid_savedpictures"></span><span id="FOLDERID_SAVEDPICTURES"></span><dl> <span data-ttu-id="33615-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1503">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1503">GUID</span></span></td>
<td><span data-ttu-id="33615-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span><span class="sxs-lookup"><span data-stu-id="33615-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1505">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1505">Display Name</span></span></td>
<td><span data-ttu-id="33615-1506">Сохраненные изображения</span><span class="sxs-lookup"><span data-stu-id="33615-1506">Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1507">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1507">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1508">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1508">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1509">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1509">Default Path</span></span></td>
<td><span data-ttu-id="33615-1510">%Усерпрофиле%\пиктурес\савед изображения</span><span class="sxs-lookup"><span data-stu-id="33615-1510">%USERPROFILE%\Pictures\Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1511">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1511">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1512">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1512">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1513">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1513">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1514">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1514">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1515">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1515">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1516">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1516">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedPicturesLibrary"></span><span id="folderid_savedpictureslibrary"></span><span id="FOLDERID_SAVEDPICTURESLIBRARY"></span><dl> <span data-ttu-id="33615-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1518">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1518">GUID</span></span></td>
<td><span data-ttu-id="33615-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span><span class="sxs-lookup"><span data-stu-id="33615-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1520">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1520">Display Name</span></span></td>
<td><span data-ttu-id="33615-1521">Библиотека сохраненных изображений</span><span class="sxs-lookup"><span data-stu-id="33615-1521">Saved Pictures Library</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1522">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1522">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1523">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1523">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1524">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1524">Default Path</span></span></td>
<td><span data-ttu-id="33615-1525">%аппдате%\микрософт\виндовс\либрариес\саведпиктурес.либрари-мс</span><span class="sxs-lookup"><span data-stu-id="33615-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1526">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1526">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1527">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1527">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1528">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1528">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1529">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1529">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1530">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1530">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1531">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1531">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedSearches"></span><span id="folderid_savedsearches"></span><span id="FOLDERID_SAVEDSEARCHES"></span><dl> <span data-ttu-id="33615-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1533">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1533">GUID</span></span></td>
<td><span data-ttu-id="33615-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span><span class="sxs-lookup"><span data-stu-id="33615-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1535">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1535">Display Name</span></span></td>
<td><span data-ttu-id="33615-1536">Поиск</span><span class="sxs-lookup"><span data-stu-id="33615-1536">Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1537">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1537">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1538">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1538">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1539">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1539">Default Path</span></span></td>
<td><span data-ttu-id="33615-1540">%усерпрофиле%\сеарчес</span><span class="sxs-lookup"><span data-stu-id="33615-1540">%USERPROFILE%\Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1541">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1541">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1542">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1542">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1543">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1543">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1544">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1544">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1545">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1545">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1546">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1546">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Screenshots"></span><span id="folderid_screenshots"></span><span id="FOLDERID_SCREENSHOTS"></span><dl> <span data-ttu-id="33615-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1548">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1548">GUID</span></span></td>
<td><span data-ttu-id="33615-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span><span class="sxs-lookup"><span data-stu-id="33615-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1550">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1550">Display Name</span></span></td>
<td><span data-ttu-id="33615-1551">Снимки экрана</span><span class="sxs-lookup"><span data-stu-id="33615-1551">Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1552">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1552">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1553">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1553">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1554">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1554">Default Path</span></span></td>
<td><span data-ttu-id="33615-1555">%усерпрофиле%\пиктурес\скриншотс</span><span class="sxs-lookup"><span data-stu-id="33615-1555">%USERPROFILE%\Pictures\Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1556">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1556">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1557">Нет, значение, введенное в Windows 8</span><span class="sxs-lookup"><span data-stu-id="33615-1557">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1558">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1558">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1559">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1559">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1560">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1560">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1561">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1561">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_CSC"></span><span id="folderid_search_csc"></span><dl> <span data-ttu-id="33615-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1563">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1563">GUID</span></span></td>
<td><span data-ttu-id="33615-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span><span class="sxs-lookup"><span data-stu-id="33615-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1565">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1565">Display Name</span></span></td>
<td><span data-ttu-id="33615-1566">Автономные файлы</span><span class="sxs-lookup"><span data-stu-id="33615-1566">Offline Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1567">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1567">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1568">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-1568">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1569">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1569">Default Path</span></span></td>
<td><span data-ttu-id="33615-1570">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-1570">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1571">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1571">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1572">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1572">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1573">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1573">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1574">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1574">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1575">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1575">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1576">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1576">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SearchHistory"></span><span id="folderid_searchhistory"></span><span id="FOLDERID_SEARCHHISTORY"></span><dl> <span data-ttu-id="33615-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1578">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1578">GUID</span></span></td>
<td><span data-ttu-id="33615-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span><span class="sxs-lookup"><span data-stu-id="33615-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1580">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1580">Display Name</span></span></td>
<td><span data-ttu-id="33615-1581">Журнал</span><span class="sxs-lookup"><span data-stu-id="33615-1581">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1582">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1582">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1583">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1583">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1584">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1584">Default Path</span></span></td>
<td><span data-ttu-id="33615-1585">%локалаппдата%\микрософт\виндовс\коннектедсеарч\хистори</span><span class="sxs-lookup"><span data-stu-id="33615-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1586">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1586">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1587">Нет, значение, введенное в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33615-1587">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1588">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1588">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1589">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1589">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1590">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1590">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1591">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1591">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchHome"></span><span id="folderid_searchhome"></span><span id="FOLDERID_SEARCHHOME"></span><dl> <span data-ttu-id="33615-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1593">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1593">GUID</span></span></td>
<td><span data-ttu-id="33615-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span><span class="sxs-lookup"><span data-stu-id="33615-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1595">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1595">Display Name</span></span></td>
<td><span data-ttu-id="33615-1596">Результаты поиска</span><span class="sxs-lookup"><span data-stu-id="33615-1596">Search Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1597">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1597">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1598">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-1598">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1599">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1599">Default Path</span></span></td>
<td><span data-ttu-id="33615-1600">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-1600">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1601">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1601">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1602">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1602">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1603">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1603">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1604">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1604">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1605">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1605">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1606">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1606">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_MAPI"></span><span id="folderid_search_mapi"></span><dl> <span data-ttu-id="33615-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1608">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1608">GUID</span></span></td>
<td><span data-ttu-id="33615-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span><span class="sxs-lookup"><span data-stu-id="33615-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1610">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1610">Display Name</span></span></td>
<td><span data-ttu-id="33615-1611">Microsoft Office Outlook</span><span class="sxs-lookup"><span data-stu-id="33615-1611">Microsoft Office Outlook</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1612">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1612">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1613">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-1613">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1614">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1614">Default Path</span></span></td>
<td><span data-ttu-id="33615-1615">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-1615">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1616">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1616">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1617">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1617">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1618">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1618">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1619">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1619">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1620">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1620">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1621">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1621">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchTemplates"></span><span id="folderid_searchtemplates"></span><span id="FOLDERID_SEARCHTEMPLATES"></span><dl> <span data-ttu-id="33615-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1623">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1623">GUID</span></span></td>
<td><span data-ttu-id="33615-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span><span class="sxs-lookup"><span data-stu-id="33615-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1625">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1625">Display Name</span></span></td>
<td><span data-ttu-id="33615-1626">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="33615-1626">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1627">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1627">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1628">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1628">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1629">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1629">Default Path</span></span></td>
<td><span data-ttu-id="33615-1630">%локалаппдата%\микрософт\виндовс\коннектедсеарч\темплатес</span><span class="sxs-lookup"><span data-stu-id="33615-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1631">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1631">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1632">Нет, значение, введенное в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33615-1632">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1633">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1633">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1634">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1634">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1635">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1635">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1636">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1636">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SendTo"></span><span id="folderid_sendto"></span><span id="FOLDERID_SENDTO"></span><dl> <span data-ttu-id="33615-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1638">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1638">GUID</span></span></td>
<td><span data-ttu-id="33615-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span><span class="sxs-lookup"><span data-stu-id="33615-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1640">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1640">Display Name</span></span></td>
<td><span data-ttu-id="33615-1641">Cервера</span><span class="sxs-lookup"><span data-stu-id="33615-1641">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1642">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1642">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1643">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1643">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1644">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1644">Default Path</span></span></td>
<td><span data-ttu-id="33615-1645">%аппдата%\микрософт\виндовс\сендто</span><span class="sxs-lookup"><span data-stu-id="33615-1645">%APPDATA%\Microsoft\Windows\SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1646">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1646">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1647">CSIDL_SENDTO</span><span class="sxs-lookup"><span data-stu-id="33615-1647">CSIDL_SENDTO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1648">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1648">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1649">Cервера</span><span class="sxs-lookup"><span data-stu-id="33615-1649">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1650">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1650">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1651">%усерпрофиле%\сендто</span><span class="sxs-lookup"><span data-stu-id="33615-1651">%USERPROFILE%\SendTo</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SidebarDefaultParts"></span><span id="folderid_sidebardefaultparts"></span><span id="FOLDERID_SIDEBARDEFAULTPARTS"></span><dl> <span data-ttu-id="33615-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1653">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1653">GUID</span></span></td>
<td><span data-ttu-id="33615-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span><span class="sxs-lookup"><span data-stu-id="33615-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1655">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1655">Display Name</span></span></td>
<td><span data-ttu-id="33615-1656">Приложения</span><span class="sxs-lookup"><span data-stu-id="33615-1656">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1657">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1657">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1658">РАЗДЕЛЯЕМ</span><span class="sxs-lookup"><span data-stu-id="33615-1658">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1659">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1659">Default Path</span></span></td>
<td><span data-ttu-id="33615-1660">%Програмфилес%\виндовс Сидебар\гаджетс</span><span class="sxs-lookup"><span data-stu-id="33615-1660">%ProgramFiles%\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1661">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1661">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1662">Нет, новое для Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-1662">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1663">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1663">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1664">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1664">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1665">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1665">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1666">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1666">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SidebarParts"></span><span id="folderid_sidebarparts"></span><span id="FOLDERID_SIDEBARPARTS"></span><dl> <span data-ttu-id="33615-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1668">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1668">GUID</span></span></td>
<td><span data-ttu-id="33615-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span><span class="sxs-lookup"><span data-stu-id="33615-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1670">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1670">Display Name</span></span></td>
<td><span data-ttu-id="33615-1671">Приложения</span><span class="sxs-lookup"><span data-stu-id="33615-1671">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1672">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1672">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1673">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1673">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1674">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1674">Default Path</span></span></td>
<td><span data-ttu-id="33615-1675">%Локалаппдата%\микрософт\виндовс Сидебар\гаджетс</span><span class="sxs-lookup"><span data-stu-id="33615-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1676">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1676">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1677">Нет, новое для Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-1677">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1678">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1678">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1679">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1679">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1680">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1680">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1681">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1681">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDrive"></span><span id="folderid_skydrive"></span><span id="FOLDERID_SKYDRIVE"></span><dl> <span data-ttu-id="33615-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1683">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1683">GUID</span></span></td>
<td><span data-ttu-id="33615-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span><span class="sxs-lookup"><span data-stu-id="33615-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1685">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1685">Display Name</span></span></td>
<td><span data-ttu-id="33615-1686">OneDrive</span><span class="sxs-lookup"><span data-stu-id="33615-1686">OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1687">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1687">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1688">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1688">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1689">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1689">Default Path</span></span></td>
<td><span data-ttu-id="33615-1690">%усерпрофиле%\онедриве</span><span class="sxs-lookup"><span data-stu-id="33615-1690">%USERPROFILE%\OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1691">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1691">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1692">Нет, значение, введенное в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33615-1692">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1693">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1693">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1694">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1694">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1695">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1695">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1696">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1696">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveCameraRoll"></span><span id="folderid_skydrivecameraroll"></span><span id="FOLDERID_SKYDRIVECAMERAROLL"></span><dl> <span data-ttu-id="33615-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1698">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1698">GUID</span></span></td>
<td><span data-ttu-id="33615-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span><span class="sxs-lookup"><span data-stu-id="33615-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1700">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1700">Display Name</span></span></td>
<td><span data-ttu-id="33615-1701">Пленка</span><span class="sxs-lookup"><span data-stu-id="33615-1701">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1702">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1702">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1703">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1703">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1704">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1704">Default Path</span></span></td>
<td><span data-ttu-id="33615-1705">%Усерпрофиле%\онедриве\пиктурес\камера</span><span class="sxs-lookup"><span data-stu-id="33615-1705">%USERPROFILE%\OneDrive\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1706">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1706">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1707">Нет, значение, введенное в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33615-1707">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1708">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1708">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1709">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1709">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1710">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1710">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1711">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1711">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveDocuments"></span><span id="folderid_skydrivedocuments"></span><span id="FOLDERID_SKYDRIVEDOCUMENTS"></span><dl> <span data-ttu-id="33615-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1713">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1713">GUID</span></span></td>
<td><span data-ttu-id="33615-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span><span class="sxs-lookup"><span data-stu-id="33615-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1715">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1715">Display Name</span></span></td>
<td><span data-ttu-id="33615-1716">Документы</span><span class="sxs-lookup"><span data-stu-id="33615-1716">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1717">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1717">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1718">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1718">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1719">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1719">Default Path</span></span></td>
<td><span data-ttu-id="33615-1720">%усерпрофиле%\онедриве\документс</span><span class="sxs-lookup"><span data-stu-id="33615-1720">%USERPROFILE%\OneDrive\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1721">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1721">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1722">Нет, значение, введенное в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33615-1722">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1723">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1723">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1724">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1724">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1725">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1725">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1726">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1726">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDrivePictures"></span><span id="folderid_skydrivepictures"></span><span id="FOLDERID_SKYDRIVEPICTURES"></span><dl> <span data-ttu-id="33615-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1728">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1728">GUID</span></span></td>
<td><span data-ttu-id="33615-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span><span class="sxs-lookup"><span data-stu-id="33615-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1730">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1730">Display Name</span></span></td>
<td><span data-ttu-id="33615-1731">Изображения</span><span class="sxs-lookup"><span data-stu-id="33615-1731">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1732">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1732">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1733">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1733">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1734">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1734">Default Path</span></span></td>
<td><span data-ttu-id="33615-1735">%усерпрофиле%\онедриве\пиктурес</span><span class="sxs-lookup"><span data-stu-id="33615-1735">%USERPROFILE%\OneDrive\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1736">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1736">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1737">Нет, значение, введенное в Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33615-1737">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1738">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1738">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1739">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1739">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1740">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1740">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1741">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1741">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_StartMenu"></span><span id="folderid_startmenu"></span><span id="FOLDERID_STARTMENU"></span><dl> <span data-ttu-id="33615-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1743">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1743">GUID</span></span></td>
<td><span data-ttu-id="33615-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span><span class="sxs-lookup"><span data-stu-id="33615-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1745">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1745">Display Name</span></span></td>
<td><span data-ttu-id="33615-1746">Меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="33615-1746">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1747">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1747">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1748">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1748">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1749">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1749">Default Path</span></span></td>
<td><span data-ttu-id="33615-1750">Меню%Аппдата%\микрософт\виндовс\старт</span><span class="sxs-lookup"><span data-stu-id="33615-1750">%APPDATA%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1751">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1751">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1752">CSIDL_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="33615-1752">CSIDL_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1753">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1753">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1754">Меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="33615-1754">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1755">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1755">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1756">Меню%Усерпрофиле%\старт</span><span class="sxs-lookup"><span data-stu-id="33615-1756">%USERPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Startup"></span><span id="folderid_startup"></span><span id="FOLDERID_STARTUP"></span><dl> <span data-ttu-id="33615-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1758">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1758">GUID</span></span></td>
<td><span data-ttu-id="33615-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span><span class="sxs-lookup"><span data-stu-id="33615-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1760">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1760">Display Name</span></span></td>
<td><span data-ttu-id="33615-1761">Запуск</span><span class="sxs-lookup"><span data-stu-id="33615-1761">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1762">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1762">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1763">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1763">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1764">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1764">Default Path</span></span></td>
<td><span data-ttu-id="33615-1765">%Аппдата%\микрософт\виндовс\старт Мену\програмс\стартуп</span><span class="sxs-lookup"><span data-stu-id="33615-1765">%APPDATA%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1766">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1766">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="33615-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1768">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1768">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1769">Запуск</span><span class="sxs-lookup"><span data-stu-id="33615-1769">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1770">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1770">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1771">%Усерпрофиле%\старт Мену\програмс\стартуп</span><span class="sxs-lookup"><span data-stu-id="33615-1771">%USERPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncManagerFolder"></span><span id="folderid_syncmanagerfolder"></span><span id="FOLDERID_SYNCMANAGERFOLDER"></span><dl> <span data-ttu-id="33615-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1773">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1773">GUID</span></span></td>
<td><span data-ttu-id="33615-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span><span class="sxs-lookup"><span data-stu-id="33615-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1775">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1775">Display Name</span></span></td>
<td><span data-ttu-id="33615-1776">Центр синхронизации</span><span class="sxs-lookup"><span data-stu-id="33615-1776">Sync Center</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1777">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1777">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1778">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-1778">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1779">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1779">Default Path</span></span></td>
<td><span data-ttu-id="33615-1780">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-1780">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1781">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1781">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1782">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-1782">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1783">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1783">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1784">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1784">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1785">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1785">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1786">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1786">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SyncResultsFolder"></span><span id="folderid_syncresultsfolder"></span><span id="FOLDERID_SYNCRESULTSFOLDER"></span><dl> <span data-ttu-id="33615-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1788">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1788">GUID</span></span></td>
<td><span data-ttu-id="33615-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span><span class="sxs-lookup"><span data-stu-id="33615-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1790">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1790">Display Name</span></span></td>
<td><span data-ttu-id="33615-1791">Результаты синхронизации</span><span class="sxs-lookup"><span data-stu-id="33615-1791">Sync Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1792">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1792">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1793">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-1793">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1794">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1794">Default Path</span></span></td>
<td><span data-ttu-id="33615-1795">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-1795">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1796">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1796">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1797">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-1797">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1798">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1798">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1799">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1799">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1800">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1800">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1801">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1801">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncSetupFolder"></span><span id="folderid_syncsetupfolder"></span><span id="FOLDERID_SYNCSETUPFOLDER"></span><dl> <span data-ttu-id="33615-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1803">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1803">GUID</span></span></td>
<td><span data-ttu-id="33615-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span><span class="sxs-lookup"><span data-stu-id="33615-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1805">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1805">Display Name</span></span></td>
<td><span data-ttu-id="33615-1806">Настройка синхронизации</span><span class="sxs-lookup"><span data-stu-id="33615-1806">Sync Setup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1807">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1807">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1808">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-1808">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1809">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1809">Default Path</span></span></td>
<td><span data-ttu-id="33615-1810">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-1810">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1811">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1811">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1812">Нет, значение, введенное в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-1812">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1813">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1813">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1814">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1814">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1815">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1815">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1816">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1816">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_System"></span><span id="folderid_system"></span><span id="FOLDERID_SYSTEM"></span><dl> <span data-ttu-id="33615-1817"><dt><strong>FOLDERID_System</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1817"><dt><strong>FOLDERID_System</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1818">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1818">GUID</span></span></td>
<td><span data-ttu-id="33615-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span><span class="sxs-lookup"><span data-stu-id="33615-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1820">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1820">Display Name</span></span></td>
<td><span data-ttu-id="33615-1821">System32</span><span class="sxs-lookup"><span data-stu-id="33615-1821">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1822">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1822">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1823">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1823">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1824">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1824">Default Path</span></span></td>
<td><span data-ttu-id="33615-1825">%WINDIR%\System32</span><span class="sxs-lookup"><span data-stu-id="33615-1825">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1826">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1826">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1827">CSIDL_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="33615-1827">CSIDL_SYSTEM</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1828">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1828">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1829">папке</span><span class="sxs-lookup"><span data-stu-id="33615-1829">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1830">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1830">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1831">%WINDIR%\System32</span><span class="sxs-lookup"><span data-stu-id="33615-1831">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SystemX86"></span><span id="folderid_systemx86"></span><span id="FOLDERID_SYSTEMX86"></span><dl> <span data-ttu-id="33615-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1833">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1833">GUID</span></span></td>
<td><span data-ttu-id="33615-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span><span class="sxs-lookup"><span data-stu-id="33615-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1835">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1835">Display Name</span></span></td>
<td><span data-ttu-id="33615-1836">System32</span><span class="sxs-lookup"><span data-stu-id="33615-1836">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1837">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1837">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1838">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1838">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1839">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1839">Default Path</span></span></td>
<td><span data-ttu-id="33615-1840">%WINDIR%\System32</span><span class="sxs-lookup"><span data-stu-id="33615-1840">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1841">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1841">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1842">CSIDL_SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="33615-1842">CSIDL_SYSTEMX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1843">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1843">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1844">папке</span><span class="sxs-lookup"><span data-stu-id="33615-1844">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1845">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1845">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1846">%WINDIR%\System32</span><span class="sxs-lookup"><span data-stu-id="33615-1846">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Templates"></span><span id="folderid_templates"></span><span id="FOLDERID_TEMPLATES"></span><dl> <span data-ttu-id="33615-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1848">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1848">GUID</span></span></td>
<td><span data-ttu-id="33615-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span><span class="sxs-lookup"><span data-stu-id="33615-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1850">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1850">Display Name</span></span></td>
<td><span data-ttu-id="33615-1851">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="33615-1851">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1852">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1852">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1853">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1853">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1854">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1854">Default Path</span></span></td>
<td><span data-ttu-id="33615-1855">%аппдата%\микрософт\виндовс\темплатес</span><span class="sxs-lookup"><span data-stu-id="33615-1855">%APPDATA%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1856">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1856">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1857">CSIDL_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="33615-1857">CSIDL_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1858">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1858">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1859">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="33615-1859">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1860">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1860">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1861">%усерпрофиле%\темплатес</span><span class="sxs-lookup"><span data-stu-id="33615-1861">%USERPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_TreeProperties"></span><span id="folderid_treeproperties"></span><span id="FOLDERID_TREEPROPERTIES"></span><dl> <span data-ttu-id="33615-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="33615-1863">Не используется в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="33615-1863">Not used in Windows Vista.</span></span> <span data-ttu-id="33615-1864">Не поддерживается в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="33615-1864">Unsupported as of Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserPinned"></span><span id="folderid_userpinned"></span><span id="FOLDERID_USERPINNED"></span><dl> <span data-ttu-id="33615-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1866">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1866">GUID</span></span></td>
<td><span data-ttu-id="33615-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span><span class="sxs-lookup"><span data-stu-id="33615-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1868">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1868">Display Name</span></span></td>
<td><span data-ttu-id="33615-1869">Пользователь закреплен</span><span class="sxs-lookup"><span data-stu-id="33615-1869">User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1870">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1870">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1871">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1871">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1872">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1872">Default Path</span></span></td>
<td><span data-ttu-id="33615-1873">%Аппдата%\микрософт\интернет Експлорер\куикк Лаунч\усер закреплена</span><span class="sxs-lookup"><span data-stu-id="33615-1873">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1874">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1874">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1875">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-1875">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1876">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1876">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1877">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1877">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1878">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1878">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1879">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1879">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProfiles"></span><span id="folderid_userprofiles"></span><span id="FOLDERID_USERPROFILES"></span><dl> <span data-ttu-id="33615-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1881">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1881">GUID</span></span></td>
<td><span data-ttu-id="33615-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span><span class="sxs-lookup"><span data-stu-id="33615-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1883">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1883">Display Name</span></span></td>
<td><span data-ttu-id="33615-1884">Пользователи</span><span class="sxs-lookup"><span data-stu-id="33615-1884">Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1885">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1885">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1886">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1886">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1887">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1887">Default Path</span></span></td>
<td><span data-ttu-id="33615-1888">%системдриве%\усерс</span><span class="sxs-lookup"><span data-stu-id="33615-1888">%SystemDrive%\Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1889">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1889">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1890">Нет, новое для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33615-1890">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1891">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1891">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1892">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1892">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1893">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1893">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1894">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1894">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFiles"></span><span id="folderid_userprogramfiles"></span><span id="FOLDERID_USERPROGRAMFILES"></span><dl> <span data-ttu-id="33615-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1896">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1896">GUID</span></span></td>
<td><span data-ttu-id="33615-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span><span class="sxs-lookup"><span data-stu-id="33615-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1898">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1898">Display Name</span></span></td>
<td><span data-ttu-id="33615-1899">Programs</span><span class="sxs-lookup"><span data-stu-id="33615-1899">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1900">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1900">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1901">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1901">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1902">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1902">Default Path</span></span></td>
<td><span data-ttu-id="33615-1903">%локалаппдата%\програмс</span><span class="sxs-lookup"><span data-stu-id="33615-1903">%LOCALAPPDATA%\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1904">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1904">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1905">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-1905">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1906">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1906">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1907">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1907">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1908">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1908">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1909">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1909">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFilesCommon"></span><span id="folderid_userprogramfilescommon"></span><span id="FOLDERID_USERPROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="33615-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1911">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1911">GUID</span></span></td>
<td><span data-ttu-id="33615-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span><span class="sxs-lookup"><span data-stu-id="33615-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1913">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1913">Display Name</span></span></td>
<td><span data-ttu-id="33615-1914">Programs</span><span class="sxs-lookup"><span data-stu-id="33615-1914">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1915">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1915">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1916">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1916">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1917">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1917">Default Path</span></span></td>
<td><span data-ttu-id="33615-1918">%локалаппдата%\програмс\коммон</span><span class="sxs-lookup"><span data-stu-id="33615-1918">%LOCALAPPDATA%\Programs\Common</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1919">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1919">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1920">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-1920">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1921">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1921">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1922">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1922">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1923">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1923">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1924">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1924">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UsersFiles"></span><span id="folderid_usersfiles"></span><span id="FOLDERID_USERSFILES"></span><dl> <span data-ttu-id="33615-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1926">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1926">GUID</span></span></td>
<td><span data-ttu-id="33615-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span><span class="sxs-lookup"><span data-stu-id="33615-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1928">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1928">Display Name</span></span></td>
<td><span data-ttu-id="33615-1929">Полное имя пользователя (например, Жан Philippe бублик), которое было указано при создании учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="33615-1929">The user's full name (for instance, Jean Philippe Bagel) entered when the user account was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1930">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1930">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1931">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-1931">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1932">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1932">Default Path</span></span></td>
<td><span data-ttu-id="33615-1933">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-1933">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1934">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1934">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1935">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-1935">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1936">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1936">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1937">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1937">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1938">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1938">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1939">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1939">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UsersLibraries"></span><span id="folderid_userslibraries"></span><span id="FOLDERID_USERSLIBRARIES"></span><dl> <span data-ttu-id="33615-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1941">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1941">GUID</span></span></td>
<td><span data-ttu-id="33615-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span><span class="sxs-lookup"><span data-stu-id="33615-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1943">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1943">Display Name</span></span></td>
<td><span data-ttu-id="33615-1944">Библиотеки</span><span class="sxs-lookup"><span data-stu-id="33615-1944">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1945">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1945">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1946">ВИРТУАЛИЗАЦИ</span><span class="sxs-lookup"><span data-stu-id="33615-1946">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1947">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1947">Default Path</span></span></td>
<td><span data-ttu-id="33615-1948">Неприменимо — виртуальная папка</span><span class="sxs-lookup"><span data-stu-id="33615-1948">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1949">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1949">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1950">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-1950">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1951">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1951">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1952">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1952">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1953">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1953">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1954">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1954">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Videos"></span><span id="folderid_videos"></span><span id="FOLDERID_VIDEOS"></span><dl> <span data-ttu-id="33615-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1956">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1956">GUID</span></span></td>
<td><span data-ttu-id="33615-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span><span class="sxs-lookup"><span data-stu-id="33615-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1958">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1958">Display Name</span></span></td>
<td><span data-ttu-id="33615-1959">Видео</span><span class="sxs-lookup"><span data-stu-id="33615-1959">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1960">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1960">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1961">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1961">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1962">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1962">Default Path</span></span></td>
<td><span data-ttu-id="33615-1963">%усерпрофиле%\видеос</span><span class="sxs-lookup"><span data-stu-id="33615-1963">%USERPROFILE%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1964">CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1964">CSIDL</span></span></td>
<td><span data-ttu-id="33615-1965">CSIDL_MYVIDEO</span><span class="sxs-lookup"><span data-stu-id="33615-1965">CSIDL_MYVIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1966">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1966">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1967">Мои видеоролики</span><span class="sxs-lookup"><span data-stu-id="33615-1967">My Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1968">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1968">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1969">Видео%USERPROFILE%\My документы</span><span class="sxs-lookup"><span data-stu-id="33615-1969">%USERPROFILE%\My Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_VideosLibrary"></span><span id="folderid_videoslibrary"></span><span id="FOLDERID_VIDEOSLIBRARY"></span><dl> <span data-ttu-id="33615-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1971">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1971">GUID</span></span></td>
<td><span data-ttu-id="33615-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span><span class="sxs-lookup"><span data-stu-id="33615-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1973">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1973">Display Name</span></span></td>
<td><span data-ttu-id="33615-1974">Видео</span><span class="sxs-lookup"><span data-stu-id="33615-1974">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1975">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1975">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1976">ИЗУЧЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33615-1976">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1977">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1977">Default Path</span></span></td>
<td><span data-ttu-id="33615-1978">%аппдата%\микрософт\виндовс\либрариес\видеос.либрари-мс</span><span class="sxs-lookup"><span data-stu-id="33615-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1979">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1979">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1980">Нет, значение введено в Windows 7</span><span class="sxs-lookup"><span data-stu-id="33615-1980">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1981">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1981">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1982">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1982">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1983">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1983">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1984">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-1984">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Windows"></span><span id="folderid_windows"></span><span id="FOLDERID_WINDOWS"></span><dl> <span data-ttu-id="33615-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="33615-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33615-1986">Код GUID</span><span class="sxs-lookup"><span data-stu-id="33615-1986">GUID</span></span></td>
<td><span data-ttu-id="33615-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span><span class="sxs-lookup"><span data-stu-id="33615-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1988">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1988">Display Name</span></span></td>
<td><span data-ttu-id="33615-1989">Windows</span><span class="sxs-lookup"><span data-stu-id="33615-1989">Windows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1990">Тип папки</span><span class="sxs-lookup"><span data-stu-id="33615-1990">Folder Type</span></span></td>
<td><span data-ttu-id="33615-1991">FIXED</span><span class="sxs-lookup"><span data-stu-id="33615-1991">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1992">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-1992">Default Path</span></span></td>
<td><span data-ttu-id="33615-1993">%windir%</span><span class="sxs-lookup"><span data-stu-id="33615-1993">%windir%</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1994">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-1994">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="33615-1995">CSIDL_WINDOWS</span><span class="sxs-lookup"><span data-stu-id="33615-1995">CSIDL_WINDOWS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33615-1996">Устаревшее отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33615-1996">Legacy Display Name</span></span></td>
<td><span data-ttu-id="33615-1997">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="33615-1997">WINDOWS</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33615-1998">Устаревший путь по умолчанию</span><span class="sxs-lookup"><span data-stu-id="33615-1998">Legacy Default Path</span></span></td>
<td><span data-ttu-id="33615-1999">%windir%</span><span class="sxs-lookup"><span data-stu-id="33615-1999">%windir%</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="33615-2000">Примечания</span><span class="sxs-lookup"><span data-stu-id="33615-2000">Remarks</span></span>

<span data-ttu-id="33615-2001">Интерпретация определенных значений **кновнфолдерид** зависит от того, является ли папка частью 32-разрядного или 64-разрядного приложения и работает ли это приложение в 32-разрядной или 64-разрядной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="33615-2001">The interpretation of certain **KNOWNFOLDERID** values depends on whether the folder is part of a 32-bit or 64-bit application and whether that application is running on a 32-bit or 64-bit operating system.</span></span> <span data-ttu-id="33615-2002">Если приложению необходимо различать, например **программные файлы** и **программные файлы (x86)**, необходимо использовать правильный **кновнфолдерид** для ситуации.</span><span class="sxs-lookup"><span data-stu-id="33615-2002">If your application needs to distinguish between, for example, **Program Files** and **Program Files (x86)**, you must use the right **KNOWNFOLDERID** for the situation.</span></span>

<span data-ttu-id="33615-2003">В следующих таблицах приводится сводка использования **кновнфолдерид** в этих случаях.</span><span class="sxs-lookup"><span data-stu-id="33615-2003">The following tables summarize the **KNOWNFOLDERID** use in those cases.</span></span>


<span data-ttu-id="33615-2004">**FOLDERID \_ ProgramFiles**</span><span class="sxs-lookup"><span data-stu-id="33615-2004">**FOLDERID\_ProgramFiles**</span></span> 

| <span data-ttu-id="33615-2005">Операционная система</span><span class="sxs-lookup"><span data-stu-id="33615-2005">Operating System</span></span> | <span data-ttu-id="33615-2006">Приложение</span><span class="sxs-lookup"><span data-stu-id="33615-2006">Application</span></span> | <span data-ttu-id="33615-2007">кновнфолдерид</span><span class="sxs-lookup"><span data-stu-id="33615-2007">KNOWNFOLDERID</span></span> | <span data-ttu-id="33615-2008">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-2008">Default Path</span></span> | <span data-ttu-id="33615-2009">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-2009">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="33615-2010">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2010">32 bit</span></span> | <span data-ttu-id="33615-2011">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2011">32 bit</span></span> | <span data-ttu-id="33615-2012">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="33615-2012">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="33615-2013">% SystemDrive% \\ программных файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2013">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="33615-2014">\_программные \_ файлы CSid</span><span class="sxs-lookup"><span data-stu-id="33615-2014">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="33615-2015">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2015">32 bit</span></span> | <span data-ttu-id="33615-2016">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2016">32 bit</span></span> | <span data-ttu-id="33615-2017">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="33615-2017">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="33615-2018">% SystemDrive% \\ программных файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2018">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="33615-2019">Код CSID \_ программы \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="33615-2019">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="33615-2020">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2020">32 bit</span></span> | <span data-ttu-id="33615-2021">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2021">32 bit</span></span> | <span data-ttu-id="33615-2022">FOLDERID \_ ProgramFilesX64 (не поддерживается в 32-разрядных операционных системах)</span><span class="sxs-lookup"><span data-stu-id="33615-2022">FOLDERID\_ProgramFilesX64 (not supported under 32-bit operating systems)</span></span> | <span data-ttu-id="33615-2023">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-2023">Not applicable</span></span> | <span data-ttu-id="33615-2024">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-2024">Not applicable</span></span> |
| <span data-ttu-id="33615-2025">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2025">64 bit</span></span> | <span data-ttu-id="33615-2026">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2026">64 bit</span></span> | <span data-ttu-id="33615-2027">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="33615-2027">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="33615-2028">% SystemDrive% \\ программных файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2028">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="33615-2029">\_программные \_ файлы CSid</span><span class="sxs-lookup"><span data-stu-id="33615-2029">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="33615-2030">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2030">64 bit</span></span> | <span data-ttu-id="33615-2031">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2031">64 bit</span></span> | <span data-ttu-id="33615-2032">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="33615-2032">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="33615-2033">% SystemDrive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="33615-2033">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="33615-2034">Код CSID \_ программы \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="33615-2034">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="33615-2035">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2035">64 bit</span></span> | <span data-ttu-id="33615-2036">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2036">64 bit</span></span> | <span data-ttu-id="33615-2037">FOLDERID \_ ProgramFilesX64</span><span class="sxs-lookup"><span data-stu-id="33615-2037">FOLDERID\_ProgramFilesX64</span></span> | <span data-ttu-id="33615-2038">% SystemDrive% \\ программных файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2038">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="33615-2039">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-2039">None</span></span> |
| <span data-ttu-id="33615-2040">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2040">64 bit</span></span> | <span data-ttu-id="33615-2041">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2041">32 bit</span></span> | <span data-ttu-id="33615-2042">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="33615-2042">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="33615-2043">% SystemDrive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="33615-2043">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="33615-2044">\_программные \_ файлы CSid</span><span class="sxs-lookup"><span data-stu-id="33615-2044">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="33615-2045">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2045">64 bit</span></span> | <span data-ttu-id="33615-2046">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2046">32 bit</span></span> | <span data-ttu-id="33615-2047">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="33615-2047">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="33615-2048">% SystemDrive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="33615-2048">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="33615-2049">Код CSID \_ программы \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="33615-2049">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="33615-2050">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2050">64 bit</span></span> | <span data-ttu-id="33615-2051">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2051">32 bit</span></span> | <span data-ttu-id="33615-2052">FOLDERID \_ ProgramFilesX64 (не поддерживается для 32-разрядных приложений)</span><span class="sxs-lookup"><span data-stu-id="33615-2052">FOLDERID\_ProgramFilesX64 (not supported for 32-bit applications)</span></span> | <span data-ttu-id="33615-2053">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-2053">Not applicable</span></span> | <span data-ttu-id="33615-2054">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-2054">Not applicable</span></span> |


<span data-ttu-id="33615-2055">**FOLDERID \_ програмфилескоммон**</span><span class="sxs-lookup"><span data-stu-id="33615-2055">**FOLDERID\_ProgramFilesCommon**</span></span>

| <span data-ttu-id="33615-2056">Операционная система</span><span class="sxs-lookup"><span data-stu-id="33615-2056">Operating System</span></span> | <span data-ttu-id="33615-2057">Приложение</span><span class="sxs-lookup"><span data-stu-id="33615-2057">Application</span></span> | <span data-ttu-id="33615-2058">кновнфолдерид</span><span class="sxs-lookup"><span data-stu-id="33615-2058">KNOWNFOLDERID</span></span> | <span data-ttu-id="33615-2059">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-2059">Default Path</span></span> | <span data-ttu-id="33615-2060">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-2060">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="33615-2061">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2061">32 bit</span></span> | <span data-ttu-id="33615-2062">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2062">32 bit</span></span> | <span data-ttu-id="33615-2063">FOLDERID \_ програмфилескоммон</span><span class="sxs-lookup"><span data-stu-id="33615-2063">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="33615-2064">% ProgramFiles% \\ общих файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2064">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="33615-2065">\_Общие программные \_ файлы \_ CSid</span><span class="sxs-lookup"><span data-stu-id="33615-2065">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="33615-2066">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2066">32 bit</span></span> | <span data-ttu-id="33615-2067">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2067">32 bit</span></span> | <span data-ttu-id="33615-2068">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="33615-2068">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="33615-2069">% ProgramFiles% \\ общих файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2069">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="33615-2070">\_Программные \_ файлы CSid \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="33615-2070">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="33615-2071">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2071">32 bit</span></span> | <span data-ttu-id="33615-2072">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2072">32 bit</span></span> | <span data-ttu-id="33615-2073">FOLDERID \_ ProgramFilesCommonX64 (не определено)</span><span class="sxs-lookup"><span data-stu-id="33615-2073">FOLDERID\_ProgramFilesCommonX64 (undefined)</span></span> | <span data-ttu-id="33615-2074">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-2074">Not applicable</span></span> | <span data-ttu-id="33615-2075">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="33615-2075">Not applicable</span></span> |
| <span data-ttu-id="33615-2076">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2076">64 bit</span></span> | <span data-ttu-id="33615-2077">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2077">64 bit</span></span> | <span data-ttu-id="33615-2078">FOLDERID \_ програмфилескоммон</span><span class="sxs-lookup"><span data-stu-id="33615-2078">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="33615-2079">% ProgramFiles% \\ общих файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2079">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="33615-2080">\_Общие программные \_ файлы \_ CSid</span><span class="sxs-lookup"><span data-stu-id="33615-2080">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="33615-2081">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2081">64 bit</span></span> | <span data-ttu-id="33615-2082">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2082">64 bit</span></span> | <span data-ttu-id="33615-2083">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="33615-2083">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="33615-2084">% ProgramFiles (x86)% \\ общих файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2084">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="33615-2085">\_Программные \_ файлы CSid \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="33615-2085">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="33615-2086">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2086">64 bit</span></span> | <span data-ttu-id="33615-2087">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2087">64 bit</span></span> | <span data-ttu-id="33615-2088">FOLDERID \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="33615-2088">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="33615-2089">% ProgramFiles% \\ общих файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2089">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="33615-2090">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-2090">None</span></span> |
| <span data-ttu-id="33615-2091">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2091">64 bit</span></span> | <span data-ttu-id="33615-2092">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2092">32 bit</span></span> | <span data-ttu-id="33615-2093">FOLDERID \_ програмфилескоммон</span><span class="sxs-lookup"><span data-stu-id="33615-2093">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="33615-2094">% ProgramFiles (x86)% \\ общих файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2094">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="33615-2095">\_Общие программные \_ файлы \_ CSid</span><span class="sxs-lookup"><span data-stu-id="33615-2095">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="33615-2096">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2096">64 bit</span></span> | <span data-ttu-id="33615-2097">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2097">32 bit</span></span> | <span data-ttu-id="33615-2098">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="33615-2098">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="33615-2099">% ProgramFiles (x86)% \\ общих файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2099">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="33615-2100">\_Программные \_ файлы CSid \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="33615-2100">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="33615-2101">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2101">64 bit</span></span> | <span data-ttu-id="33615-2102">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2102">32 bit</span></span> | <span data-ttu-id="33615-2103">FOLDERID \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="33615-2103">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="33615-2104">% ProgramFiles% \\ общих файлов</span><span class="sxs-lookup"><span data-stu-id="33615-2104">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="33615-2105">Нет</span><span class="sxs-lookup"><span data-stu-id="33615-2105">None</span></span> |


<span data-ttu-id="33615-2106">**FOLDERID \_ система**</span><span class="sxs-lookup"><span data-stu-id="33615-2106">**FOLDERID\_System**</span></span>

| <span data-ttu-id="33615-2107">Операционная система</span><span class="sxs-lookup"><span data-stu-id="33615-2107">Operating System</span></span> | <span data-ttu-id="33615-2108">Приложение</span><span class="sxs-lookup"><span data-stu-id="33615-2108">Application</span></span> | <span data-ttu-id="33615-2109">кновнфолдерид</span><span class="sxs-lookup"><span data-stu-id="33615-2109">KNOWNFOLDERID</span></span> | <span data-ttu-id="33615-2110">Default Path</span><span class="sxs-lookup"><span data-stu-id="33615-2110">Default Path</span></span> | <span data-ttu-id="33615-2111">Эквивалент CSID</span><span class="sxs-lookup"><span data-stu-id="33615-2111">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="33615-2112">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2112">32 bit</span></span> | <span data-ttu-id="33615-2113">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2113">32 bit</span></span> | <span data-ttu-id="33615-2114">FOLDERID \_ система</span><span class="sxs-lookup"><span data-stu-id="33615-2114">FOLDERID\_System</span></span> | <span data-ttu-id="33615-2115">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="33615-2115">%windir%\\system32</span></span> | <span data-ttu-id="33615-2116">система CSID \_</span><span class="sxs-lookup"><span data-stu-id="33615-2116">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="33615-2117">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2117">32 bit</span></span> | <span data-ttu-id="33615-2118">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2118">32 bit</span></span> | <span data-ttu-id="33615-2119">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="33615-2119">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="33615-2120">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="33615-2120">%windir%\\system32</span></span> | <span data-ttu-id="33615-2121">SYSTEMX86 CSID \_</span><span class="sxs-lookup"><span data-stu-id="33615-2121">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="33615-2122">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2122">64 bit</span></span> | <span data-ttu-id="33615-2123">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2123">64 bit</span></span> | <span data-ttu-id="33615-2124">FOLDERID \_ система</span><span class="sxs-lookup"><span data-stu-id="33615-2124">FOLDERID\_System</span></span> | <span data-ttu-id="33615-2125">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="33615-2125">%windir%\\system32</span></span> | <span data-ttu-id="33615-2126">система CSID \_</span><span class="sxs-lookup"><span data-stu-id="33615-2126">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="33615-2127">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2127">64 bit</span></span> | <span data-ttu-id="33615-2128">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2128">64 bit</span></span> | <span data-ttu-id="33615-2129">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="33615-2129">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="33615-2130">% WINDIR% \\ SysWOW64</span><span class="sxs-lookup"><span data-stu-id="33615-2130">%windir%\\syswow64</span></span> | <span data-ttu-id="33615-2131">SYSTEMX86 CSID \_</span><span class="sxs-lookup"><span data-stu-id="33615-2131">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="33615-2132">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2132">64 bit</span></span> | <span data-ttu-id="33615-2133">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2133">32 bit</span></span> | <span data-ttu-id="33615-2134">FOLDERID \_ система</span><span class="sxs-lookup"><span data-stu-id="33615-2134">FOLDERID\_System</span></span> | <span data-ttu-id="33615-2135">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="33615-2135">%windir%\\system32</span></span> | <span data-ttu-id="33615-2136">система CSID \_</span><span class="sxs-lookup"><span data-stu-id="33615-2136">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="33615-2137">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2137">64 bit</span></span> | <span data-ttu-id="33615-2138">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="33615-2138">32 bit</span></span> | <span data-ttu-id="33615-2139">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="33615-2139">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="33615-2140">% WINDIR% \\ SysWOW64</span><span class="sxs-lookup"><span data-stu-id="33615-2140">%windir%\\syswow64</span></span> | <span data-ttu-id="33615-2141">SYSTEMX86 CSID \_</span><span class="sxs-lookup"><span data-stu-id="33615-2141">CSIDL\_SYSTEMX86</span></span> |


<span data-ttu-id="33615-2142">Мы использовали строки среды для предоставления универсальных путей в этой статье.</span><span class="sxs-lookup"><span data-stu-id="33615-2142">We have used environment strings to provide generic paths throughout this topic.</span></span> <span data-ttu-id="33615-2143">В следующих таблицах приведены примеры путей, которые представляют эти строки среды.</span><span class="sxs-lookup"><span data-stu-id="33615-2143">The following tables give examples of the paths those environment strings represent.</span></span> <span data-ttu-id="33615-2144">В некоторых случаях эти пути могут не совпадать с параметрами на определенном компьютере из-за выбора, сделанного во время установки или перенаправления папок более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="33615-2144">In some cases, these paths might not match those on a particular computer because of choices made during installation or later folder redirection.</span></span> <span data-ttu-id="33615-2145">Обратите внимание, что некоторые пути для Windows Vista изменились.</span><span class="sxs-lookup"><span data-stu-id="33615-2145">Note that some paths have changed for Windows Vista.</span></span>


<span data-ttu-id="33615-2146">**Windows Vista и более поздние версии**</span><span class="sxs-lookup"><span data-stu-id="33615-2146">**Windows Vista and later**</span></span>

| <span data-ttu-id="33615-2147">Строка среды</span><span class="sxs-lookup"><span data-stu-id="33615-2147">Environment String</span></span> | <span data-ttu-id="33615-2148">Пример пути</span><span class="sxs-lookup"><span data-stu-id="33615-2148">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="33615-2149">ALLUSERSPROFILE</span><span class="sxs-lookup"><span data-stu-id="33615-2149">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="33615-2150">C: \\ папка ProgramData</span><span class="sxs-lookup"><span data-stu-id="33615-2150">C:\\ProgramData</span></span> |
| <span data-ttu-id="33615-2151">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="33615-2151">%APPDATA%</span></span> | <span data-ttu-id="33615-2152">C: \\ Users \\ *username* \\ AppData \\ роуминг</span><span class="sxs-lookup"><span data-stu-id="33615-2152">C:\\Users\\*username*\\AppData\\Roaming</span></span> |
| <span data-ttu-id="33615-2153">LocalAppData</span><span class="sxs-lookup"><span data-stu-id="33615-2153">%LOCALAPPDATA%</span></span> | <span data-ttu-id="33615-2154">C: \\ Users \\ *username* \\ AppData \\ Local</span><span class="sxs-lookup"><span data-stu-id="33615-2154">C:\\Users\\*username*\\AppData\\Local</span></span> |
| <span data-ttu-id="33615-2155">Папка ProgramData</span><span class="sxs-lookup"><span data-stu-id="33615-2155">%ProgramData%</span></span> | <span data-ttu-id="33615-2156">C: \\ папка ProgramData</span><span class="sxs-lookup"><span data-stu-id="33615-2156">C:\\ProgramData</span></span> |
| <span data-ttu-id="33615-2157">ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="33615-2157">%ProgramFiles%</span></span> | <span data-ttu-id="33615-2158">C: \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="33615-2158">C:\\Program Files</span></span> |
| <span data-ttu-id="33615-2159">%ProgramFiles(x86)%</span><span class="sxs-lookup"><span data-stu-id="33615-2159">%ProgramFiles(x86)%</span></span> | <span data-ttu-id="33615-2160">C: \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="33615-2160">C:\\Program Files (x86)</span></span> |
| <span data-ttu-id="33615-2161">ЗАКРЫТЫЙ</span><span class="sxs-lookup"><span data-stu-id="33615-2161">%PUBLIC%</span></span> | <span data-ttu-id="33615-2162">В. \\ Пользователи, \\ открытые</span><span class="sxs-lookup"><span data-stu-id="33615-2162">C:\\Users\\Public</span></span> |
| <span data-ttu-id="33615-2163">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="33615-2163">%SystemDrive%</span></span> | <span data-ttu-id="33615-2164">В.</span><span class="sxs-lookup"><span data-stu-id="33615-2164">C:</span></span> |
| <span data-ttu-id="33615-2165">Филе</span><span class="sxs-lookup"><span data-stu-id="33615-2165">%USERPROFILE%</span></span> | <span data-ttu-id="33615-2166">C: \\ Users \\ *username*</span><span class="sxs-lookup"><span data-stu-id="33615-2166">C:\\Users\\*username*</span></span> |
| <span data-ttu-id="33615-2167">%windir%</span><span class="sxs-lookup"><span data-stu-id="33615-2167">%windir%</span></span> | <span data-ttu-id="33615-2168">C: \\ Windows</span><span class="sxs-lookup"><span data-stu-id="33615-2168">C:\\Windows</span></span> |


<span data-ttu-id="33615-2169">**Windows XP и более ранние версии**</span><span class="sxs-lookup"><span data-stu-id="33615-2169">**Windows XP and earlier**</span></span>

| <span data-ttu-id="33615-2170">Строка среды</span><span class="sxs-lookup"><span data-stu-id="33615-2170">Environment String</span></span> | <span data-ttu-id="33615-2171">Пример пути</span><span class="sxs-lookup"><span data-stu-id="33615-2171">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="33615-2172">ALLUSERSPROFILE</span><span class="sxs-lookup"><span data-stu-id="33615-2172">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="33615-2173">В. \\ документы и параметры \\ все пользователи</span><span class="sxs-lookup"><span data-stu-id="33615-2173">C:\\Documents and Settings\\All Users</span></span> |
| <span data-ttu-id="33615-2174">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="33615-2174">%APPDATA%</span></span> | <span data-ttu-id="33615-2175">C: \\ Documents and Settings \\ *имя_пользователя* \\ Application Data</span><span class="sxs-lookup"><span data-stu-id="33615-2175">C:\\Documents and Settings\\*username*\\Application Data</span></span> |
| <span data-ttu-id="33615-2176">ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="33615-2176">%ProgramFiles%</span></span> | <span data-ttu-id="33615-2177">C: \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="33615-2177">C:\\Program Files</span></span> |
| <span data-ttu-id="33615-2178">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="33615-2178">%SystemDrive%</span></span> | <span data-ttu-id="33615-2179">В.</span><span class="sxs-lookup"><span data-stu-id="33615-2179">C:</span></span> |
| <span data-ttu-id="33615-2180">Филе</span><span class="sxs-lookup"><span data-stu-id="33615-2180">%USERPROFILE%</span></span> | <span data-ttu-id="33615-2181">C: \\ \\ *имя пользователя* документов и параметров</span><span class="sxs-lookup"><span data-stu-id="33615-2181">C:\\Documents and Settings\\*username*</span></span> |
| <span data-ttu-id="33615-2182">%windir%</span><span class="sxs-lookup"><span data-stu-id="33615-2182">%windir%</span></span> | <span data-ttu-id="33615-2183">C: \\ Windows</span><span class="sxs-lookup"><span data-stu-id="33615-2183">C:\\Windows</span></span> |


## <a name="requirements"></a><span data-ttu-id="33615-2184">Требования</span><span class="sxs-lookup"><span data-stu-id="33615-2184">Requirements</span></span>


| <span data-ttu-id="33615-2185">Требование</span><span class="sxs-lookup"><span data-stu-id="33615-2185">Requirement</span></span> | <span data-ttu-id="33615-2186">Значение</span><span class="sxs-lookup"><span data-stu-id="33615-2186">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="33615-2187">Header</span><span class="sxs-lookup"><span data-stu-id="33615-2187">Header</span></span><br/> | <dl> <span data-ttu-id="33615-2188"><dt>Кновнфолдерс. h</dt></span><span class="sxs-lookup"><span data-stu-id="33615-2188"><dt>Knownfolders.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33615-2189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33615-2189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33615-2190">**CSID**</span><span class="sxs-lookup"><span data-stu-id="33615-2190">**CSIDL**</span></span>](csidl.md)
</dt> <dt>

[<span data-ttu-id="33615-2191">Известные папки</span><span class="sxs-lookup"><span data-stu-id="33615-2191">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="33615-2192">Работа с известными папками в приложениях</span><span class="sxs-lookup"><span data-stu-id="33615-2192">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
</dt> <dt>

[<span data-ttu-id="33615-2193">Расширение известных папок с помощью пользовательских папок</span><span class="sxs-lookup"><span data-stu-id="33615-2193">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
</dt> <dt>

<span data-ttu-id="33615-2194">[Пример: известные папки](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33615-2194">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
