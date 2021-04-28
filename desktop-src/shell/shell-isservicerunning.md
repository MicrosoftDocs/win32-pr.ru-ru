---
description: Shell. Иссервицеруннинг-метод — возвращает значение, указывающее, запущена ли определенная служба.
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
ms.openlocfilehash: 01af900bb7930ec7b6dde0b0700c83f211733dc3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083728"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="c9868-103">Shell. Иссервицеруннинг, метод</span><span class="sxs-lookup"><span data-stu-id="c9868-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="c9868-104">Возвращает значение, указывающее, запущена ли определенная служба.</span><span class="sxs-lookup"><span data-stu-id="c9868-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9868-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9868-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="c9868-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9868-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9868-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9868-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c9868-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c9868-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="c9868-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9868-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9868-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c9868-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="c9868-111">JScript</span></span>

<span data-ttu-id="c9868-112">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="c9868-112">Type: **Variant\***</span></span>

<span data-ttu-id="c9868-113">Возвращает **значение true** , если служба, указанная параметром *ссервиценаме* , запущена. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c9868-113">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="c9868-114">VB</span><span class="sxs-lookup"><span data-stu-id="c9868-114">VB</span></span>

<span data-ttu-id="c9868-115">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="c9868-115">Type: **Variant\***</span></span>

<span data-ttu-id="c9868-116">Возвращает **значение true** , если служба, указанная параметром *ссервиценаме* , запущена. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c9868-116">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9868-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="c9868-117">Remarks</span></span>

<span data-ttu-id="c9868-118">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c9868-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="c9868-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="c9868-119">Examples</span></span>

<span data-ttu-id="c9868-120">В следующих примерах показано использование **иссервицеруннинг** для определения того, запущена ли служба "темы" для приложения.</span><span class="sxs-lookup"><span data-stu-id="c9868-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="c9868-121">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="c9868-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="c9868-122">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="c9868-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="c9868-123">Сценариев</span><span class="sxs-lookup"><span data-stu-id="c9868-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="c9868-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c9868-124">Requirements</span></span>



| <span data-ttu-id="c9868-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c9868-125">Requirement</span></span> | <span data-ttu-id="c9868-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c9868-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9868-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9868-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c9868-128">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c9868-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9868-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9868-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c9868-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9868-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c9868-131">Header</span><span class="sxs-lookup"><span data-stu-id="c9868-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9868-132"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9868-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c9868-133">IDL</span><span class="sxs-lookup"><span data-stu-id="c9868-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9868-134"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9868-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c9868-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c9868-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9868-136"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c9868-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
