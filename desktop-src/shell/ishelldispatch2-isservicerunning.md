---
description: Возвращает значение, указывающее, запущена ли определенная служба.
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: IShellDispatch2. Иссервицеруннинг, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f39cd7da3d9959830208ab971b636e146e549775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984684"
---
# <a name="ishelldispatch2isservicerunning-method"></a><span data-ttu-id="ec3d4-103">IShellDispatch2. Иссервицеруннинг, метод</span><span class="sxs-lookup"><span data-stu-id="ec3d4-103">IShellDispatch2.IsServiceRunning method</span></span>

<span data-ttu-id="ec3d4-104">Возвращает значение, указывающее, запущена ли определенная служба.</span><span class="sxs-lookup"><span data-stu-id="ec3d4-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec3d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec3d4-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="ec3d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec3d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec3d4-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec3d4-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3d4-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ec3d4-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ec3d4-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="ec3d4-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec3d4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec3d4-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ec3d4-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="ec3d4-111">JScript</span></span>

<span data-ttu-id="ec3d4-112">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="ec3d4-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="ec3d4-113">Возвращает \*значение _ true\*\*, если запущена служба, указанная параметром *ссервиценаме* . в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ec3d4-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="ec3d4-114">VB</span><span class="sxs-lookup"><span data-stu-id="ec3d4-114">VB</span></span>

<span data-ttu-id="ec3d4-115">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="ec3d4-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="ec3d4-116">Возвращает \*значение _ true\*\*, если запущена служба, указанная параметром *ссервиценаме* . в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ec3d4-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec3d4-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ec3d4-117">Remarks</span></span>

<span data-ttu-id="ec3d4-118">Этот метод реализован и доступен через метод [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3d4-118">This method is implemented and accessed through the [**Shell.IsServiceRunning**](./shell-isservicerunning.md) method.</span></span>

<span data-ttu-id="ec3d4-119">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ec3d4-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="ec3d4-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="ec3d4-120">Examples</span></span>

<span data-ttu-id="ec3d4-121">В следующих примерах показано использование **иссервицеруннинг** для определения того, запущена ли служба "темы" для приложения.</span><span class="sxs-lookup"><span data-stu-id="ec3d4-121">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="ec3d4-122">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="ec3d4-122">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="ec3d4-123">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="ec3d4-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



<span data-ttu-id="ec3d4-124">Сценариев</span><span class="sxs-lookup"><span data-stu-id="ec3d4-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="ec3d4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ec3d4-125">Requirements</span></span>



| <span data-ttu-id="ec3d4-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ec3d4-126">Requirement</span></span> | <span data-ttu-id="ec3d4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ec3d4-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3d4-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec3d4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ec3d4-129">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ec3d4-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec3d4-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec3d4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ec3d4-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec3d4-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ec3d4-132">Header</span><span class="sxs-lookup"><span data-stu-id="ec3d4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec3d4-133"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec3d4-133"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ec3d4-134">IDL</span><span class="sxs-lookup"><span data-stu-id="ec3d4-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ec3d4-135"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ec3d4-135"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ec3d4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ec3d4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec3d4-137"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="ec3d4-137"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
