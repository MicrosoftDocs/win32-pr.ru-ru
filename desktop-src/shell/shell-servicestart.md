---
description: Запускает именованную службу.
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Метод Shell. Сервицестарт (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8cd3b910306fc995d15e9731823614717450ef55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909879"
---
# <a name="shellservicestart-method"></a><span data-ttu-id="288b5-103">Shell. Сервицестарт, метод</span><span class="sxs-lookup"><span data-stu-id="288b5-103">Shell.ServiceStart method</span></span>

<span data-ttu-id="288b5-104">Запускает именованную службу.</span><span class="sxs-lookup"><span data-stu-id="288b5-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="288b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="288b5-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="288b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="288b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="288b5-107">*ссервиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="288b5-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="288b5-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="288b5-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="288b5-109">**Строка** , содержащая имя службы.</span><span class="sxs-lookup"><span data-stu-id="288b5-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="288b5-110">*вперсистент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="288b5-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="288b5-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="288b5-111">Type: **Variant**</span></span>

<span data-ttu-id="288b5-112">Задайте значение **true** , чтобы служба автоматически запускалась диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="288b5-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="288b5-113">Задайте значение **false** , чтобы оставить конфигурацию службы без изменений.</span><span class="sxs-lookup"><span data-stu-id="288b5-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="288b5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="288b5-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="288b5-115">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="288b5-115">JScript</span></span>

<span data-ttu-id="288b5-116">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="288b5-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="288b5-117">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="288b5-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="288b5-118">VB</span><span class="sxs-lookup"><span data-stu-id="288b5-118">VB</span></span>

<span data-ttu-id="288b5-119">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="288b5-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="288b5-120">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="288b5-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="288b5-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="288b5-121">Remarks</span></span>

<span data-ttu-id="288b5-122">Метод возвращает **значение false** , если служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="288b5-122">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="288b5-123">Перед вызовом этого метода можно вызвать [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) для определения состояния службы.</span><span class="sxs-lookup"><span data-stu-id="288b5-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="288b5-124">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="288b5-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="288b5-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="288b5-125">Examples</span></span>

<span data-ttu-id="288b5-126">В следующих примерах показано использование **сервицестарт** для запуска службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="288b5-126">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="288b5-127">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="288b5-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="288b5-128">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="288b5-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



<span data-ttu-id="288b5-129">Сценариев</span><span class="sxs-lookup"><span data-stu-id="288b5-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="288b5-130">Требования</span><span class="sxs-lookup"><span data-stu-id="288b5-130">Requirements</span></span>



| <span data-ttu-id="288b5-131">Требование</span><span class="sxs-lookup"><span data-stu-id="288b5-131">Requirement</span></span> | <span data-ttu-id="288b5-132">Значение</span><span class="sxs-lookup"><span data-stu-id="288b5-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="288b5-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="288b5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="288b5-134">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="288b5-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="288b5-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="288b5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="288b5-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="288b5-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="288b5-137">Header</span><span class="sxs-lookup"><span data-stu-id="288b5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="288b5-138"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="288b5-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="288b5-139">IDL</span><span class="sxs-lookup"><span data-stu-id="288b5-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="288b5-140"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="288b5-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="288b5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="288b5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="288b5-142"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="288b5-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
