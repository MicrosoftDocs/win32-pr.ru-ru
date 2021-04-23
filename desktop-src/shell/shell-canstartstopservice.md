---
description: Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: Метод Shell. Канстартстопсервице (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1d92fa076141bdebc8a2f24059a65e842e5a3d6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998754"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="7ae4f-103">Shell. Канстартстопсервице, метод</span><span class="sxs-lookup"><span data-stu-id="7ae4f-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="7ae4f-104">Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.</span><span class="sxs-lookup"><span data-stu-id="7ae4f-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae4f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ae4f-105">Syntax</span></span>


```JScript
retVal = Shell.CanStartStopService(
  sServiceName
)
```


```VB

Shell.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="7ae4f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ae4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ae4f-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ae4f-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae4f-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="7ae4f-108">Type: **String**</span></span>

<span data-ttu-id="7ae4f-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="7ae4f-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ae4f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ae4f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7ae4f-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="7ae4f-111">JScript</span></span>

<span data-ttu-id="7ae4f-112">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="7ae4f-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="7ae4f-113">Возвращает \*значение _ true\*\*, если пользователь может запускать и прекращать работу службы. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7ae4f-113">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="7ae4f-114">VB</span><span class="sxs-lookup"><span data-stu-id="7ae4f-114">VB</span></span>

<span data-ttu-id="7ae4f-115">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="7ae4f-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="7ae4f-116">Возвращает \*значение _ true\*\*, если пользователь может запускать и прекращать работу службы. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7ae4f-116">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae4f-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ae4f-117">Remarks</span></span>

<span data-ttu-id="7ae4f-118">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7ae4f-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="7ae4f-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="7ae4f-119">Examples</span></span>

<span data-ttu-id="7ae4f-120">В следующих примерах показано использование **канстартстопсервице** для JScript и VBScript.</span><span class="sxs-lookup"><span data-stu-id="7ae4f-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="7ae4f-121">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="7ae4f-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



<span data-ttu-id="7ae4f-122">Сценариев</span><span class="sxs-lookup"><span data-stu-id="7ae4f-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="7ae4f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7ae4f-123">Requirements</span></span>



| <span data-ttu-id="7ae4f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7ae4f-124">Requirement</span></span> | <span data-ttu-id="7ae4f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7ae4f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae4f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ae4f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7ae4f-127">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7ae4f-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ae4f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ae4f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7ae4f-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ae4f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7ae4f-130">Header</span><span class="sxs-lookup"><span data-stu-id="7ae4f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ae4f-131"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ae4f-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7ae4f-132">IDL</span><span class="sxs-lookup"><span data-stu-id="7ae4f-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ae4f-133"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ae4f-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7ae4f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7ae4f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ae4f-135"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="7ae4f-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




