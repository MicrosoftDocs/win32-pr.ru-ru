---
description: Извлекает из реестра параметр ограничений группы.
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: Метод IShellDispatch2. Unrestricted (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f666a9ed3407d12eb9cf2c28ae062a9886d7a2cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984693"
---
# <a name="ishelldispatch2isrestricted-method"></a><span data-ttu-id="6ef72-103">IShellDispatch2. Unrestricted, метод</span><span class="sxs-lookup"><span data-stu-id="6ef72-103">IShellDispatch2.IsRestricted method</span></span>

<span data-ttu-id="6ef72-104">Извлекает из реестра параметр ограничений группы.</span><span class="sxs-lookup"><span data-stu-id="6ef72-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef72-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ef72-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="6ef72-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ef72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ef72-107">*сграуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ef72-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ef72-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6ef72-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6ef72-109">**Строка** , содержащая имя группы.</span><span class="sxs-lookup"><span data-stu-id="6ef72-109">A **String** that contains the group name.</span></span> <span data-ttu-id="6ef72-110">Это значение представляет собой имя подраздела реестра, в котором будет проверяться ограничение.</span><span class="sxs-lookup"><span data-stu-id="6ef72-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="6ef72-111">*срестриктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ef72-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ef72-112">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6ef72-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6ef72-113">**Строка** , содержащая ограничение, значение которого необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="6ef72-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ef72-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ef72-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6ef72-115">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="6ef72-115">JScript</span></span>

<span data-ttu-id="6ef72-116">Тип: \**Integer \** _</span><span class="sxs-lookup"><span data-stu-id="6ef72-116">Type: \**Integer\** _</span></span>

<span data-ttu-id="6ef72-117">Значение ограничения.</span><span class="sxs-lookup"><span data-stu-id="6ef72-117">The value of the restriction.</span></span> <span data-ttu-id="6ef72-118">Если указанное ограничение не найдено, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="6ef72-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="6ef72-119">VB</span><span class="sxs-lookup"><span data-stu-id="6ef72-119">VB</span></span>

<span data-ttu-id="6ef72-120">Тип: _*Integer \**_</span><span class="sxs-lookup"><span data-stu-id="6ef72-120">Type: _*Integer\**_</span></span>

<span data-ttu-id="6ef72-121">Значение ограничения.</span><span class="sxs-lookup"><span data-stu-id="6ef72-121">The value of the restriction.</span></span> <span data-ttu-id="6ef72-122">Если указанное ограничение не найдено, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="6ef72-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ef72-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ef72-123">Remarks</span></span>

<span data-ttu-id="6ef72-124">Этот метод реализован и доступен через метод [_ *Shell. Unrestricted* \*](./shell-isrestricted.md) .</span><span class="sxs-lookup"><span data-stu-id="6ef72-124">This method is implemented and accessed through the [_ *Shell.IsRestricted*\*](./shell-isrestricted.md) method.</span></span>

<span data-ttu-id="6ef72-125">**Ограничение** сначала ищет имя подраздела, которое соответствует *сграуп* в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="6ef72-125">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="6ef72-126">Ограничения объявляются в виде значений отдельных подразделов политики.</span><span class="sxs-lookup"><span data-stu-id="6ef72-126">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="6ef72-127">Если ограничение с именем в *срестриктион* находится в подразделе с именем в *сграуп*, то функция **Unrestricted** возвращает текущее значение ограничения.</span><span class="sxs-lookup"><span data-stu-id="6ef72-127">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="6ef72-128">Если ограничение не найдено в разделе **hKey \_ локальный \_ компьютер**, то этот же подраздел проверяется в разделе **hKey \_ текущий \_ пользователь**.</span><span class="sxs-lookup"><span data-stu-id="6ef72-128">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="6ef72-129">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6ef72-129">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="6ef72-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="6ef72-130">Examples</span></span>

<span data-ttu-id="6ef72-131">В приведенных ниже примерах показано использование параметра **ундокквисаутлогон** **для получения** значения данных из ограничения для подраздела **System** .</span><span class="sxs-lookup"><span data-stu-id="6ef72-131">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="6ef72-132">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="6ef72-132">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="6ef72-133">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="6ef72-133">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



<span data-ttu-id="6ef72-134">Сценариев</span><span class="sxs-lookup"><span data-stu-id="6ef72-134">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="6ef72-135">Требования</span><span class="sxs-lookup"><span data-stu-id="6ef72-135">Requirements</span></span>



| <span data-ttu-id="6ef72-136">Требование</span><span class="sxs-lookup"><span data-stu-id="6ef72-136">Requirement</span></span> | <span data-ttu-id="6ef72-137">Значение</span><span class="sxs-lookup"><span data-stu-id="6ef72-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef72-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ef72-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6ef72-139">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6ef72-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ef72-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ef72-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6ef72-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ef72-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6ef72-142">Header</span><span class="sxs-lookup"><span data-stu-id="6ef72-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ef72-143"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ef72-143"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6ef72-144">IDL</span><span class="sxs-lookup"><span data-stu-id="6ef72-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ef72-145"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ef72-145"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6ef72-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6ef72-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ef72-147"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="6ef72-147"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
