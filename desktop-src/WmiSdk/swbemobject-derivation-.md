---
description: Свойство производности \_ объекта SWbemObject содержит массив строк, описывающих производную иерархию класса для экземпляра, на который указывает ссылка.
ms.assetid: 8a4daab0-7d10-4a37-aacd-1f3f499b859a
ms.tgt_platform: multiple
title: Свойство SWbemObject.Derivation_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Derivation_
- ISWbemObject.Derivation_
- ISWbemObject.get_Derivation_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84e7b4e53a1a5544c92bb5116f3f83189789487f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702553"
---
# <a name="swbemobjectderivation_-property"></a><span data-ttu-id="c5b84-103">SWbemObject. производное \_ свойство</span><span class="sxs-lookup"><span data-stu-id="c5b84-103">SWbemObject.Derivation\_ property</span></span>

<span data-ttu-id="c5b84-104">Свойство **производности \_** объекта [**SWbemObject**](swbemobject.md) содержит массив строк, описывающих производную иерархию класса для экземпляра, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="c5b84-104">The **Derivation\_** property of the [**SWbemObject**](swbemobject.md) object contains an array of strings that describe the class derivation hierarchy for the instance being referenced.</span></span> <span data-ttu-id="c5b84-105">Первый элемент массива определяет родительский класс, а последний элемент определяет класс династию.</span><span class="sxs-lookup"><span data-stu-id="c5b84-105">The first element in the array defines the parent class and the last element defines the dynasty class.</span></span> <span data-ttu-id="c5b84-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c5b84-106">This property is read-only.</span></span>

<span data-ttu-id="c5b84-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c5b84-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c5b84-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c5b84-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b84-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5b84-109">Syntax</span></span>


```VB
SWbemObject.Derivation_ As String
```



## <a name="property-value"></a><span data-ttu-id="c5b84-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c5b84-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="c5b84-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="c5b84-111">Examples</span></span>

<span data-ttu-id="c5b84-112">Следующий пример сценария VBScript описывает, как получить иерархию классов для Win32 \_ LogicalDisk.</span><span class="sxs-lookup"><span data-stu-id="c5b84-112">The following VBScript sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```VB
on Error resume next

Set c = GetObject("winmgmts://./root/cimv2:win32_logicaldisk")
d = c.Derivation_

for x = LBound(d) to UBound(d)
 WScript.Echo d(x)
Next

if err <> 0 then
 WScript.Echo Err.Description
end if
```



<span data-ttu-id="c5b84-113">Следующий пример Perl описывает, как получить иерархию классов для Win32 \_ LogicalDisk.</span><span class="sxs-lookup"><span data-stu-id="c5b84-113">he following Perl sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```
use strict;
use Win32::OLE;

my ($C, $D, @collection);

eval {$C = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("win32_logicaldisk") };
unless ($@) 
{
 @collection = in $C;
 eval {$D = $collection[0]->Derivation_();};
 print "\n";
 unless ($@) 
 {
  print map{"$_\n"} @{$D};
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="c5b84-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c5b84-114">Requirements</span></span>



| <span data-ttu-id="c5b84-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c5b84-115">Requirement</span></span> | <span data-ttu-id="c5b84-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c5b84-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b84-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5b84-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b84-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5b84-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5b84-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5b84-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b84-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5b84-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5b84-121">Header</span><span class="sxs-lookup"><span data-stu-id="c5b84-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5b84-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5b84-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5b84-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c5b84-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5b84-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c5b84-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c5b84-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c5b84-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5b84-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5b84-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5b84-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="c5b84-127">CLSID</span></span><br/>                    | <span data-ttu-id="c5b84-128">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="c5b84-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="c5b84-129">IID</span><span class="sxs-lookup"><span data-stu-id="c5b84-129">IID</span></span><br/>                      | <span data-ttu-id="c5b84-130">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="c5b84-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




