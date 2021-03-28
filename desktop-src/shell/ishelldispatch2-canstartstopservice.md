---
description: Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: IShellDispatch2. Канстартстопсервице, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 92655c2c561284f00204826e1848a75f00f4a04d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543130"
---
# <a name="ishelldispatch2canstartstopservice-method"></a><span data-ttu-id="83344-103">IShellDispatch2. Канстартстопсервице, метод</span><span class="sxs-lookup"><span data-stu-id="83344-103">IShellDispatch2.CanStartStopService method</span></span>

<span data-ttu-id="83344-104">Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.</span><span class="sxs-lookup"><span data-stu-id="83344-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="83344-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83344-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.CanStartStopService(
  sServiceName
)
```


```VB

IShellDispatch2.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="83344-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83344-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83344-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83344-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83344-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="83344-108">Type: **String**</span></span>

<span data-ttu-id="83344-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="83344-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83344-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83344-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="83344-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="83344-111">JScript</span></span>

<span data-ttu-id="83344-112">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="83344-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="83344-113">Возвращает \*значение _ true\*\*, если пользователь может запускать и прекращать работу службы. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="83344-113">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="83344-114">VB</span><span class="sxs-lookup"><span data-stu-id="83344-114">VB</span></span>

<span data-ttu-id="83344-115">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="83344-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="83344-116">Возвращает \*значение _ true\*\*, если пользователь может запускать и прекращать работу службы. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="83344-116">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="83344-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="83344-117">Remarks</span></span>

<span data-ttu-id="83344-118">Этот метод реализован и доступен через метод [**Shell. канстартстопсервице**](./shell-canstartstopservice.md) .</span><span class="sxs-lookup"><span data-stu-id="83344-118">This method is implemented and accessed through the [**Shell.CanStartStopService**](./shell-canstartstopservice.md) method.</span></span>

<span data-ttu-id="83344-119">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="83344-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="83344-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="83344-120">Examples</span></span>

<span data-ttu-id="83344-121">В следующих примерах показано использование **канстартстопсервице** для JScript и VBScript.</span><span class="sxs-lookup"><span data-stu-id="83344-121">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="83344-122">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="83344-122">JScript:</span></span>


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



<span data-ttu-id="83344-123">Сценариев</span><span class="sxs-lookup"><span data-stu-id="83344-123">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="83344-124">Требования</span><span class="sxs-lookup"><span data-stu-id="83344-124">Requirements</span></span>



| <span data-ttu-id="83344-125">Требование</span><span class="sxs-lookup"><span data-stu-id="83344-125">Requirement</span></span> | <span data-ttu-id="83344-126">Значение</span><span class="sxs-lookup"><span data-stu-id="83344-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83344-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83344-127">Minimum supported client</span></span><br/> | <span data-ttu-id="83344-128">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="83344-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83344-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83344-129">Minimum supported server</span></span><br/> | <span data-ttu-id="83344-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83344-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="83344-131">Header</span><span class="sxs-lookup"><span data-stu-id="83344-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="83344-132"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="83344-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="83344-133">IDL</span><span class="sxs-lookup"><span data-stu-id="83344-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="83344-134"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="83344-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="83344-135">DLL</span><span class="sxs-lookup"><span data-stu-id="83344-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83344-136"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="83344-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
