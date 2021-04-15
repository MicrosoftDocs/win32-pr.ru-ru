---
description: Отображает панель браузера.
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Метод Shell. Шовбровсербар (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d112399e62825714b4c060aeddcb8618ff73d478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985540"
---
# <a name="shellshowbrowserbar-method"></a><span data-ttu-id="97992-103">Shell. Шовбровсербар, метод</span><span class="sxs-lookup"><span data-stu-id="97992-103">Shell.ShowBrowserBar method</span></span>

<span data-ttu-id="97992-104">Отображает панель браузера.</span><span class="sxs-lookup"><span data-stu-id="97992-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="97992-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97992-105">Syntax</span></span>


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="97992-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="97992-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97992-107">*склсид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97992-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97992-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="97992-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="97992-109">**Строка** , содержащая форму строки CLSID отображаемой панели браузера.</span><span class="sxs-lookup"><span data-stu-id="97992-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="97992-110">Объект должен быть зарегистрирован в качестве объекта панели обозревателя с \_ категорией компонента CATID инфобанд.</span><span class="sxs-lookup"><span data-stu-id="97992-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="97992-111">Дополнительные сведения см. в разделе [Создание настраиваемых панелей обозревателя, панелей инструментов и полос рабочего стола](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="97992-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="97992-112">*вшов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97992-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97992-113">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="97992-113">Type: **Variant**</span></span>

<span data-ttu-id="97992-114">Задайте значение **true** , чтобы отобразить панель браузера, или **значение false** , чтобы скрыть ее.</span><span class="sxs-lookup"><span data-stu-id="97992-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97992-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97992-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="97992-116">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="97992-116">JScript</span></span>

<span data-ttu-id="97992-117">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="97992-117">Type: \**Variant\** _</span></span>

<span data-ttu-id="97992-118">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="97992-118">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="97992-119">VB</span><span class="sxs-lookup"><span data-stu-id="97992-119">VB</span></span>

<span data-ttu-id="97992-120">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="97992-120">Type: \**Variant\** _</span></span>

<span data-ttu-id="97992-121">Возвращает *значение _ true*\* при успешном выполнении; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="97992-121">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="97992-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="97992-122">Remarks</span></span>

<span data-ttu-id="97992-123">Можно отобразить одну из стандартных панелей обозревателя, задав для параметра *склсид* значение CLSID этой панели обозревателя.</span><span class="sxs-lookup"><span data-stu-id="97992-123">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="97992-124">Ниже перечислены стандартные панели обозревателя и их строки CLSID.</span><span class="sxs-lookup"><span data-stu-id="97992-124">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="97992-125">Панель обозревателя</span><span class="sxs-lookup"><span data-stu-id="97992-125">Explorer Bar</span></span> | <span data-ttu-id="97992-126">Строка CLSID</span><span class="sxs-lookup"><span data-stu-id="97992-126">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="97992-127">Избранное</span><span class="sxs-lookup"><span data-stu-id="97992-127">Favorites</span></span>    | <span data-ttu-id="97992-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="97992-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="97992-129">Папки</span><span class="sxs-lookup"><span data-stu-id="97992-129">Folders</span></span>      | <span data-ttu-id="97992-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="97992-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="97992-131">Журнал</span><span class="sxs-lookup"><span data-stu-id="97992-131">History</span></span>      | <span data-ttu-id="97992-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="97992-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="97992-133">Найти</span><span class="sxs-lookup"><span data-stu-id="97992-133">Search</span></span>       | <span data-ttu-id="97992-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="97992-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="97992-135">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="97992-135">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="97992-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="97992-136">Examples</span></span>

<span data-ttu-id="97992-137">В следующих примерах показано использование **оболочки. шовбровсербар** для отображения панели браузера **избранного** .</span><span class="sxs-lookup"><span data-stu-id="97992-137">The following examples show the use of **Shell.ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="97992-138">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="97992-138">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="97992-139">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="97992-139">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



<span data-ttu-id="97992-140">Сценариев</span><span class="sxs-lookup"><span data-stu-id="97992-140">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="97992-141">Требования</span><span class="sxs-lookup"><span data-stu-id="97992-141">Requirements</span></span>



| <span data-ttu-id="97992-142">Требование</span><span class="sxs-lookup"><span data-stu-id="97992-142">Requirement</span></span> | <span data-ttu-id="97992-143">Значение</span><span class="sxs-lookup"><span data-stu-id="97992-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97992-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97992-144">Minimum supported client</span></span><br/> | <span data-ttu-id="97992-145">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="97992-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97992-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97992-146">Minimum supported server</span></span><br/> | <span data-ttu-id="97992-147">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97992-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="97992-148">Header</span><span class="sxs-lookup"><span data-stu-id="97992-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="97992-149"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="97992-149"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="97992-150">IDL</span><span class="sxs-lookup"><span data-stu-id="97992-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97992-151"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97992-151"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="97992-152">DLL</span><span class="sxs-lookup"><span data-stu-id="97992-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97992-153"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="97992-153"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
