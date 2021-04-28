---
description: Shell. Канстартстопсервице — определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.
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
ms.openlocfilehash: 29561519b95329093ef1f7bfc64023fd1ac4533d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083692"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="a51e5-103">Shell. Канстартстопсервице, метод</span><span class="sxs-lookup"><span data-stu-id="a51e5-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="a51e5-104">Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.</span><span class="sxs-lookup"><span data-stu-id="a51e5-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="a51e5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a51e5-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="a51e5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a51e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a51e5-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a51e5-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a51e5-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e5-108">Type: **String**</span></span>

<span data-ttu-id="a51e5-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="a51e5-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a51e5-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a51e5-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a51e5-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="a51e5-111">JScript</span></span>

<span data-ttu-id="a51e5-112">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="a51e5-112">Type: **Variant\***</span></span>

<span data-ttu-id="a51e5-113">Возвращает **значение true** , если пользователь может запускать и прекращать работу службы. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a51e5-113">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="a51e5-114">VB</span><span class="sxs-lookup"><span data-stu-id="a51e5-114">VB</span></span>

<span data-ttu-id="a51e5-115">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="a51e5-115">Type: **Variant\***</span></span>

<span data-ttu-id="a51e5-116">Возвращает **значение true** , если пользователь может запускать и прекращать работу службы. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a51e5-116">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a51e5-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="a51e5-117">Remarks</span></span>

<span data-ttu-id="a51e5-118">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a51e5-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="a51e5-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="a51e5-119">Examples</span></span>

<span data-ttu-id="a51e5-120">В следующих примерах показано использование **канстартстопсервице** для JScript и VBScript.</span><span class="sxs-lookup"><span data-stu-id="a51e5-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="a51e5-121">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="a51e5-121">JScript:</span></span>


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



<span data-ttu-id="a51e5-122">Сценариев</span><span class="sxs-lookup"><span data-stu-id="a51e5-122">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a51e5-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a51e5-123">Requirements</span></span>



| <span data-ttu-id="a51e5-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a51e5-124">Requirement</span></span> | <span data-ttu-id="a51e5-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a51e5-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a51e5-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a51e5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a51e5-127">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a51e5-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a51e5-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a51e5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a51e5-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a51e5-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a51e5-130">Header</span><span class="sxs-lookup"><span data-stu-id="a51e5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a51e5-131"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a51e5-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a51e5-132">IDL</span><span class="sxs-lookup"><span data-stu-id="a51e5-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a51e5-133"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a51e5-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a51e5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a51e5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a51e5-135"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a51e5-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




