---
description: Останавливает именованную службу.
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
ms.openlocfilehash: 6a4a76c1f53309c14875eeaf6f3f4c0839a511bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984669"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="0c669-103">IShellDispatch2. Сервицестоп, метод</span><span class="sxs-lookup"><span data-stu-id="0c669-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="0c669-104">Останавливает именованную службу.</span><span class="sxs-lookup"><span data-stu-id="0c669-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c669-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c669-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="0c669-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c669-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c669-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c669-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c669-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="0c669-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="0c669-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="0c669-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="0c669-110">*вперсистент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c669-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c669-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="0c669-111">Type: **Variant**</span></span>

<span data-ttu-id="0c669-112">Задайте значение **true** , чтобы служба была запущена диспетчером управления службами при вызове [**сервицестарт**](ishelldispatch2-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="0c669-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="0c669-113">Чтобы оставить конфигурацию службы без изменений, установите для *вперсистент* значение **false**.</span><span class="sxs-lookup"><span data-stu-id="0c669-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c669-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c669-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0c669-115">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="0c669-115">JScript</span></span>

<span data-ttu-id="0c669-116">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="0c669-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="0c669-117">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0c669-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="0c669-118">VB</span><span class="sxs-lookup"><span data-stu-id="0c669-118">VB</span></span>

<span data-ttu-id="0c669-119">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="0c669-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="0c669-120">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0c669-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c669-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c669-121">Remarks</span></span>

<span data-ttu-id="0c669-122">Этот метод реализован и доступен через метод [**Shell. сервицестоп**](./shell-servicestop.md) .</span><span class="sxs-lookup"><span data-stu-id="0c669-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="0c669-123">Метод возвращает **значение false** , если служба уже остановлена.</span><span class="sxs-lookup"><span data-stu-id="0c669-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="0c669-124">Перед вызовом этого метода можно вызвать [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) для определения состояния службы.</span><span class="sxs-lookup"><span data-stu-id="0c669-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="0c669-125">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0c669-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="0c669-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="0c669-126">Examples</span></span>

<span data-ttu-id="0c669-127">В следующих примерах показано использование **сервицестоп** для завершения работы службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0c669-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="0c669-128">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="0c669-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="0c669-129">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="0c669-129">JScript:</span></span>


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



<span data-ttu-id="0c669-130">Сценариев</span><span class="sxs-lookup"><span data-stu-id="0c669-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0c669-131">Требования</span><span class="sxs-lookup"><span data-stu-id="0c669-131">Requirements</span></span>



| <span data-ttu-id="0c669-132">Требование</span><span class="sxs-lookup"><span data-stu-id="0c669-132">Requirement</span></span> | <span data-ttu-id="0c669-133">Значение</span><span class="sxs-lookup"><span data-stu-id="0c669-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c669-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c669-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0c669-135">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0c669-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c669-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c669-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0c669-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0c669-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0c669-138">Header</span><span class="sxs-lookup"><span data-stu-id="0c669-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c669-139"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c669-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="0c669-140">IDL</span><span class="sxs-lookup"><span data-stu-id="0c669-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0c669-141"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0c669-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="0c669-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0c669-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c669-143"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="0c669-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
