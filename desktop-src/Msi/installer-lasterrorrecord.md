---
description: Метод Ластерроррекорд объекта Installer возвращает объект Record, содержащий параметры ошибки для самой последней ошибки из функции, которая вызвала запись об ошибке.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Метод Installer. Ластерроррекорд
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b368f30b04734b2d253a7d5f2aa64f0d61c930e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651598"
---
# <a name="installerlasterrorrecord-method"></a><span data-ttu-id="1cf50-103">Метод Installer. Ластерроррекорд</span><span class="sxs-lookup"><span data-stu-id="1cf50-103">Installer.LastErrorRecord method</span></span>

<span data-ttu-id="1cf50-104">Метод **ластерроррекорд** объекта [**Installer**](installer-object.md) возвращает объект [**Record**](record-object.md) , содержащий параметры ошибки для самой последней ошибки из функции, которая вызвала запись об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1cf50-104">The **LastErrorRecord** method of the [**Installer**](installer-object.md) object returns a [**Record**](record-object.md) object that contains error parameters for the most recent error from the function that produced the error record.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cf50-105">Syntax</span></span>


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a><span data-ttu-id="1cf50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cf50-106">Parameters</span></span>

<span data-ttu-id="1cf50-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1cf50-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cf50-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1cf50-108">Return value</span></span>

<span data-ttu-id="1cf50-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1cf50-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cf50-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1cf50-110">Remarks</span></span>

<span data-ttu-id="1cf50-111">Объект [**Record**](record-object.md) сбрасывается после выполнения этой функции любой функции, которая создает запись об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1cf50-111">The [**Record**](record-object.md) object is reset after the execution of this function of any function that generates an error record.</span></span>

<span data-ttu-id="1cf50-112">Только следующие назначенные функции создают запись об ошибке:</span><span class="sxs-lookup"><span data-stu-id="1cf50-112">Only the following designated functions generate an error record:</span></span>

-   [<span data-ttu-id="1cf50-113">**Метод Опендатабасе (объект установщика)**</span><span class="sxs-lookup"><span data-stu-id="1cf50-113">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="1cf50-114">**Сохраните**</span><span class="sxs-lookup"><span data-stu-id="1cf50-114">**Commit**</span></span>](database-commit.md)
-   [<span data-ttu-id="1cf50-115">**OpenView**</span><span class="sxs-lookup"><span data-stu-id="1cf50-115">**OpenView**</span></span>](database-openview.md)
-   [<span data-ttu-id="1cf50-116">**Импорт**</span><span class="sxs-lookup"><span data-stu-id="1cf50-116">**Import**</span></span>](database-import.md)
-   [<span data-ttu-id="1cf50-117">**Экспорт**</span><span class="sxs-lookup"><span data-stu-id="1cf50-117">**Export**</span></span>](database-export.md)
-   [<span data-ttu-id="1cf50-118">**AutoMerge**</span><span class="sxs-lookup"><span data-stu-id="1cf50-118">**Merge**</span></span>](database-merge.md)
-   [<span data-ttu-id="1cf50-119">**Преобразование**</span><span class="sxs-lookup"><span data-stu-id="1cf50-119">**GenerateTransform**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="1cf50-120">**апплитрансформ**</span><span class="sxs-lookup"><span data-stu-id="1cf50-120">**ApplyTransform**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="1cf50-121">**Работать**</span><span class="sxs-lookup"><span data-stu-id="1cf50-121">**Execute**</span></span>](view-execute.md)
-   [<span data-ttu-id="1cf50-122">**Изменений**</span><span class="sxs-lookup"><span data-stu-id="1cf50-122">**Modify**</span></span>](view-modify.md)
-   [<span data-ttu-id="1cf50-123">**сетстреам**</span><span class="sxs-lookup"><span data-stu-id="1cf50-123">**SetStream**</span></span>](record-setstream.md)
-   [<span data-ttu-id="1cf50-124">**SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="1cf50-124">**SummaryInformation**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="1cf50-125">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="1cf50-125">**SourcePath**</span></span>](session-sourcepath.md)
-   [<span data-ttu-id="1cf50-126">**TargetPath**</span><span class="sxs-lookup"><span data-stu-id="1cf50-126">**TargetPath**</span></span>](session-targetpath.md)
-   [<span data-ttu-id="1cf50-127">**компоненткуррентстате**</span><span class="sxs-lookup"><span data-stu-id="1cf50-127">**ComponentCurrentState**</span></span>](session-componentcurrentstate.md)
-   [<span data-ttu-id="1cf50-128">**компонентрекуестстате**</span><span class="sxs-lookup"><span data-stu-id="1cf50-128">**ComponentRequestState**</span></span>](session-componentrequeststate.md)
-   [<span data-ttu-id="1cf50-129">**феатурекуррентстате**</span><span class="sxs-lookup"><span data-stu-id="1cf50-129">**FeatureCurrentState**</span></span>](session-featurecurrentstate.md)
-   [<span data-ttu-id="1cf50-130">**феатуререкуестстате**</span><span class="sxs-lookup"><span data-stu-id="1cf50-130">**FeatureRequestState**</span></span>](session-featurerequeststate.md)
-   [<span data-ttu-id="1cf50-131">**феатурекост**</span><span class="sxs-lookup"><span data-stu-id="1cf50-131">**FeatureCost**</span></span>](session-featurecost.md)
-   [<span data-ttu-id="1cf50-132">**феатуревалидстатес**</span><span class="sxs-lookup"><span data-stu-id="1cf50-132">**FeatureValidStates**</span></span>](session-featurevalidstates.md)
-   [<span data-ttu-id="1cf50-133">**сетинсталллевел**</span><span class="sxs-lookup"><span data-stu-id="1cf50-133">**SetInstallLevel**</span></span>](session-setinstalllevel.md)

