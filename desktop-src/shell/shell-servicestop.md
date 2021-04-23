---
description: Останавливает именованную службу.
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
ms.openlocfilehash: 31388078fe1c0e15c2e54efc86f0ff76bcfb7ed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265079"
---
# <a name="shellservicestop-method"></a><span data-ttu-id="c5cfb-103">Shell. Сервицестоп, метод</span><span class="sxs-lookup"><span data-stu-id="c5cfb-103">Shell.ServiceStop method</span></span>

<span data-ttu-id="c5cfb-104">Останавливает именованную службу.</span><span class="sxs-lookup"><span data-stu-id="c5cfb-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5cfb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5cfb-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="c5cfb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5cfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5cfb-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5cfb-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5cfb-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c5cfb-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c5cfb-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="c5cfb-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c5cfb-110">*вперсистент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5cfb-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5cfb-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="c5cfb-111">Type: **Variant**</span></span>

<span data-ttu-id="c5cfb-112">Задайте значение **true** , чтобы служба была запущена диспетчером управления службами при вызове [**сервицестарт**](./shell-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="c5cfb-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](./shell-servicestart.md) is called.</span></span> <span data-ttu-id="c5cfb-113">Чтобы оставить конфигурацию службы без изменений, установите для *вперсистент* значение **false**.</span><span class="sxs-lookup"><span data-stu-id="c5cfb-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5cfb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5cfb-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c5cfb-115">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="c5cfb-115">JScript</span></span>

<span data-ttu-id="c5cfb-116">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="c5cfb-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="c5cfb-117">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c5cfb-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="c5cfb-118">VB</span><span class="sxs-lookup"><span data-stu-id="c5cfb-118">VB</span></span>

<span data-ttu-id="c5cfb-119">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="c5cfb-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="c5cfb-120">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c5cfb-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5cfb-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5cfb-121">Remarks</span></span>

<span data-ttu-id="c5cfb-122">Метод возвращает **значение false** , если служба уже остановлена.</span><span class="sxs-lookup"><span data-stu-id="c5cfb-122">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="c5cfb-123">Перед вызовом этого метода можно вызвать [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) для определения состояния службы.</span><span class="sxs-lookup"><span data-stu-id="c5cfb-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="c5cfb-124">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c5cfb-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="c5cfb-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="c5cfb-125">Examples</span></span>

<span data-ttu-id="c5cfb-126">В следующих примерах показано использование **сервицестоп** для завершения работы службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c5cfb-126">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="c5cfb-127">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="c5cfb-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="c5cfb-128">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="c5cfb-128">JScript:</span></span>


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



<span data-ttu-id="c5cfb-129">Сценариев</span><span class="sxs-lookup"><span data-stu-id="c5cfb-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c5cfb-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c5cfb-130">Requirements</span></span>



| <span data-ttu-id="c5cfb-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c5cfb-131">Requirement</span></span> | <span data-ttu-id="c5cfb-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c5cfb-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5cfb-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5cfb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c5cfb-134">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c5cfb-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5cfb-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5cfb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c5cfb-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c5cfb-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c5cfb-137">Header</span><span class="sxs-lookup"><span data-stu-id="c5cfb-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5cfb-138"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5cfb-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c5cfb-139">IDL</span><span class="sxs-lookup"><span data-stu-id="c5cfb-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5cfb-140"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5cfb-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c5cfb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c5cfb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5cfb-142"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c5cfb-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
