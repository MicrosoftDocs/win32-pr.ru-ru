---
description: Функция Уикреатепатчпаккаже принимает файл создания пакета (PCP-файл) и создает пакет исправлений установщик Windows (MSP-пакет).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: Уикреатепатчпаккаже (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896669"
---
# <a name="uicreatepatchpackage-patchwizdll"></a><span data-ttu-id="049f0-103">Уикреатепатчпаккаже (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="049f0-103">UiCreatePatchPackage (Patchwiz.dll)</span></span>

<span data-ttu-id="049f0-104">Функция Уикреатепатчпаккаже принимает файл создания пакета (PCP-файл) и создает пакет исправлений установщик Windows (MSP-пакет).</span><span class="sxs-lookup"><span data-stu-id="049f0-104">The UiCreatePatchPackage function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="049f0-105">Вызов [Msimsp.exe](msimsp-exe.md) является рекомендуемым методом для использования [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="049f0-105">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="049f0-106">Функция [уикреатепатчпаккажеекс](uicreatepatchpackageex--patchwiz-dll-.md) доступна в версии 4,0 Patchwiz.dll и расширяет функциональные возможности функции уикреатепатчпаккаже.</span><span class="sxs-lookup"><span data-stu-id="049f0-106">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function is available in version 4.0 of Patchwiz.dll and extends the functionality of the UiCreatePatchPackage function.</span></span>

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
);
```

## <a name="parameters"></a><span data-ttu-id="049f0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="049f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="049f0-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*сзпкппас*</span><span class="sxs-lookup"><span data-stu-id="049f0-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="049f0-109">Полный путь к файлу свойств создания исправления (файл. PCP) для этого исправления.</span><span class="sxs-lookup"><span data-stu-id="049f0-109">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="049f0-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*сзпатчпас*</span><span class="sxs-lookup"><span data-stu-id="049f0-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="049f0-111">Полный путь к создаваемому пакету исправлений установщик Windows (MSP-файл).</span><span class="sxs-lookup"><span data-stu-id="049f0-111">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="049f0-112">Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен.</span><span class="sxs-lookup"><span data-stu-id="049f0-112">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="049f0-113">Если он имеет **значение NULL** или является пустой строкой, функция использует значение Патчаутпутпас в [таблице свойств (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="049f0-113">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="049f0-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*сзлогпас*</span><span class="sxs-lookup"><span data-stu-id="049f0-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="049f0-115">Полный путь к текстовому файлу журнала, который будет добавлен.</span><span class="sxs-lookup"><span data-stu-id="049f0-115">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="049f0-116">Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен.</span><span class="sxs-lookup"><span data-stu-id="049f0-116">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="049f0-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*хвндстатус*</span><span class="sxs-lookup"><span data-stu-id="049f0-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="049f0-118">Обработчик для окна, отображающего текст состояния.</span><span class="sxs-lookup"><span data-stu-id="049f0-118">Handle to a window that displays the status text.</span></span> <span data-ttu-id="049f0-119">Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен.</span><span class="sxs-lookup"><span data-stu-id="049f0-119">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="049f0-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*сзтемпфолдер*</span><span class="sxs-lookup"><span data-stu-id="049f0-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="049f0-121">Расположение временных файлов.</span><span class="sxs-lookup"><span data-stu-id="049f0-121">Location for temporary files.</span></span> <span data-ttu-id="049f0-122">Этот параметр может иметь **значение NULL** или быть пустой строкой, но не может быть пропущен.</span><span class="sxs-lookup"><span data-stu-id="049f0-122">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="049f0-123">Расположение по умолчанию:% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="049f0-123">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="049f0-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*фремоветемпфолдерконтентс*</span><span class="sxs-lookup"><span data-stu-id="049f0-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="049f0-125">Если **значение — true**, удалите временную папку и все ее содержимое, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="049f0-125">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="049f0-126">Если задано **значение false** и имеется папка, функция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="049f0-126">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="049f0-127">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="049f0-127">Return Values</span></span>

<span data-ttu-id="049f0-128">См. таблицу в разделе [возвращаемые значения для уикреатепатчпаккаже](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="049f0-128">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="049f0-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="049f0-129">Remarks</span></span>

<span data-ttu-id="049f0-130">Пример создания PCP-файла и использования Уикреатепатчпаккаже для создания пакета исправлений установщик Windows см. в разделе [Пример небольшого обновления исправлений](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="049f0-130">For an example of authoring a .pcp file and using UiCreatePatchPackage to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="049f0-131">Для создания исправления требуется несжатый образ установки, например административный образ или несжатый образ установки с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="049f0-131">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="049f0-132">Уикреатепатчпаккаже не создает двоичные исправления для файлов в ящиках.</span><span class="sxs-lookup"><span data-stu-id="049f0-132">UiCreatePatchPackage does not generate binary patches for files in cabinets.</span></span>

 

 



