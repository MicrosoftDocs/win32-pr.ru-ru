---
description: IShellDispatch2. Сервицестарт-метод — запускает именованную службу.
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: IShellDispatch2. Сервицестарт, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c0f4fa218c4def993025ff18bffd0cc54def9818
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117052"
---
# <a name="ishelldispatch2servicestart-method"></a><span data-ttu-id="84d6e-103">IShellDispatch2. Сервицестарт, метод</span><span class="sxs-lookup"><span data-stu-id="84d6e-103">IShellDispatch2.ServiceStart method</span></span>

<span data-ttu-id="84d6e-104">Запускает именованную службу.</span><span class="sxs-lookup"><span data-stu-id="84d6e-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="84d6e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84d6e-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="84d6e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84d6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84d6e-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84d6e-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84d6e-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="84d6e-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="84d6e-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="84d6e-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="84d6e-110">*вперсистент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84d6e-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84d6e-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="84d6e-111">Type: **Variant**</span></span>

<span data-ttu-id="84d6e-112">Задайте значение **true** , чтобы служба автоматически запускалась диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="84d6e-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="84d6e-113">Задайте значение **false** , чтобы оставить конфигурацию службы без изменений.</span><span class="sxs-lookup"><span data-stu-id="84d6e-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84d6e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84d6e-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="84d6e-115">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="84d6e-115">JScript</span></span>

<span data-ttu-id="84d6e-116">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="84d6e-116">Type: **Variant\***</span></span>

<span data-ttu-id="84d6e-117">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="84d6e-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="84d6e-118">VB</span><span class="sxs-lookup"><span data-stu-id="84d6e-118">VB</span></span>

<span data-ttu-id="84d6e-119">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="84d6e-119">Type: **Variant\***</span></span>

<span data-ttu-id="84d6e-120">Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="84d6e-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="84d6e-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="84d6e-121">Remarks</span></span>

<span data-ttu-id="84d6e-122">Этот метод реализован и доступен через метод [**Shell. сервицестарт**](./shell-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="84d6e-122">This method is implemented and accessed through the [**Shell.ServiceStart**](./shell-servicestart.md) method.</span></span>

<span data-ttu-id="84d6e-123">Метод возвращает **значение false** , если служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="84d6e-123">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="84d6e-124">Перед вызовом этого метода можно вызвать [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) для определения состояния службы.</span><span class="sxs-lookup"><span data-stu-id="84d6e-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="84d6e-125">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="84d6e-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="84d6e-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="84d6e-126">Examples</span></span>

<span data-ttu-id="84d6e-127">В следующих примерах показано использование **сервицестарт** для запуска службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="84d6e-127">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="84d6e-128">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="84d6e-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="84d6e-129">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="84d6e-129">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



<span data-ttu-id="84d6e-130">Сценариев</span><span class="sxs-lookup"><span data-stu-id="84d6e-130">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="84d6e-131">Требования</span><span class="sxs-lookup"><span data-stu-id="84d6e-131">Requirements</span></span>



| <span data-ttu-id="84d6e-132">Требование</span><span class="sxs-lookup"><span data-stu-id="84d6e-132">Requirement</span></span> | <span data-ttu-id="84d6e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="84d6e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84d6e-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84d6e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="84d6e-135">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="84d6e-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84d6e-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84d6e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="84d6e-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84d6e-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="84d6e-138">Header</span><span class="sxs-lookup"><span data-stu-id="84d6e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="84d6e-139"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="84d6e-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="84d6e-140">IDL</span><span class="sxs-lookup"><span data-stu-id="84d6e-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84d6e-141"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84d6e-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="84d6e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="84d6e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84d6e-143"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="84d6e-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
