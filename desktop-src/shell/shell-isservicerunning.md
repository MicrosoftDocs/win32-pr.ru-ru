---
description: Возвращает значение, указывающее, запущена ли определенная служба.
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Метод Shell. Иссервицеруннинг (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3a65be4955c6f49e8e6baa49cd9dedb82fc5cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909880"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="5e87c-103">Shell. Иссервицеруннинг, метод</span><span class="sxs-lookup"><span data-stu-id="5e87c-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="5e87c-104">Возвращает значение, указывающее, запущена ли определенная служба.</span><span class="sxs-lookup"><span data-stu-id="5e87c-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e87c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e87c-105">Syntax</span></span>


```JScript
retVal = Shell.IsServiceRunning(
  sServiceName
)
```


```VB

Shell.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="5e87c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e87c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e87c-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e87c-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e87c-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="5e87c-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="5e87c-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="5e87c-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e87c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e87c-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="5e87c-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="5e87c-111">JScript</span></span>

<span data-ttu-id="5e87c-112">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="5e87c-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="5e87c-113">Возвращает \*значение _ true\*\*, если запущена служба, указанная параметром *ссервиценаме* . в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="5e87c-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="5e87c-114">VB</span><span class="sxs-lookup"><span data-stu-id="5e87c-114">VB</span></span>

<span data-ttu-id="5e87c-115">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="5e87c-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="5e87c-116">Возвращает \*значение _ true\*\*, если запущена служба, указанная параметром *ссервиценаме* . в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="5e87c-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e87c-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="5e87c-117">Remarks</span></span>

<span data-ttu-id="5e87c-118">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5e87c-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="5e87c-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="5e87c-119">Examples</span></span>

<span data-ttu-id="5e87c-120">В следующих примерах показано использование **иссервицеруннинг** для определения того, запущена ли служба "темы" для приложения.</span><span class="sxs-lookup"><span data-stu-id="5e87c-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="5e87c-121">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="5e87c-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="5e87c-122">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="5e87c-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="5e87c-123">Сценариев</span><span class="sxs-lookup"><span data-stu-id="5e87c-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="5e87c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="5e87c-124">Requirements</span></span>



| <span data-ttu-id="5e87c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="5e87c-125">Requirement</span></span> | <span data-ttu-id="5e87c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="5e87c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e87c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e87c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5e87c-128">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5e87c-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e87c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e87c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5e87c-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5e87c-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5e87c-131">Header</span><span class="sxs-lookup"><span data-stu-id="5e87c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e87c-132"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e87c-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5e87c-133">IDL</span><span class="sxs-lookup"><span data-stu-id="5e87c-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e87c-134"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e87c-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5e87c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5e87c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e87c-136"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="5e87c-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
