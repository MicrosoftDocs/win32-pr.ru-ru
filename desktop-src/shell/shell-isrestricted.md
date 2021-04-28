---
description: Метод Shell. Strict — получает параметр ограничения группы из реестра.
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Метод Shell. Unrestricted (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e428c914cf95d282fd721071009efc70fcb3a4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104262"
---
# <a name="shellisrestricted-method"></a><span data-ttu-id="ce879-103">Shell. Strict, метод</span><span class="sxs-lookup"><span data-stu-id="ce879-103">Shell.IsRestricted method</span></span>

<span data-ttu-id="ce879-104">Извлекает из реестра параметр ограничений группы.</span><span class="sxs-lookup"><span data-stu-id="ce879-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce879-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce879-105">Syntax</span></span>


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="ce879-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce879-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce879-107">*сграуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce879-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce879-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ce879-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ce879-109">**Строка** , содержащая имя группы.</span><span class="sxs-lookup"><span data-stu-id="ce879-109">A **String** that contains the group name.</span></span> <span data-ttu-id="ce879-110">Это значение представляет собой имя подраздела реестра, в котором будет проверяться ограничение.</span><span class="sxs-lookup"><span data-stu-id="ce879-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="ce879-111">*срестриктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce879-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce879-112">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ce879-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ce879-113">**Строка** , содержащая ограничение, значение которого необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="ce879-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce879-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce879-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ce879-115">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="ce879-115">JScript</span></span>

<span data-ttu-id="ce879-116">Тип: **Integer \***</span><span class="sxs-lookup"><span data-stu-id="ce879-116">Type: **Integer\***</span></span>

<span data-ttu-id="ce879-117">Значение ограничения.</span><span class="sxs-lookup"><span data-stu-id="ce879-117">The value of the restriction.</span></span> <span data-ttu-id="ce879-118">Если указанное ограничение не найдено, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="ce879-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="ce879-119">VB</span><span class="sxs-lookup"><span data-stu-id="ce879-119">VB</span></span>

<span data-ttu-id="ce879-120">Тип: **Integer \***</span><span class="sxs-lookup"><span data-stu-id="ce879-120">Type: **Integer\***</span></span>

<span data-ttu-id="ce879-121">Значение ограничения.</span><span class="sxs-lookup"><span data-stu-id="ce879-121">The value of the restriction.</span></span> <span data-ttu-id="ce879-122">Если указанное ограничение не найдено, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="ce879-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce879-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="ce879-123">Remarks</span></span>

<span data-ttu-id="ce879-124">**Ограничение** сначала ищет имя подраздела, которое соответствует *сграуп* в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="ce879-124">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="ce879-125">Ограничения объявляются в виде значений отдельных подразделов политики.</span><span class="sxs-lookup"><span data-stu-id="ce879-125">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="ce879-126">Если ограничение с именем в *срестриктион* находится в подразделе с именем в *сграуп*, то функция **Unrestricted** возвращает текущее значение ограничения.</span><span class="sxs-lookup"><span data-stu-id="ce879-126">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="ce879-127">Если ограничение не найдено в разделе **hKey \_ локальный \_ компьютер**, то этот же подраздел проверяется в разделе **hKey \_ текущий \_ пользователь**.</span><span class="sxs-lookup"><span data-stu-id="ce879-127">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="ce879-128">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ce879-128">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="ce879-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="ce879-129">Examples</span></span>

<span data-ttu-id="ce879-130">В приведенных ниже примерах показано использование параметра **ундокквисаутлогон** **для получения** значения данных из ограничения для подраздела **System** .</span><span class="sxs-lookup"><span data-stu-id="ce879-130">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="ce879-131">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="ce879-131">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="ce879-132">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="ce879-132">JScript:</span></span>


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



<span data-ttu-id="ce879-133">Сценариев</span><span class="sxs-lookup"><span data-stu-id="ce879-133">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ce879-134">Требования</span><span class="sxs-lookup"><span data-stu-id="ce879-134">Requirements</span></span>



| <span data-ttu-id="ce879-135">Требование</span><span class="sxs-lookup"><span data-stu-id="ce879-135">Requirement</span></span> | <span data-ttu-id="ce879-136">Значение</span><span class="sxs-lookup"><span data-stu-id="ce879-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce879-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce879-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ce879-138">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ce879-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce879-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce879-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ce879-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce879-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ce879-141">Header</span><span class="sxs-lookup"><span data-stu-id="ce879-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce879-142"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce879-142"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ce879-143">IDL</span><span class="sxs-lookup"><span data-stu-id="ce879-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ce879-144"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ce879-144"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ce879-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ce879-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce879-146"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="ce879-146"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
