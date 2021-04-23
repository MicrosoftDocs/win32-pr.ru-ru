---
title: Метод WSMan. Креатересаурцелокатор (Всмандисп. h)
description: Создает объект ResourceLocator, который можно использовать вместо указания URI ресурса в операциях с объектами сеанса, таких как Session. Get, Session. Where или Session. Enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Креатересаурцелокатор
- Служба удаленного управления Windows метода Креатересаурцелокатор, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Креатересаурцелокатор
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988568"
---
# <a name="wsmancreateresourcelocator-method"></a><span data-ttu-id="b0c41-106">Метод WSMan. Креатересаурцелокатор</span><span class="sxs-lookup"><span data-stu-id="b0c41-106">WSMan.CreateResourceLocator method</span></span>

<span data-ttu-id="b0c41-107">Создает объект [**ResourceLocator**](resourcelocator.md) , который можно использовать вместо указания URI ресурса в операциях с объектами [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="b0c41-107">Creates a [**ResourceLocator**](resourcelocator.md) object that can be used instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0c41-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0c41-108">Syntax</span></span>


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b0c41-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0c41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0c41-110">*универсальный код ресурса* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b0c41-110">*uri* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0c41-111">URI ресурса для ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0c41-111">The resource URI for the resource.</span></span> <span data-ttu-id="b0c41-112">Дополнительные сведения о строках URI см. в разделе [URI ресурсов](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="b0c41-112">For more information about URI strings, see [Resource URIs](resource-uris.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0c41-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0c41-113">Return value</span></span>

<span data-ttu-id="b0c41-114">Объект [**ResourceLocator**](resourcelocator.md) , который затем можно использовать для выполнения локальных или удаленных операций WinRM.</span><span class="sxs-lookup"><span data-stu-id="b0c41-114">A [**ResourceLocator**](resourcelocator.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0c41-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0c41-115">Remarks</span></span>

<span data-ttu-id="b0c41-116">Если свойство **фрагментдиалект** не указано в объекте [**ResourceLocator**](resourcelocator.md) , по умолчанию используется спецификация XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="b0c41-116">If the **FragmentDialect** property is not specified in the [**ResourceLocator**](resourcelocator.md) object, the default is the XPath 1.0 specification.</span></span> <span data-ttu-id="b0c41-117">Дополнительные сведения см. на веб-сайте [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="b0c41-117">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="examples"></a><span data-ttu-id="b0c41-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="b0c41-118">Examples</span></span>

<span data-ttu-id="b0c41-119">Следующий пример кода VBScript создает объект [**ResourceLocator**](resourcelocator.md) и получает значение свойства **Description** сетевого адаптера из экземпляра [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) с индексом "1".</span><span class="sxs-lookup"><span data-stu-id="b0c41-119">The following VBScript code example creates a [**ResourceLocator**](resourcelocator.md) object and gets the network adapter **Description** property value from the instance of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) with an Index of "1".</span></span>


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a><span data-ttu-id="b0c41-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b0c41-120">Requirements</span></span>



| <span data-ttu-id="b0c41-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b0c41-121">Requirement</span></span> | <span data-ttu-id="b0c41-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b0c41-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c41-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0c41-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b0c41-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0c41-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b0c41-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0c41-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b0c41-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0c41-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b0c41-127">Header</span><span class="sxs-lookup"><span data-stu-id="b0c41-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0c41-128"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0c41-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0c41-129">IDL</span><span class="sxs-lookup"><span data-stu-id="b0c41-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0c41-130"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0c41-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b0c41-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b0c41-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0c41-132"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b0c41-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b0c41-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b0c41-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0c41-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0c41-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0c41-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0c41-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0c41-136">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="b0c41-136">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="b0c41-137">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="b0c41-137">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="b0c41-138">**Session**</span><span class="sxs-lookup"><span data-stu-id="b0c41-138">**Session**</span></span>](session.md)
</dt> </dl>

 

