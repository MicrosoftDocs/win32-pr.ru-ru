---
description: Запускает именованную службу.
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
ms.openlocfilehash: 508b4f1c05625acdaed2b5a235ee697cceb544c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984673"
---
# <a name="ishelldispatch2servicestart-method"></a><span data-ttu-id="a4dbe-103">IShellDispatch2. Сервицестарт, метод</span><span class="sxs-lookup"><span data-stu-id="a4dbe-103">IShellDispatch2.ServiceStart method</span></span>

<span data-ttu-id="a4dbe-104">Запускает именованную службу.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4dbe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4dbe-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="a4dbe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4dbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4dbe-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4dbe-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4dbe-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a4dbe-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a4dbe-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="a4dbe-110">*вперсистент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4dbe-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4dbe-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="a4dbe-111">Type: **Variant**</span></span>

<span data-ttu-id="a4dbe-112">Задайте значение **true** , чтобы служба автоматически запускалась диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="a4dbe-113">Задайте значение **false** , чтобы оставить конфигурацию службы без изменений.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4dbe-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4dbe-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a4dbe-115">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="a4dbe-115">JScript</span></span>

<span data-ttu-id="a4dbe-116">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="a4dbe-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="a4dbe-117">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="a4dbe-118">VB</span><span class="sxs-lookup"><span data-stu-id="a4dbe-118">VB</span></span>

<span data-ttu-id="a4dbe-119">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="a4dbe-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="a4dbe-120">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4dbe-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="a4dbe-121">Remarks</span></span>

<span data-ttu-id="a4dbe-122">Этот метод реализован и доступен через метод [**Shell. сервицестарт**](./shell-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="a4dbe-122">This method is implemented and accessed through the [**Shell.ServiceStart**](./shell-servicestart.md) method.</span></span>

<span data-ttu-id="a4dbe-123">Метод возвращает **значение false** , если служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-123">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="a4dbe-124">Перед вызовом этого метода можно вызвать [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) для определения состояния службы.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="a4dbe-125">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="a4dbe-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="a4dbe-126">Examples</span></span>

<span data-ttu-id="a4dbe-127">В следующих примерах показано использование **сервицестарт** для запуска службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-127">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="a4dbe-128">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="a4dbe-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="a4dbe-129">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="a4dbe-129">JScript:</span></span>


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



<span data-ttu-id="a4dbe-130">Сценариев</span><span class="sxs-lookup"><span data-stu-id="a4dbe-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a4dbe-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a4dbe-131">Requirements</span></span>



| <span data-ttu-id="a4dbe-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a4dbe-132">Requirement</span></span> | <span data-ttu-id="a4dbe-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a4dbe-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4dbe-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4dbe-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a4dbe-135">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a4dbe-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4dbe-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4dbe-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a4dbe-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a4dbe-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a4dbe-138">Header</span><span class="sxs-lookup"><span data-stu-id="a4dbe-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4dbe-139"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4dbe-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a4dbe-140">IDL</span><span class="sxs-lookup"><span data-stu-id="a4dbe-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a4dbe-141"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a4dbe-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a4dbe-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a4dbe-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4dbe-143"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a4dbe-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
