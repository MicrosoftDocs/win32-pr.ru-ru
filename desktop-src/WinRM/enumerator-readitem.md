---
title: Метод Enumerator. ReadItem (Всмандисп. h)
description: Извлекает элемент из ресурса и возвращает XML-представление элемента.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода ReadItem
- Служба удаленного управления Windows метода ReadItem, объект Enumerator
- Объект перечислителя служба удаленного управления Windows, метод ReadItem
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071396"
---
# <a name="enumeratorreaditem-method"></a><span data-ttu-id="e4b5a-106">Метод Enumerator. ReadItem</span><span class="sxs-lookup"><span data-stu-id="e4b5a-106">Enumerator.ReadItem method</span></span>

<span data-ttu-id="e4b5a-107">Извлекает элемент из ресурса и возвращает XML-представление элемента.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-107">Retrieves an item from the resource and returns an XML representation of the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b5a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4b5a-108">Syntax</span></span>


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a><span data-ttu-id="e4b5a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4b5a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b5a-110">*ресурсов*</span><span class="sxs-lookup"><span data-stu-id="e4b5a-110">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b5a-111">Универсальный код ресурса (URI) элемента.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-111">The URI of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b5a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4b5a-112">Return value</span></span>

<span data-ttu-id="e4b5a-113">XML-представление элемента.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-113">The XML representation of the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b5a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4b5a-114">Remarks</span></span>

<span data-ttu-id="e4b5a-115">Чтобы ограничить количество считываемых элементов, задайте свойство [**Session.Batчитемс**](session-batchitems.md) .</span><span class="sxs-lookup"><span data-stu-id="e4b5a-115">To limit the number of items that are read, set the [**Session.BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="e4b5a-116">Обратите внимание, что освобождение объекта перечисления очищает все ожидающие запросы перечисления.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-116">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span>

<span data-ttu-id="e4b5a-117">Метод [**Session. Enumerate**](session-enumerate.md) не получает коллекцию точно так же, как [запрос WMI](/windows/desktop/WmiSdk/querying-wmi), такой как `SELECT * from Win32_LogicalDisk` , возвращает коллекцию в [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span><span class="sxs-lookup"><span data-stu-id="e4b5a-117">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in the same way that a [WMI query](/windows/desktop/WmiSdk/querying-wmi), such as `SELECT * from Win32_LogicalDisk`, returns a collection in an [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span></span> <span data-ttu-id="e4b5a-118">Для чтения файла в виде текстового потока создается объект скрипта [TextStream](/previous-versions//312a5kbt(v=vs.85)) и вызывается метод [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) для чтения каждой строки файла.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-118">To read a file as a text stream, you create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="e4b5a-119">Аналогичным образом вызывается метод **Session. Enumerate** для получения объекта [**перечислителя**](enumerator.md) , а затем вызывается метод **Enumerator. ReadItem** .</span><span class="sxs-lookup"><span data-stu-id="e4b5a-119">In a similar way, you call the **Session.Enumerate** method to obtain an [**Enumerator**](enumerator.md) object and then call the **Enumerator.ReadItem** method.</span></span> <span data-ttu-id="e4b5a-120">Как и при чтении из текстового файла, можно проверить свойство [**Enumerator. атендофстреам**](enumerator-atendofstream.md) , чтобы проверить, достигли ли вы конца элементов данных.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-120">As in reading from the text file, you can check the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

## <a name="examples"></a><span data-ttu-id="e4b5a-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="e4b5a-121">Examples</span></span>

<span data-ttu-id="e4b5a-122">В следующем примере VBScript вызывается метод [**Session. Enumerate**](session-enumerate.md) для получения списка запланированных заданий.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-122">The following VBScript example calls the [**Session.Enumerate**](session-enumerate.md) method to obtain a list of scheduled jobs.</span></span> <span data-ttu-id="e4b5a-123">Подпрограмма DisplayOutput использует XML-файл преобразования средства командной строки WinRM (Всмткст. xsl) для вывода данных в табличной форме.</span><span class="sxs-lookup"><span data-stu-id="e4b5a-123">The DisplayOutput subroutine uses the Winrm command line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e4b5a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e4b5a-124">Requirements</span></span>



| <span data-ttu-id="e4b5a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e4b5a-125">Requirement</span></span> | <span data-ttu-id="e4b5a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e4b5a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b5a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4b5a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b5a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4b5a-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e4b5a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4b5a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b5a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4b5a-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e4b5a-131">Header</span><span class="sxs-lookup"><span data-stu-id="e4b5a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b5a-132"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b5a-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4b5a-133">IDL</span><span class="sxs-lookup"><span data-stu-id="e4b5a-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4b5a-134"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4b5a-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e4b5a-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e4b5a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4b5a-136"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e4b5a-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e4b5a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e4b5a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4b5a-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4b5a-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4b5a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4b5a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b5a-140">**Перечислитель**</span><span class="sxs-lookup"><span data-stu-id="e4b5a-140">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="e4b5a-141">Перечисление или составление списка всех экземпляров ресурса</span><span class="sxs-lookup"><span data-stu-id="e4b5a-141">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

