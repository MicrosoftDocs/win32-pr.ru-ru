---
description: Shell. Сервицестоп метод — останавливает именованную службу.
ms.assetid: AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947
title: Метод Shell. Сервицестоп (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5307fabe79ab9e634ca1e2815c0b90d59b13b1f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104162"
---
# <a name="shellservicestop-method"></a><span data-ttu-id="31ffb-103">Shell. Сервицестоп, метод</span><span class="sxs-lookup"><span data-stu-id="31ffb-103">Shell.ServiceStop method</span></span>

<span data-ttu-id="31ffb-104">Останавливает именованную службу.</span><span class="sxs-lookup"><span data-stu-id="31ffb-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ffb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31ffb-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="31ffb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31ffb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ffb-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31ffb-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ffb-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="31ffb-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="31ffb-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="31ffb-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="31ffb-110">*вперсистент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31ffb-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ffb-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="31ffb-111">Type: **Variant**</span></span>

<span data-ttu-id="31ffb-112">Задайте значение **true** , чтобы служба была запущена диспетчером управления службами при вызове [**сервицестарт**](./shell-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="31ffb-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](./shell-servicestart.md) is called.</span></span> <span data-ttu-id="31ffb-113">Чтобы оставить конфигурацию службы без изменений, установите для *вперсистент* значение **false**.</span><span class="sxs-lookup"><span data-stu-id="31ffb-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ffb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31ffb-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="31ffb-115">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="31ffb-115">JScript</span></span>

<span data-ttu-id="31ffb-116">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="31ffb-116">Type: **Variant\***</span></span>

<span data-ttu-id="31ffb-117">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="31ffb-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="31ffb-118">VB</span><span class="sxs-lookup"><span data-stu-id="31ffb-118">VB</span></span>

<span data-ttu-id="31ffb-119">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="31ffb-119">Type: **Variant\***</span></span>

<span data-ttu-id="31ffb-120">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="31ffb-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="31ffb-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="31ffb-121">Remarks</span></span>

<span data-ttu-id="31ffb-122">Метод возвращает **значение false** , если служба уже остановлена.</span><span class="sxs-lookup"><span data-stu-id="31ffb-122">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="31ffb-123">Перед вызовом этого метода можно вызвать [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) для определения состояния службы.</span><span class="sxs-lookup"><span data-stu-id="31ffb-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="31ffb-124">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="31ffb-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="31ffb-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="31ffb-125">Examples</span></span>

<span data-ttu-id="31ffb-126">В следующих примерах показано использование **сервицестоп** для завершения работы службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="31ffb-126">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="31ffb-127">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="31ffb-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="31ffb-128">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="31ffb-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



<span data-ttu-id="31ffb-129">Сценариев</span><span class="sxs-lookup"><span data-stu-id="31ffb-129">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="31ffb-130">Требования</span><span class="sxs-lookup"><span data-stu-id="31ffb-130">Requirements</span></span>



| <span data-ttu-id="31ffb-131">Требование</span><span class="sxs-lookup"><span data-stu-id="31ffb-131">Requirement</span></span> | <span data-ttu-id="31ffb-132">Значение</span><span class="sxs-lookup"><span data-stu-id="31ffb-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31ffb-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31ffb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="31ffb-134">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31ffb-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31ffb-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31ffb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="31ffb-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31ffb-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="31ffb-137">Header</span><span class="sxs-lookup"><span data-stu-id="31ffb-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="31ffb-138"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="31ffb-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="31ffb-139">IDL</span><span class="sxs-lookup"><span data-stu-id="31ffb-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31ffb-140"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="31ffb-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="31ffb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="31ffb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31ffb-142"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="31ffb-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