<span data-ttu-id="1cf50-134">Следующий пример в языке VBScript использует вызов [**опендатабасе**](installer-opendatabase.md) , чтобы продемонстрировать, как получить расширенные сведения об ошибке из одного из методов или свойств, поддерживающих метод **ластерроррекорд** .</span><span class="sxs-lookup"><span data-stu-id="1cf50-134">The following sample in VBScript uses a call to [**OpenDatabase**](installer-opendatabase.md) to show how to obtain extended error information from one of the methods or properties that support the **LastErrorRecord** method.</span></span> <span data-ttu-id="1cf50-135">В примере создается сообщение об ошибке при сбое метода **опендатабасе** .</span><span class="sxs-lookup"><span data-stu-id="1cf50-135">The sample constructs an error message when the **OpenDatabase** method fails.</span></span> <span data-ttu-id="1cf50-136">Объект **Err** используется для определения того, была ли обнаружена ошибка.</span><span class="sxs-lookup"><span data-stu-id="1cf50-136">The **Err** object is used to determine whether an error was encountered.</span></span>


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a><span data-ttu-id="1cf50-137">Требования</span><span class="sxs-lookup"><span data-stu-id="1cf50-137">Requirements</span></span>



| <span data-ttu-id="1cf50-138">Требование</span><span class="sxs-lookup"><span data-stu-id="1cf50-138">Requirement</span></span> | <span data-ttu-id="1cf50-139">Значение</span><span class="sxs-lookup"><span data-stu-id="1cf50-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf50-140">Версия</span><span class="sxs-lookup"><span data-stu-id="1cf50-140">Version</span></span><br/> | <span data-ttu-id="1cf50-141">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1cf50-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1cf50-142">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1cf50-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1cf50-143">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="1cf50-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1cf50-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1cf50-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="1cf50-145"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cf50-145"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1cf50-146">IID</span><span class="sxs-lookup"><span data-stu-id="1cf50-146">IID</span></span><br/>     | <span data-ttu-id="1cf50-147">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1cf50-147">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




