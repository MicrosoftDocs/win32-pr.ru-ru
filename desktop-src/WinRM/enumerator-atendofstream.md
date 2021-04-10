---
title: Свойство Enumerator. Атендофстреам (Всмандисп. h)
description: Возвращает логическое значение, указывающее, имеются ли в коллекции другие элементы.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства Атендофстреам
- Служба удаленного управления Windows свойства Атендофстреам, объект Enumerator
- Служба удаленного управления Windows объекта перечислителя, свойство Атендофстреам
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023798f6c868e434218dd1a4dbdf1928bf4526a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135499"
---
# <a name="enumeratoratendofstream-property"></a><span data-ttu-id="96ca6-106">Свойство Enumerator. Атендофстреам</span><span class="sxs-lookup"><span data-stu-id="96ca6-106">Enumerator.AtEndOfStream property</span></span>

<span data-ttu-id="96ca6-107">Возвращает логическое значение, указывающее, имеются ли в коллекции другие элементы.</span><span class="sxs-lookup"><span data-stu-id="96ca6-107">Gets a Boolean value that indicates whether there are any more items in the collection.</span></span>

<span data-ttu-id="96ca6-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="96ca6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ca6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96ca6-109">Syntax</span></span>


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="96ca6-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="96ca6-110">Property value</span></span>

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="96ca6-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Условия**</span><span class="sxs-lookup"><span data-stu-id="96ca6-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</span></span>


</dt> <dd>

<span data-ttu-id="96ca6-112">В коллекции больше нет элементов.</span><span class="sxs-lookup"><span data-stu-id="96ca6-112">No more items are in the collection.</span></span>

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="96ca6-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**IsFalse**</span><span class="sxs-lookup"><span data-stu-id="96ca6-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</span></span>


</dt> <dd>

<span data-ttu-id="96ca6-114">Доступны дополнительные элементы.</span><span class="sxs-lookup"><span data-stu-id="96ca6-114">More items are available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96ca6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96ca6-115">Remarks</span></span>

<span data-ttu-id="96ca6-116">Если объект [**перечислителя**](enumerator.md) освобождается после получения всех необходимых данных, все ожидающие запросы перечисления удаляются.</span><span class="sxs-lookup"><span data-stu-id="96ca6-116">If you free the [**Enumerator**](enumerator.md) object after you have obtained all the data required, then any pending enumeration requests are removed.</span></span> <span data-ttu-id="96ca6-117">Дополнительные сведения см. [в разделе перечисление или составление списка всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="96ca6-117">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="examples"></a><span data-ttu-id="96ca6-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="96ca6-118">Examples</span></span>

<span data-ttu-id="96ca6-119">В следующем примере на языке VBScript перечисляются экземпляры операционной системы.</span><span class="sxs-lookup"><span data-stu-id="96ca6-119">The following VBScript example enumerates operating system instances.</span></span> <span data-ttu-id="96ca6-120">Обратите внимание, что освобождение объекта перечисления очищает все ожидающие запросы перечисления.</span><span class="sxs-lookup"><span data-stu-id="96ca6-120">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span> <span data-ttu-id="96ca6-121">Подпрограмма DisplayOutput форматирует выходные данные таким же образом, как средство WinRM. cmd.</span><span class="sxs-lookup"><span data-stu-id="96ca6-121">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

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



## <a name="requirements"></a><span data-ttu-id="96ca6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="96ca6-122">Requirements</span></span>



| <span data-ttu-id="96ca6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="96ca6-123">Requirement</span></span> | <span data-ttu-id="96ca6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="96ca6-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="96ca6-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96ca6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="96ca6-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96ca6-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="96ca6-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96ca6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="96ca6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96ca6-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="96ca6-129">Header</span><span class="sxs-lookup"><span data-stu-id="96ca6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="96ca6-130"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="96ca6-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="96ca6-131">IDL</span><span class="sxs-lookup"><span data-stu-id="96ca6-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96ca6-132"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96ca6-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="96ca6-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96ca6-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="96ca6-134"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="96ca6-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="96ca6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="96ca6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96ca6-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96ca6-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96ca6-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96ca6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ca6-138">**Перечислитель**</span><span class="sxs-lookup"><span data-stu-id="96ca6-138">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="96ca6-139">Перечисление или вывод всех экземпляров ресурса</span><span class="sxs-lookup"><span data-stu-id="96ca6-139">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





