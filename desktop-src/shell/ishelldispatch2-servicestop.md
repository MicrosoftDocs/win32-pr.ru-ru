---
description: IShellDispatch2. Сервицестоп, метод — останавливает именованную службу.
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: IShellDispatch2. Сервицестоп, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 651138eb687cfd83406bc6e1a7fcf520ff001171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117032"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="191e1-103">IShellDispatch2. Сервицестоп, метод</span><span class="sxs-lookup"><span data-stu-id="191e1-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="191e1-104">Останавливает именованную службу.</span><span class="sxs-lookup"><span data-stu-id="191e1-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="191e1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="191e1-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="191e1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="191e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="191e1-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="191e1-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="191e1-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="191e1-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="191e1-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="191e1-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="191e1-110">*вперсистент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="191e1-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="191e1-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="191e1-111">Type: **Variant**</span></span>

<span data-ttu-id="191e1-112">Задайте значение **true** , чтобы служба была запущена диспетчером управления службами при вызове [**сервицестарт**](ishelldispatch2-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="191e1-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="191e1-113">Чтобы оставить конфигурацию службы без изменений, установите для *вперсистент* значение **false**.</span><span class="sxs-lookup"><span data-stu-id="191e1-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="191e1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="191e1-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="191e1-115">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="191e1-115">JScript</span></span>

<span data-ttu-id="191e1-116">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="191e1-116">Type: **Variant\***</span></span>

<span data-ttu-id="191e1-117">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="191e1-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="191e1-118">VB</span><span class="sxs-lookup"><span data-stu-id="191e1-118">VB</span></span>

<span data-ttu-id="191e1-119">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="191e1-119">Type: **Variant\***</span></span>

<span data-ttu-id="191e1-120">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="191e1-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="191e1-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="191e1-121">Remarks</span></span>

<span data-ttu-id="191e1-122">Этот метод реализован и доступен через метод [**Shell. сервицестоп**](./shell-servicestop.md) .</span><span class="sxs-lookup"><span data-stu-id="191e1-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="191e1-123">Метод возвращает **значение false** , если служба уже остановлена.</span><span class="sxs-lookup"><span data-stu-id="191e1-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="191e1-124">Перед вызовом этого метода можно вызвать [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) для определения состояния службы.</span><span class="sxs-lookup"><span data-stu-id="191e1-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="191e1-125">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="191e1-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="191e1-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="191e1-126">Examples</span></span>

<span data-ttu-id="191e1-127">В следующих примерах показано использование **сервицестоп** для завершения работы службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="191e1-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="191e1-128">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="191e1-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="191e1-129">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="191e1-129">JScript:</span></span>


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



<span data-ttu-id="191e1-130">Сценариев</span><span class="sxs-lookup"><span data-stu-id="191e1-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="191e1-131">Требования</span><span class="sxs-lookup"><span data-stu-id="191e1-131">Requirements</span></span>



| <span data-ttu-id="191e1-132">Требование</span><span class="sxs-lookup"><span data-stu-id="191e1-132">Requirement</span></span> | <span data-ttu-id="191e1-133">Значение</span><span class="sxs-lookup"><span data-stu-id="191e1-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="191e1-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="191e1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="191e1-135">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="191e1-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="191e1-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="191e1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="191e1-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="191e1-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="191e1-138">Header</span><span class="sxs-lookup"><span data-stu-id="191e1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="191e1-139"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="191e1-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="191e1-140">IDL</span><span class="sxs-lookup"><span data-stu-id="191e1-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="191e1-141"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="191e1-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="191e1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="191e1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="191e1-143"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="191e1-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
